# <a name="managedebookassignment-resource-type"></a>Tipo de recurso managedEBookAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades que se usan para asignar un libro electrónico a un grupo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedEBookAssignments](../api/intune_books_managedebookassignment_list.md)|Colección [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)|Enumere las propiedades y las relaciones de los objetos [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).|
|[Obtener managedEBookAssignment](../api/intune_books_managedebookassignment_get.md)|[managedEBookAssignment](../resources/intune_books_managedebookassignment.md)|Lea las propiedades y las relaciones del objeto [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).|
|[Crear managedEBookAssignment](../api/intune_books_managedebookassignment_create.md)|[managedEBookAssignment](../resources/intune_books_managedebookassignment.md)|Cree un objeto [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).|
|[Eliminar managedEBookAssignment](../api/intune_books_managedebookassignment_delete.md)|Ninguna|Elimina un [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).|
|[Actualizar managedEBookAssignment](../api/intune_books_managedebookassignment_update.md)|[managedEBookAssignment](../resources/intune_books_managedebookassignment.md)|Actualice las propiedades de un objeto [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|El destino de la asignación para el libro electrónico.|
|installIntent|[installIntent](../resources/intune_shared_installintent.md)|La intención de instalación para el libro electrónico. Los valores posibles son: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedEBookAssignment"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedEBookAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "String"
}
```








