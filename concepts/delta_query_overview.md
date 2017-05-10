#  <a name="use-delta-query-to-track-changes-in-microsoft-graph-data-preview"></a>Usar la consulta de delta para realizar el seguimiento de los cambios en datos de Microsoft Graph (versión preliminar)

La consulta de delta permite a las aplicaciones detectar entidades recién creadas, actualizadas o eliminadas sin realizar una operación de lectura completa del recurso de destino con cada solicitud. Las aplicaciones de Microsoft Graph pueden usar consultas de delta para sincronizar los cambios de forma eficaz con un almacén de datos local.

## <a name="use-delta-query-to-track-changes-in-a-resource-collection"></a>Usar la consulta de delta para realizar el seguimiento de los cambios en una colección de recursos

El patrón de llamada típico es el siguiente:

1.  La aplicación empieza con una llamada a una solicitud GET con la función delta en el recurso deseado.
2.  Microsoft Graph enviará una respuesta que contiene el recurso solicitado y un [token de estado](#state-tokens).

     a.  Si se devuelve una dirección URL `nextLink`, hay más páginas de datos para recuperar en la sesión. La aplicación continúa realizando solicitudes mediante la dirección URL `nextLink` hasta que se incluya dirección URL `deltaLink` en la respuesta.

     b.  Si se devuelve dirección URL `deltaLink`, no hay más datos sobre el estado existente del recurso para devolver. Para las solicitudes futuras, la aplicación usa la dirección URL `deltaLink` para obtener información sobre los cambios en el recurso.
     
3.  Cuando la aplicación necesita obtener información sobre los cambios en el recurso, realiza una nueva solicitud con la dirección URL `deltaLink` recibida en el paso 2. Esta solicitud *puede* realizarse inmediatamente después de completar el paso 2, o cuando la aplicación comprueba los cambios.
4.  Microsoft Graph devuelve una respuesta que describe los cambios en el recurso desde la solicitud anterior, y una dirección URL `nextLink` o `deltaLink`.

### <a name="state-tokens"></a>Tokens de estado

Una respuesta GET de consulta de delta siempre incluye una dirección URL especificada en un encabezado de respuesta `nextLink` o `deltaLink`. La dirección URL `nextLink` incluye un _skipToken_ y una dirección URL `deltaLink` incluye un _deltaToken_. 

Estos tokens son opacos para el cliente. A continuación se muestra la información que necesita saber sobre ellos:

- Cada token refleja el estado y representa una instantánea del recurso en esa ronda de seguimiento de cambios. 
- Los tokens de estado también codifican e incluyen otros parámetros de consulta (como `$select`) especificados en la solicitud de consulta de delta inicial. Por lo tanto, no es necesario repetirlos en las solicitudes de consulta de delta siguientes.
- Al llevar a cabo consultas de delta, puede copiar y aplicar las direcciones URL `nextLink` o `deltaLink` a la siguiente llamada a función **delta** sin tener que examinar el contenido de la dirección URL, incluido su token de estado.


### <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Si un cliente usa un parámetro de consulta, debe especificarse en la solicitud inicial. Microsoft Graph codifica automáticamente el parámetro especificado en los `nextLink` o `deltaLink` proporcionados en la respuesta. La aplicación de llamada solo necesita especificar los parámetros de consulta deseados una vez por adelantado. Microsoft Graph agrega los parámetros especificados automáticamente para todas las solicitudes subsiguientes.

Para los usuarios y grupos, existen restricciones en el uso de algunos parámetros de la consulta:

-   Si se usa un parámetro de consulta `$select`, este indica que el cliente prefiere registrar los cambios solo en las propiedades o relaciones especificadas en la instrucción `$select`. Si se produce un cambio en una propiedad que no está activada, el recurso en el que se ha producido el cambio no aparecerá en la respuesta de delta tras una solicitud posterior.
-   `$expand` no es compatible.

## <a name="resource-representation-in-the-delta-query-response"></a>Representación de recursos en la respuesta de consulta de delta

-   Las instancias de un recurso compatible recién creadas se representan en la respuesta de consulta de delta con su representación estándar.

-   Instancias actualizadas están representadas por sus **id** con *al menos* las propiedades que se han actualizado, aunque pueden incluirse otras propiedades.

-   Los cambios en las relaciones de usuarios y grupos se representan como anotaciones en la representación de recursos estándar. Estas anotaciones usan el formato `propertyName@delta` y solo aparecen si el cliente decide realizar el seguimiento de los cambios en la relación con el parámetro `$select` de forma explícita.

-   Las instancias eliminadas se representan solo con sus **id** y un nodo `@removed`. El nodo `@removed` puede incluir información adicional sobre por qué se quitó la instancia.

> **Nota acerca de futuros cambios**: Instancias eliminadas aparecen actualmente con el nodo `@removed` con el siguiente formato *"@removed": "razón de eliminación"*. Sin embargo, se introducirá un cambio importante en el futuro. Antes de que la consulta de delta pase de /beta a /v1.0, se anidará un objeto en el nodo quitado para dar más información. Por ejemplo, *@removed {motivo: "motivo de eliminación"}*. Este objeto puede ampliarse en el futuro para incluir metadatos adicionales sobre la eliminación.

## <a name="supported-resources"></a>Recursos admitidos

La consulta de delta se admite actualmente en versión preliminar en el punto de conexión /beta de Microsoft Graph para los siguientes recursos.

| **Colección de recursos** | **API** |
|:------ | :------ |
| Eventos en una vista de calendario (intervalo de fechas) del calendario principal | La función [delta](../api-reference/beta/api/event_delta.md) del recurso [event](../api-reference/beta/resources/event.md) |
| Grupos | La función [delta](../api-reference/beta/api/group_delta.md) del recurso [group](../api-reference/beta/resources/group.md) |
| Carpetas de correo | La función [delta](../api-reference/beta/api/mailfolder_delta.md) del recurso [mailFolder](../api-reference/beta/resources/mailFolder.md) |
| Mensajes de una carpeta | La función [delta](../api-reference/beta/api/message_delta.md) del recurso [message](../api-reference/beta/resources/message.md) | 
| Carpetas de contactos personales | La función [delta](../api-reference/beta/api/contactfolder_delta.md) del recurso [contactFolder](../api-reference/beta/resources/contactfolder.md) |
| Contactos personales en una carpeta | La función [delta](../api-reference/beta/api/contact_delta.md) del recurso [contact](../api-reference/beta/resources/contact.md) |
| Usuarios | La función [delta](../api-reference/beta/api/user_delta.md) del recurso [user](../api-reference/beta/resources/user.md) | 
| Elementos de la unidad\* | La función [delta](../api-reference/beta/api/item_delta.md) del recurso [driveItem](../api-reference/beta/resources/driveItem.md) |


> \* La v1.0 ya es compatible con el seguimiento de cambios a unidades y sus elementos secundarios. El patrón de uso es similar a los demás recursos compatibles con algunas diferencias secundarias de sintaxis. La consulta de delta para unidades se actualizará en el futuro para que sea coherente con otros tipos de recursos. Para obtener más detalles sobre la sintaxis actual, vea: <https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/item_delta>

## <a name="prerequisites"></a>Requisitos previos

Los mismos [permisos](../authorization/permission_scopes.md) que se requieren para leer un recurso específico también son necesarios para realizar la consulta de delta en ellos.

## <a name="known-limitations"></a>Limitaciones conocidas

Para ver las limitaciones conocidas al usar la consulta de delta, consulte la [sección Consulta de delta](../overview/release_notes.md#delta-query) del artículo de problemas conocidos.

## <a name="delta-query-request-examples"></a>Ejemplos de solicitud de consulta de Delta 

- [Obtener cambios incrementales para los eventos en una vista de calendario (versión preliminar)](../Concepts/delta_query_events.md)
- [Obtener los cambios incrementales para los mensajes de una carpeta (versión preliminar)](./delta_query_messages.md)
- [Obtener los cambios incrementales de grupos (versión preliminar)](./delta_query_groups.md)
- [Obtener los cambios incrementales de usuarios (versión preliminar)](./delta_query_users.md)