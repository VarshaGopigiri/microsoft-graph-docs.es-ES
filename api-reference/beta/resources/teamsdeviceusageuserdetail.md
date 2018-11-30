---
title: tipo de recurso teamsDeviceUsageUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 4eeec5f07a0a604249617ac87a62ea12b4052395
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090432"
---
# <a name="teamsdeviceusageuserdetail-resource-type"></a>tipo de recurso teamsDeviceUsageUserDetail

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo    |
| :---------------- | :------ |
| reportRefreshDate | Fecha    |
| userPrincipalName | String  |
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
