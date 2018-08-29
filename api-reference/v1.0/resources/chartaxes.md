# <a name="chartaxes-resource-type"></a>Tipo de recurso ChartAxes

Representa los ejes del gráfico.


## <a name="methods"></a>Métodos
Ninguno

## <a name="properties"></a>Propiedades
Ninguno

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|categoryAxis|[WorkbookChartAxis](chartaxis.md)|Representa el eje de categorías de un gráfico. Solo lectura.|
|seriesAxis|[WorkbookChartAxis](chartaxis.md)|Representa el eje de series de un gráfico tridimensional. Solo lectura.|
|valueAxis|[WorkbookChartAxis](chartaxis.md)|Representa el eje de valores de un eje. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartAxes"
}-->

```json
{
  "categoryAxis": {"@odata.type": "microsoft.graph.workbookChartAxis"},
  "seriesAxis": {"@odata.type": "microsoft.graph.workbookChartAxis"},
  "valueAxis": {"@odata.type": "microsoft.graph.workbookChartAxis"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxes resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->