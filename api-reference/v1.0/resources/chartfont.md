# <a name="chartfont-resource-type"></a>Tipo de recurso ChartFont

Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto de gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartFont](../api/chartfont_get.md) | [WorkbookChartFont](chartfont.md) |Lee las propiedades y relaciones del objeto chartFont.|
|[Update](../api/chartfont_update.md) | [WorkbookChartFont](chartfont.md)   |Actualiza el objeto ChartFont. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|bold|booleano|Representa el estado de negrita de la fuente.|
|color|cadena|Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.|
|italic|booleano|Representa el estado de cursiva de la fuente.|
|name|cadena|Nombre de fuente (por ejemplo, "Calibri")|
|Tamaño|doble|Tamaño de la fuente (por ejemplo, 11).|
|underline|cadena|Tipo de subrayado aplicado a la fuente. Los valores posibles son: `None` y `Single`.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartFont"
}-->

```json
{
  "bold": true,
  "color": "string",
  "italic": true,
  "name": "string",
  "size": 1024,
  "underline": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartFont resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->