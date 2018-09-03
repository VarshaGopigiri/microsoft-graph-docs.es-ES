---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enviar una invitación para obtener acceso a un elemento
ms.openlocfilehash: c68289049503e70e04b2e403ca09cfc1f67e4096
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23268735"
---
# <a name="send-a-sharing-invitation"></a>Enviar una invitación para uso compartido

Envía una invitación para uso compartido para un **DriveItem**.
Una invitación para uso compartido proporciona permisos a los destinatarios y, opcionalmente, les envía un correo electrónico con un [vínculo para uso compartido][].

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

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
| destinatarios       | Colección ([DriveRecipient][]) | Una colección de los destinatarios que recibirán acceso y la invitación para uso compartido.
| message          | Cadena                         | Un mensaje con formato de texto sin formato que se incluye en la invitación para uso compartido. La longitud máxima es de 2000 caracteres.
| requireSignIn    | Booleano                        | Especifica si el destinatario de la invitación debe iniciar sesión para ver el elemento compartido.
| sendInvitation   | Booleano                        | Si es verdadero, se envía un [vínculo para uso compartido][] al destinatario. De lo contrario, se concede un permiso directamente sin enviar una notificación.
| roles            | Colección (Cadena)             | Especifica los roles que se conceden a los destinatarios de la invitación para uso compartido.

## <a name="example"></a>Ejemplo

Este ejemplo envía una invitación para uso compartido a un usuario con la dirección de correo electrónico "ryan@contoso.org" y un mensaje sobre un archivo en el que colabora.
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

Consulte [Respuestas de error][error-response] para obtener más información sobre la manera en que se reciben los errores.


[driveRecipient]: ../resources/driverecipient.md
[error-response]: ../../../concepts/errors.md
[vínculo para uso compartido]: ../resources/permission.md#sharing-links

<!-- {
  "type": "#page.annotation",
  "description": "Add permissions to an item and optionally send a sharing notification.",
  "keywords": "retrieve,item,metadata",
  "section": "documentation",
  "tocPath": "Sharing/Add permissions"
} -->
