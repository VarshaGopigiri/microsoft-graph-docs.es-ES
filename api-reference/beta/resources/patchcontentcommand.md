# <a name="patchcontentcommand-resource-type"></a>Tipo de recurso patchContentCommand

Cambios que se deben realizar en una solicitud de revisión de una página de OneNote.

## <a name="json-representation"></a>Representación JSON

Aquí se muestra una representación JSON del recurso, que se envía en el cuerpo de la solicitud [PATCH pages/{id}`](../api/page_update.md). 

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onenotePatchContentCommand"
}-->

```json
{
  "action": "String",
  "content": "string",
  "position": "String",
  "target": "string"
}

```

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|action|Cadena|La acción que se debe efectuar en el elemento de destino. Los valores posibles son `replace`, `append`, `delete`, `insert` o `prepend`.|
|content|Cadena|Cadena de HTML sintácticamente correcto para agregar a la página y datos binarios de cualquier imagen o archivo. Si el contenido incluye datos binarios, la solicitud se debe enviar mediante el tipo de contenido `multipart/form-data` con una parte "Comandos". |
|position|Cadena|Ubicación donde se debe agregar el contenido provisto, en relación con el elemento de destino. Los valores posibles son `after` (predeterminado) y `before`.|
|target|Cadena|Elemento que se va a actualizar. Debe ser el `#<data-id>` o el `<id>` generado del elemento, o bien la palabra clave `body` o `title`.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "patchContentCommand resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->