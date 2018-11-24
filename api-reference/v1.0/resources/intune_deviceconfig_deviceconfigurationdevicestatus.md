# <a name="deviceconfigurationdevicestatus-resource-type"></a>Tipo de recurso deviceConfigurationDeviceStatus

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceConfigurationDeviceStatuses](../api/intune_deviceconfig_deviceconfigurationdevicestatus_list.md)|Colección [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md)|Enumere las propiedades y las relaciones de los objetos [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md).|
|[Obtener deviceConfigurationDeviceStatus](../api/intune_deviceconfig_deviceconfigurationdevicestatus_get.md)|[deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md)|Lea las propiedades y las relaciones del objeto [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md).|
|[Crear deviceConfigurationDeviceStatus](../api/intune_deviceconfig_deviceconfigurationdevicestatus_create.md)|[deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md)|Cree un objeto [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md).|
|[Eliminar deviceConfigurationDeviceStatus](../api/intune_deviceconfig_deviceconfigurationdevicestatus_delete.md)|Ninguna|Elimina un [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md)|
|[Actualizar deviceConfigurationDeviceStatus](../api/intune_deviceconfig_deviceconfigurationdevicestatus_update.md)|[deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md)|Actualice las propiedades de un objeto [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|deviceDisplayName|cadena|Nombre de dispositivo de DevicePolicyStatus.|
|userName|cadena|El nombre de usuario que se está notificando|
|deviceModel|cadena|El modelo de dispositivo que se está notificando|
|complianceGracePeriodExpirationDateTime|DateTimeOffset|La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo|
|estado|[complianceStatus](../resources/intune_shared_compliancestatus.md)|Estado de cumplimiento del informe de directiva. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.|
|lastReportedDateTime|DateTimeOffset|Fecha y hora de la última modificación del informe de directiva.|
|userPrincipalName|cadena|UserPrincipalName.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationDeviceStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStatus",
  "id": "String (identifier)",
  "deviceDisplayName": "String",
  "userName": "String",
  "deviceModel": "String",
  "complianceGracePeriodExpirationDateTime": "String (timestamp)",
  "status": "String",
  "lastReportedDateTime": "String (timestamp)",
  "userPrincipalName": "String"
}
```



