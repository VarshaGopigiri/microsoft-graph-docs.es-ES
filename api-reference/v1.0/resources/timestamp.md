# <a name="timestamp-resource-type"></a>tipo de recurso timeStamp

Información sobre la fecha y la hora de un momento dado.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeStamp"
}-->

```json
{
  "date": "String (timestamp)",
  "time": "String (timestamp)",
  "timeZone": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|date|Date|La fecha de la marca de tiempo.|
|time|TimeOfDay|La hora de la marca de tiempo.|
|timeZone|Cadena|La zona horaria de la marca de tiempo, que se corresponde con una de las 24 áreas longitudinales del mundo.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeStamp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->