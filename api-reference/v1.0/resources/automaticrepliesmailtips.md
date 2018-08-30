# <a name="automaticrepliesmailtips-resource-type"></a>Tipo de recurso automaticRepliesMailTips


[Sugerencias de correo electrónico](../resources/mailtips.md) acerca de las respuestas automáticas que se han configurado en un buzón de correo.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:-----|:-----|:-----|
| message | Cadena | El mensaje de respuesta automática. |
| messageLanguage | [localeInfo](../resources/localeinfo.md) | El idioma en el que se encuentra el mensaje de respuesta automática. |
| scheduledEndTime | [dateTimeTimeZone](../resources/datetimetimezone.md) | La fecha y la hora en que las respuestas automáticas se configuran para finalizar. |
| scheduledStartTime | [dateTimeTimeZone](../resources/datetimetimezone.md) | La fecha y la hora en que las respuestas automáticas están configuradas para comenzar. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "messageLanguage",
    "scheduledEndTime",
    "scheduledStartTime"
  ],
  "@odata.type": "microsoft.graph.automaticRepliesMailTips"
}-->

```json
{
  "message": "string",
  "messageLanguage": {"@odata.type": "microsoft.graph.localeInfo"},
  "scheduledEndTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "scheduledStartTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "automaticRepliesMailTips resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->