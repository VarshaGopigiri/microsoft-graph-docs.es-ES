---
title: tipo de recurso emailActivityUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 16512c3a8a4dab62d4a71406d6c33d52a5a9bc08
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818007"
---
# <a name="emailactivityuserdetail-resource-type"></a>tipo de recurso emailActivityUserDetail

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo              |
| :---------------- | :---------------- |
| reportRefreshDate | Fecha              |
| userPrincipalName | Cadena            |
| displayName       | Cadena            |
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
