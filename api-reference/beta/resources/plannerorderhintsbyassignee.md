# Tipo de recurso plannerOrderHintsByAssignee
<a id="plannerorderhintsbyassignee-resource-type" class="xliff"></a>

El recurso **plannerOrderHintsByAssignee** es un recurso que contiene [sugerencias de orden](planner_order_hint_format.md) para las personas asignadas en un recurso [plannerTask](plannerTask.md), para indicar el orden de la tarea en la vista Asignado a del panel de tareas. Este tipo es un tipo abierto. Las propiedades son los identificadores de los usuarios asignados a la tarea, mientras que los valores son sugerencias de orden.

## Propiedades
<a id="properties" class="xliff"></a>
El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar los identificadores de los usuarios asignados a la tarea como nombres de propiedad, así como una [sugerencia de orden](planner_order_hint_format.md) válida como valor. Las propiedades no se pueden quitar de este tipo. El servicio quitará automáticamente los valores a medida que se actualicen las asignaciones de la [plannerTask](plannerTask.md).

Ejemplo:

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerOrderHintsByAssignee"
}-->

```json
{
  "ca2a1df2-e36b-4987-9f6b-0ea462f4eb47": "String",
  "4e98f8f1-bb03-4015-b8e0-19bb370949d8": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerOrderHintsByAssignee resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->