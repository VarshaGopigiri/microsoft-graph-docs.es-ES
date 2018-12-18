---
title: Tipo de recurso updateWindowsDeviceAccountActionParameter
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: ba23c3b302d1a988a814c31ab0a1efcec405641f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332217"
---
# <a name="updatewindowsdeviceaccountactionparameter-resource-type"></a>Tipo de recurso updateWindowsDeviceAccountActionParameter

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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





