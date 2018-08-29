# <a name="chartaxistitle-resource-type"></a>Tipo de recurso ChartAxisTitle

Representa el título del eje de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener ChartAxisTitle](../api/chartaxistitle_get.md) | [WorkbookChartAxisTitle](chartaxistitle.md) |Lee las propiedades y relaciones del objeto chartAxisTitle.|
|[Actualizar](../api/chartaxistitle_update.md) | [WorkbookChartAxisTitle](chartaxistitle.md)    |Actualiza el objeto ChartAxisTitle. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|texto.|cadena|Representa el título del eje.|
|visible|booleano|Valor booleano que especifica la visibilidad del título de un eje.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[WorkbookChartAxisTitleFormat](chartaxistitleformat.md)|Representa el formato del título del eje del gráfico. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartAxisTitle"
}-->

```json
{
  "text": "string",
  "visible": true,
  "format": {"@odata.type":"microsoft.graph.workbookChartAxisTitleFormat"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxisTitle resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->