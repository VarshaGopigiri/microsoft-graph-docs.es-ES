---
title: tipo de recurso yammerDeviceUsageUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 8812b61d974815fd1cdf1bbe1549a21193e5a2f4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090435"
---
# <a name="yammerdeviceusageuserdetail-resource-type"></a>tipo de recurso yammerDeviceUsageUserDetail

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo    |
| :---------------- | :------ |
| reportRefreshDate | Fecha    |
| userPrincipalName | String  |
| displayName       | String  |
| userState         | String  |
| stateChangeDate   | Fecha    |
| lastActivityDate  | Fecha    |
| usedWeb           | Booleano |
| usedWindowsPhone  | Booleano |
| usedAndroidPhone  | Booleano |
| usediPhone        | Booleano |
| usediPad          | Booleano |
| usedOthers        | Booleano |
| reportPeriod      | String  |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yammerDeviceUsageUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "displayName": "String", 
  "userState": "String", 
  "stateChangeDate": "Date", 
  "lastActivityDate": "Date", 
  "usedWeb": true, 
  "usedWindowsPhone": true, 
  "usedAndroidPhone": true, 
  "usediPhone": true, 
  "usediPad": true, 
  "usedOthers": true, 
  "reportPeriod": "String"
}
```
