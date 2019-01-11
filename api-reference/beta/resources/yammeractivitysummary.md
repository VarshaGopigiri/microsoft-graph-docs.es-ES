---
title: tipo de recurso yammerActivitySummary
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 438cb55f4682d533876ef9a01561a3d69c4f1ea2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836655"
---
# <a name="yammeractivitysummary-resource-type"></a>tipo de recurso yammerActivitySummary

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   |
| :---------------- | :----- |
| reportRefreshDate | Fecha   |
| gustado             | Int64  |
| registrado            | Int64  |
| lectura              | Int64  |
| reportDate        | Fecha   |
| reportPeriod      | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yammerActivitySummary"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "liked": 1024, 
  "posted": 1024, 
  "read": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
