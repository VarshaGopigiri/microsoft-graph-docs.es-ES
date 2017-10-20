---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener permisos
ms.openlocfilehash: 34171ca2c862857069f904103681ecc9b1646fc7
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="get-sharing-permission-for-a-file-or-folder"></a>Obtener permiso de uso compartido de un archivo o una carpeta

Devuelva el permiso efectivo de uso compartido para un recurso de permiso en concreto.

Los permisos efectivos de un elemento pueden provenir de dos orígenes: permisos que se establecen directamente en el propio elemento o permisos que se heredan de los antecesores del elemento.

Los autores de llamadas pueden distinguir si el permiso se hereda o no comprobando la propiedad `inheritedFrom`. Esta propiedad es un recurso [ItemReference](../resources/itemReference.md) que hace referencia al antecesor del que se hereda el permiso.

Los niveles de permiso de SharePoint establecidos en un elemento se devuelven con un prefijo "SP". Por ejemplo, SP.View Only, SP.Limited Access, SP.View Web Analytics Data. Vea [Lista completa de roles de SharePoint](https://technet.microsoft.com/en-us/library/cc721640.aspx#section1).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All    |
|Aplicación | Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
GET /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
GET /me/drive/items/{item-id}/permissions/{perm-id}
GET /sites/{site-id}/drive/items/{item-id}/permissions/{perm-id}
GET /users/{user-id}/drive/items/{item-id}/permissions/{perm-id}
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite el [parámetro de consulta $select](../../../concepts/query_parameters.md) para dar forma a la respuesta.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [Permission](../resources/permission.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud para obtener acceso a un permiso en una carpeta.

<!-- { "blockType": "request", "name": "get-item-permission", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/permissions/{perm-id}
```

### <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un recurso [Permission](../resources/permission.md) para el identificador especificado. 

<!-- {"blockType": "response", "@odata.type": "microsoft.graph.permission", "truncated": true} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "grantedTo": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "efee1b77-fb3b-4f65-99d6-274c11914d12"
    }
  },
  "id": "1",
  "roles": [ "write" ]
}
```

## <a name="remarks"></a>Comentarios

El recurso [Permission](../resources/permission.md) usa _facetas_ para proporcionar información sobre el tipo de permiso que representa el recurso.

Los permisos con una faceta [**link**](../resources/sharinglink.md) representan vínculos para compartir creados en el elemento. Los vínculos para compartir contienen un token único que proporciona acceso al elemento a cualquier usuario con el vínculo.

Los permisos con una faceta [**invitation**](../resources/sharinginvitation.md) representan los permisos agregados al invitar a usuarios o grupos específicos para que tengan acceso al archivo.

### <a name="error-responses"></a>Respuestas de error

Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.

[error-response]: ../../../concepts/errors.md

<!-- {
  "type": "#page.annotation",
  "description": "Get a DriveItem's sharing permissions",
  "keywords": "permission, permissions, sharing",
  "section": "documentation",
  "tocPath": "Sharing/Permissions"
} -->
