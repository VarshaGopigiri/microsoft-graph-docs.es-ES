# <a name="itemattachment-resource-type"></a>Tipo de recurso itemAttachment

Contacto, evento o mensaje que se adjunta a otro evento, mensaje o publicación.  

Derivado de [attachment](attachment.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Get](../api/attachment_get.md) | [itemAttachment](itemattachment.md) |Lee las propiedades y relaciones del objeto itemAttachment.|
|[Delete](../api/attachment_delete.md) | None |Elimina el objeto itemAttachment. |

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|contentType|String|El tipo de contenido de los datos adjuntos.|
|id|String| El identificador de los datos adjuntos.|
|isInline|Boolean|Se establece en true si los datos adjuntos están insertados, como una imagen incrustada en el cuerpo del elemento.|
|lastModifiedDateTime|DateTimeOffset|Última fecha y hora en que se modificaron los datos adjuntos.|
|name|String|Nombre para mostrar de los datos adjuntos.|
|size|Int32|El tamaño en bytes de los datos adjuntos.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|item|[OutlookItem](outlookitem.md)|Evento o mensaje adjunto. Propiedad de navegación.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "item"
  ],
  "@odata.type": "microsoft.graph.itemAttachment"
}-->

```json
{
  "contentType": "string",
  "id": "string (identifier)",
  "isInline": true,
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "size": 1024
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "itemAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
