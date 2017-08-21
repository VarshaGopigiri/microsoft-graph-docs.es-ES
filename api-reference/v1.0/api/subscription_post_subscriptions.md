# <a name="create-subscription"></a>Crear suscripción

Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos en Microsoft Graph.
## <a name="prerequisites"></a>Requisitos previos
La creación de una suscripción requiere un ámbito de lectura para el recurso. Por ejemplo, para obtener mensajes de notificaciones, la aplicación necesita el permiso `Mail.Read`. En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso.

| Tipo de recurso o elemento        | Ámbito               |
|-----------------------------|---------------------|
| Contactos                    | Contacts.Read       |
| Conversaciones               | Group.Read.All      |
| Eventos                      | Calendars.Read      |
| Mensajes                    | Mail.Read           |
| Unidad de disco (OneDrive del usuario)    | Files.ReadWrite     |
| Unidades de disco (unidades de disco y contenido compartido de SharePoint) | Files.ReadWrite.All |

 ***Nota:*** El punto de conexión /v1.0 permite permisos de aplicación para la mayoría de recursos. Las conversaciones de un grupo y los elementos de raíz de unidad de OneDrive no son compatibles con los permisos de la aplicación.

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->

```http
POST /subscriptions

```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y un objeto de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Este es un ejemplo de solicitud para enviar una notificación cuando el usuario recibe un nuevo correo electrónico.
<!-- {
  "blockType": "request",
  "name": "create_subscription_from_subscriptions"
}-->
```http
POST https://graph.microsoft.com/v1.0/subscriptions
Content-type: application/json

{
   "changeType": "created,updated",
   "notificationUrl": "https://webhook.azurewebsites.net/api/send/myNotifyClient",
   "resource": "me/mailFolders('Inbox')/messages",
   "expirationDateTime":"2016-11-20T18:23:45.9356913Z",
   "clientState": "subscription-identifier"
}
```
En el cuerpo de la solicitud, proporcione una representación JSON del objeto de [suscripción](../resources/subscription.md). El campo *clientState* es opcional.

##### <a name="resources-examples"></a>Ejemplos de recursos
A continuación puede ver algunos valores válidos para la propiedad de recurso de la suscripción:

| Tipo de recurso | Ejemplos |
|:------ |:----- |
|Correo|me/mailfolders("inbox")/messages<br />me/messages|
|Contactos|me/contacts|
|Calendarios|me/events|
|Conversaciones|groups("*{id}*")/conversations|
|Unidades|me/drive/root|

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.subscription"
} -->
```http
HTTP/1.1 201 Created

{
  "id":"7f105c7d-2dc5-4530-97cd-4e7ae6534c07",
  "resource":"me/mailFolders('Inbox')/messages",
  "changeType":"created, updated",
  "clientState":"subscription-identifier",
  "notificationUrl":"https://webhook.azurewebsites.net/api/send/myNotifyClient",
  "expirationDateTime":"2016-11-20T18:23:45.9356913Z"
}
```
## <a name="subscription-validation"></a>Validación de suscripciones
Para evitar que las suscripciones equivocadas envíen notificaciones a direcciones URL arbitrarias, el extremo de la notificación de suscripción debe ser capaz de responder a una solicitud de validación. Durante el procesamiento del `POST` al extremo de `/subscriptions`, Microsoft Graph enviará una solicitud de `POST` a su `notificationUrl` de la siguiente forma: 
```http
POST https://webhook.azurewebsites.net/api/send/myNotifyClient?validationToken=<token>
```
El extremo de notificación debe enviar en menos de 10 segundos una respuesta 200 con el valor `<token>` como cuerpo y un tipo de contenido `text/plain`, como se muestra a continuación, o se descartará la solicitud de creación.
```http
HTTP/1.1 200 OK
Content-type: text/plain
Content-length: 7
<token>
```
## <a name="notification-payload"></a>Carga de notificaciones
Cuando el recurso suscrito cambia, la herramienta de webhooks envía una notificación a su dirección URL de notificación con la siguiente carga.  El extremo de notificación debe enviar una respuesta 200 o 204 sin cuerpo de respuesta en menos de 30 segundos o se intentará volver a enviar la notificación en intervalos que aumentan de manera exponencial.  Los servicios que tardan constantemente 30 segundos o más pueden limitarse y recibir un conjunto de notificaciones más escaso.

Los servicios también pueden devolver una respuesta 422 desde una notificación, en cuyo caso la suscripción se eliminará automáticamente y la secuencia de notificaciones se detendrá.

En función del recurso suscrito, un campo resourceData adicional puede proporcionar más información.

```http
{
   "value":[
      {
         "subscriptionId":"7f105c7d-2dc5-4530-97cd-4e7ae6534c07",
         "subscriptionExpirationDateTime":"2015-11-20T18:23:45.9356913Z",
         "clientState":"subscription-identifier",
         "changeType":"Created",
         "resource":"Users/ddfcd489-628b-7d04-b48b-20075df800e5@1717622f-1d94-c0d4-9d74-f907ad6677b4/messages/AAMkADMxZmEzMDM1LTFjODQtNGVkMC04YzY3LTBjZTRlNDFjNGE4MwBGAAAAAAAr-q_ZG7oXSaqxum7oZW5RBwCoeN6SYXGLRrvRm_CYrrfQAAAAAAEMAACoeN6SYXGLRrvRm_CYrrfQAACvtMe6AAA=",
         "resourceData":{
            "@odata.type":"#Microsoft.Graph.Message",
            "@odata.id":"Users/ddfcd489-628b-7d04-b48b-20075df800e5@1717622f-1d94-c0d4-9d74-f907ad6677b4/messages/AAMkADMxZmEzMDM1LTFjODQtNGVkMC04YzY3LTBjZTRlNDFjNGE4MwBGAAAAAAAr-q_ZG7oXSaqxum7oZW5RBwCoeN6SYXGLRrvRm_CYrrfQAAAAAAEMAACoeN6SYXGLRrvRm_CYrrfQAACvtMe6AAA=",
            "@odata.etag":"W/\"CQAAABYAAACoeN6SYXGLRrvRm+CYrrfQAACvvGdb\"",
            "Id":"AAMkADMxZmEzMDM1LTFjODQtNGVkMC04YzY3LTBjZTRlNDFjNGE4MwBGAAAAAAAr-q_ZG7oXSaqxum7oZW5RBwCoeN6SYXGLRrvRm_CYrrfQAAAAAAEMAACoeN6SYXGLRrvRm_CYrrfQAACvtMe6AAA="
         }
      }
   ]
}
```
Al recibir notificaciones de suscripciones de unidad, el campo resourceData será NULL y se deberá llamar a la API de [delta](item_delta.md) para determinar los cambios que han ocurrido. Aquí tiene un ejemplo de notificación de unidad:
```http
{
  "subscriptionId": "aa269f87-2a92-4cff-a43e-2771878c3727",
  "clientState": "My client state",
  "changeType": "updated",
  "resource": "me/drive/root",
  "subscriptionExpirationDateTime": "2016-08-26T23:08:37.00+00:00",
  "resourceData": null
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
