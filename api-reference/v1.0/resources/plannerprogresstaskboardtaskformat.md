# <a name="plannerprogresstaskboardtaskformat-resource-type"></a>Tipo de recurso plannerProgressTaskBoardTaskFormat

El recurso **plannerProgressTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Progreso del panel de tareas (una vista organizada por el estado del campo PorcentajeCompletado en el objeto de la tarea, con columnas para No iniciado, En curso y Completado). Cada [task](plannertask.md) tendrá un objeto **plannerProgressTaskBoardTaskFormat** asociado.


### <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerProgressTaskBoardTaskFormat](../api/plannerprogresstaskboardtaskformat_get.md) | [plannerProgressTaskBoardTaskFormat](plannerprogresstaskboardtaskformat.md) |Leer las propiedades y las relaciones del objeto **plannerProgressTaskBoardTaskFormat**.|
|[Update](../api/plannerprogresstaskboardtaskformat_update.md) | [plannerProgressTaskBoardTaskFormat](plannerprogresstaskboardtaskformat.md)    |Actualizar el objeto **plannerProgressTaskBoardTaskFormat**. |

### <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|id|String| Solo lectura. Identificador del recurso. Tiene 28 caracteres y distingue entre mayúsculas y minúsculas. La [validación del formato](planner_identifiers_disclaimer.md) se efectúa en el servicio.|
|orderHint|String|Valor de sugerencia usado para ordenar la tarea en la vista Progreso del panel de tareas. El formato se define tal como se describe [aquí](planner_order_hint_format.md).|

### <a name="relationships"></a>Relaciones
Ninguno


### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerProgressTaskBoardTaskFormat"
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
  "description": "plannerProgressTaskBoardTaskFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->