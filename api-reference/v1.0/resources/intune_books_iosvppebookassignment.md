# <a name="iosvppebookassignment-resource-type"></a>Tipo de recurso iosVppEBookAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades que se usan para asignar a un grupo un libro electrónico de VPP para iOS.

Hereda de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosVppEBookAssignments](../api/intune_books_iosvppebookassignment_list.md)|Colección [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md)|Enumere las propiedades y las relaciones de los objetos [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).|
|[Obtener iosVppEBookAssignment](../api/intune_books_iosvppebookassignment_get.md)|[iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md)|Lea las propiedades y las relaciones del objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).|
|[Crear iosVppEBookAssignment](../api/intune_books_iosvppebookassignment_create.md)|[iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md)|Cree un objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).|
|[Eliminar iosVppEBookAssignment](../api/intune_books_iosvppebookassignment_delete.md)|Ninguna|Elimina un [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).|
|[Actualizar iosVppEBookAssignment](../api/intune_books_iosvppebookassignment_update.md)|[iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md)|Actualice las propiedades de un objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)|
|destino|[deviceAndAppManagementAssignmentTarget](../resources/intune_books_deviceandappmanagementassignmenttarget.md)|El destino de la asignación para el libro electrónico. Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)|
|installIntent|Cadena|El objetivo de instalación para el libro electrónico. Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md). Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosVppEBookAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppEBookAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "String"
}
```



