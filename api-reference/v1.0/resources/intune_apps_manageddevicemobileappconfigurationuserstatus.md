# <a name="manageddevicemobileappconfigurationuserstatus-resource-type"></a>Tipo de recurso managedDeviceMobileAppConfigurationUserStatus

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de configuración de aplicaciones móviles de MDM para un usuario.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedDeviceMobileAppConfigurationUserStatuses](../api/intune_apps_manageddevicemobileappconfigurationuserstatus_list.md)|Colección [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md)|Enumere las propiedades y las relaciones de los objetos [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md).|
|[Obtener managedDeviceMobileAppConfigurationUserStatus](../api/intune_apps_manageddevicemobileappconfigurationuserstatus_get.md)|[managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md)|Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md).|
|[Crear managedDeviceMobileAppConfigurationUserStatus](../api/intune_apps_manageddevicemobileappconfigurationuserstatus_create.md)|[managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md)|Cree un objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md).|
|[Eliminar managedDeviceMobileAppConfigurationUserStatus](../api/intune_apps_manageddevicemobileappconfigurationuserstatus_delete.md)|Ninguna|Elimina un [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md)|
|[Actualizar managedDeviceMobileAppConfigurationUserStatus](../api/intune_apps_manageddevicemobileappconfigurationuserstatus_update.md)|[managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md)|Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|userDisplayName|cadena|Nombre de usuario de DevicePolicyStatus.|
|devicesCount|Int32|Número de dispositivos para dicho usuario.|
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
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfigurationUserStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationUserStatus",
  "id": "String (identifier)",
  "userDisplayName": "String",
  "devicesCount": 1024,
  "status": "String",
  "lastReportedDateTime": "String (timestamp)",
  "userPrincipalName": "String"
}
```



