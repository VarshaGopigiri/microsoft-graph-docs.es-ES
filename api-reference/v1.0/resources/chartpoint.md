# <a name="chartpoint-resource-type"></a>Tipo de recurso ChartPoint

Representa un punto de una serie de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartPoint](../api/chartpoint_get.md) | [WorkbookChartPoint](chartpoint.md) |Lee las propiedades y relaciones del objeto chartPoint.|
|[Lista](../api/chartpoint_list.md) | Colección de [WorkbookChartPoint](chartpoint.md) |Obtiene la colección de objetos chartPoint. |
|[Itemat](../api/chartpointscollection_itemat.md)|[WorkbookChartPoint](chartpoint.md)|Recupera un punto en función de su posición dentro de la serie.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|value|Json|Devuelve el valor de un punto del gráfico. Solo lectura.|
|id|cadena|identificador único|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[WorkbookChartPointFormat](chartpointformat.md)|Encapsula las propiedades de formato del punto del gráfico. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartPoint"
}-->

```json
{
  "value": "string",
  "id": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartPoint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->