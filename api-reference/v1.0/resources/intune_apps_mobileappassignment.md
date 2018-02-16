# <a name="mobileappassignment-resource-type"></a>Tipo de recurso mobileAppAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase que contiene las propiedades que se usan para la asignación de grupo de una aplicación móvil.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar mobileAppAssignments](../api/intune_apps_mobileappassignment_list.md)|Colección [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)|Enumere las propiedades y las relaciones de los objetos [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md).|
|[Obtener mobileAppAssignment](../api/intune_apps_mobileappassignment_get.md)|[mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)|Lea las propiedades y las relaciones del objeto [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md).|
|[Crear mobileAppAssignment](../api/intune_apps_mobileappassignment_create.md)|[mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)|Cree un objeto [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md).|
|[Eliminar mobileAppAssignment](../api/intune_apps_mobileappassignment_delete.md)|Ninguna|Elimina un [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md).|
|[Actualizar mobileAppAssignment](../api/intune_apps_mobileappassignment_update.md)|[mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)|Actualice las propiedades de un objeto [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|objetivo|cadena|El objetivo de instalación definido por el administrador. Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.|
|destino|[deviceAndAppManagementAssignmentTarget](../resources/intune_apps_deviceandappmanagementassignmenttarget.md)|La asignación de grupo de destino definida por el administrador.|
|configuración|[mobileAppAssignmentSettings](../resources/intune_apps_mobileappassignmentsettings.md)|La asignación de la configuración para el destino definida por el administrador.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppAssignment",
  "id": "String (identifier)",
  "intent": "String",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "settings": {
    "@odata.type": "microsoft.graph.mobileAppAssignmentSettings"
  }
}
```



