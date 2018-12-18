---
title: tipo de recurso teamsDeviceUsageDistributionUserCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
ms.openlocfilehash: 01b9f67f30a7b2f13aac65cbcd4795792ee0aaa0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27345853"
---
# <a name="teamsdeviceusagedistributionusercounts-resource-type"></a>tipo de recurso teamsDeviceUsageDistributionUserCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   |
| :---------------- | :----- |
| reportRefreshDate | Date   |
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
