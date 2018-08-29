# <a name="iosmobileappconfiguration-resource-type"></a>Tipo de recurso iosMobileAppConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades, las propiedades heredadas y las acciones para las configuraciones de la aplicación móvil de iOS.

Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosMobileAppConfigurations](../api/intune_apps_iosmobileappconfiguration_list.md)|Colección [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md)|Enumera las propiedades y las relaciones de los objetos [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md).|
|[Obtener iosMobileAppConfiguration](../api/intune_apps_iosmobileappconfiguration_get.md)|[iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md)|Lee las propiedades y las relaciones del objeto [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md).|
|[Crear iosMobileAppConfiguration](../api/intune_apps_iosmobileappconfiguration_create.md)|[iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md)|Crea un nuevo objeto [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md).|
|[Eliminar iosMobileAppConfiguration](../api/intune_apps_iosmobileappconfiguration_delete.md)|Ninguno|Elimina una [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md).|
|[Actualizar iosMobileAppConfiguration](../api/intune_apps_iosmobileappconfiguration_update.md)|[iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md)|Actualiza las propiedades de un objeto [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|
|targetedMobileApps|Colección string|La aplicación asociada. Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|
|versión|Int32|Versión de la configuración del dispositivo. Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|
|encodedSettingXml|Binario|Binario Base64 de la configuración de la aplicación mdm.|
|configuración|Colección [appConfigurationSettingItem](../resources/intune_apps_appconfigurationsettingitem.md)|Elementos de opción de configuración de la aplicación.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [managedDeviceMobileAppConfigurationAssignment](../resources/intune_apps_manageddevicemobileappconfigurationassignment.md)|La lista de asignaciones de grupo para la configuración de la aplicación. Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|
|deviceStatuses|Colección de [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md)|Lista de ManagedDeviceMobileAppConfigurationDeviceStatus. Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|
|userStatuses|Colección [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md)|Lista de ManagedDeviceMobileAppConfigurationUserStatus. Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|
|deviceStatusSummary|[managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md)|Resumen del estado del dispositivo de la configuración de aplicaciones. Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|
|userStatusSummary|[managedDeviceMobileAppConfigurationUserSummary](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md)|Resumen del estado del usuario de la configuración de aplicaciones. Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.managedDeviceMobileAppConfiguration",
  "@odata.type": "microsoft.graph.iosMobileAppConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosMobileAppConfiguration",
  "id": "String (identifier)",
  "targetedMobileApps": [
    "String"
  ],
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024,
  "encodedSettingXml": "binary",
  "settings": [
    {
      "@odata.type": "microsoft.graph.appConfigurationSettingItem",
      "appConfigKey": "String",
      "appConfigKeyType": "String",
      "appConfigKeyValue": "String"
    }
  ]
}
```



