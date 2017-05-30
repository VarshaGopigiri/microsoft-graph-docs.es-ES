# <a name="nameditem-resource-type"></a>Tipo de recurso NamedItem

Representa un nombre definido para un rango de celdas o un valor. Los nombres pueden ser objetos primitivos con nombre (como puede verse en el tipo siguiente), un objeto de rango o una referencia a un rango. Este objeto puede usarse para obtener un objeto de rango asociado a nombres.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Add](../api/nameditem_add.md)|[NamedItem](nameditem.md)|Agrega un nuevo nombre a la colección del ámbito especificado.|
|[AddFormulaLocal](../api/nameditem_addformulalocal.md)|[NamedItem](nameditem.md)|Agrega un nuevo nombre a la colección del ámbito especificado empleando la configuración regional del usuario para la fórmula.|
|[Get NamedItem](../api/nameditem_get.md) | [NamedItem](nameditem.md) |Lee las propiedades y relaciones del objeto namedItem.|
|[Update](../api/nameditem_update.md) | [NamedItem](nameditem.md)    |Actualiza el objeto NamedItem. |
|[Range](../api/nameditem_range.md)|[Range](range.md)|Devuelve el objeto de intervalo asociado al nombre. Produce una excepción si el tipo del elemento con nombre no es un intervalo.|
|[List](../api/nameditem_list.md) | Colección [NamedItem](nameditem.md) |Obtiene la colección de objetos namedItem. |


## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|name|string|El nombre del objeto. Solo lectura.|
|comment|string|Representa el comentario asociado a este nombre.|
|scope|string|Indica si el nombre está en el ámbito del libro o de una hoja de cálculo específica. Solo lectura.|
|type|string|Indica el tipo de referencia que está asociado al nombre. Valores posibles: `String`, `Integer`, `Double`, `Boolean`, `Range`. Solo lectura.|
|value|object|Representa la fórmula a la que debe hacer referencia el nombre, según su definición. Por ejemplo =Sheet14!$B$2:$H$12, =4.75, etc. Solo lectura.|
|visible|boolean|Especifica si el objeto está visible o no.|

## <a name="relationships"></a>Relaciones
| Relación       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|worksheet|[worksheet](worksheet.md)|Devuelve la hoja de cálculo que tiene como ámbito el elemento con nombre. Solo está disponible si el elemento tiene como ámbito la hoja de cálculo. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.namedItem"
}-->

```json
{
  "name": "string",
  "comment": "string",
  "scope": "string",
  "type": "string",
  "value": {"@odata.type": "microsoft.graph.range"},
  "visible": true
  
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "NamedItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
