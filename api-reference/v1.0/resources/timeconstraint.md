# <a name="timeconstraint-resource-type"></a>Tipo de recurso timeConstraint

Los períodos de tiempo para una actividad del carácter especificado.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeconstraint"
}-->

```json
{
  "activityDomain": "String",
  "timeslots": [{"@odata.type": "microsoft.graph.timeSlot"}]
}

```
## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|activityDomain|String|La naturaleza de la actividad, opcional. Los valores posibles son: `unknown`, `work`, `personal`. Actualmente [findMeetingTimes](../api/user_findmeetingtimes.md) supone que el valor es siempre `work` y devuelve cualquier sugerencia de reunión solo durante las horas de trabajo del organizador o el asistente.|
|ranuras de intervalo de tiempo|Colección[timeSlot](timeslot.md)|Matriz de periodos de tiempo.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeConstraint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->