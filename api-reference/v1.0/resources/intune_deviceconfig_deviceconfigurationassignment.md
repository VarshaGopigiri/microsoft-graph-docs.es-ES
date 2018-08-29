# <a name="deviceconfigurationassignment-resource-type"></a>Tipo de recurso deviceConfigurationAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

La entidad de asignación de la configuración de dispositivo asigna un grupo AAD a una configuración de dispositivo específico.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceConfigurationAssignments](../api/intune_deviceconfig_deviceconfigurationassignment_list.md)|Colección [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|Enumere las propiedades y las relaciones de los objetos [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).|
|[Obtener deviceConfigurationAssignment](../api/intune_deviceconfig_deviceconfigurationassignment_get.md)|[deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|Lea las propiedades y las relaciones del objeto [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).|
|[Crear deviceConfigurationAssignment](../api/intune_deviceconfig_deviceconfigurationassignment_create.md)|[deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|Cree un objeto [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).|
|[Eliminar deviceConfigurationAssignment](../api/intune_deviceconfig_deviceconfigurationassignment_delete.md)|Ninguna|Elimina un [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).|
|[Actualizar deviceConfigurationAssignment](../api/intune_deviceconfig_deviceconfigurationassignment_update.md)|[deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|Actualice las propiedades de un objeto [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|La clave de la asignación.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|El destino de la tarea para la configuración del dispositivo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.deviceConfigurationAssignment"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



