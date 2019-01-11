---
title: " tipo de recurso averageComparativeScore"
description: Este recurso contiene diversos calificaciones distintas en función de diferentes ámbitos (por ejemplo, promedio por industria vertical, promedio por tamaño de puestos de la empresa y así sucesivamente) y categoría de control (identidad, datos, dispositivos, aplicaciones, infraestructura).
localization_priority: Normal
ms.openlocfilehash: c32c1349edd70e80c1bf0fb12a36bd07e06ed39f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834597"
---
#  <a name="averagecomparativescore-resource-type"></a>tipo de recurso averageComparativeScore

Este recurso contiene diversos calificaciones distintas en función de diferentes ámbitos (por ejemplo, promedio por industria vertical, promedio por tamaño de puestos de la empresa y así sucesivamente) y categoría de control (identidad, datos, dispositivos, aplicaciones, infraestructura).

|Propiedad |Tipo |Description |
|:--|:--|:--|
|   base   |   Cadena  |   Tipo de ámbito (por AllTenants, TotalSeats, IndustryTypes).  |
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
