---
title: tipo de recurso skypeForBusinessParticipantActivityUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: d65d7fd9c2c3389e47a8b1f94538be158efd2642
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086884"
---
# <a name="skypeforbusinessparticipantactivityusercounts-resource-type"></a>tipo de recurso skypeForBusinessParticipantActivityUserCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   |
| :---------------- | :----- |
| mensajería instantánea                | Int64  |
| Recurso        | Int64  |
| uso compartido de aplicaciones        | Int64  |
| web               | Int64  |
| dialInOut3rdParty | Int64  |
| reportRefreshDate | Fecha   |
| reportDate        | Fecha   |
| reportPeriod      | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessParticipantActivityUserCounts"
} -->

```json
{
  "im": 1024, 
  "audioVideo": 196, 
  "appSharing": 196, 
  "web": 196, 
  "dialInOut3rdParty": 196, 
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
