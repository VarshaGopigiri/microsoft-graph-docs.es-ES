---
title: tipo de recurso teamsDeviceUsageUserCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 07a43b024d133e5ac1d8eb8a2665fd3027001edb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857354"
---
# <a name="teamsdeviceusageusercounts-resource-type"></a>tipo de recurso teamsDeviceUsageUserCounts

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
| reportDate        | Fecha   |
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
