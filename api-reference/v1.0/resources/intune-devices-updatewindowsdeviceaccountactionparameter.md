---
title: Tipo de recurso updateWindowsDeviceAccountActionParameter
description: Todavía no documentado
ms.openlocfilehash: f6403e4c3b106b318b7d551796911f6bcc0253c2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031011"
---
# <a name="updatewindowsdeviceaccountactionparameter-resource-type"></a>Tipo de recurso updateWindowsDeviceAccountActionParameter

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|deviceAccount|[windowsDeviceAccount](../resources/intune-devices-windowsdeviceaccount.md)|Todavía no documentado|
|passwordRotationEnabled|Booleano|Todavía no documentado|
|calendarSyncEnabled|Booleano|Todavía no documentado|
|deviceAccountEmail|cadena|Todavía no documentado|
|exchangeServer|cadena|Todavía no documentado|
|sessionInitiationProtocalAddress|cadena|Todavía no documentado|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.updateWindowsDeviceAccountActionParameter"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.updateWindowsDeviceAccountActionParameter",
  "deviceAccount": {
    "@odata.type": "microsoft.graph.windowsDeviceAccount",
    "password": "String"
  },
  "passwordRotationEnabled": true,
  "calendarSyncEnabled": true,
  "deviceAccountEmail": "String",
  "exchangeServer": "String",
  "sessionInitiationProtocalAddress": "String"
}
```



