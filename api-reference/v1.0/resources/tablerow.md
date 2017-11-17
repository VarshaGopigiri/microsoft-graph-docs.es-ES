# <a name="tablerow-resource-type"></a>Tipo de recurso TableRow

Representa una fila de una tabla.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get TableRow](../api/tablerow_get.md) | [TableRow](tablerow.md) |Lee las propiedades y relaciones del objeto tableRow.|
|[Update](../api/tablerow_update.md) | [TableRow](tablerow.md)    |Actualiza el objeto TableRow. |
|[Range](../api/tablerow_range.md)|[Range](range.md)|Devuelve el objeto de rango asociado a toda la fila.|
|[Delete](../api/tablerow_delete.md)|None|Elimina la fila de la tabla.|
|[List](../api/tablerow_list.md) | Colección [TableRow](tablerow.md) |Obtiene la colección de objetos tableRow. |
|[Itemat](../api/tablerowcollection_itemat.md)|[TableRow](tablerow.md)|Obtiene una fila en función de su posición en la colección.|
|[Add](../api/tablerowcollection_add.md)|[TableRow](tablerow.md)|Agrega una nueva fila a la tabla.|

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|index|int|Devuelve el número de índice de la fila dentro de la colección de filas de la tabla. Indizado con cero. Solo lectura.|
|values|json|Representa los valores sin formato del intervalo especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.tableRow"
}-->

```json
{
  "index": 1024,
  "values": "json"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableRow resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->