---
title: tipo de recurso teamsUserActivityUserDetail
description: La siguiente es una representación JSON del recurso.
ms.openlocfilehash: 4e40ea4adf07450e6b51555df47579955a2a0286
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089813"
---
# <a name="teamsuseractivityuserdetail-resource-type"></a>tipo de recurso teamsUserActivityUserDetail

## <a name="properties"></a>Propiedades

| Propiedad                | Tipo              |
| :---------------------- | :---------------- |
| reportRefreshDate       | Fecha              |
| userPrincipalName       | String            |
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
