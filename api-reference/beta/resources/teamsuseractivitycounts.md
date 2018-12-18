---
title: tipo de recurso teamsUserActivityCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
ms.openlocfilehash: f67540f4172993b1076d9590438262b0d4da1846
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334520"
---
# <a name="teamsuseractivitycounts-resource-type"></a>tipo de recurso teamsUserActivityCounts

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo   |
| :------------------ | :----- |
| reportRefreshDate   | Date   |
| reportDate          | Date   |
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
