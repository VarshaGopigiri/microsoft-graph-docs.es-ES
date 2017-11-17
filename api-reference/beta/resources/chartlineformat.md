# <a name="chartlineformat-resource-type"></a>Tipo de recurso ChartLineFormat

Encapsula las opciones de formato para los elementos de línea.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartLineFormat](../api/chartlineformat_get.md) | [ChartLineFormat](chartlineformat.md) |Lee las propiedades y relaciones del objeto chartLineFormat.|
|[Update](../api/chartlineformat_update.md) | [ChartLineFormat](chartlineformat.md)    |Actualiza el objeto ChartLineFormat. |
|[Clear](../api/chartlineformat_clear.md)|None|Borra el formato de línea de un elemento de gráfico.|

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|color|string|Código de color HTML que representa el color de las líneas del gráfico.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartLineFormat"
}-->

```json
{
  "color": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartLineFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->