---
title: tipo de recurso yammerActivityUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: a1ca33efe8327b1c1e52de25714df9c0bd45ee05
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089134"
---
# <a name="yammeractivityuserdetail-resource-type"></a>tipo de recurso yammerActivityUserDetail

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo              |
| :---------------- | :---------------- |
| reportRefreshDate | Fecha              |
| userPrincipalName | String            |
| displayName       | String            |
| userState         | String            |
| stateChangeDate   | Fecha              |
| lastActivityDate  | Fecha              |
| postedCount       | Int64             |
| readCount         | Int64             |
| likedCount        | Int64             |
| assignedProducts  | Colección String |
| reportPeriod      | String            |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yammerActivityUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "displayName": "String", 
  "userState": "String", 
  "stateChangeDate": "Date", 
  "lastActivityDate": "Date", 
  "postedCount": 1024, 
  "readCount": 1024, 
  "likedCount": 1024, 
  "assignedProducts": ["String"], 
  "reportPeriod": "String"
}
```
