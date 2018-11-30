---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar quién tiene acceso a un archivo
ms.openlocfilehash: 1b7dd2fd435e523c0dad86a419bf9e46dbcf5c8f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029037"
---
# <a name="list-sharing-permissions-on-a-driveitem"></a>Mostrar permisos de uso compartido en un objeto DriveItem

Muestre los permisos de uso compartido efectivos de un objeto [DriveItem](../resources/driveitem.md).

## <a name="access-to-sharing-permissions"></a>Acceso a permisos de uso compartido

La colección de permisos incluye información potencialmente confidencial y puede no estar disponible para todos los autores de llamadas.

* Para el propietario del elemento, se devolverán todos los permisos de uso compartido. Esto incluye los copropietarios.
* Para un autor de llamada que no sea el propietario, se devuelven solo los permisos de uso compartido que se aplican al autor de la llamada.
* Las propiedades de permisos de uso compartido que contienen información confidencial (por ejemplo, `shareId` y `webUrl`) se devuelven solo a los autores de llamadas que pueden crear el permiso de uso compartido.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All    |
|Aplicación | Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/permissions
GET /groups/{group-id}/drive/items/{item-id}/permissions
GET /me/drive/items/{item-id}/permissions
GET /me/drive/root:/{path}:/permissions
GET /sites/{siteId}/drive/items/{itemId}/permissions
GET /users/{userId}/drive/items/{itemId}/permissions
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$select` para personalizar la respuesta.

## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre          | Tipo   | Descripción                                                                                                                                     |
|:--------------|:-------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| if-none-match | string | Si se incluye este encabezado de la solicitud y el ETag proporcionado coincide con el ETag actual del elemento, se devuelve una respuesta `HTTP 304 Not Modified`. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de recursos [Permission](../resources/permission.md) en el cuerpo de la respuesta.

Los permisos de uso compartido efectivos de un objeto DriveItem pueden provenir de dos orígenes:

* Permisos de uso compartido que se aplican directamente en el propio objeto DriveItem
* Permisos de uso compartido heredados de los antecesores del objeto DriveItem

Los autores de llamadas pueden distinguir si el permiso se hereda o no comprobando la propiedad **inheritedFrom**. Esta propiedad es un recurso [**itemReference**](../resources/itemreference.md) que hace referencia al antecesor del que se hereda el permiso.

Los niveles de permiso de SharePoint establecidos en un elemento se devuelven con un prefijo "SP". Por ejemplo, SP.View Only, SP.Limited Access, SP.View Web Analytics Data. Vea [Lista completa de roles de SharePoint](https://technet.microsoft.com/en-us/library/cc721640.aspx#section1).

## <a name="example"></a>Ejemplo

En este ejemplo, se recupera la colección de permisos en un elemento de la unidad del usuario que ha iniciado sesión.

<!-- { "blockType": "request", "name": "get-item-permissions", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/permissions
```

### <a name="response"></a>Respuesta

Esta respuesta de ejemplo incluye tres permisos, el primero es un vínculo para compartir con permisos de edición, el segundo es un permiso explícito para un usuario llamado John, que se ha heredado de una carpeta principal, y el tercero es un vínculo para compartir de lectura y escritura creado por una aplicación.

<!-- {"blockType": "response", "@odata.type": "Collection(microsoft.graph.permission)", "truncated": true} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "1",
      "roles": ["write"],
      "link": {
        "webUrl": "https://onedrive.live.com/redir?resid=5D33DD65C6932946!70859&authkey=!AL7N1QAfSWcjNU8&ithint=folder%2cgif",
        "type": "edit"
      }
    },
    {
      "id": "2",
      "roles": ["write"],
      "grantedTo": {
        "user": {
          "id": "5D33DD65C6932946",
          "displayName": "John Doe"
        }
      },
      "inheritedFrom": {
        "driveId": "1234567890ABD",
        "id": "1234567890ABC!123",
        "path": "/drive/root:/Documents" }
    },
    {
      "id": "3",
      "roles": ["write"],
      "link": {
        "webUrl": "https://onedrive.live.com/redir?resid=5D33DD65C6932946!70859&authkey=!AL7N1QAfSWcjNU8&ithint=folder%2cgif",
        "type": "edit",
        "application": {
          "id": "12345",
          "displayName": "Contoso Time Manager"
        }
      }
    }
  ]
}
```

## <a name="remarks"></a>Comentarios

La relación **permisos** del objeto DriveItem no se puede expandir como parte de una llamada a [get DriveItem](driveitem-get.md) o una colección de objetos DriveItem. Debe tener acceso a la propiedad de permisos directamente.

## <a name="error-responses"></a>Respuestas de error

Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "List an item's permissions",
  "keywords": "permission, permissions, sharing",
  "section": "documentation",
  "tocPath": "Sharing/Permissions"
} -->
