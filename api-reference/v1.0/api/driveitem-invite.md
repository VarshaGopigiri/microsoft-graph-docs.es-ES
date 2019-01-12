---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enviar una invitación para obtener acceso a un elemento
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 23e58c063e31f8ad68ac887a4fd1d2cd4dcd5274
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976964"
---
# <a name="send-a-sharing-invitation"></a>Enviar una invitación para uso compartido

Envía una invitación para compartir para un **DriveItem**.
Una invitación para compartir proporciona permisos a los destinatarios y, opcionalmente, envía un correo electrónico con un [vínculo de uso compartido][].

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.ReadWrite, Files.ReadWrite.All    |
|Aplicación | Files.ReadWrite.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{drive-id}/items/{item-id}/invite
POST /groups/{group-id}/drive/items/{item-id}/invite
POST /me/drive/items/{item-id}/invite
POST /sites/{siteId}/drive/items/{itemId}/invite
POST /users/{userId}/drive/items/{itemId}/invite
```

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

<!-- { "blockType": "ignored", "scopes": "files.readwrite" } -->

```json
{
  "requireSignIn": false,
  "sendInvitation": false,
  "roles": [ "read | write"],
  "recipients": [
    { "@odata.type": "microsoft.graph.driveRecipient" },
    { "@odata.type": "microsoft.graph.driveRecipient" }
  ],
  "message": "string"
}
```

| Parámetro        | Tipo                           | Descripción
|:-----------------|:-------------------------------|:-------------------------
| destinatarios       | Collection([DriveRecipient][]) | Una colección de los destinatarios que recibirán acceso y la invitación para uso compartido.
| message          | String                         | Un mensaje con formato de texto sin formato que se incluye en la invitación para uso compartido. La longitud máxima es de 2000 caracteres.
| requireSignIn    | Boolean                        | Especifica si se requiere el destinatario de la invitación para iniciar sesión para ver el elemento compartido.
| sendInvitation   | Boolean                        | Si es true, un [vínculo de uso compartido][] se envía al destinatario. De lo contrario, se concede un permiso directamente sin enviar una notificación.
| roles            | Collection(String)             | Especificar los roles que se van a conceder a los destinatarios de la invitación para compartir.

## <a name="example"></a>Ejemplo

En este ejemplo se envía una invitación para compartir para un usuario con la dirección de correo electrónico "ryan@contoso.com" con un mensaje acerca de un archivo que se han colaborado en.
La invitación concede a Ryan acceso de lectura y escritura al archivo.

### <a name="http-request"></a>Solicitud HTTP

Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [permission](../resources/permission.md) en el cuerpo de la respuesta.

<!-- { "blockType": "request", "name": "send-sharing-invite", "scopes": "files.readwrite", "target": "action" } -->

```json
POST /me/drive/items/{item-id}/invite
Content-type: application/json

{
  "recipients": [
    {
      "email": "ryan@contoso.com"
    }
  ],
  "message": "Here's the file that we're collaborating on.",
  "requireSignIn": true,
  "sendInvitation": true,
  "roles": [ "write" ]
}
```

### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.permission)", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "grantedTo": {
        "user": {
          "displayName": "Ryan Gregg",
          "id": "42F177F1-22C0-4BE3-900D-4507125C5C20"
        }
      },
      "id": "CCFC7CA3-7A19-4D57-8CEF-149DB9DDFA62",
      "invitation": {
        "email": "ryan@contoso.com",
        "signInRequired": true
      },
      "roles": [ "write" ]
    }
  ]
}
```

## <a name="remarks"></a>Comentarios

* Los objetos [Drives](../resources/drive.md) con un valor **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en el objeto DriveItem raíz.
* Para obtener una lista de los roles disponibles, consulte [Enumeración de roles](../resources/permission.md#roles-enumeration).

## <a name="error-responses"></a>Respuestas de error

Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.


[driveRecipient]: ../resources/driverecipient.md
[error-response]: /graph/errors
[uso compartido de vínculo]: ../resources/permission.md#sharing-links

<!-- {
  "type": "#page.annotation",
  "description": "Add permissions to an item and optionally send a sharing notification.",
  "keywords": "retrieve,item,metadata",
  "section": "documentation",
  "tocPath": "Sharing/Add permissions"
} -->
