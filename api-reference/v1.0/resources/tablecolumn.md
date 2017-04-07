# <a name="tablecolumn-resource-type"></a>Tipo de recurso TableColumn

Representa una columna en una tabla.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get TableColumn](../api/tablecolumn_get.md) | [TableColumn](tablecolumn.md) |Lee las propiedades y relaciones del objeto tableColumn.|
|[Update](../api/tablecolumn_update.md) | [TableColumn](tablecolumn.md)    |Actualiza el objeto TableColumn. |
|[Databodyrange](../api/tablecolumn_databodyrange.md)|[Range](range.md)|Obtiene el objeto de rango asociado al cuerpo de datos de la columna.|
|[Headerrowrange](../api/tablecolumn_headerrowrange.md)|[Range](range.md)|Obtiene el objeto de rango asociado a la fila de encabezado de la columna.|
|[Range](../api/tablecolumn_range.md)|[Range](range.md)|Obtiene el objeto de rango asociado a toda la columna.|
|[Totalrowrange](../api/tablecolumn_totalrowrange.md)|[Range](range.md)|Obtiene el objeto de rango asociado a la fila de totales de la columna.|
|[Delete](../api/tablecolumn_delete.md)|None|Elimina la columna de la tabla.|
|[List](../api/tablecolumn_list.md) | Colección [TableColumn](tablecolumn.md) |Obtiene la colección de objetos tableColumn. |
|[Itemat](../api/tablecolumncollection_itemat.md)|[TableColumn](tablecolumn.md)|Obtiene una columna en función de su posición en la colección.|
|[Add](../api/tablecolumncollection_add.md)|[TableColumn](tablecolumn.md)|Agrega una nueva columna a la tabla.|


## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|id|int|Devuelve una clave única que identifica la columna de la tabla. Solo lectura.|
|Index|int|Devuelve el número de índice de la columna dentro de la colección de columnas de la tabla. Indizado con cero. Solo lectura.|
|name|string|Devuelve el nombre de la columna de la tabla. Solo lectura.|
|values|json|Representa los valores sin formato del intervalo especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|filter|[Filter](filter.md)|Recupera el filtro aplicado a la columna. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.tableColumn"
}-->

```json
{
  "id": 1024,
  "index": 1024,
  "name": "string",
  "values": "json"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableColumn resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->