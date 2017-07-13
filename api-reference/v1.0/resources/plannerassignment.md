<span data-ttu-id="b602d-p103">La sugerencia usada para ordenar las personas a las que se ha asignado una tarea. El formato se define tal como se describe [aquí](planner_order_hint_format.md).</span><span class="sxs-lookup"><span data-stu-id="b602d-p103">Hint used to order assignees in a task. The format is defined as outlined [here](planner_order_hint_format.md).</span></span>|La sugerencia usada para ordenar las personas a las que se ha asignado una tarea. El formato se define tal como se describe [aquí](planner_order_hint_format.md).|

## <span data-ttu-id="b602d-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b602d-120">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>
<span data-ttu-id="b602d-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b602d-121">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerAssignment"
}-->

```json
{
  "assignedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "assignedDateTime": "String (timestamp)",
  "orderHint": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->