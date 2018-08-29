# <a name="plannerappliedcategories-resource-type"></a><span data-ttu-id="8a818-101">Tipo de recurso plannerAppliedCategories</span><span class="sxs-lookup"><span data-stu-id="8a818-101">plannerAppliedCategories resource type</span></span>


<span data-ttu-id="8a818-p101">El recurso **AppliedCategoriesCollection** representa la colección de categorías (o de etiquetas) que se han aplicado a una tarea. Forma parte del objeto [plannerTask](plannertask.md). Puede haber hasta 6 categorías aplicadas a una tarea. Las descripciones de las categorías (por ejemplo, `category1`, `category2`, etc.) forman parte del objeto [plan details](plannerplandetails.md). Este es un tipo abierto.</span><span class="sxs-lookup"><span data-stu-id="8a818-p101">The **AppliedCategoriesCollection** resource represents the collection of categories (or labels) that have been applied to a task. It is part of the [plannerTask](plannertask.md) object. There can be up to 6 categories applied to a task. Category descriptions, e.g. `category1`, `category2` etc., are part of the [plan details](plannerplandetails.md) object. This is an open type.</span></span>

## <a name="properties"></a><span data-ttu-id="8a818-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a818-107">Properties</span></span>
<span data-ttu-id="8a818-p102">El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar `category1`, `category2`, `category3`, `category4`, `category5` o `category6` como propiedades con sus valores como booleano `true` cuando se apliquen las categorías correspondientes en la tarea. A continuación se muestra un ejemplo. Si no se aplican, las propiedades se quitan automáticamente estableciendo sus valores en el booleano `false`.</span><span class="sxs-lookup"><span data-stu-id="8a818-p102">Properties of an Open Type can be defined by the client. In this case though, the client must provide `category1`, `category2`, `category3`, `category4`, `category5` and/or `category6` as properties with their values being the `true` boolean when the corresponding categories are applied on the task. Example is shown below. When they do not apply, properties are automatically removed by setting their values to the `false` boolean.</span></span> 

## <a name="json-representation"></a><span data-ttu-id="8a818-112">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8a818-112">JSON representation</span></span>

<span data-ttu-id="8a818-113">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8a818-113">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [ "String-value" ],
  "@odata.type": "microsoft.graph.plannerAppliedCategories"
}-->

```json
{
  "String-value": true
}
```

<span data-ttu-id="8a818-114">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8a818-114">Example:</span></span> 

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