# <a name="deviceconfiguration-resource-type"></a>Tipo de recurso deviceConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceConfigurations](../api/intune_deviceconfig_deviceconfiguration_list.md)|Colección [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|[Obtener deviceConfiguration](../api/intune_deviceconfig_deviceconfiguration_get.md)|[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|Lea las propiedades y las relaciones del objeto [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).|
|[Acción assign](../api/intune_deviceconfig_deviceconfiguration_assign.md)|Colección [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto.|
|descripción|cadena|Descripción proporcionada por el administrador de la configuración del dispositivo.|
|displayName|cadena|Nombre proporcionado por el administrador de la configuración del dispositivo.|
|versión|Int32|Versión de la configuración del dispositivo.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|Asignaciones|Colección [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|La lista de tareas para el perfil de configuración del dispositivo.|
|deviceStatuses|Colección [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md)|Estado de instalación de configuración del dispositivo por dispositivo.|
|userStatuses|Colección [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md)|Estado de instalación de configuración del dispositivo por usuario.|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md)|Información general del estado del dispositivo sobre la configuración de dispositivos|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md)|Información general del estado de los usuarios sobre la configuración de dispositivos|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md)|Resumen de dispositivo del estado de configuración de la configuración de dispositivos|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024
}
```



