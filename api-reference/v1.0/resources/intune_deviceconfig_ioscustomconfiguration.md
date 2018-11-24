# <a name="ioscustomconfiguration-resource-type"></a>Tipo de recurso iosCustomConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso iosCustomConfiguration.

Hereda de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosCustomConfigurations](../api/intune_deviceconfig_ioscustomconfiguration_list.md)|Colección [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md).|
|[Obtener iosCustomConfiguration](../api/intune_deviceconfig_ioscustomconfiguration_get.md)|[iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md)|Lea las propiedades y las relaciones del objeto [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md).|
|[Crear iosCustomConfiguration](../api/intune_deviceconfig_ioscustomconfiguration_create.md)|[iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md)|Cree un objeto [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md).|
|[Eliminar iosCustomConfiguration](../api/intune_deviceconfig_ioscustomconfiguration_delete.md)|Ninguna|Elimina un [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md).|
|[Actualizar iosCustomConfiguration](../api/intune_deviceconfig_ioscustomconfiguration_update.md)|[iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md)|Actualice las propiedades de un objeto [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|versión|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|payloadName|Cadena|Nombre que se muestra al usuario.|
|payloadFileName|Cadena|Nombre de archivo de carga útil (*.mobileconfig | *.xml).|
|carga útil|Binario|Carga útil. (Matriz de bytes codificada UTF8)|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|La lista de tareas para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceStatuses|Colección [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md)|Estado de instalación de configuración del dispositivo por dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|userStatuses|Colección [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md)|Estado de instalación de configuración de dispositivo por usuario. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md)|Información general sobre el estado de dispositivos de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md)|Información general sobre el estado de usuarios de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md)|Resumen de dispositivo sobre el estado de configuración de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosCustomConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosCustomConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "payloadName": "String",
  "payloadFileName": "String",
  "payload": "binary"
}
```



