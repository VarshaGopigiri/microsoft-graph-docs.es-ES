# <a name="chartseries-resource-type"></a>Tipo de recurso ChartSeries

Representa una serie de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartSeries](../api/chartseries_get.md) | [WorkbookChartSeries](chartseries.md) |Lee las propiedades y relaciones del objeto chartSeries.|
|[Create ChartPoints](../api/chartseries_post_points.md) |[ChartPoints](chartpoint.md)| Crea un nuevo ChartPoints publicándolo en la colección points.|
|[List points](../api/chartseries_list_points.md) |Colección [ChartPoints](chartpoint.md)| Obtiene la colección de objetos ChartPoints.|
|[Update](../api/chartseries_update.md) | [WorkbookChartSeries](chartseries.md) |Actualiza el objeto ChartSeries. |
|[List](../api/chartseries_list.md) | Colección de [WorkbookChartSeries](chartseries.md) |Obtiene la colección de objetos chartSeries. |
|[Itemat](../api/chartseriescollection_itemat.md)|[WorkbookChartSeries](chartseries.md)|Recupera una serie en función de su posición en la colección|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|name|cadena|Representa el nombre de una serie de un gráfico.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[WorkbookChartSeriesFormat](chartseriesformat.md)|Representa el formato de una serie del gráfico, que incluye el formato de relleno y de línea. Solo lectura.|
|points|Colección de [WorkbookChartPoint](chartpoint.md)|Representa una colección de todos los puntos de la serie. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartSeries"
}-->

```json
{
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartSeries resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->