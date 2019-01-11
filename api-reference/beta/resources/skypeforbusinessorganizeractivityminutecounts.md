---
title: tipo de recurso skypeForBusinessOrganizerActivityMinuteCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 6b3b38c61ebb7b294de9ea5fc2641a7527bf04f7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823208"
---
# <a name="skypeforbusinessorganizeractivityminutecounts-resource-type"></a>tipo de recurso skypeForBusinessOrganizerActivityMinuteCounts

## <a name="properties"></a>Propiedades

| Propiedad           | Tipo   |
| :----------------- | :----- |
| Recurso         | Int64  |
| dialInOut3rdParty  | Int64  |
| dialInOutMicrosoft | Int64  |
| reportRefreshDate  | Fecha   |
| reportDate         | Fecha   |
| reportPeriod       | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessOrganizerActivityMinuteCounts"
} -->

```json
{
  "audioVideo": 1024, 
  "dialInMicrosoft": 1024, 
  "dialOutMicrosoft": 1024, 
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
