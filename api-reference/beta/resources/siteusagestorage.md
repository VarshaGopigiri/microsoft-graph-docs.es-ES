---
title: tipo de recurso siteUsageStorage
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: c136b776e0c96a8bc63a1c82ae2ad17f059026cc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928104"
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
