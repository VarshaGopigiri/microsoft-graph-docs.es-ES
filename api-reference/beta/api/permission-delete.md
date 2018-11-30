---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Eliminar el acceso a un elemento
ms.openlocfilehash: 726818b14a694380e46bfd38280e4cba9effb67d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088309"
---
# <a name="delete-a-sharing-permission-from-a-file-or-folder"></a>Eliminar un permiso de uso compartido de un archivo o una carpeta

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Quita el acceso a un [DriveItem](../resources/driveitem.md).

Solo se pueden eliminar los permisos de uso compartido **no** heredados.
La propiedad **inheritedFrom** debe ser `null`.

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
DELETE /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
DELETE /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
DELETE /me/drive/items/{item-id}/permissions/{perm-id}
DELETE /sites/{site-id}/drive/items/{item-id}/permissions/{perm-id}
DELETE /users/{user-id}/drive/items/{item-id}/permissions/{perm-id}
```

## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre          | Tipo   | Descripción                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| if-match      | string | Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará. |


## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.

## <a name="example"></a>Ejemplo

En este ejemplo, se quita el permiso identificado como {perm-id} del elemento {item-id} del OneDrive del usuario actual.

<!-- { "blockType": "request", "name": "delete-permission", "scopes": "files.readwrite" }-->

```http
DELETE https://graph.microsoft.com/beta/me/drive/root/items/{item-id}/permissions/{perm-id}
```

### <a name="response"></a>Respuesta

<!-- { "blockType": "response", "truncated": false } -->

```http
HTTP/1.1 204 No Content
```

## <a name="remarks"></a>Comentarios

* Los [Drives](../resources/drive.md) con un **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en la DriveItem raíz. 

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Remove an item's sharing permissions",
  "keywords": "permission, permissions, sharing, remove permissions, delete permissions",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Delete permission"
}-->
