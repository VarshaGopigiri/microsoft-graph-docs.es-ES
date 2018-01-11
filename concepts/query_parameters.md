# <a name="use-query-parameters-to-customize-responses"></a>Usar parámetros de consulta para personalizar respuestas

Microsoft Graph proporciona parámetros de consulta opcionales que puede usar para especificar y controlar la cantidad de datos devueltos en una respuesta. Se admiten los siguientes parámetros de consulta.

>**Nota:** Haga clic en los ejemplos para probarlos en [Probador de Graph][graph-explorer].

| Nombre                     | Descripción | Ejemplo
|:-------------------------|:------------|:---------|
| [$count](#count-parameter)         | Recupera el número total de recursos coincidentes. | [`/me/messages?$top=2&$count=true`][count-example]
| [$expand](#expand-parameter)       | Recupera los recursos relacionados.|[`/groups?$expand=members`][expand-example]
| [$filter](#filter-parameter)       | Filtra los resultados (filas).|[`/users?$filter=startswith(givenName,'J')`][filter-example]
| [$format](#format-parameter)       | Devuelve los resultados en el formato de medio especificado.|[`/users?$format=json`][format-example]
| [$orderby](#orderby-parameter)     | Ordena los resultados.|[`/users?$orderby=displayName desc`][orderby-example]
| [$search](#search-parameter)       | Devuelve los resultados en función de los criterios de búsqueda. Actualmente, se admite en las colecciones de **mensajes** y **usuarios**.|[`/me/messages?$search=pizza`][search-example]
| [$select](#select-parameter)       | Filtra las propiedades (columnas).|[`/users?$select=givenName,surname`][select-example]
| [$skip](#skip-parameter)           | Indexa en un conjunto de resultados. También se usa en algunas API para implementar la paginación y se puede usar junto a `$top` para paginar manualmente los resultados. | [`/me/messages?$skip=11`][skip-example]
| [$skipToken](#skiptoken-parameter) | Recupera la siguiente página de resultados de conjuntos de resultados que abarcan varias páginas. (Algunas API usan `$skip` en su lugar). | `/users?$skiptoken=X%274453707402000100000017...`|
| [$top](#top-parameter)             | Establece el tamaño de la página de resultados. |[`/users?$top=2`][top-example]



Estos parámetros son compatibles con el [lenguaje de consulta de OData V4][odata-query]. No todos los parámetros se admiten en todas las API de Microsoft Graph, y la compatibilidad puede variar considerablemente entre los puntos de conexión `v1.0` y `beta`. 

> **Nota:** En el punto de conexión `beta`, el prefijo `$` es opcional. Por ejemplo, en lugar de `$filter`, puede usar `filter`. Para obtener más detalles y ejemplos, vea [Compatibilidad con los parámetros de consulta sin el prefijo "$" en Microsoft Graph](http://dev.office.com/queryparametersinMicrosoftGraph).

## <a name="encoding-query-parameters"></a>Codificación de parámetros de consulta

Los valores de los parámetros de consulta deben ser codificados por porcentaje. Muchos clientes HTTP, exploradores y herramientas (como el [Probador de Graph][graph-explorer]) le servirán de ayuda. Si una consulta produce un error, puede deberse a que los valores de los parámetros de consulta no se han codificado correctamente.

Una dirección URL sin codificar tiene el siguiente aspecto:

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(givenName, 'J')
```

Una dirección URL codificada correctamente tiene el siguiente aspecto:

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(givenName%2C+'J')
```

## <a name="count-parameter"></a>parámetro de recuento

Use el parámetro de consulta `$count` para incluir un recuento del número total de elementos de una colección junto con la página de valores de datos que se devuelve desde Microsoft Graph. 

Por ejemplo, la siguiente solicitud devolverá tanto la colección de **contactos** del usuario actual como el número de elementos de la colección de **contactos** en la propiedad `@odata.count`.

```http
GET  https://graph.microsoft.com/v1.0/me/contacts?$count=true
```

[Probar en el Probador de Graph](https://developer.microsoft.com/graph/graph-explorer?request=me/contacts?$count=true&method=GET&version=v1.0)


>**Nota:** `$count` no se admite con colecciones de recursos que se derivan de [directoryObject](../api-reference/v1.0/resources/directoryobject.md), como las colecciones de [usuarios](../api-reference/v1.0/resources/user.md) o [grupos](../api-reference/v1.0/resources/group.md).

## <a name="expand-parameter"></a>parámetro de expansión

Muchos de los recursos de Microsoft Graph exponen ambas propiedades declaradas de los recursos, así como sus relaciones con otros recursos. Estas relaciones también se denominan propiedades de referencia o propiedades de navegación, y pueden hacer referencia a un único recurso o a una colección de recursos. Por ejemplo, las carpetas de correo, el administrador y los informes directos de un usuario se exponen como relaciones. 

Normalmente, se pueden consultar las propiedades de un recurso o una de sus relaciones en una sola solicitud, pero no ambas. Puede usar el parámetro de cadena de consulta `$expand` para incluir en los resultados de la consulta el recurso expandido o la colección a la que se hace referencia con una única relación (propiedad de navegación).

En el ejemplo siguiente se obtiene la información de la unidad raíz junto con los elementos secundarios de nivel superior de una unidad:

```http
GET https://graph.microsoft.com/v1.0/me/drive/root?$expand=children
```

[Probar en el Probador de Graph](https://developer.microsoft.com/graph/graph-explorer?request=me/drive/root?$expand=children&method=GET&version=v1.0)

Con algunas colecciones de recursos, también se pueden especificar las propiedades que se van a devolver en los recursos expandidos si se agrega un parámetro `$select`. En el ejemplo siguiente se realiza la misma consulta que en el anterior, pero se usa una instrucción [`$select`](#select-parameter) para limitar las propiedades devueltas para los elementos secundarios expandidos a las propiedades **id** y **name**.

```http
GET https://graph.microsoft.com/v1.0/me/drive/root?$expand=children($select=id,name)
```

[Probar en el Probador de Graph][expand-example]

> **Nota:** No todas las relaciones y recursos admiten el parámetro de consulta `$expand`. Por ejemplo, se pueden expandir las relaciones **directReports**, **manager** y **memberOf** de un usuario, pero no se pueden expandir sus relaciones **events**, **messages** o **photo**. No todos los recursos o relaciones admiten el uso de `$select` en elementos expandidos. 
> 
> Con recursos de Azure AD que se derivan de [directoryObject](../api-reference/v1.0/resources/directoryobject.md), como [user](../api-reference/v1.0/resources/user.md) y [group](../api-reference/v1.0/resources/group.md), solo se admite `$expand` para `beta` y normalmente devuelve un máximo de 20 elementos para la relación expandida.

## <a name="filter-parameter"></a>parámetro de filtrado

Use el parámetro de consulta `$filter` para recuperar solo un subconjunto de una colección. 

Por ejemplo, para buscar usuarios cuyos nombres para mostrar comiencen por la letra "J", use `startswith`.

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(displayName,'J')
```

[Probar en el Probador de Graph][filter-example]

La compatibilidad con los operadores `$filter` varía en función de la API de Microsoft Graph. Generalmente, se admiten los siguientes operadores lógicos: 

- igual a (`eq`)
- no es igual a (`ne`)
- mayor que (`gt`)
- mayor o igual que (`ge`)
- menor que (`lt`), menor o igual que (`le`)
- y (`and`)
- o (`or`)
- no (`not`)
 
El operador de cadena `startswith` se suele admitir. El operador lambda `any` se admite con algunas API. Para obtener algunos ejemplos de uso, vea la tabla siguiente. Para obtener detalles adicionales sobre la sintaxis de `$filter`, vea el [protocolo OData][odata-filter].  

En la tabla siguiente se muestran algunos ejemplos de uso del parámetro de consulta `$filter`.

> **Nota:** Haga clic en los ejemplos para probarlos en [Probador de Graph][graph-explorer].

| Descripción | Ejemplo
|:------------|:--------|
| Buscar usuarios con el nombre Mary en varias propiedades. | [`https://graph.microsoft.com/v1.0/users?$filter=startswith(displayName,'mary') or startswith(givenName,'mary') or startswith(surname,'mary') or startswith(mail,'mary') or startswith(userPrincipalName,'mary')`](https://developer.microsoft.com/graph/graph-explorer?request=users?$filter=startswith(displayName,'mary')+or+startswith(givenName,'mary')+or+startswith(surname,'mary')+or+startswith(mail,'mary')+or+startswith(userPrincipalName,'mary')&method=GET&version=v1.0) 
| Obtener todos los eventos del usuario que inició sesión que comiencen después del 1/7/2017. | [`https://graph.microsoft.com/v1.0/me/events?$filter=start/dateTime ge '2017-07-01T08:00'`](https://developer.microsoft.com/graph/graph-explorer?request=me/events?$filter=start/dateTime+ge+'2017-07-01T08:00'&method=GET&version=v1.0) 
| Obtener todos los correos electrónicos de una dirección específica recibidos por el usuario que inició sesión. | [`https://graph.microsoft.com/v1.0/me/messages?$filter=from/emailAddress/address eq 'someuser@example.com'`](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$filter=from/emailAddress/address+eq+'someuser@.com'&method=GET&version=v1.0) 
| Obtener todos los correos electrónicos recibidos en abril de 2017 por el usuario que inició sesión. | [`https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messages?$filter=ReceivedDateTime ge 2017-04-01 and receivedDateTime lt 2017-05-01`](https://developer.microsoft.com/graph/graph-explorer?request=me/mailFolders/inbox/messages?$filter=ReceivedDateTime+ge+2017-04-01+and+receivedDateTime+lt+2017-05-01&method=GET&version=v1.0) 
| Obtener todos los correos electrónicos no leídos en la Bandeja de entrada del usuario que inició sesión. | [`https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messages?$filter=isRead eq false`](https://developer.microsoft.com/graph/graph-explorer?request=me/mailFolders/inbox/messages?$filter=isRead+eq+false&method=GET&version=v1.0) 
| Enumerar todos los grupos de Office 365 de una organización. | [`https://graph.microsoft.com/v1.0/groups?$filter=groupTypes/any(c:c+eq+'Unified')`](https://developer.microsoft.com/graph/graph-explorer?request=groups?$filter=groupTypes/any(c:c+eq+'Unified')&method=GET&version=v1.0) 

> **Nota:** Los operadores `$filter` siguientes no se admiten para recursos de Azure AD: `ne`, `gt`, `ge`, `lt`, `le` y `not`. El operador de cadena `contains` actualmente no se admite en ningún recurso de Microsoft Graph.

## <a name="format-parameter"></a>parámetro de formato

Use el parámetro de consulta `$format` para especificar el formato de medio de los elementos devueltos desde Microsoft Graph

Por ejemplo, la solicitud siguiente devuelve los usuarios de la organización en formato JSON:

```http
GET https://graph.microsoft.com/v1.0/users?$format=json
```

[Probar en el Probador de Graph][format-example]

> **Nota**: El parámetro de consulta `$format` admite varios formatos, como atom, xml y json, pero puede que no todos los formatos devuelvan resultados.

## <a name="orderby-parameter"></a>parámetro orderby

Use el parámetro de consulta `$orderby` para especificar el criterio de ordenación de los elementos devueltos desde Microsoft Graph

Por ejemplo, la solicitud siguiente devuelve los usuarios de la organización ordenados por su nombre para mostrar:

```http
GET https://graph.microsoft.com/v1.0/users?$orderby=displayName
```
[Probar en el Probador de Graph][orderby-example]

También puede ordenar por entidades de tipo complejo. La solicitud siguiente obtiene los mensajes y los ordena por el campo **address** de la propiedad **from**, que es del tipo complejo **emailAddress**:

```http
GET https://graph.microsoft.com/v1.0/me/messages?$orderby=from/emailAddress/address
```
[Probar en el Probador de Graph](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$orderby=from/emailAddress/address&method=GET&version=v1.0)

Para ordenar los resultados en orden ascendente o descendente, anexe `asc` o `desc` al nombre del campo, separado por un espacio. Por ejemplo, `?$orderby=name%20desc`.

Con algunas API se pueden ordenar los resultados por varias propiedades. Por ejemplo, en la siguiente solicitud se ordenan los mensajes en la Bandeja de entrada del usuario; primero por el nombre de la persona que lo envió en orden descendente (de la Z a la A) y, después, por asunto en orden ascendente (el valor predeterminado).

```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/Inbox/messages?$orderby=from/emailAddress/name desc,subject
```

[Probar en el Probador de Graph](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$orderby=from/emailAddress/name%20desc,subject&method=GET&version=v1.0)

Si especifica $filter, el servidor deducirá un criterio de ordenación para los resultados. Si usa tanto `$orderby` como `$filter`, porque el servidor siempre deduce un criterio de ordenación para los resultados de un `$filter`, las propiedades del `$filter` deben estar primero en `$orderby`, antes que cualquier otra propiedad y deben estar en el orden en el que aparecen en el parámetro `$filter`. 

En el siguiente ejemplo, se muestra una consulta filtrada por las propiedades **subject** y **importance**, y después ordenada por las propiedades **subject**, **importance** y **receivedDateTime** en orden descendente.

```http
GET https://graph.microsoft.com/v1.0/me/messages?$filter=Subject eq 'welcome to exchange unified messaging' and importance eq 'normal'&$orderby=subject,importance,receivedDateTime desc
```

[Probar en el Probador de Graph](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$filter=subject%20eq%20%27welcome to exchange unified messaging%27%20and%20importance%20eq%20%27normal%27%20&$orderby=subject,importance,receivedDateTime%20desc&method=GET&version=v1.0)

 > **Nota:** Con recursos de Azure AD que se derivan de [directoryObject](../api-reference/v1.0/resources/directoryobject.md), como [user](../api-reference/v1.0/resources/user.md) y [group](../api-reference/v1.0/resources/group.md), no se puede combinar `$orderby` con expresiones`$filter`. 

## <a name="search-parameter"></a>parámetro de búsqueda

Use el parámetro de consulta `$search` para restringir los resultados de una solicitud para que coincidan con un criterio de búsqueda

> **Nota:** Actualmente **solo** se pueden buscar las colecciones [message](../api-reference/v1.0/resources/message.md) y [person](../api-reference/v1.0/resources/person.md). Una solicitud `$search` devuelve hasta 250 resultados. No puede usar [`$filter`](#filter-parameter) o [`$orderby`](#orderby-parameter) en una solicitud de búsqueda.

### <a name="using-search-on-message-collections"></a>Uso de $search en colecciones de mensajes

Las aplicaciones de Office 365, como Outlook y SharePoint, admiten la sintaxis del lenguaje de consulta de palabras clave (KQL) para realizar búsquedas. Esto proporciona la comodidad de un dominio de detección común para sus almacenes de datos. 

Cuando busca en las colecciones de mensajes, los resultados se ordenan por la fecha y la hora en que se ha enviado el mensaje. 

Puede especificar las siguientes propiedades en un **mensaje** en un criterio `$search`:

- **attachments**
- **bccRecipients**
- **body**
- **category**
- **ccRecipients**
- **content**
- **from**
- **hasAttachments**
- **participants**
- **receivedDateTime**
- **sender**
- **subject**
- **toRecipients**

Si realiza una búsqueda en mensajes y especifica un solo valor, la búsqueda se lleva a cabo con las propiedades de búsqueda predeterminadas de **from**, **subject** y **body**.

En el ejemplo siguiente, se devuelven todos los mensajes del buzón del usuario que ha iniciado sesión que contienen la palabra "pizza" en cualquiera de las tres propiedades de búsqueda predeterminadas:

```http
GET https://graph.microsoft.com/v1.0/me/messages?$search="pizza"
```

[Probar en el Probador de Graph][search-example]

En el ejemplo siguiente, se buscan todos los mensajes en el buzón del usuario que se enviaron desde una dirección de correo específica:

```http
GET https://graph.microsoft.com/v1.0/me/messages?$search="from:help@contoso.com"
```
Para obtener más información sobre KQL, como la sintaxis, operadores compatibles y sugerencias de búsqueda, vea los artículos siguientes:

- [Referencia de la sintaxis del lenguaje de consultas de palabras clave (KQL)](https://docs.microsoft.com/es-ES/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)

- 
  [Propiedades de mensajes y operadores de búsqueda para eDiscovery local en Exchange 2016](https://technet.microsoft.com/en-us/library/dn774955(v=exchg.160).aspx)

### <a name="using-search-on-person-collections"></a>Uso de $search en colecciones de usuarios

Puede usar la API de contactos de Microsoft Graph para recuperar los contactos más relevantes para un usuario. La relevancia viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario. La API de contactos admite el parámetro de consulta `$search`.

Las búsquedas de contactos se realizan en las propiedades **displayName** y **emailAddress** del recurso [person](../api-reference/v1.0/resources/person.md). Las búsquedas implementan un algoritmo de coincidencia aproximada. Se devolverán resultados basados en una coincidencia exacta y también en inferencias sobre la intención de la búsqueda. Por ejemplo, imagine un usuario con el nombre para mostrar "Tyler Lee" y la dirección de correo tylerle@example.com que se encuentra en la colección de **usuarios** del usuario que inició sesión. Todas las búsquedas siguientes devolverán resultados que contengan Tyler.

```http
GET https://graph.microsoft.com/v1.0/me/people?$search=tyler                //matches both Tyler's name and email
GET https://graph.microsoft.com/v1.0/me/people?$search=tylerle              //matches Tyler's email
GET https://graph.microsoft.com/v1.0/me/people?$search="tylerle@example.com"  //matches Tyler's email. Note the quotes to enclose '@'.
GET https://graph.microsoft.com/v1.0/me/people?$search=tiler                //fuzzy match with Tyler's name 
GET https://graph.microsoft.com/v1.0/me/people?$search="tyler lee"          //matches Tyler's name. Note the quotes to enclose the space.
```

También puede realizar búsquedas de contactos interesados en un tema determinado. Las búsquedas se realizan en función de inferencias derivadas de las conversaciones de correo del usuario. Por ejemplo, la búsqueda siguiente devolverá un conjunto de contactos relevantes para el usuario que inició sesión que han expresado interés en pizza en sus comunicaciones con el usuario. Tenga en cuenta que la frase de búsqueda se escribe entre comillas.

```http
GET https://graph.microsoft.com/v1.0/me/people/?$search="topic:pizza"                
```

Por último, puede combinar búsquedas de contactos y de temas en la misma solicitud mediante la combinación de los dos tipos de expresión de búsqueda.

```http
GET https://graph.microsoft.com/v1.0/me/people/?$search="tyl topic:pizza"                
```

Esta solicitud realiza básicamente dos búsquedas: una búsqueda parcial en las propiedades **displayName** y **emailAddress** de los contactos pertinentes del usuario que ha iniciado sesión, y una búsqueda de tema para "pizza" en los contactos pertinentes del usuario. Después, los resultados se clasificarán, se ordenarán y se devolverán. Tenga en cuenta que la búsqueda no es restrictiva; puede obtener resultados que contengan contactos que coincidan con "tyl" de forma aproximada, o que están interesados en "pizza", o ambos.

Para más información sobre la API de contactos, vea [Obtener información sobre contactos relevantes](./people_example.md).  

## <a name="select-parameter"></a>parámetro de selección

Use el parámetro de consulta `$select` para devolver un conjunto de propiedades diferente al predeterminado para un recurso individual o una colección de recursos. Con $select, puede especificar un subconjunto o un superconjunto de las propiedades predeterminadas.

Por ejemplo, al recuperar los mensajes del usuario que ha iniciado sesión, puede especificar que solo se devuelvan las propiedades **from** y **subject**:

```http
GET https://graph.microsoft.com/v1.0/me/messages?$select=from,subject
```

[Probar en el Probador de Graph][select-example]

> **Importante:** En general, se recomienda usar `$select` para limitar las propiedades devueltas por una consulta a las necesarias para la aplicación. Esto es especialmente cierto para las consultas que potencialmente pueden devolver un conjunto de resultados grande. Limitar las propiedades devueltas en cada fila reducirá la carga en la red y ayudará a mejorar el rendimiento de la aplicación.
>
> En `v1.0`, algunos recursos de Azure AD que se derivan de [directoryObject](../api-reference/v1.0/resources/directoryobject.md), como [user](../api-reference/v1.0/resources/user.md) y [group](../api-reference/v1.0/resources/group.md), devuelven un subconjunto predeterminado limitado de propiedades en las operaciones de lectura. Para estos recursos, debe usar `$select` para devolver propiedades fuera el conjunto predeterminado.  

## <a name="skip-parameter"></a>parámetros de omisión

Use el parámetro de consulta `$skip` para establecer el número de elementos que se omitirán al inicio de una colección. Por ejemplo, la solicitud siguiente devuelve eventos para el usuario ordenados por fecha de creación, empezando por el evento 21 de la colección:

```http
GET  https://graph.microsoft.com/v1.0/me/events?$orderby=createdDateTime&$skip=20
```
[Probar en el Probador de Graph][skip-example]

> **Nota:** En algunas API de Microsoft Graph, como Correo y Calendario de Outlook (**message**, **event** y **calendar**), se usa `$skip` para implementar la paginación. Cuando los resultados de una consulta ocupen varias páginas, estas API devolverán una propiedad `@odata:nextLink` con una dirección URL que contendrá un parámetro `$skip`. Puede usar esta dirección URL para devolver la siguiente página de resultados. Para obtener más información, vea [Paginación](./paging.md).

## <a name="skiptoken-parameter"></a>parámetro skipToken

Algunas consultas devuelven varias páginas de datos debido a la paginación del servidor o al uso del parámetro [`$top`](#top-parameter) para limitar el tamaño de página de la respuesta. Muchas API de Microsoft Graph usan el parámetro de consulta `skipToken` para hacer referencia a las páginas siguientes del resultado. El parámetro `$skiptoken` contiene un token opaco que hace referencia a la siguiente página de resultados y se devuelve en la dirección URL proporcionada en la propiedad `@odata.nextLink` en la respuesta. Para obtener más información, vea [Paginación](./paging.md).


## <a name="top-parameter"></a>parámetro superior

Use el parámetro de consulta `$top` para especificar el tamaño de página del conjunto de resultados. 

Si quedan más elementos en el conjunto de resultados, el cuerpo de la respuesta contendrá un parámetro `@odata.nextLink`. Este parámetro contiene una dirección URL que se puede usar para obtener la siguiente página de resultados. Para obtener más información, vea [Paginación](./paging.md). 

Por ejemplo, la solicitud siguiente devuelve los cinco primeros mensajes en el buzón del usuario:

```http
GET https://graph.microsoft.com/v1.0/me/messages?$top=5
```

[Probar en el Probador de Graph][top-example]


## <a name="error-handling-for-query-parameters"></a>Control de errores para parámetros de consulta

Algunas solicitudes devolverán un mensaje de error si no se admite un parámetro de consulta especificado. Por ejemplo, no se puede usar `$expand` en la relación `user/photo`. 

```http
https://graph.microsoft.com/beta/me?$expand=photo
```

```json
{
    "error":{
        "code":"ExpandNotSupported",
        "message":"Expand is not allowed for property 'Photo' according to the entity schema.",
        "innerError":{
            "request-id":"1653fefd-bc31-484b-bb10-8dc33cb853ec",
            "date":"2017-07-31T20:55:01"
        }
    }
}
```

Pero es importante tener en cuenta que los parámetros de consulta especificados en una solicitud pueden devolver un error silenciosamente. Esto puede suceder con parámetros de consulta no admitidos, así como con combinaciones no compatibles de parámetros de consulta. En estos casos, debe examinar los datos devueltos por la solicitud para determinar si los parámetros de consulta especificados tuvieron el efecto previsto. 

[graph-explorer]: https://developer.microsoft.com/graph/graph-explorer
[odata-filter]: http://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part2-url-conventions/odata-v4.0-errata03-os-part2-url-conventions-complete.html#_Toc453752358
[odata-query]: http://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part2-url-conventions/odata-v4.0-errata03-os-part2-url-conventions-complete.html#_Toc453752356
[count-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$top=2%26$count=true&method=GET&version=v1.0
[expand-example]: https://developer.microsoft.com/graph/graph-explorer?request=groups$expand=members&method=GET&version=v1.0
[filter-example]: https://developer.microsoft.com/graph/graph-explorer?request=users?$filter=startswith(givenName,'J')&method=GET&version=v1.0
[format-example]: https://developer.microsoft.com/graph/graph-explorer?request=users?$format=json&method=GET&version=v1.0
[orderby-example]: https://developer.microsoft.com/graph/graph-explorer?request=users?$orderby=displayName%20DESC&method=GET&version=v1.0
[search-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=pizza&method=GET&version=v1.0
[select-example]: https://developer.microsoft.com/graph/graph-explorer?request=users?$select=givenName,surname&method=GET&version=v1.0
[skip-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$skip=11&method=GET&version=v1.0
[top-example]: https://developer.microsoft.com/graph/graph-explorer?request=users?$top=2&method=GET&version=v1.0


