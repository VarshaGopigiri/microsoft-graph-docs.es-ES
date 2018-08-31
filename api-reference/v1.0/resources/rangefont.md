# <a name="rangefont-resource-type"></a>Tipo de recurso RangeFont

Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get RangeFont](../api/rangefont_get.md) | [WorkbookRangeFont](rangefont.md) |Lee las propiedades y relaciones del objeto rangeFont.|
|[Update](../api/rangefont_update.md) | [WorkbookRangeFont](rangefont.md)   |Actualiza el objeto RangeFont. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|bold|booleano|Representa el estado de negrita de la fuente.|
|color|cadena|Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.|
|italic|booleano|Representa el estado de cursiva de la fuente.|
|name|cadena|Nombre de fuente (por ejemplo, "Calibri")|
|size|doble|Tamaño de fuente|
|underline|cadena|Tipo de subrayado aplicado a la fuente. Los valores posibles son: `None`, `Single`, `Double`, `SingleAccountant` y `DoubleAccountant`.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookRangeFont"
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
  "description": "RangeFont resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->