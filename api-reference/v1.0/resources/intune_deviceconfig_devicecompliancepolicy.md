# <a name="devicecompliancepolicy-resource-type"></a>Tipo de recurso deviceCompliancePolicy

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esta es la clase base para la directiva de cumplimiento. Las directivas de cumplimiento son específicas de la plataforma y las directivas de cumplimiento por plataforma individual se heredan desde ahí. 
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceCompliancePolicies](../api/intune_deviceconfig_devicecompliancepolicy_list.md)|Colección [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|[Obtener deviceCompliancePolicy](../api/intune_deviceconfig_devicecompliancepolicy_get.md)|[deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|Lea las propiedades y las relaciones del objeto [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|[Acción assign](../api/intune_deviceconfig_devicecompliancepolicy_assign.md)|Colección [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md)|Todavía no documentado|
|[Acción scheduleActionsForRules](../api/intune_deviceconfig_devicecompliancepolicy_scheduleactionsforrules.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto.|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo.|
|versión|Int32|Versión de la configuración del dispositivo.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|scheduledActionsForRule|Colección [deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md)|La lista de acción programada para esta regla|
|deviceStatuses|Colección [deviceComplianceDeviceStatus](../resources/intune_deviceconfig_devicecompliancedevicestatus.md)|Lista de DeviceComplianceDeviceStatus.|
|userStatuses|Colección [deviceComplianceUserStatus](../resources/intune_deviceconfig_devicecomplianceuserstatus.md)|Lista de DeviceComplianceUserStatus.|
|deviceStatusOverview|[deviceComplianceDeviceOverview](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md)|Información general del estado de los dispositivos sobre el cumplimiento de dispositivos|
|userStatusOverview|[deviceComplianceUserOverview](../resources/intune_deviceconfig_devicecomplianceuseroverview.md)|Información general del estado de los usuarios sobre el cumplimiento de dispositivos|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md)|Resumen de dispositivo del estado de configuración de cumplimiento|
|asignaciones|Colección [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md)|El conjunto de asignaciones para esta directiva de cumplimiento.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "abstract": true,
  "@odata.type": "microsoft.graph.deviceCompliancePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicy",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024
}
```



