---
title: tipo de recurso advancedThreatProtectionOnboardingDeviceSettingState
description: Estado de incorporación de ATP para un dispositivo dado.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 26cc9d42238dd19b256b80e7e70ac605e8742d3d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953087"
---
# <a name="advancedthreatprotectiononboardingdevicesettingstate-resource-type"></a>tipo de recurso advancedThreatProtectionOnboardingDeviceSettingState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estado de incorporación de ATP para un dispositivo dado.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista advancedThreatProtectionOnboardingDeviceSettingStates](../api/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate-list.md)|colección de [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md)|Propiedades de la lista y relaciones de los objetos [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) .|
|[Obtener advancedThreatProtectionOnboardingDeviceSettingState](../api/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate-get.md)|[advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md)|Leer las propiedades y las relaciones del objeto [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) .|
|[Crear advancedThreatProtectionOnboardingDeviceSettingState](../api/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate-create.md)|[advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md)|Crear un nuevo objeto [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) .|
|[Eliminar advancedThreatProtectionOnboardingDeviceSettingState](../api/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate-delete.md)|Ninguno|Elimina un [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md).|
|[Actualizar advancedThreatProtectionOnboardingDeviceSettingState](../api/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate-update.md)|[advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md)|Actualizar las propiedades de un objeto [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad|
|platformType|[deviceType](../resources/intune-shared-devicetype.md)|Tipo de plataforma del dispositivo. Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.|
|ajustes|String|El nombre de la clase de configuración y el nombre de propiedad.|
|settingName|String|El nombre de configuración que se está notificando|
|deviceId|Cadena|El identificador del dispositivo que se está notificando|
|deviceName|String|El nombre del dispositivo que se está notificando|
|userId|Cadena|El identificador del usuario que se está notificando|
|userEmail|String|La dirección de correo electrónico del usuario que se está notificando|
|userName|String|El nombre de usuario que se está notificando|
|userPrincipalName|String|El nombre principal de usuario que se está notificando|
|deviceModel|Cadena|El modelo de dispositivo que se está notificando|
|estado|[complianceStatus](../resources/intune-shared-compliancestatus.md)|El estado de cumplimiento de la configuración. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.|
|complianceGracePeriodExpirationDateTime|DateTimeOffset|La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.advancedThreatProtectionOnboardingDeviceSettingState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.advancedThreatProtectionOnboardingDeviceSettingState",
  "id": "String (identifier)",
  "platformType": "String",
  "setting": "String",
  "settingName": "String",
  "deviceId": "String",
  "deviceName": "String",
  "userId": "String",
  "userEmail": "String",
  "userName": "String",
  "userPrincipalName": "String",
  "deviceModel": "String",
  "state": "String",
  "complianceGracePeriodExpirationDateTime": "String (timestamp)"
}
```





