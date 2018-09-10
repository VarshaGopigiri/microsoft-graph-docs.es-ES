# <a name="devicecompliancescheduledactionforrule-resource-type"></a>Tipo de recurso deviceComplianceScheduledActionForRule

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Acción programada para la regla
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceComplianceScheduledActionForRules](../api/intune_deviceconfig_devicecompliancescheduledactionforrule_list.md)|Colección [deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md)|Enumere las propiedades y las relaciones de los objetos [deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md).|
|[Obtener deviceComplianceScheduledActionForRule](../api/intune_deviceconfig_devicecompliancescheduledactionforrule_get.md)|[deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md)|Lea las propiedades y las relaciones del objeto [deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md).|
|[Crear deviceComplianceScheduledActionForRule](../api/intune_deviceconfig_devicecompliancescheduledactionforrule_create.md)|[deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md)|Cree un objeto [deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md).|
|[Eliminar deviceComplianceScheduledActionForRule](../api/intune_deviceconfig_devicecompliancescheduledactionforrule_delete.md)|Ninguna|Elimina un [deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md).|
|[Actualizar deviceComplianceScheduledActionForRule](../api/intune_deviceconfig_devicecompliancescheduledactionforrule_update.md)|[deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md)|Actualice las propiedades de un objeto [deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|ruleName|String|Nombre de la regla a la que se aplica esta acción programada.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|scheduledActionConfigurations|Colección [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md)|La lista de las configuraciones de las acciones programadas para esta directiva de cumplimiento.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceScheduledActionForRule"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
  "id": "String (identifier)",
  "ruleName": "String"
}
```








