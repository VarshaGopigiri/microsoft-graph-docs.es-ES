---
title: tipo de recurso skypeForBusinessActivityCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: e59bd33b1709780bac9726ee716ef9d81ef33c1f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810132"
---
# <a name="skypeforbusinessactivitycounts-resource-type"></a>tipo de recurso skypeForBusinessActivityCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   |
| :---------------- | :----- |
| peerToPeer        | Int64  |
| organizados         | Int64  |
| participó      | Int64  |
| reportRefreshDate | Fecha   |
| reportDate        | Fecha   |
| reportPeriod      | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessActivityCounts"
} -->

```json
{
  "peerToPeer": 1024, 
  "organized": 1024, 
  "participated": 1024, 
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
