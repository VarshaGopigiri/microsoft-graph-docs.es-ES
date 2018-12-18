---
title: Tipo de recurso deviceCompliancePolicyDeviceStateSummary
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 006b1ca71f8441898ba758397334c7ae31ac5690
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27318812"
---
# <a name="devicecompliancepolicydevicestatesummary-resource-type"></a>Tipo de recurso deviceCompliancePolicyDeviceStateSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceCompliancePolicyDeviceStateSummary](../api/intune-deviceconfig-devicecompliancepolicydevicestatesummary-get.md)|[deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md)|Lea las propiedades y las relaciones del objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).|
|[Actualizar deviceCompliancePolicyDeviceStateSummary](../api/intune-deviceconfig-devicecompliancepolicydevicestatesummary-update.md)|[deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md)|Actualice las propiedades de un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|inGracePeriodCount|Int32|Número de dispositivos que se encuentran en el período de gracia|
|configManagerCount|Int32|Número de dispositivos cuyo cumplimiento lo administra System Center Configuration Manager|
|id|String|Clave de la entidad.|
|unknownDeviceCount|Int32|Número de dispositivos desconocidos|
|notApplicableDeviceCount|Int32|Número de dispositivos no aplicables|
|compliantDeviceCount|Int32|Número de dispositivos compatibles|
|remediatedDeviceCount|Int32|Número de dispositivos corregidos|
|nonCompliantDeviceCount|Int32|Número de dispositivos no compatibles|
|errorDeviceCount|Int32|Número de dispositivos con error|
|conflictDeviceCount|Int32|Número de dispositivos en conflicto|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCompliancePolicyDeviceStateSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyDeviceStateSummary",
  "inGracePeriodCount": 1024,
  "configManagerCount": 1024,
  "id": "String (identifier)",
  "unknownDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "compliantDeviceCount": 1024,
  "remediatedDeviceCount": 1024,
  "nonCompliantDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "conflictDeviceCount": 1024
}
```





