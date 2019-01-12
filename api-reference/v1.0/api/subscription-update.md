---
title: Update subscription
description: Renueva una suscripción ampliando su tiempo de expiración.
localization_priority: Normal
author: piotrci
ms.openlocfilehash: a980d1fdc50a3295a309ccb1d58c0ebf5b5b6133
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976635"
---
# <a name="update-subscription"></a>Actualizar suscripción

Renueva una suscripción ampliando su tiempo de expiración.

Las suscripciones caducan después de un período de tiempo que varía en función del tipo de recurso. Con el fin de evitar la pérdida de notificaciones, una aplicación debe renovar sus suscripciones antes de su fecha de expiración. Vea la [suscripción](../resources/subscription.md) para la longitud máxima de una suscripción para cada tipo de recurso.

## <a name="permissions"></a>Permisos

En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de recurso o elemento        | Permiso          |
|-----------------------------|---------------------|
| Contactos                    | Contacts.Read       |
| Conversaciones               | Group.Read.All      |
| Eventos                      | Calendars.Read      |
| Mensajes                    | Mail.Read           |
| Grupos                      | Group.Read.All      |
| Usuarios                       | User.Read.All       |
| Unidad de disco (OneDrive del usuario)    | Files.ReadWrite     |
| Unidades (contenido de SharePoint compartido y unidades) | Files.ReadWrite.All |
|Alerta de seguridad| SecurityEvents.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
PATCH /subscriptions/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_subscription"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/subscriptions/{id}
Content-type: application/json

{
   "expirationDateTime":"2016-11-22T18:23:45.9356913Z"
}
```

##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.subscription"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 252

{
  "id":"7f105c7d-2dc5-4530-97cd-4e7ae6534c07",
  "resource":"me/messages",
  "applicationId": "24d3b144-21ae-4080-943f-7067b395b913",
  "changeType":"created,updated",
  "clientState":"subscription-identifier",
  "notificationUrl":"https://webhook.azurewebsites.net/api/send/myNotifyClient",
  "expirationDateTime":"2016-11-22T18:23:45.9356913Z",
  "creatorId": "8ee44408-0679-472c-bc2a-692812af3437"
}
```

<!-- {
  "type": "#page.annotation",
  "description": "Update subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
