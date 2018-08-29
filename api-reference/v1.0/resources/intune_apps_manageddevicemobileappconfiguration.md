# <a name="manageddevicemobileappconfiguration-resource-type"></a>Tipo de recurso managedDeviceMobileAppConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase abstracta para la configuración de aplicaciones móviles para dispositivos inscritos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedDeviceMobileAppConfigurations](../api/intune_apps_manageddevicemobileappconfiguration_list.md)|Colección [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md).|
|[Obtener managedDeviceMobileAppConfiguration](../api/intune_apps_manageddevicemobileappconfiguration_get.md)|[managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|targetedMobileApps|Colección string|La aplicación asociada.|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto.|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo.|
|versión|Int32|Versión de la configuración del dispositivo.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [managedDeviceMobileAppConfigurationAssignment](../resources/intune_apps_manageddevicemobileappconfigurationassignment.md)|La lista de asignaciones de grupo para la configuración de la aplicación.|
|deviceStatuses|Colección de [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md)|Lista de ManagedDeviceMobileAppConfigurationDeviceStatus.|
|userStatuses|Colección [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md)|Lista de ManagedDeviceMobileAppConfigurationUserStatus.|
|deviceStatusSummary|[managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md)|Resumen del estado del dispositivo de la configuración de aplicaciones|
|userStatusSummary|[managedDeviceMobileAppConfigurationUserSummary](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md)|Resumen del estado del usuario de la configuración de aplicaciones|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "abstract": true,
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfiguration"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfiguration",
  "id": "String (identifier)",
  "targetedMobileApps": [
    "String"
  ],
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024
}
```



