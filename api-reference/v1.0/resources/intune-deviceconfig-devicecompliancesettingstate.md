---
title: Tipo de recurso deviceComplianceSettingState
description: Estados de configuración de cumplimiento del dispositivo para un dispositivo determinado.
author: tfitzmac
ms.openlocfilehash: e4edce4b22b70c6018703e086d606b84781b6b91
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326177"
---
# <a name="devicecompliancesettingstate-resource-type"></a>Tipo de recurso deviceComplianceSettingState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estados de configuración de cumplimiento del dispositivo para un dispositivo determinado.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceComplianceSettingStates](../api/intune-deviceconfig-devicecompliancesettingstate-list.md)|Colección [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md)|Enumere las propiedades y las relaciones de los objetos [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).|
|[Obtener deviceComplianceSettingState](../api/intune-deviceconfig-devicecompliancesettingstate-get.md)|[deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md)|Lea las propiedades y las relaciones del objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).|
|[Crear deviceComplianceSettingState](../api/intune-deviceconfig-devicecompliancesettingstate-create.md)|[deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md)|Cree un objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).|
|[Eliminar deviceComplianceSettingState](../api/intune-deviceconfig-devicecompliancesettingstate-delete.md)|Ninguno|Elimina un [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).|
|[Actualizar deviceComplianceSettingState](../api/intune-deviceconfig-devicecompliancesettingstate-update.md)|[deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md)|Actualice las propiedades de un objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad|
|ajustes|String|El nombre de la clase de configuración y el nombre de propiedad.|
|settingName|String|El nombre de configuración que se está notificando|
|deviceId|String|El identificador del dispositivo que se está notificando|
|deviceName|String|El nombre del dispositivo que se está notificando|
|userId|String|El identificador del usuario que se está notificando|
|userEmail|String|La dirección de correo electrónico del usuario que se está notificando|
|userName|String|El nombre de usuario que se está notificando|
|userPrincipalName|String|El nombre principal de usuario que se está notificando|
|deviceModel|String|El modelo de dispositivo que se está notificando|
|state|[complianceStatus](../resources/intune-shared-compliancestatus.md)|El estado de cumplimiento de la configuración. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.|
|complianceGracePeriodExpirationDateTime|DateTimeOffset|La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceSettingState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceSettingState",
  "id": "String (identifier)",
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



