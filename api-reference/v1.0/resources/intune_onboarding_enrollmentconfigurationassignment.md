# <a name="enrollmentconfigurationassignment-resource-type"></a>Tipo de recurso enrollmentConfigurationAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar enrollmentConfigurationAssignments](../api/intune_onboarding_enrollmentconfigurationassignment_list.md)|Colección [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md)|Enumere las propiedades y las relaciones de los objetos [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md).|
|[Obtener enrollmentConfigurationAssignment](../api/intune_onboarding_enrollmentconfigurationassignment_get.md)|[enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md)|Lea las propiedades y las relaciones del objeto [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md).|
|[Crear enrollmentConfigurationAssignment](../api/intune_onboarding_enrollmentconfigurationassignment_create.md)|[enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md)|Cree un objeto [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md).|
|[Eliminar enrollmentConfigurationAssignment](../api/intune_onboarding_enrollmentconfigurationassignment_delete.md)|Ninguna|Elimina un [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md).|
|[Actualizar enrollmentConfigurationAssignment](../api/intune_onboarding_enrollmentconfigurationassignment_update.md)|[enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md)|Actualice las propiedades de un objeto [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Todavía no documentado|
|destino|[deviceAndAppManagementAssignmentTarget](../resources/intune_onboarding_deviceandappmanagementassignmenttarget.md)|Todavía no documentado|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.enrollmentConfigurationAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.enrollmentConfigurationAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



