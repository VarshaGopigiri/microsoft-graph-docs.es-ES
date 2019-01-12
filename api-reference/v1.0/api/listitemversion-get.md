---
title: Obtener un recurso ListItemVersion
description: Recupere los metadatos de una versión específica de un recurso ListItem.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 3e45cf260a9f526a7309c63791ed2cb6b8196e45
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972540"
---
# <a name="get-a-listitemversion-resource"></a>Obtener un recurso ListItemVersion

Recupere los metadatos de una versión específica de un recurso [ListItem](../resources/listitem.md).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|            Tipo de permiso             | Permisos (de menos a más privilegiados) |
| :------------------------------------- | :------------------------------------------ |
| Delegado (cuenta profesional o educativa)     | Sites.Read.All, Sites.ReadWrite.All         |
| Delegado (cuenta personal de Microsoft) | N/D                                         |
| Aplicación                            | Sites.Read.All, Sites.ReadWrite.All         |


## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored"} -->

```http
GET /sites/{site-id}/items/{item-id}/versions/{version-id}
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}
```


## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [ListItemVersion](../resources/listitemversion.md) en el cuerpo de la respuesta.


## <a name="example"></a>Ejemplo

Este ejemplo recupera una versión de un recurso listItem y expande la colección fields para solicitar los valores de los campos en el recurso listItem.

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "get-single-version-listItem", "scopes": "files.read sites.read.all", "tags": "service.graph service.sharepoint" } -->

```http
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}?expand=fields
```

### <a name="response"></a>Respuesta

Devuelve una colección de versiones:

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.listItemVersion", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "id": "1.0",
    "lastModifiedBy": {
    "user": {
        "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
        "displayName": "Ryan Gregg"
    }
    },
    "lastModifiedDateTime": "2017-09-14T12:34:53.912Z",
    "fields": {  }
}
```

<!-- {
  "type": "#page.annotation",
  "description": "List, review, and download previous versions of a driveItem",
  "keywords": "version, version history, versions",
  "section": "documentation",
  "tocPath": "Items/Version history"
} -->
