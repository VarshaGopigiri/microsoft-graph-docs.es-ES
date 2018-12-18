---
title: Tipo de recurso deviceCompliancePolicySettingStateSummary
description: Resumen de estado de la configuración de directiva cumplimiento de dispositivo en la cuenta.
author: tfitzmac
ms.openlocfilehash: d070dd0021cd9529c55f6f4a31d8a61d0cb32413
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314955"
---
# <a name="devicecompliancepolicysettingstatesummary-resource-type"></a>Tipo de recurso deviceCompliancePolicySettingStateSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Resumen de estado de la configuración de directiva cumplimiento de dispositivo en la cuenta.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceCompliancePolicySettingStateSummaries](../api/intune-deviceconfig-devicecompliancepolicysettingstatesummary-list.md)|Colección [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md)|Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md).|
|[Obtener deviceCompliancePolicySettingStateSummary](../api/intune-deviceconfig-devicecompliancepolicysettingstatesummary-get.md)|[deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md)|Lea las propiedades y las relaciones del objeto [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md).|
|[Crear deviceCompliancePolicySettingStateSummary](../api/intune-deviceconfig-devicecompliancepolicysettingstatesummary-create.md)|[deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md)|Cree un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md).|
|[Eliminar deviceCompliancePolicySettingStateSummary](../api/intune-deviceconfig-devicecompliancepolicysettingstatesummary-delete.md)|Ninguna|Elimina un [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md).|
|[Actualizar deviceCompliancePolicySettingStateSummary](../api/intune-deviceconfig-devicecompliancepolicysettingstatesummary-update.md)|[deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md)|Actualice las propiedades de un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|ajustes|String|El nombre de la clase de configuración y el nombre de propiedad.|
|settingName|String|Nombre de la configuración.|
|platformType|[policyPlatformType](../resources/intune-deviceconfig-policyplatformtype.md)|Plataforma de configuración. Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile` y `all`.|
|unknownDeviceCount|Int32|Número de dispositivos desconocidos|
|notApplicableDeviceCount|Int32|Número de dispositivos no aplicables|
|compliantDeviceCount|Int32|Número de dispositivos compatibles|
|remediatedDeviceCount|Int32|Número de dispositivos corregidos|
|nonCompliantDeviceCount|Int32|Número de dispositivos no compatibles|
|errorDeviceCount|Int32|Número de dispositivos con error|
|conflictDeviceCount|Int32|Número de dispositivos en conflicto|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|deviceComplianceSettingStates|Colección [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md)|Todavía no documentado|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCompliancePolicySettingStateSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingStateSummary",
  "id": "String (identifier)",
  "setting": "String",
  "settingName": "String",
  "platformType": "String",
  "unknownDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "compliantDeviceCount": 1024,
  "remediatedDeviceCount": 1024,
  "nonCompliantDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "conflictDeviceCount": 1024
}
```





