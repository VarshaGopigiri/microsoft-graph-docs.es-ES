# <a name="manageddevicemobileappconfigurationdevicestatus-resource-type"></a>tipo de recurso managedDeviceMobileAppConfigurationDeviceStatus

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene propiedades, las propiedades heredadas y acciones para un estado de configuración de aplicación móvil de MDM para un dispositivo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista managedDeviceMobileAppConfigurationDeviceStatuses](../api/intune_apps_manageddevicemobileappconfigurationdevicestatus_list.md)|colección de [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md)|Propiedades de la lista y relaciones de los objetos [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md) .|
|[Obtener managedDeviceMobileAppConfigurationDeviceStatus](../api/intune_apps_manageddevicemobileappconfigurationdevicestatus_get.md)|[managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md)|Leer las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md) .|
|[Crear managedDeviceMobileAppConfigurationDeviceStatus](../api/intune_apps_manageddevicemobileappconfigurationdevicestatus_create.md)|[managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md)|Crear un nuevo objeto [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md) .|
|[Eliminar managedDeviceMobileAppConfigurationDeviceStatus](../api/intune_apps_manageddevicemobileappconfigurationdevicestatus_delete.md)|Ninguno|Elimina un [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md).|
|[Actualizar managedDeviceMobileAppConfigurationDeviceStatus](../api/intune_apps_manageddevicemobileappconfigurationdevicestatus_update.md)|[managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md)|Actualizar las propiedades de un objeto [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|deviceDisplayName|String|Nombre de dispositivo de DevicePolicyStatus.|
|userName|String|El nombre de usuario que se está notificando|
|deviceModel|String|El modelo de dispositivo que se está notificando|
|complianceGracePeriodExpirationDateTime|DateTimeOffset|La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo|
|status|[complianceStatus](../resources/intune_shared_compliancestatus.md)|Estado de cumplimiento del informe de directiva. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.|
|lastReportedDateTime|DateTimeOffset|Fecha y hora de la última modificación del informe de directiva.|
|userPrincipalName|String|UserPrincipalName.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfigurationDeviceStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceStatus",
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



