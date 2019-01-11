---
title: Tipo de recurso deviceExchangeAccessStateSummary
description: Resumen del estado de acceso del dispositivo a Exchange
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b8ca08b026b8e1cdbac4bd0dc73331a9d5df80fc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889988"
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





