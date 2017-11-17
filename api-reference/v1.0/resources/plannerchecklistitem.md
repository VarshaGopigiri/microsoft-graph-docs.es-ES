<span data-ttu-id="83c49-p104">Se usa para establecer el orden relativo de los elementos de la lista de comprobación. El formato se define tal como se describe [aquí](planner_order_hint_format.md).</span><span class="sxs-lookup"><span data-stu-id="83c49-p104">Used to set the relative order of items in the checklist. The format is defined as outlined [here](planner_order_hint_format.md).</span></span>|Se usa para establecer el orden relativo de los elementos de la lista de comprobación. El formato se define tal como se describe [aquí](planner_order_hint_format.md).|
|<span data-ttu-id="83c49-125">title</span><span class="sxs-lookup"><span data-stu-id="83c49-125">title</span></span>|<span data-ttu-id="83c49-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="83c49-126">String</span></span>|<span data-ttu-id="83c49-127">Título del elemento de la lista de comprobación</span><span class="sxs-lookup"><span data-stu-id="83c49-127">Title of the checklist item</span></span>|

## <span data-ttu-id="83c49-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="83c49-128">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>
<span data-ttu-id="83c49-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="83c49-129">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerChecklistItem"
}-->

```json
{
  "isChecked": true,
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "orderHint": "String",
  "title": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerChecklistItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->