---
title: Tipo de recurso BaseItemVersion
description: El recurso **baseItemVersion** representa una versión anterior de un elemento o una entidad.
ms.openlocfilehash: c4fc95fd419bf8b2f20ab202874ca31a2b1d63f6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030084"
---
# <a name="baseitemversion-resource-type"></a>Tipo de recurso BaseItemVersion

El recurso **baseItemVersion** representa una versión anterior de un elemento o una entidad.


## <a name="json-representation"></a>Representación JSON

<!--{
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.baseItemVersion",
  "@type.aka": "oneDrive.baseItemVersion"
}-->

```json
{
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "publication": { "@odata.type": "microsoft.graph.publicationFacet" }
}
```

## <a name="properties"></a>Propiedades

|      Nombre de propiedad       |                         Tipo                         |                               Descripción                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| **id**                   | string                                               | El identificador de la versión. Solo lectura.                                       |
| **lastModifiedBy**       | [IdentitySet](../resources/identityset.md)           | Identidad del usuario que modificó por última vez la versión. Solo lectura.        |
| **lastModifiedDateTime** | [DateTimeOffset](../resources/timestamp.md)          | Fecha y hora de la última modificación de la versión. Solo lectura.                 |
| **publication**          | [PublicationFacet](../resources/publicationfacet.md) | Indica el estado de publicación de esta versión concreta. Solo lectura. |


<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
