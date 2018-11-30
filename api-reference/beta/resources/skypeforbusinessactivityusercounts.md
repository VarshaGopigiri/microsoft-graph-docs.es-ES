---
title: tipo de recurso skypeForBusinessActivityUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: eee736958540f2a3fb42cf3c76a37da4ebe78afd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091166"
---
# <a name="skypeforbusinessactivityusercounts-resource-type"></a>tipo de recurso skypeForBusinessActivityUserCounts

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
  "@odata.type": "microsoft.graph.skypeForBusinessActivityUserCounts"
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
