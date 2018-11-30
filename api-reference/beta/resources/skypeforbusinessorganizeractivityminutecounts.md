---
title: tipo de recurso skypeForBusinessOrganizerActivityMinuteCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: f11d303bd8737d9fb2870042ee93557343d44a2f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089174"
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
