---
title: tipo de recurso teamsDeviceUsageUserCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
ms.openlocfilehash: 1255a8e1e92bb461d5c100c72e9030f57db5f8fa
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306513"
---
# <a name="teamsdeviceusageusercounts-resource-type"></a>tipo de recurso teamsDeviceUsageUserCounts

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
| reportDate        | Date   |
| reportPeriod      | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsDeviceUsageUserCounts"
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
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
