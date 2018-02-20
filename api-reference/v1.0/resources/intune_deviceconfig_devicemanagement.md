# <a name="devicemanagement-resource-type"></a>Tipo de recurso deviceManagement

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceManagement](../api/intune_deviceconfig_devicemanagement_get.md)|[deviceManagement](../resources/intune_deviceconfig_devicemanagement.md)|Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_deviceconfig_devicemanagement.md).|
|[Actualizar deviceManagement](../api/intune_deviceconfig_devicemanagement_update.md)|[deviceManagement](../resources/intune_deviceconfig_devicemanagement.md)|Actualice las propiedades de un objeto [deviceManagement](../resources/intune_deviceconfig_devicemanagement.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único|
|configuración|[deviceManagementSettings](../resources/intune_deviceconfig_devicemanagementsettings.md)|Configuración de niveles de cuenta.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|deviceConfigurations|Colección [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|Las configuraciones de dispositivos.|
|deviceCompliancePolicies|Colección [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|Las directivas de cumplimiento de dispositivos.|
|softwareUpdateStatusSummary|[softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md)|El resumen del estado de la actualización de software.|
|deviceCompliancePolicyDeviceStateSummary|[deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md)|El resumen del estado de cumplimiento de dispositivos para esta cuenta.|
|deviceCompliancePolicySettingStateSummaries|Colección [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md)|Los estados de resumen de la configuración de directiva de cumplimiento para esta cuenta.|
|deviceConfigurationDeviceStateSummaries|[deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md)|El resumen de estado del dispositivo de la configuración de dispositivo para esta cuenta.|
|iosUpdateStatuses|Colección [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md)|Los estados de instalación de actualización del software de iOS para esta cuenta.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)",
  "settings": {
    "@odata.type": "microsoft.graph.deviceManagementSettings",
    "deviceComplianceCheckinThresholdDays": 1024,
    "isScheduledActionEnabled": true,
    "secureByDefault": true
  }
}
```



