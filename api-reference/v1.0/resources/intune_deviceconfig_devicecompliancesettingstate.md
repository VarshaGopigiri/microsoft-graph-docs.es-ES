# <a name="devicecompliancesettingstate-resource-type"></a>Tipo de recurso deviceComplianceSettingState

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estados de configuración de cumplimiento del dispositivo para un dispositivo determinado.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceComplianceSettingStates](../api/intune_deviceconfig_devicecompliancesettingstate_list.md)|Colección [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md)|Enumere las propiedades y las relaciones de los objetos [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).|
|[Obtener deviceComplianceSettingState](../api/intune_deviceconfig_devicecompliancesettingstate_get.md)|[deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md)|Lea las propiedades y las relaciones del objeto [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).|
|[Crear deviceComplianceSettingState](../api/intune_deviceconfig_devicecompliancesettingstate_create.md)|[deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md)|Cree un objeto [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).|
|[Eliminar deviceComplianceSettingState](../api/intune_deviceconfig_devicecompliancesettingstate_delete.md)|Ninguno|Elimina un [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).|
|[Actualizar deviceComplianceSettingState](../api/intune_deviceconfig_devicecompliancesettingstate_update.md)|[deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md)|Actualice las propiedades de un objeto [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad|
|ajustes|Cadena|El nombre de la clase de configuración y el nombre de propiedad.|
|settingName|Cadena|El nombre de configuración que se está notificando|
|deviceId|Cadena|El identificador del dispositivo que se está notificando|
|deviceName|Cadena|El nombre del dispositivo que se está notificando|
|userId|Cadena|El identificador del usuario que se está notificando|
|userEmail|Cadena|La dirección de correo electrónico del usuario que se está notificando|
|userName|Cadena|El nombre de usuario que se está notificando|
|userPrincipalName|Cadena|El nombre principal de usuario que se está notificando|
|deviceModel|Cadena|El modelo de dispositivo que se está notificando|
|estado|[complianceStatus](../resources/intune_shared_compliancestatus.md)|El estado de cumplimiento de la configuración. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.|
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



