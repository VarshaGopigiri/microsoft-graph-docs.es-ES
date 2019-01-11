---
title: Tipo de recurso PublicationFacet
description: El recurso **publicationFacet** proporciona información detallada sobre el estado publicado de un recurso driveItemVersion o driveItem.
localization_priority: Normal
ms.openlocfilehash: 3d722f56cf1d587483c672fb7a1b7c05abd3671b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810532"
---
# <a name="publicationfacet-resource-type"></a>Tipo de recurso PublicationFacet

El recurso **publicationFacet** proporciona información detallada sobre el estado publicado de un recurso [driveItemVersion](driveitemversion.md) o [driveItem](driveitem.md).

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.publicationFacet"
}-->

```json
{
  "level": "published | checkout",
  "versionId": "string"
}
```

## <a name="properties"></a>Propiedades

|   Propiedad    |  Tipo  | Descripción |
| :------------ | :----- | :---------- |
| **level**     | Cadena | El estado de publicación de este documento. `published` o `checkout`. Solo lectura.  |
| **versionId** | Cadena | El identificador único de la versión que está visible para el llamador actual. Solo lectura.  |


<!-- {
  "type": "#page.annotation",
  "description": "The photo facet provides details about the camera and settings on the camera for photos.",
  "keywords": "camera make,camera model, exposure, f-stop, iso",
  "section": "documentation",
  "suppressions": [
    " Warning: /api-reference/v1.0/resources/publicationfacet.md:
      Found potential enums in resource example that weren't defined in a table:(published,checkout) are in resource, but () are in table"
  ],
  "tocPath": "Facets/Photo"
} -->
