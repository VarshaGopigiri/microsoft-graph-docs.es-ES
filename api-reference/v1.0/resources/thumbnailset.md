---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: ThumbnailSet
ms.openlocfilehash: 2ba45363b684142b91aac62d4b2a5b0d371d6b3d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030173"
---
# <a name="thumbnailset-resource-type"></a>Tipo de recurso ThumbnailSet

El recurso **ThumbnailSet** es una colección de claves de recursos [thumbnail](thumbnail.md). Se usa para representar un conjunto de miniaturas asociadas a un DriveItem.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "source",
    "small",
    "medium",
    "large"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.thumbnailSet",
  "openType": true
}-->

```json
{
  "id": "string (identifier)",
  "large": { "@odata.type": "microsoft.graph.thumbnail" },
  "medium": { "@odata.type": "microsoft.graph.thumbnail" },
  "small": { "@odata.type": "microsoft.graph.thumbnail" },
  "source": { "@odata.type": "microsoft.graph.thumbnail" }
}
```

## <a name="properties"></a>Propiedades

| Propiedad | Tipo                      | Descripción                                                                       |
|:---------|:--------------------------|:----------------------------------------------------------------------------------|
| id       | String                    | Identificador del elemento. Solo lectura.                                                |
| large    | [Thumbnail](thumbnail.md) | Miniatura escalada de 1920 x 1920.                                                     |
| medium   | [Thumbnail](thumbnail.md) | Miniatura escalada de 176 x 176.                                                       |
| small    | [Thumbnail](thumbnail.md) | Miniatura recortada de 48 x 48.                                                        |
| source   | [Thumbnail](thumbnail.md) | Imagen en miniatura personalizada o imagen original usada para generar otras miniaturas. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ThumbnailSet enables access to thumbnails of different sizes",
  "section": "documentation",
  "tocPath": "Resources/ThumbnailSet"
} -->
