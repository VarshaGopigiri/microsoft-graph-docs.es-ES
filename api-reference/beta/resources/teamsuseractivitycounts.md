---
title: tipo de recurso teamsUserActivityCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: bcc0e9d1ed5c93c3d9f4ba97165d0413025a89cd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987527"
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
