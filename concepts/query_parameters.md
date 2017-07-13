# Usar parámetros de consulta para personalizar respuestas
<a id="use-query-parameters-to-customize-responses" class="xliff"></a>

Microsoft Graph proporciona parámetros de consulta opcionales que puede usar para especificar y controlar la cantidad de datos devueltos en una respuesta. Se admiten los siguientes parámetros de consulta.

|Nombre|Descripción|Ejemplo (haga clic en los ejemplos para probar en [Probador de Graph][graph-explorer])
|:---------------|:--------|:-------|
|[$filter](#filter)|Filtra los resultados (filas).|[`/users?$filter=startswith(givenName,'J')`](https://developer.microsoft.com/en-us/graph/graph-explorer?request=users?$filter=startswith(givenName,'J')&method=GET&version=v1.0)
|[$select](#select)|Filtra las propiedades (columnas).|[`/users?$select=givenName,surname`](https://developer.microsoft.com/en-us/graph/graph-explorer?request=users?$select=givenName,surname&method=GET&version=v1.0)
|[$expand](#expand)|Recupera los recursos relacionados.|[`/groups/{id}?$expand=members`](https://developer.microsoft.com/en-us/graph/graph-explorer?request=groups/22be6ccb-15a5-459f-94ac-d1393bdd9e66?$expand=members&method=GET&version=v1.0)
|[$orderby](#orderby)|Ordena los resultados.|[`/users?$orderby=displayName,userPrincipalName desc`](https://developer.microsoft.com/en-us/graph/graph-explorer?request=users?$orderby=displayName,userPrincipalName%20DESC&method=GET&version=v1.0)
|[$top](#top)|Limita los resultados. Se usa normalmente con `$skipToken`.|[`/users?$top=2`](https://developer.microsoft.com/en-us/graph/graph-explorer?request=users?$top=2&method=GET&version=v1.0)
|[$skipToken](#skiptoken)|Se usa con `$top` para recuperar una página de resultados.|Vea `nextLink` desde la consulta $top para obtener un ejemplo.
|[$count](#count)|Recupera el número total de recursos coincidentes.|[`/me/messages?$top=2&$count=true`](https://developer.microsoft.com/en-us/graph/graph-explorer?request=me/messages?$top=2%26$count=true&method=GET&version=v1.0)
<!-- TODO: figure out whether $search is actually used
|[`$search`](#search)|A property and value pair separated by a colon.|
-->

Estos parámetros son compatibles con el [lenguaje de consulta de OData V4][odata-query].

> **Nota:** En el punto de conexión `beta`, el prefijo `$` es opcional. Por ejemplo, en lugar de `$filter`, puede usar `filter`. Para obtener más detalles y ejemplos, vea [Compatibilidad con los parámetros de consulta sin el prefijo "$" en Microsoft Graph](http://dev.office.com/queryparametersinMicrosoftGraph).

**Codificación de los parámetros de consulta:**

Los valores de los parámetros de consulta deben ser codificados por porcentaje. Muchos clientes, exploradores y herramientas HTTP (por ejemplo, el [Probador de Graph][graph-explorer]) le servirán de ayuda. Si una consulta produce un error, una razón posible es el error al codificar los valores de los parámetros de consulta correctamente.

Una dirección URL sin codificar tiene el siguiente aspecto:

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(givenName, 'J')
```

Una dirección URL codificada correctamente tiene el siguiente aspecto:

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(givenName%2C+'J')
```

## filter
<a id="filter" class="xliff"></a>

`$filter` puede usarse para recuperar solo un subconjunto de una colección. Por ejemplo, para buscar usuarios cuyos nombres para mostrar comiencen por `J`, use `startswith`.

[Probar en el Probador de Graph](https://developer.microsoft.com/en-us/graph/graph-explorer?request=users?$filter=startswith(givenName,'J')&method=GET&version=v1.0)

**Solicitud:**

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(displayName,'J')
```

**Respuesta:**

```json
{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users",
    "value": [
        {
            "id": "e013b9f3-a1ab-48d1-907b-e716c39d6363",
            "businessPhones": [
                "4255550100"
            ],
            "displayName": "Jan Madden",
            "givenName": "Jan",
            "jobTitle": null,
            "mail": "demo32@a830edad9050849NDA1.onmicrosoft.com",
            "mobilePhone": null,
            "officeLocation": null,
            "preferredLanguage": null,
            "surname": "Madden",
            "userPrincipalName": "demo32@a830edad9050849NDA1.onmicrosoft.com"
        },
        {
            "id": "89efe8ed-d141-4151-a3e4-570a70022dff",
            "businessPhones": [
                "+1 425 555 0109"
            ],
            "displayName": "Janet Schorr",
            "givenName": "Janet",
            "jobTitle": "Product Marketing Manager",
            "mail": "janets@a830edad9050849NDA1.onmicrosoft.com",
            "mobilePhone": null,
            "officeLocation": "18/2111",
            "preferredLanguage": null,
            "surname": "Schorr",
            "userPrincipalName": "janets@a830edad9050849NDA1.onmicrosoft.com"
        },
        ...
    ]
}
```

`$filter` tiene una sintaxis muy rica y expresiva con muchos operadores integrados. Los operadores lógicos incluyen es igual a (`eq`), no es igual a (`ne`), mayor que (`gt`), mayor o igual que (`gte`) y (`and`), o (`or`), no (`not`) etc. Los operadores aritméticos incluyen sumar (`add`), restar (`sub`), etc. Los operadores de cadena incluyen contiene (`contains`), empieza con (`startswith`), etc. Los operadores lambda incluyen cualquier (`any`) y todos (`all`). Para obtener detalles adicionales sobre la sintaxis `$filter`, vea el [protocolo OData][odata-filter].


## select
<a id="select" class="xliff"></a>

En una colección o una entidad individual, para especificar un conjunto diferente de propiedades que se van a devolver en lugar del conjunto predeterminado, use el parámetro de consulta `$select`. El parámetro `$select` permite elegir un subconjunto o un superconjunto del conjunto predeterminado que se haya devuelto. Por ejemplo, al recuperar los mensajes, quizás quiera que solo se devuelvan las propiedades `from` y `subject` de los mensajes.

```http
GET https://graph.microsoft.com/v1.0/me/messages?$select=from,subject
```

<!--For example, when retrieving the children of an item on a drive, you want to select that only the `name` and `size` properties of items are returned.

```http
GET https://graph.microsoft.com/v1.0/me/drive/root/children?$select=name,size
```

By submitting the request with the `$select=name,size` query string, the objects
in the response will only have those property values included.

```json
{
  "value": [
    {
      "id": "13140a9sd9aba",
      "name": "Documents",
      "size": 1024
    },
    {
      "id": "123901909124a",
      "name": "Pictures",
      "size": 1012010210
    }
  ]
}
```-->

## expand
<a id="expand" class="xliff"></a>

En las solicitudes de la API de Microsoft Graph, las navegaciones a un objeto o a una colección del elemento al que se hace referencia no se expanden automáticamente. Esto es así por diseño para reducir el tráfico de la red y el tiempo que se tarda en generar una respuesta desde el servicio. Sin embargo, en algunos casos puede que desee incluir esos resultados en una respuesta.

Puede usar el parámetro de cadena de consulta `$expand` para indicar a la API que expanda una colección u objeto secundarios y que incluya esos resultados.

Por ejemplo, para recuperar la información de la unidad raíz y los elementos secundarios del nivel superior en una unidad, use el parámetro `$expand`. En este ejemplo, también se usa una instrucción [`$select`](#select) para devolver solo las propiedades `id` y `name` de los elementos secundarios.

```http
GET https://graph.microsoft.com/v1.0/me/drive/root?$expand=children($select=id,name)
```

> **Nota:** El número máximo de objetos expandidos para una solicitud es 20. Asimismo, si realiza una consulta en el recurso [`user`](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/user), puede usar `$expand` para obtener las propiedades de un solo objeto secundario o de una colección a la vez. El ejemplo siguiente obtiene objetos `user`, cada uno con hasta 20 objetos `directReport` en la colección `directReports` ampliada:

```http
GET https://graph.microsoft.com/v1.0/users?$expand=directReports
```

Otros recursos también pueden tener un límite, así que siempre compruébelo para evitar posibles errores.

## orderby
<a id="orderby" class="xliff"></a>

Para especificar el orden de clasificación de los elementos devueltos de la API de Microsoft Graph, use el parámetro de consulta `$orderby`.

Por ejemplo, para devolver los usuarios de la organización ordenados por su nombre para mostrar, la sintaxis será la siguiente:

```http
GET https://graph.microsoft.com/v1.0/users?$orderby=displayName
```

También puede ordenar por entidades de tipo complejo. En el ejemplo siguiente se obtienen los mensajes y los ordena por el campo `address` de la propiedad `from`, que es del tipo complejo `emailAddress`:

```http
GET https://graph.microsoft.com/v1.0/me/messages?$orderby=from/emailAddress/address
```

Para ordenar los resultados en orden ascendente o descendente, anexe `asc` o `desc` al nombre del campo, separado por un espacio. Por ejemplo, `?$orderby=name%20desc`.

 > **Nota:** Si realiza una consulta en el recurso de [`user`](../api-reference/v1.0/resources/user.md), `$orderby` no se podrá combinar con expresiones de filtro.

## top
<a id="top" class="xliff"></a>

Para especificar el número máximo de elementos a devolver en un conjunto de resultados, use el parámetro de consulta `$top`. El parámetro de consulta `$top` identifica un subconjunto de la colección. Este subconjunto se forma al seleccionar solo los primeros N elementos del conjunto, donde N es un entero positivo especificado mediante este parámetro de consulta. Por ejemplo, para devolver los cinco primeros mensajes en el buzón del usuario, la sintaxis es la siguiente:

```http
GET https://graph.microsoft.com/v1.0/me/messages?$top=5
```

## skip
<a id="skip" class="xliff"></a>

Para establecer el número de elementos que se omitirán antes de recuperar elementos de una colección, use el parámetro de consulta `$skip`. Por ejemplo, para que se devuelvan los eventos ordenados por fecha de creación y comenzando por el evento 21, la sintaxis será la siguiente:

```http
GET  https://graph.microsoft.com/v1.0/me/events?$orderby=createdDateTime&$skip=20
```

## skipToken
<a id="skiptoken" class="xliff"></a>

Para solicitar la segunda y las páginas posteriores de datos de Graph, use el parámetro de consulta `$skipToken`. El parámetro de consulta `$skipToken` se proporciona en direcciones URL devueltas de Graph cuando este ha devuelto un subconjunto parcial de resultados, normalmente debido a la paginación del lado del servidor. Identifica en una colección el punto en el que el servidor ha terminado de enviar los resultados y se devuelve a Graph para indicar el punto desde el cual debe reanudar el envío de los resultados. Por ejemplo, el valor de un parámetro de consulta `$skipToken` podría identificar el décimo elemento de una colección o el número 20 de una colección que contuviera 50, o bien cualquier otra posición de la colección.

En algunas respuestas, verá un valor `@odata.nextLink`. Algunas de ellas incluirán un valor `$skipToken`. El valor `$skipToken` es como un marcador que indica al servicio el punto en el que deberá reanudarse para obtener el siguiente conjunto de resultados. El siguiente es un ejemplo de un valor `@odata.nextLink` de una respuesta en la que se han solicitado los usuarios ordenados por `displayName`:

```json
"@odata.nextLink": "https://graph.microsoft.com/v1.0/users?$orderby=displayName&$skiptoken=X%2783630372100000000000000000000%27"
```

Para devolver la siguiente página de usuarios de su organización, la sintaxis será como la que se muestra a continuación.

```http
GET  https://graph.microsoft.com/v1.0/users?$orderby=displayName&$skiptoken=X%2783630372100000000000000000000%27
```

## count
<a id="count" class="xliff"></a>

Use `$count` como parámetro de consulta para incluir un recuento del número total de elementos de una colección junto con la página de valores de datos que se devuelve de Graph, como en el ejemplo siguiente:

```http
GET  https://graph.microsoft.com/v1.0/me/contacts?$count=true
```

Esta acción devolvería tanto la colección de `contacts` como el número de elementos de la colección de `contacts` en la propiedad `@odata.count`.

>**Nota:** Esto no es compatible con las colecciones de [`directoryObject`](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/directoryobject).

## search
<a id="search" class="xliff"></a>

Para restringir los resultados de una solicitud que coincidan con un criterio de búsqueda, use el parámetro de consulta `$search`.

> **Nota:** Actualmente **solo** puede buscar las colecciones [message](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/message) y [person](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/resources/person). Una solicitud `$search` devuelve hasta 250 resultados. No puede usar [`$filter`](#filter) o [`$orderby`](#orderby) en una solicitud de búsqueda.

Los criterios de búsqueda se expresan mediante la Sintaxis de consulta avanzada (AQS). Los resultados se ordenan por la fecha y la hora en que se ha enviado el mensaje.

Puede especificar las siguientes propiedades en `message` en un criterio `$search`: `attachments`, `bccRecipients`, `body`, `category`, `ccRecipients`, `content`, `from`, `hasAttachments`, `participants`, `receivedDateTime`, `sender`, `subject`, `toRecipients`

Si realiza una búsqueda en mensajes y especifica un solo valor, la búsqueda se realiza con las propiedades de búsqueda predeterminadas de `from`, `subject` y `body`.

En el ejemplo siguiente, se devuelven todos los mensajes del buzón del usuario que ha iniciado sesión que contienen la palabra "pizza" en cualquiera de las tres propiedades de búsqueda predeterminadas:

```http
GET https://graph.microsoft.com/v1.0/me/messages?$search="pizza"
```

En el ejemplo siguiente se buscan todos los mensajes en el buzón del usuario que se enviaron desde una dirección de correo específica:

```http
GET https://graph.microsoft.com/v1.0/me/messages?$search="from:help@contoso.com"
```

[graph-explorer]: https://graph.microsoft.io/en-us/graph-explorer
[odata-filter]: http://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part2-url-conventions/odata-v4.0-errata03-os-part2-url-conventions-complete.html#_Toc453752358
[odata-query]: http://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part2-url-conventions/odata-v4.0-errata03-os-part2-url-conventions-complete.html#_Toc453752356
