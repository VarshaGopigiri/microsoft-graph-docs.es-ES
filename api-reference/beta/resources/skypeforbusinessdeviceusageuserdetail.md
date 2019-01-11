---
title: tipo de recurso skypeForBusinessDeviceUsageUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 95f2f6cf1f3f6c54c4b6b4b39a7118cd8a94b224
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858383"
---
# <a name="skypeforbusinessdeviceusageuserdetail-resource-type"></a>tipo de recurso skypeForBusinessDeviceUsageUserDetail

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo    |
| :---------------- | :------ |
| reportRefreshDate | Fecha    |
| userPrincipalName | Cadena  |
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
