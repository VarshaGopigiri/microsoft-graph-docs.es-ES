---
title: tipo de recurso teamsUserActivityUserCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
ms.openlocfilehash: f4e10f1e34d4c6bdbed83279b98632c504630bc7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330460"
---
# <a name="teamsuseractivityusercounts-resource-type"></a>tipo de recurso teamsUserActivityUserCounts

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo   |
| :------------------ | :----- |
| reportRefreshDate   | Date   |
| reportDate          | Date   |
| teamChatMessages    | Int64  |
| privateChatMessages | Int64  |
| llamadas               | Int64  |
| reuniones            | Int64  |
| otherActions        | Int64  |
| reportPeriod        | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsUserActivityUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "teamChatMessages": 1024, 
  "privateChatMessages": 1024, 
  "calls": 1024, 
  "meetings": 1024, 
  "otherActions": 1024, 
  "reportPeriod": "String"
}
```
