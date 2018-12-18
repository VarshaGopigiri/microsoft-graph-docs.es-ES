---
title: Tipo de recurso deviceConfigurationDeviceOverview
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 1936b8256c5755c44e613c1626664cef3f7a0ccc
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324433"
---
# <a name="deviceconfigurationdeviceoverview-resource-type"></a>Tipo de recurso deviceConfigurationDeviceOverview

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceConfigurationDeviceOverview](../api/intune-deviceconfig-deviceconfigurationdeviceoverview-get.md)|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|Lea las propiedades y las relaciones del objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md).|
|[Actualizar deviceConfigurationDeviceOverview](../api/intune-deviceconfig-deviceconfigurationdeviceoverview-update.md)|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|Actualice las propiedades de un objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|pendingCount|Int32|Número de dispositivos pendientes|
|notApplicableCount|Int32|Número de dispositivos no aplicables|
|successCount|Int32|Número de dispositivos correctos|
|errorCount|Int32|Número de dispositivos con error|
|failedCount|Int32|Número de dispositivos erróneos|
|lastUpdateDateTime|DateTimeOffset|Última hora de actualización|
|configurationVersion|Int32|Versión de la directiva para esa información general|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationDeviceOverview"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceOverview",
  "id": "String (identifier)",
  "pendingCount": 1024,
  "notApplicableCount": 1024,
  "successCount": 1024,
  "errorCount": 1024,
  "failedCount": 1024,
  "lastUpdateDateTime": "String (timestamp)",
  "configurationVersion": 1024
}
```



