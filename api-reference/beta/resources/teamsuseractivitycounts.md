---
title: tipo de recurso teamsUserActivityCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 39e90b4c9dc6b9929959139ba67ddb090d143e38
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089801"
---
# <a name="teamsuseractivitycounts-resource-type"></a>tipo de recurso teamsUserActivityCounts

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo   |
| :------------------ | :----- |
| reportRefreshDate   | Fecha   |
| reportDate          | Fecha   |
| teamChatMessages    | Int64  |
| privateChatMessages | Int64  |
| llamadas               | Int64  |
| reuniones            | Int64  |
| reportPeriod        | String |


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsUserActivityCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "teamChatMessages": 1024, 
  "privateChatMessages": 1024, 
  "calls": 1024, 
  "meetings": 1024, 
  "reportPeriod": "String"
}
```
