<a id="rangeview-resource-type" class="xliff"></a>
# Tipo de recurso rangeView
RangeView representa un conjunto de celdas visibles del intervalo primario.

<a id="methods" class="xliff"></a>
## Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[List rows](../api/workbookrangeview_list_rows.md) |Colección [workbookRangeView](workbookrangeview.md)| Obtenga una colección de objetos workbookRangeView.|
|[Itemat](../api/workbookrangeview_itemat.md)|[workbookRangeView](workbookrangeview.md)|Obtengaun elemento de vista de rango basándose en el índice.|
|[Range](../api/workbookrangeview_range.md)|[workbookRange](range.md)|Devuelve el objeto de rango asociado a la vista de rango.|


<a id="properties" class="xliff"></a>
## Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|columnCount|Int32|Devuelve el número de columnas visibles. Solo lectura.|
|formulas|Json|Representa la fórmula en notación de estilo A1. |
|formulasLocal|Json|Representa la fórmula en notación de estilo A1, en el idioma del usuario y en la configuración regional del formato numérico. Por ejemplo, la fórmula "=SUM(A1, 1.5)" en inglés se convertiría en "=SUMME(A1; 1,5)" en alemán.    |
|formulasR1C1|Json|Representa la fórmula en notación de estilo R1C1.   |
|index|Int32|Índice de la página.|
|numberFormat|Json|Representa el código de formato numérico de Excel para la celda especificada. Solo lectura. |
|rowCount|Int32|Devuelve el número de filas visibles. Solo lectura.  |
|text|Json|Valores de texto del rango especificado. El valor Text no dependerá del ancho de la celda. La sustitución del signo # que tiene lugar en la interfaz de usuario de Excel no afectará al valor de texto devuelto por la API. Solo lectura.    |
|valueTypes|Json|Representa el tipo de datos de cada celda. Solo lectura. Los valores posibles son: Unknown, Empty, String, Integer, Double, Boolean, Error. |
|values|Json|Representa los valores sin formato de la vista del intervalo especificado. Los datos devueltos pueden ser de tipo cadena, número o booleano. La celda que contenga un error devolverá la cadena de error.   |

<a id="relationships" class="xliff"></a>
## Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|rows|Colección [workbookRangeView](workbookrangeview.md)| Representa una colección de vistas de intervalo asociadas a este. Solo lectura.    Solo lectura.|

<a id="json-representation" class="xliff"></a>
## Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.workbookRangeView"
}-->
```json
{
  "cellAddresses": "Json",
  "columnCount": 1024,
  "formulas": "Json",
  "formulasLocal": "Json",
  "formulasR1C1": "Json",
  "id": "String (identifier)",
  "index": 1024,
  "numberFormat": "Json",
  "rowCount": 1024,
  "text": "Json",
  "valueTypes": "Json",
  "values": "Json"
}
```
