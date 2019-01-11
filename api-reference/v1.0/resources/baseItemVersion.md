---
title: Tipo de recurso BaseItemVersion
description: El recurso **baseItemVersion** representa una versión anterior de un elemento o una entidad.
localization_priority: Normal
ms.openlocfilehash: bd28f9c8dc5be2bc6422aca2eb756aba78b8e393
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876968"
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

|      Nombre de la propiedad       |                         Tipo                         |                               Descripción                               |
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
