---
title: tipo de recurso emailActivityUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 4f74b4af41c44e41b07bae1a8421011bc5188efc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083139"
---
# <a name="emailactivityuserdetail-resource-type"></a>tipo de recurso emailActivityUserDetail

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo              |
| :---------------- | :---------------- |
| reportRefreshDate | Fecha              |
| userPrincipalName | String            |
| displayName       | String            |
| isDeleted         | Booleano           |
| deletedDate       | Fecha              |
| lastActivityDate  | Fecha              |
| sendCount         | Int64             |
| receiveCount      | Int64             |
| readCount         | Int64             |
| assignedProducts  | Colección String |
| reportPeriod      | String            |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.emailActivityUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "displayName": "String", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "lastActivityDate": "Date", 
  "sendCount": 1024, 
  "receiveCount": 1024, 
  "readCount": 1024, 
  "assignedProducts": ["String"], 
  "reportPeriod": "String"
}
```
