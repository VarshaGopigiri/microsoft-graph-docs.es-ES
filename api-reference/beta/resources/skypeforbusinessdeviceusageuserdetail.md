---
title: tipo de recurso skypeForBusinessDeviceUsageUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: b62920d124fd52e0f653c128eeb0956cdfe0c680
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084716"
---
# <a name="skypeforbusinessdeviceusageuserdetail-resource-type"></a>tipo de recurso skypeForBusinessDeviceUsageUserDetail

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo    |
| :---------------- | :------ |
| reportRefreshDate | Fecha    |
| userPrincipalName | String  |
| lastActivityDate  | Fecha    |
| usedWindows       | Booleano |
| usedWindowsPhone  | Booleano |
| usedAndroidPhone  | Booleano |
| usediPhone        | Booleano |
| usediPad          | Booleano |
| reportPeriod      | String  |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessDeviceUsageUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "lastActivityDate": "Date", 
  "usedWindows": true, 
  "usedWindowsPhone": true, 
  "usedAndroidPhone": true, 
  "usediPhone": true, 
  "usediPad": true, 
  "reportPeriod": "String"
}
```
