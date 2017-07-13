<span data-ttu-id="355f7-p102">El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar `category1`, `category2`, `category3`, `category4`, `category5` o `category6` como propiedades con sus valores como booleano `true` cuando se apliquen las categorías correspondientes en la tarea. A continuación se muestra un ejemplo. Si no se aplican, las propiedades se quitan automáticamente estableciendo sus valores en el booleano `false`.</span><span class="sxs-lookup"><span data-stu-id="355f7-p102">Properties of an Open Type can be defined by the client. In this case though, the client must provide `category1`, `category2`, `category3`, `category4`, `category5` and/or `category6` as properties with their values being the `true` boolean when the corresponding categories are applied on the task. Example is shown below. When they do not apply, properties are automatically removed by setting their values to the `false` boolean.</span></span>
El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar `category1`, `category2`, `category3`, `category4`, `category5` o `category6` como propiedades con sus valores como booleano `true` cuando se apliquen las categorías correspondientes en la tarea. A continuación se muestra un ejemplo. Si no se aplican, las propiedades se quitan automáticamente estableciendo sus valores en el booleano `false`. 

## <span data-ttu-id="355f7-112">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="355f7-112">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>

<span data-ttu-id="355f7-113">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="355f7-113">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerAppliedCategories"
}-->

```json
{
  "String-value": true
}
```

<span data-ttu-id="355f7-114">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="355f7-114">Example:</span></span> 

```json
{
  "category1": true,
  "category3": true,
  "category5": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAppliedCategories resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->