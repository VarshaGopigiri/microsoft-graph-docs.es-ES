# Tipo de recurso extensionSchemaProperty
<a id="extensionschemaproperty-resource-type" class="xliff"></a>

Use los recursos **extensionSchemaProperty** para definir el nombre y el tipo de una propiedad como parte de una definición [schemaExtension](schemaextension.md).


## Propiedades
<a id="properties" class="xliff"></a>
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|name|Cadena| El nombre de la propiedad fuertemente tipada definida como parte de una extensión de esquema.|
|tipo|String| Tipo de la propiedad que se define como parte de una extensión de esquema.  Los valores permitidos son *Binary, Boolean, DateTime, Integer* y *String*.  Consulte la tabla siguiente para obtener más detalles.|

#### Tipos de datos de propiedad admitidos
<a id="supported-property-data-types" class="xliff"></a> 
Se admiten los siguientes tipos de datos al definir una propiedad en una extensión de esquema:

| Tipo de propiedad | Observaciones |
|-------------|------------|
| Binario | Máximo de 256 bytes. |
| Booleano | No se admite para los mensajes, eventos y publicaciones. |
| DateTime | Debe especificarse en el formato ISO 8601. Se almacenarán en UTC. |
| Entero | Valor de 32 bits. No se admite para los mensajes, eventos y publicaciones. |
| String | 256 caracteres como máximo. |

## Representación JSON
<a id="json-representation" class="xliff"></a>
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.extensionSchemaProperty"
}-->

```json
{
  "name": "String",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "extensionSchemaProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->