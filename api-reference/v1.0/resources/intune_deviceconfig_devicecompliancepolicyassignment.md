# <a name="devicecompliancepolicyassignment-resource-type"></a>Tipo de recurso deviceCompliancePolicyAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Asignación de directivas de cumplimiento de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceCompliancePolicyAssignments](../api/intune_deviceconfig_devicecompliancepolicyassignment_list.md)|Colección [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md)|Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md).|
|[Obtener deviceCompliancePolicyAssignment](../api/intune_deviceconfig_devicecompliancepolicyassignment_get.md)|[deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md)|Lea las propiedades y las relaciones del objeto [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md).|
|[Crear deviceCompliancePolicyAssignment](../api/intune_deviceconfig_devicecompliancepolicyassignment_create.md)|[deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md)|Cree un objeto [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md).|
|[Eliminar deviceCompliancePolicyAssignment](../api/intune_deviceconfig_devicecompliancepolicyassignment_delete.md)|Ninguna|Elimina un [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md).|
|[Actualizar deviceCompliancePolicyAssignment](../api/intune_deviceconfig_devicecompliancepolicyassignment_update.md)|[deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md)|Actualice las propiedades de un objeto [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|Destino de la asignación de directivas de cumplimiento|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.deviceCompliancePolicyAssignment"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



