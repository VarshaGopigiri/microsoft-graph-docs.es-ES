# <a name="plannercategorydescriptions-resource-type"></a>Tipo de recurso plannerCategoryDescriptions

El recurso **plannerCategoryDescriptions** representa las etiquetas descriptivas de las categorías que se han definido para un plan. Pertenece al objeto [plan details](plannerplandetails.md). Puede haber hasta 6 categorías definidas. 


### <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|category1|Cadena|Etiqueta asociada a la categoría 1|
|category2|Cadena|Etiqueta asociada a la categoría 2|
|category3|Cadena|Etiqueta asociada a la categoría 3|
|category4|Cadena|Etiqueta asociada a la categoría 4|
|category5|Cadena|Etiqueta asociada a la categoría 5|
|category6|Cadena|Etiqueta asociada a la categoría 6|

### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerCategoryDescriptions"
}-->

```json
{
  "category1": "String",
  "category2": "String",
  "category3": "String",
  "category4": "String",
  "category5": "String",
  "category6": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerCategoryDescriptions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->