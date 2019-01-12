---
title: tipo de recurso mailboxUsageStorage
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 44b97c7b18264e01c86b34bfd8265246f80ab031
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917870"
---
# <a name="mailboxusagestorage-resource-type"></a>tipo de recurso mailboxUsageStorage

## <a name="properties"></a>Propiedades

| Propiedad           | Tipo   |
| :----------------- | :----- |
| reportRefreshDate  | Fecha   |
| storageUsedInBytes | Int64  |
| reportDate         | Fecha   |
| reportPeriod       | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mailboxUsageStorage"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "storageUsedInBytes": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
