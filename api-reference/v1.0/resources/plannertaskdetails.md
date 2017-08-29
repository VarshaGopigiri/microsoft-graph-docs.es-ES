# <a name="plannertaskdetails-resource-type"></a>Tipo de recurso plannerTaskDetails

El recurso **plannerTaskDetails** representa la información adicional de una tarea. Cada objeto [task](plannertask.md) tiene un objeto details.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerTaskDetails](../api/plannertaskdetails_get.md) | [plannerTaskDetails](plannertaskdetails.md) |Leer las propiedades y las relaciones del objeto **plannerTaskDetails**.|
|[Update](../api/plannertaskdetails_update.md) | [plannerTaskDetails](plannertaskdetails.md)    |Actualizar el objeto **plannerTaskDetails**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|checklist|[plannerChecklistItems](plannerchecklistitems.md)|Colección de elementos de la lista de comprobación de la tarea.|
|description|String|Descripción de la tarea|
|id|String| Solo lectura. Id. de los detalles de la tarea. Tiene 28 caracteres y distingue entre mayúsculas y minúsculas. La [validación del formato](planner_identifiers_disclaimer.md) se efectúa en el servicio.|
|previewType|string|Establece el tipo de vista previa que aparece en la tarea. Los valores posibles son `automatic`, `noPreview`, `checklist`, `description` y `reference`. Si se establece en `automatic`, la aplicación que visualiza la tarea elige la vista previa mostrada.|
|references|[plannerExternalReferences](plannerexternalreferences.md)|La colección de referencias de la tarea.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerTaskDetails"
}-->

```json
{
  "checklist": {"@odata.type": "microsoft.graph.plannerChecklistItems"},
  "description": "String",
  "id": "String (identifier)",
  "previewType": "string",
  "references": {"@odata.type": "microsoft.graph.plannerExternalReferences"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerTaskDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->