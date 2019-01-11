---
title: tipo de recurso siteUsageStorage
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 1f656feacdbba3418049bd9f3072270aa04af798
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879929"
---
# <a name="siteusagestorage-resource-type"></a>tipo de recurso siteUsageStorage

## <a name="properties"></a>Propiedades

| Propiedad           | Tipo   |
| :----------------- | :----- |
| reportRefreshDate  | Fecha   |
| siteType           | Cadena |
| storageUsedInBytes | Int64  |
| reportDate         | Fecha   |
| reportPeriod       | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.siteUsageStorage"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "siteType": "String", 
  "storageUsedInBytes": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
