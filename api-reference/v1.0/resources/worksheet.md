# <a name="worksheet-resource-type"></a>Tipo de recurso Worksheet

Una hoja de cálculo de Excel es una cuadrícula de celdas. Puede contener datos, tablas, gráficos, etc.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get Worksheet](../api/worksheet_get.md) | [WorkbookWorksheet](worksheet.md) |Lee las propiedades y relaciones del objeto worksheet.|
|[Create Chart](../api/worksheet_post_charts.md) |[WorkbookChart](chart.md)| Cree un gráfico publicando en la colección de gráficos.|
|[List names](../api/worksheet_list_names.md) |Colección [WorkbookNamedItem](nameditem.md)| Obtenga la colección del elemento con nombre asociada a la hoja de cálculo.|
|[List charts](../api/worksheet_list_charts.md) |Colección [WorkbookChart](chart.md)| Obtiene la colección de objetos Chart.|
|[Create Table](../api/worksheet_post_tables.md) |[WorkbookTable](table.md)| Crea un Table publicándolo en la colección tables.|
|[List tables](../api/worksheet_list_tables.md) |Colección de [WorkbookTable](table.md)| Obtiene una colección de objetos Table.|
|[Update](../api/worksheet_update.md) | [WorkbookWorksheet](worksheet.md)   |Actualiza el objeto Worksheet. |
|[Cell](../api/worksheet_cell.md)|[Range](range.md)|Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.|
|[Range](../api/worksheet_range.md)|[Range](range.md)|Obtiene el objeto de intervalo especificado por la dirección o el nombre.|
|[Usedrange](../api/worksheet_usedrange.md)|[Range](range.md)|El rango usado es el rango más pequeño que abarque las celdas que tienen asignado un valor o un formato. Si la hoja de cálculo está en blanco, esta función devolverá la celda superior izquierda.|
|[Delete](../api/worksheet_delete.md)|Ninguno|Elimina la hoja de cálculo del libro.|
|[List](../api/worksheet_list.md) | Colección [WorkbookWorksheet](worksheet.md) |Obtiene la colección de objetos worksheet. |
|[Add](../api/worksheetcollection_add.md)|[WorkbookWorksheet](worksheet.md)|Agrega una nueva hoja de cálculo al libro. La hoja de cálculo se agregará al final de las hojas de cálculo existentes. |
|[List pivotTables](../api/workbookworksheet_list_pivottables.md) |Colección [workbookPivotTable](workbookpivottable.md)| Obtiene una colección de objetos workbookPivotTable.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|cadena|Devuelve un valor que identifica de forma única la hoja de cálculo de un libro determinado. El valor del identificador permanece igual, incluso cuando se cambia el nombre de la hoja de cálculo o cuando esta se mueve. Solo lectura.|
|name|cadena|Nombre para mostrar de la hoja de cálculo.|
|position|entero|Posición de base cero de la hoja de cálculo dentro del libro.|
|visibility|cadena|La visibilidad de la hoja de cálculo. Los valores posibles son: `Visible`, `Hidden` y `VeryHidden`.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|charts|Colección [WorkbookChart](chart.md)|Devuelve la colección de gráficos que forman parte de la hoja de cálculo. Solo lectura.|
|names|Colección [WorkbookNamedItem](nameditem.md)|Devuelve la colección de los nombres asociados a la hoja de cálculo. Solo lectura.|
|pivotTables|Colección [workbookPivotTable](workbookpivottable.md)| Colección de tablas dinámicas que forman parte de la hoja de cálculo. |
|protection|[WorkbookWorksheetProtection](worksheetprotection.md)|Devuelve el objeto de protección de hoja de una hoja de cálculo. Solo lectura.|
|tables|Colección de [WorkbookTable](table.md)|Colección de tablas que forman parte de la hoja de cálculo. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookWorksheet"
}-->

```json
{
  "id": "string",
  "name": "string",
  "position": 1024,
  "visibility": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Worksheet resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
