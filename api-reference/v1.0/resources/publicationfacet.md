---
title: Tipo de recurso PublicationFacet
description: El recurso **publicationFacet** proporciona información detallada sobre el estado publicado de un recurso driveItemVersion o driveItem.
ms.openlocfilehash: 429ec649dc9f511a4012e6790842fdd774bead8b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029163"
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
