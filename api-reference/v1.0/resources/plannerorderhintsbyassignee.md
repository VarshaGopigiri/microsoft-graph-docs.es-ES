# <a name="plannerorderhintsbyassignee-resource-type"></a><span data-ttu-id="03a49-101">Tipo de recurso plannerOrderHintsByAssignee</span><span class="sxs-lookup"><span data-stu-id="03a49-101">plannerOrderHintsByAssignee resource type</span></span>

<span data-ttu-id="03a49-p101">El recurso **plannerOrderHintsByAssignee** es un recurso que contiene [sugerencias de orden](planner_order_hint_format.md) para las personas asignadas en un recurso [plannerTask](plannerTask.md), para indicar el orden de la tarea en la vista Asignado a del panel de tareas. Este tipo es un tipo abierto. Las propiedades son los identificadores de los usuarios asignados a la tarea, mientras que los valores son sugerencias de orden.</span><span class="sxs-lookup"><span data-stu-id="03a49-p101">The **plannerOrderHintsByAssignee** is a resource that contains [ordering hints](planner_order_hint_format.md) for assignees in a [plannerTask](plannerTask.md) resource, to indicate the order of the task in Assigned To view of the Task Board. This type is an open type. The properties are the ids of users assigned to the task, and the values are order hints.</span></span>

## <a name="properties"></a><span data-ttu-id="03a49-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03a49-105">Properties</span></span>
<span data-ttu-id="03a49-p102">El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar los identificadores de los usuarios asignados a la tarea como nombres de propiedad, así como una [sugerencia de orden](planner_order_hint_format.md) válida como valor. Las propiedades no se pueden quitar de este tipo. El servicio quitará automáticamente los valores a medida que se actualicen las asignaciones de la [plannerTask](plannerTask.md).</span><span class="sxs-lookup"><span data-stu-id="03a49-p102">Properties of an Open Type can be defined by the client. In this case, the client must provide ids of users assigned to the task as property names, and a valid [order hint](planner_order_hint_format.md) as the value. Properties cannot be removed from this type. The service will automatically remove values as the assignments on the containing [plannerTask](plannerTask.md) are updated.</span></span>

<span data-ttu-id="03a49-110">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="03a49-110">Example:</span></span>

<!-- {
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [ "ca2a1df2-e36b-4987-9f6b-0ea462f4eb47", "4e98f8f1-bb03-4015-b8e0-19bb370949d8" ],
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