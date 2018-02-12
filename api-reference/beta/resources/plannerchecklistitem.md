# Tipo de recurso plannerChecklistItem
<a id="plannerchecklistitem-resource-type" class="xliff"></a>


El recurso **plannerChecklistItem** representa un elemento de la lista de comprobación de una tarea. La lista de comprobación de una tarea está representada por el objeto [checklistItems](plannerchecklistitems.md).


## Propiedades
<a id="properties" class="xliff"></a>
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|isChecked|Booleano|El valor es `true` si el elemento está activado o `false` si no lo está.|
|lastModifiedBy|[identitySet](identityset.md)| Solo lectura. Id. del usuario que lo modificó por última vez.|
|lastModifiedDateTime|DateTimeOffset|Solo lectura. Fecha y hora en que se modificó por última vez. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|orderHint|Cadena|Se usa para establecer el orden relativo de los elementos de la lista de comprobación. El formato se define tal como se describe [aquí](planner_order_hint_format.md).|
|title|Cadena|Título del elemento de la lista de comprobación|

## Representación JSON
<a id="json-representation" class="xliff"></a>
Aquí tiene una representación JSON del recurso.

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