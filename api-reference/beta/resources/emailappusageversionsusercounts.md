---
title: tipo de recurso emailAppUsageVersionsUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 7b4a59a1e15ddf41f0e4204efc4d3e0c6549e587
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088541"
---
# <a name="emailappusageversionsusercounts-resource-type"></a>tipo de recurso emailAppUsageVersionsUserCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   |
| :---------------- | :----- |
| reportRefreshDate | Fecha   |
| outlook2016       | Int64  |
| outlook2013       | Int64  |
| outlook2010       | Int64  |
| Outlook2007       | Int64  |
| indeterminado      | Int64  |
| reportPeriod      | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.emailAppUsageVersionsUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "outlook2016": 1024, 
  "outlook2013": 1024, 
  "outlook2010": 1024, 
  "outlook2007": 1024, 
  "undetermined": 1024, 
  "reportPeriod": "String"
}
```
