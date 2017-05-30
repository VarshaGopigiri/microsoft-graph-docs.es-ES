# <a name="plannerbuckettaskboardtaskformat-resource-type"></a>Tipo de recurso plannerBucketTaskBoardTaskFormat

El recurso **plannerBucketTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Depósitos del panel de tareas (una vista organizada por tareas dentro de los depósitos a los que están asignadas). Cada [task](plannertask.md) tendrá un objeto **plannerBucketTaskBoardTaskFormat** asociado.


### <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerBucketTaskBoardTaskFormat](../api/plannerbuckettaskboardtaskformat_get.md) | [plannerBucketTaskBoardTaskFormat](plannerbuckettaskboardtaskformat.md) |Leer las propiedades y las relaciones del objeto **plannerBucketTaskBoardTaskFormat**.|
|[Update](../api/plannerbuckettaskboardtaskformat_update.md) | [plannerBucketTaskBoardTaskFormat](plannerbuckettaskboardtaskformat.md)    |Actualizar el objeto **plannerBucketTaskBoardTaskFormat**. |

### <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|id|String| Solo lectura. Identificador del recurso. Tiene 28 caracteres y distingue entre mayúsculas y minúsculas. La [validación del formato](planner_identifiers_disclaimer.md) se efectúa en el servicio.|
|orderHint|String|Sugerencia usada para ordenar tareas en la vista Depósito del panel de tareas. El formato se define tal como se describe [aquí](planner_order_hint_format.md).|

### <a name="relationships"></a>Relaciones
Ninguno


### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerBucketTaskBoardTaskFormat"
}-->

```json
{
  "id": "String (identifier)",
  "orderHint": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerBucketTaskBoardTaskFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->