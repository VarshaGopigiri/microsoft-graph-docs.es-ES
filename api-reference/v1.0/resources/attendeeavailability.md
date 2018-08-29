# <a name="attendeeavailability-resource-type"></a>Tipo de recurso attendeeAvailability

El tipo y la disponibilidad de un asistente.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attendeeAvailability"
}-->

```json
{
  "attendee": {"@odata.type": "microsoft.graph.attendeeBase"},
  "availability": "String"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|attendee|[AttendeeBase](attendeebase.md)|El tipo de asistente, ya sea una persona o un recurso, y en caso de ser una persona, si es obligatorio u opcional.|
|availability|freeBusyStatus| El estado de disponibilidad del asistente. Los valores posibles son `free`, `tentative`, `busy`, `oof`, `workingElsewhere` y `unknown`.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendeeAvailability resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
