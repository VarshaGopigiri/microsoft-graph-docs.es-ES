---
title: tipo de recurso teamsUserActivityUserDetail
description: La siguiente es una representación JSON del recurso.
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 2e3f64c7065343712f6a9d9c6a114bf95f24c171
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823656"
---
# <a name="teamsuseractivityuserdetail-resource-type"></a>tipo de recurso teamsUserActivityUserDetail

## <a name="properties"></a>Propiedades

| Propiedad                | Tipo              |
| :---------------------- | :---------------- |
| reportRefreshDate       | Fecha              |
| userPrincipalName       | Cadena            |
| lastActivityDate        | Fecha              |
| isDeleted               | Booleano           |
| deletedDate             | Fecha              |
| assignedProducts        | Colección String |
| teamChatMessageCount    | Int64             |
| privateChatMessageCount | Int64             |
| callCount               | Int64             |
| meetingCount            | Int64             |
| hasOtherAction          | Booleano           |
| reportPeriod            | String            |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsUserActivityUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "lastActivityDate": "Date", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "assignedProducts": ["String"],
  "teamChatMessageCount": 1024, 
  "privateChatMessageCount": 1024, 
  "callCount": 1024, 
  "meetingCount": 1024, 
  "hasOtherAction": true, 
  "reportPeriod": "String"
}
```
