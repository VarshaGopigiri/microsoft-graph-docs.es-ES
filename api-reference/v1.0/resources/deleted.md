# <a name="deleted-resource-type"></a>Tipo de recurso Deleted

El recurso **Deleted** indica que el elemento se ha eliminado. En esta versión de la API, la presencia (no null) del valor de recurso indica que el archivo se eliminó. Un valor null (o ausente) indica que el archivo no se elimina.

Consulte el artículo sobre cómo [ver los cambios de un elemento](../api/item_delta.md) para obtener más información sobre el seguimiento de los cambios y la búsqueda de elementos eliminados.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  "state"
  ],
  "@odata.type": "microsoft.graph.deleted"
}-->
```json
{
  "state": "string"
}
```

## <a name="properties"></a>Propiedades

| Propiedad | Tipo   | Descripción                               |
|:---------|:-------|:------------------------------------------|
| state    | String | Representa el estado del elemento eliminado. |

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "deleted resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
