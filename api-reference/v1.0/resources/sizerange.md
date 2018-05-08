# <a name="sizerange-resource-type"></a>Tipo de recurso sizeRange


Especifica los tamaños máximo y mínimo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| maximumSize | Int32 | Tamaño máximo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique. |
| minimumSize | Int32 | Tamaño mínimo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique. |


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.sizeRange"
}-->

```json
{
  "maximumSize": "Int32",
  "minimumSize": "Int32"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sizeRange resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->