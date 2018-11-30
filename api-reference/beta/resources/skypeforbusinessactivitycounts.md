---
title: tipo de recurso skypeForBusinessActivityCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 00c55df3a0a6201bd731938675880b9cbbe9cee6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089180"
---
# <a name="skypeforbusinessactivitycounts-resource-type"></a>tipo de recurso skypeForBusinessActivityCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   |
| :---------------- | :----- |
| peerToPeer        | Int64  |
| organizados         | Int64  |
| participó      | Int64  |
| reportRefreshDate | Fecha   |
| reportDate        | Fecha   |
| reportPeriod      | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessActivityCounts"
} -->

```json
{
  "peerToPeer": 1024, 
  "organized": 1024, 
  "participated": 1024, 
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
