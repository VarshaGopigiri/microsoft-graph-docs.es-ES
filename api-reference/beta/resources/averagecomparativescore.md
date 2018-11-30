---
title: " tipo de recurso averageComparativeScore"
description: Este recurso contiene diversos calificaciones distintas en función de diferentes ámbitos (por ejemplo, promedio por industria vertical, promedio por tamaño de puestos de la empresa y así sucesivamente) y categoría de control (identidad, datos, dispositivos, aplicaciones, infraestructura).
ms.openlocfilehash: 08e4ec60788b21476d8f1491ab5548c7a4ca2e01
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084444"
---
#  <a name="averagecomparativescore-resource-type"></a>tipo de recurso averageComparativeScore

Este recurso contiene diversos calificaciones distintas en función de diferentes ámbitos (por ejemplo, promedio por industria vertical, promedio por tamaño de puestos de la empresa y así sucesivamente) y categoría de control (identidad, datos, dispositivos, aplicaciones, infraestructura).

|Propiedad |Tipo |Descripción |
|:--|:--|:--|
|   base   |   String  |   Tipo de ámbito (por AllTenants, TotalSeats, IndustryTypes).  |
|   Promedio    |   Doble  | Promedio de la puntuación dentro de base especificado. |
|   deviceScore |   Doble  | Promedio de la puntuación dentro de base especificado. |
|   dataScore   |   Doble  | Promedio de la puntuación dentro de base especificado. |
|   identityScore   |   Doble  | Promedio de la puntuación dentro de base especificado. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.averageComparativeScore"
}-->

```json
{
  "basis": "String",
  "averageScore": "Double",
  "deviceScore": "Double",
  "dataScore": "Double",
  "identityScore": "Double"
}

```


<!-- {
  "type": "#page.annotation",
  "description": "averageComparativeScore resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
