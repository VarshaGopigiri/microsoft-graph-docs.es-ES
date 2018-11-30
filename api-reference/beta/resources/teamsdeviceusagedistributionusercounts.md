---
title: tipo de recurso teamsDeviceUsageDistributionUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: b039320e389e1a61832089991b2368b27e51c475
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083404"
---
# <a name="teamsdeviceusagedistributionusercounts-resource-type"></a>tipo de recurso teamsDeviceUsageDistributionUserCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   |
| :---------------- | :----- |
| reportRefreshDate | Fecha   |
| web               | Int64  |
| windowsPhone      | Int64  |
| androidPhone      | Int64  |
| IOS               | Int64  |
| mac               | Int64  |
| Windows           | Int64  |
| reportPeriod      | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsDeviceUsageDistributionUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "web": 1024, 
  "windowsPhone": 1024, 
  "androidPhone": 1024, 
  "ios": 1024, 
  "mac": 1024, 
  "windows": 1024, 
  "reportPeriod": "String"
}
```
