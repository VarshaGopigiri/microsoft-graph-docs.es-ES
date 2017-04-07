# <a name="chart-resource-type"></a>Tipo de recurso Chart

Representa un objeto de gráfico de una hoja de cálculo.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get Chart](../api/chart_get.md) | [Chart](chart.md) |Lee las propiedades y relaciones del objeto chart.|
|[Create ChartSeries](../api/chart_post_series.md) |[ChartSeries](chartseries.md)| Crea un ChartSeries publicándolo en la colección series.|
|[List series](../api/chart_list_series.md) |Colección [ChartSeries](chartseries.md)| Obtiene una colección de objetos ChartSeries.|
|[Update](../api/chart_update.md) | [Chart](chart.md)    |Actualiza el objeto Chart. |
|[Image](../api/chart_image.md)|Cadena codificada en base64 de imagen|Representa el gráfico como una imagen con codificación base64 al escalar el gráfico a las dimensiones especificadas.|
|[Delete](../api/chart_delete.md)|None|Elimina el objeto chart.|
|[Setdata](../api/chart_setdata.md)|None|Restablece los datos de origen del gráfico.|
|[Setposition](../api/chart_setposition.md)|None|Coloca el gráfico con respecto a las celdas de la hoja de cálculo.|
|[List](../api/chart_list.md) | Colección [Chart](chart.md) |Obtiene la colección de objetos chart. |
|[Itemat](../api/chartcollection_itemat.md)|[Chart](chart.md)|Obtiene un gráfico en función de su posición en la colección.|
|[Add](../api/chartcollection_add.md)|[Chart](chart.md)|Crea un gráfico.|

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|height|Double|Representa el alto, en puntos, del objeto de gráfico.|
|id|string|Obtiene un gráfico en función de su posición en la colección. Solo lectura.|
|left|Double|Distancia, en puntos, desde el lado izquierdo del gráfico hasta el origen de la hoja de cálculo.|
|name|string|Representa el nombre de un objeto de gráfico.|
|top|Double|Representa la distancia, en puntos, desde el borde superior del objeto hasta la parte superior de la fila 1 (en una hoja de cálculo) o la parte superior del área del gráfico (en un gráfico).|
|width|double|Representa el ancho, en puntos, del objeto graph.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|axes|[ChartAxes](chartaxes.md)|Representa los ejes del gráfico. Solo lectura.|
|dataLabels|[ChartDataLabels](chartdatalabels.md)|Representa la clase DataLabels del gráfico. Solo lectura.|
|format|[ChartAreaFormat](chartareaformat.md)|Encapsula las propiedades de formato del área del gráfico. Solo lectura.|
|legend|[ChartLegend](chartlegend.md)|Representa la leyenda del gráfico. Solo lectura.|
|series|Colección [ChartSeries](chartseries.md)|Representa una sola serie o una colección de series del gráfico. Solo lectura.|
|title|[ChartTitle](charttitle.md)|Representa el título del gráfico especificado, incluido el texto, la visibilidad, la posición y el formato del título. Solo lectura.|
|worksheet|[Worksheet](worksheet.md)|La hoja de cálculo que contiene el gráfico actual. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chart"
}-->

```json
{
  "height": 1024,
  "id": "string",
  "left": 1024,
  "name": "string",
  "top": 1024,
  "width": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Chart resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->