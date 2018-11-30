---
title: tipo de recurso skypeForBusinessOrganizerActivityUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 0e0b6838b58b4a3fab9a62351446bf26fc50bfbd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088148"
---
# <a name="skypeforbusinessorganizeractivityusercounts-resource-type"></a>tipo de recurso skypeForBusinessOrganizerActivityUserCounts

## <a name="properties"></a>Propiedades

| Propiedad           | Tipo   |
| :----------------- | :----- |
| mensajería instantánea                 | Int64  |
| Recurso         | Int64  |
| uso compartido de aplicaciones         | Int64  |
| web                | Int64  |
| dialInOut3rdParty  | Int64  |
| dialInOutMicrosoft | Int64  |
| reportRefreshDate  | Fecha   |
| reportDate         | Fecha   |
| reportPeriod       | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessOrganizerActivityUserCounts"
} -->

```json
{
  "im": 1024, 
  "audioVideo": 1024, 
  "appSharing": 1024, 
  "web": 1024, 
  "dialInOut3rdParty": 1024, 
  "dialInOutMicrosoft": 1024, 
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
