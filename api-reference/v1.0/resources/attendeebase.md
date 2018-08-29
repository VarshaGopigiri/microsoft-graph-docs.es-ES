# <a name="attendeebase-resource-type"></a>Tipo de recurso attendeeBase

El tipo de asistente.

Derivado de [destinatario](recipient.md).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.recipient",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attendeeBase"
}-->

```json
{
  "type": "String",
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|type|attendeeType| El tipo de asistente. Los valores posibles son: `required`, `optional` y `resource`. Nota: si el asistente es una persona, [findMeetingTimes](../api/user_findmeetingtimes.md) siempre considera que la persona es del tipo `Required`.|
|emailAddress|[emailAddress](emailAddress.md)|Incluye el nombre y la dirección de SMTP del asistente.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendeeBase resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
