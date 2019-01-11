---
title: tipo de recurso teamsDeviceUsageUserDetail
description: La siguiente es una representación JSON del recurso
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 06e2cea1154c608b61642b07adbd96aae1710903
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27807108"
---
# <a name="teamsdeviceusageuserdetail-resource-type"></a>tipo de recurso teamsDeviceUsageUserDetail

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo    |
| :---------------- | :------ |
| reportRefreshDate | Fecha    |
| userPrincipalName | Cadena  |
| lastActivityDate  | Fecha    |
| isDeleted         | Booleano |
| deletedDate       | Fecha    |
| usedWeb           | Booleano |
| usedWindowsPhone  | Booleano |
| usediOS           | Booleano |
| usedMac           | Booleano |
| usedAndroidPhone  | Booleano |
| usedWindows       | Booleano |
| reportPeriod      | String  |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsDeviceUsageUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "lastActivityDate": "Date", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "usedWeb": true, 
  "usedWindowsPhone": true, 
  "usediOS": true, 
  "usedMac": true, 
  "usedAndroidPhone": true, 
  "usedWindows": true, 
  "reportPeriod": "String"
}
```
