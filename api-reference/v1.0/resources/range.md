# <a name="range-resource-type"></a>Tipo de recurso Range

El rango representa un conjunto de una o más celdas contiguas, como una celda, una fila, una columna, un bloque de celdas, etc.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get Range](../api/range_get.md) | [Range](range.md) |Lee las propiedades y relaciones del objeto range.|
|[Update](../api/range_update.md) | [Range](range.md)   |Actualiza el objeto Range. |
|[Boundingrect](../api/range_boundingrect.md)|[Range](range.md)|Obtiene el objeto de rango más pequeño que abarca los rangos especificados. Por ejemplo, el valor GetBoundingRect de "B2:C5" y "D10:E15" es "B2:E16".|
|[Cell](../api/range_cell.md)|[Range](range.md)|Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo. La celda devuelta se ubica con respecto a la celda superior izquierda del rango.|
|[Column](../api/range_column.md)|[Range](range.md)|Obtiene una columna contenida en el intervalo.|
|[Columnsafter](../api/workbookrange_columnsafter.md)|[workbookRangeView](workbookrangeview.md)|Obtiene un número determinado de columnas a la derecha del rango especificado.|
|[Columnsbefore](../api/workbookrange_columnsbefore.md)|[workbookRangeView](workbookrangeview.md)|Obtiene un número determinado de columnas a la izquierda del rango especificado.|
|[Entirecolumn](../api/range_entirecolumn.md)|[Range](range.md)|Obtiene un objeto que representa toda la columna del rango.|
|[Entirerow](../api/range_entirerow.md)|[Range](range.md)|Obtiene un objeto que representa toda la fila del rango.|
|[Intersection](../api/range_intersection.md)|[Range](range.md)|Obtiene el objeto de intervalo que representa la intersección rectangular de los intervalos especificados.|
|[Lastcell](../api/range_lastcell.md)|[Range](range.md)|Obtiene la última celda del intervalo. Por ejemplo, la última celda de "B2:D5" es "D5".|
|[Lastcolumn](../api/range_lastcolumn.md)|[Range](range.md)|Obtiene la última columna del intervalo. Por ejemplo, la última columna de "B2:D5" es "D2:D5".|
|[Lastrow](../api/range_lastrow.md)|[Range](range.md)|Obtiene la última fila del intervalo. Por ejemplo, la última fila de "B2:D5" es "B5:D5".|
|[Offsetrange](../api/range_offsetrange.md)|[Range](range.md)|Obtiene un objeto que representa un intervalo desplazado con respecto al intervalo especificado. La dimensión del intervalo devuelto coincidirá con este intervalo. Si el intervalo resultante se fuerza fuera de los límites de la cuadrícula de la hoja de cálculo, se producirá una excepción.|
|[Row](../api/range_row.md)|[Range](range.md)|Obtiene una fila contenida en el intervalo.|
|[Rowsabove](../api/workbookrange_rowsabove.md)|[workbookRangeView](workbookrangeview.md)|Obtiene un número determinado de filas encima de un rango dado.|
|[Rowsbelow](../api/workbookrange_rowsbelow.md)|[workbookRangeView](workbookrangeview.md)|Obtiene un número determinado de filas a continuación de un intervalo dado.|
|[Usedrange](../api/range_usedrange.md)|[Range](range.md)|Devuelve el rango usado del objeto de rango especificado.|
|[Clear](../api/range_clear.md)|Ninguno|Borra valores de rango, formato, relleno, borde, etc.|
|[Delete](../api/range_delete.md)|Ninguno|Elimina las celdas asociadas al rango.|
|[Insert](../api/range_insert.md)|[Range](range.md)|Inserta una celda o un rango de celdas en la hoja de cálculo en lugar de este rango y desplaza las demás celdas para crear espacio. Devuelve un objeto Range en el espacio que queda en blanco.|
|[Merge](../api/range_merge.md)|Ninguno|Combina las celdas del intervalo en una región de la hoja de cálculo.|
|[Resizedrange](../api/workbookrange_resizedrange.md)|[workbookRangeView](workbookrangeview.md)|Obtiene un objeto de rango similar al objeto actual, pero con su esquina inferior derecha expandida (o contraída) mediante un número de filas y columnas.|
|[Unmerge](../api/range_unmerge.md)|Ninguno|Separa las celdas del intervalo en celdas independientes.|
|[Visibleview](../api/workbookrange_visibleview.md)|[workbookRangeView](workbookrangeview.md)|Obtiene el rango visible desde un rango filtrado.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|address|cadena|Representa la referencia de intervalo en estilo A1. El valor de dirección contendrá la referencia de hoja (por ejemplo, Sheet1!A1:B4). Solo lectura.|
|addressLocal|cadena|Representa la referencia del intervalo especificado en el idioma del usuario. Solo lectura.|
|cellCount|int|Número de celdas del intervalo. Solo lectura.|
|columnCount|int|Representa el número total de columnas del intervalo. Solo lectura.|
|columnHidden|booleano|Representa si todas las columnas del rango actual están ocultas.|
|columnIndex|int|Representa el número de columna de la primera celda del intervalo. Indizado con cero. Solo lectura.|
|formulas|Json|Representa la fórmula en notación de estilo A1.|
|formulasLocal|Json|Representa la fórmula en notación de estilo A1, en el idioma del usuario y en la configuración regional del formato numérico. Por ejemplo, la fórmula "=SUM(A1, 1.5)" en inglés se convertiría en "=SUMME(A1; 1,5)" en alemán.|
|formulasR1C1|Json|Representa la fórmula en notación de estilo R1C1.|
|hidden|booleano|Representa si todas las celdas del rango actual están ocultas. Solo lectura.|
|numberFormat|Json|Representa el código de formato numérico de Excel para la celda especificada.|
|rowCount|int|Devuelve el número total de filas del intervalo. Solo lectura.|
|rowHidden|booleano|Representa si todas las filas del rango actual están ocultas.|
|rowIndex|int|Devuelve el número de fila de la primera celda del intervalo. Indizado con cero. Solo lectura.|
|text|Json|Valores de texto del rango especificado. El valor Text no dependerá del ancho de la celda. La sustitución del signo # que tiene lugar en la interfaz de usuario de Excel no afectará al valor de texto devuelto por la API. Solo lectura.|
|valueTypes|Json|Representa el tipo de datos de cada celda. Los valores posibles son: `Unknown`, `Empty`, `String`, `Integer`, `Double`, `Boolean` y `Error`. Solo lectura.|
|values|Json|Representa los valores sin formato del intervalo especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[WorkbookRangeFormat](rangeformat.md)|Devuelve un objeto de formato que encapsula la fuente, el relleno, los bordes, la alineación y otras propiedades del intervalo. Solo lectura.|
|sort|[WorkbookRangeSort](rangesort.md)|Hoja de cálculo que contiene el rango actual. Solo lectura.|
|worksheet|[WorkbookWorksheet](worksheet.md)|Hoja de cálculo que contiene el rango actual. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookRange"
}-->

```json
{
  "address": "string",
  "addressLocal": "string",
  "cellCount": 1024,
  "columnCount": 1024,
  "columnHidden": true,
  "columnIndex": 1024,
  "formulas": "json",
  "formulasLocal": "json",
  "formulasR1C1": "json",
  "hidden": true,
  "numberFormat": "json",
  "rowCount": 1024,
  "rowHidden": true,
  "rowIndex": 1024,
  "text": "json",
  "valueTypes": "string",
  "values": "json"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
