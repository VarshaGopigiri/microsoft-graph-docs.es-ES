---
title: Tipo de recurso deviceExchangeAccessStateSummary
description: Resumen del estado de acceso del dispositivo a Exchange
author: tfitzmac
ms.openlocfilehash: cb04de02e44f16534e9a57383e48d989a16f8582
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326603"
---
# <a name="deviceexchangeaccessstatesummary-resource-type"></a>Tipo de recurso deviceExchangeAccessStateSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Resumen del estado de acceso del dispositivo a Exchange
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|allowedDeviceCount|Int32|Número total de dispositivos con el estado de acceso de Exchange: Permitido.|
|blockedDeviceCount|Int32|Número total de dispositivos con el estado de acceso de Exchange: Bloqueado.|
|quarantinedDeviceCount|Int32|Número total de dispositivos con el estado de acceso de Exchange: En cuarentena.|
|unknownDeviceCount|Int32|Número total de dispositivos con el estado de acceso de Exchange: Desconocido.|
|unavailableDeviceCount|Int32|Número total de dispositivos para los que no se puede encontrar el estado de acceso de Exchange.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceExchangeAccessStateSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceExchangeAccessStateSummary",
  "allowedDeviceCount": 1024,
  "blockedDeviceCount": 1024,
  "quarantinedDeviceCount": 1024,
  "unknownDeviceCount": 1024,
  "unavailableDeviceCount": 1024
}
```





