---
title: Tipo de recurso deviceComplianceDeviceOverview
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 17e37af04c61d29938dfe0dc33f12c025973d7b8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332280"
---
# <a name="devicecompliancedeviceoverview-resource-type"></a>Tipo de recurso deviceComplianceDeviceOverview

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceComplianceDeviceOverview](../api/intune-deviceconfig-devicecompliancedeviceoverview-get.md)|[deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md)|Lea las propiedades y las relaciones del objeto [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md).|
|[Actualizar deviceComplianceDeviceOverview](../api/intune-deviceconfig-devicecompliancedeviceoverview-update.md)|[deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md)|Actualice las propiedades de un objeto [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|pendingCount|Int32|Número de dispositivos pendientes|
|notApplicableCount|Int32|Número de dispositivos no aplicables|
|notApplicablePlatformCount|Int32|Número de dispositivos no aplicables debido a la plataforma de error de coincidencia y la directiva|
|successCount|Int32|Número de dispositivos correctos|
|errorCount|Int32|Número de dispositivos con error|
|failedCount|Int32|Número de dispositivos erróneos|
|conflictCount|Int32|Número de dispositivos en conflicto|
|lastUpdateDateTime|DateTimeOffset|Última hora de actualización|
|configurationVersion|Int32|Versión de la directiva para esa información general|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceDeviceOverview"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceDeviceOverview",
  "id": "String (identifier)",
  "pendingCount": 1024,
  "notApplicableCount": 1024,
  "notApplicablePlatformCount": 1024,
  "successCount": 1024,
  "errorCount": 1024,
  "failedCount": 1024,
  "conflictCount": 1024,
  "lastUpdateDateTime": "String (timestamp)",
  "configurationVersion": 1024
}
```





