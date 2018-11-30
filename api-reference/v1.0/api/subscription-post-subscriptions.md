---
title: Crear suscripción
description: Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos en Microsoft Graph.
ms.openlocfilehash: 72f9a2d97733901ea4d543045d85be60978c5e5c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030527"
---
# <a name="create-subscription"></a>Crear suscripción

Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos en Microsoft Graph.

## <a name="permissions"></a>Permisos

La creación de una suscripción requiere un ámbito de lectura para el recurso. Por ejemplo, para obtener mensajes de notificaciones, la aplicación necesita el permiso `Mail.Read`. En la tabla siguiente se muestra el permiso propuesto que se necesita para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de recurso o elemento        | Permiso          |
|-----------------------------|---------------------|
| Contactos                    | Contacts.Read       |
| Conversaciones               | Group.Read.All      |
| Eventos                      | Calendars.Read      |
| Mensajes                    | Mail.Read           |
| Groups                      | Group.Read.All      |
| Users                       | User.Read.All       |
| Unidad de disco (OneDrive del usuario)    | Files.ReadWrite     |
| Unidades (contenido de SharePoint compartido y unidades) | Files.ReadWrite.All |
|Alerta de seguridad| SecurityEvents.ReadWrite.All |

 > **Nota:** El extremo de /v1.0 permite que los permisos de aplicación para la mayoría de los recursos. Las conversaciones de un grupo y OneDrive para la unidad raíz los elementos no son compatibles con los permisos de la aplicación.

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

Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.

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
   "clientState": "secretClientValue"
}
```

En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [suscripción](../resources/subscription.md) .
El `clientState` campo es opcional.

##### <a name="resources-examples"></a>Ejemplos de recursos

A continuación puede ver algunos valores válidos para la propiedad de recurso de la suscripción:

| Tipo de recurso | Ejemplos |
|:------ |:----- |
|Correo|me/mailfolders("inbox")/messages<br />me/messages|
|Contactos|me/contacts|
|Calendarios|me/events|
|Users|users|
|Groups|grupos|
|Conversaciones|groups("*{id}*")/conversations|
|Unidades|me/drive/root|
|Alerta de seguridad|alertas de seguridad /? $filter = estado eq 'New'|

##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.subscription"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 252

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#subscriptions/$entity",
  "id": "7f105c7d-2dc5-4530-97cd-4e7ae6534c07",
  "resource": "me/mailFolders('Inbox')/messages",
  "applicationId": "24d3b144-21ae-4080-943f-7067b395b913",
  "changeType": "created,updated",
  "clientState": "secretClientValue",
  "notificationUrl": "https://webhook.azurewebsites.net/api/send/myNotifyClient",
  "expirationDateTime": "2016-11-20T18:23:45.9356913Z",
  "creatorId": "8ee44408-0679-472c-bc2a-692812af3437"
}
```

## <a name="notification-endpoint-validation"></a>Validación de extremo de notificación

El extremo de la notificación de suscripción (especificado en el `notificationUrl` (propiedad)) debe ser capaz de responder a una solicitud de validación, como se describe en [Configurar notificaciones para los cambios en los datos de usuario](/graph/webhooks#notification-endpoint-validation). Si se produce un error en la validación, la solicitud para crear la suscripción devuelve un error 400 de solicitud incorrecta.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
