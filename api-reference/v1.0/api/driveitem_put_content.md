---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: "Cargar archivos pequeños"
ms.openlocfilehash: 44d3d3033014067af968720d24e87ec5047416ae
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="upload-or-replace-the-contents-of-a-driveitem"></a>Cargar o reemplazar el contenido de un objeto DriveItem

La API de carga simple le permite proporcionar el contenido de un archivo nuevo o actualizar el contenido de un archivo existente en una sola llamada API. Este método solo admite archivos de hasta 4 MB de tamaño.

Para cargar archivos grandes, consulte [Cargar archivos de gran tamaño con una sesión de carga](driveitem_createuploadsession.md).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.ReadWrite, Files.ReadWrite.All    |
|Aplicación | Files.ReadWrite.All, Sites.ReadWrite.All |

## <a name="http-request-to-replace-an-existing-item"></a>Solicitud HTTP (para reemplazar un elemento existente)

<!-- { "blockType": "ignored" } -->

```http
PUT /drives/{drive-id}/items/{item-id}/content
PUT /groups/{group-id}/drive/items/{item-id}/content
PUT /me/drive/items/{item-id}/content
PUT /sites/{site-id}/drive/items/{item-id}/content
PUT /users/{user-id}/drive/items/{item-id}/content
```

## <a name="http-request-to-upload-a-new-file"></a>Solicitud HTTP (para cargar un archivo nuevo)

<!-- { "blockType": "ignored" } -->

```http
PUT /drives/{drive-id}/items/{parent-id}:/{filename}:/content
PUT /groups/{group-id}/drive/items/{parent-id}:/{filename}:/content
PUT /me/drive/items/{parent-id}:/{filename}:/content
PUT /sites/{site-id}/drive/items/{parent-id}:/{filename}:/content
PUT /users/{user-id}/drive/items/{parent-id}:/{filename}:/content
```

## <a name="request-body"></a>Cuerpo de solicitud

El contenido del cuerpo de la solicitud debe ser la secuencia binaria del archivo que se cargará.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un objeto [driveItem](../resources/driveitem.md) en el cuerpo de la respuesta del archivo que se ha creado o actualizado.

## <a name="example-upload-a-new-file"></a>Ejemplo (se carga un nuevo archivo)

Este ejemplo carga la cadena "The contents of the file goes here." (El contenido del archivo va aquí.) en un archivo en la unidad del usuario que ha iniciado sesión en FolderA denominado FileB.txt.

<!-- { "blockType": "request", "name": "upload-via-put", "scopes": "files.readwrite" } -->

```http
PUT /me/drive/root:/FolderA/FileB.txt:/content
Content-Type: text/plain

The contents of the file goes here.
```

### <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un recurso [driveItem][item-resource] en el cuerpo de la respuesta del archivo que se ha creado.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "0123456789abc",
  "name": "FileB.txt",
  "size": 35,
  "file": { }
}
```

## <a name="example-updating-an-existing-file"></a>Ejemplo (actualizar un archivo existente)

Este ejemplo reemplaza el contenido de un archivo con un identificador conocido.

<!-- { "blockType": "request", "name": "upload-via-put-id", "scopes": "files.readwrite" } -->

```http
PUT /me/drive/items/{item-id}/content
Content-Type: text/plain

The contents of the file goes here.
```

### <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un recurso [driveItem][item-resource] en el cuerpo de la respuesta del archivo que se ha creado.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "0123456789abc",
  "name": "FileB.txt",
  "size": 35,
  "file": { }
}
```

## <a name="error-responses"></a>Respuestas de error

Vea [Respuestas de error][error-response] para obtener los detalles sobre la manera en que se devuelven los errores.

[error-response]: ../../../concepts/errors.md
[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a new file with content or update a file's content.",
  "keywords": "insert,upsert,update,upload",
  "section": "documentation"
} -->
