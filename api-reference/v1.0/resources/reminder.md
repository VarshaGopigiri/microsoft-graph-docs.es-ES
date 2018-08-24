# <a name="reminder-resource-type"></a>Tipo de recurso reminder

Un aviso para un [evento](event.md) en un [calendario](calendar.md)de usuario.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|changeKey|Cadena|Identifica la versión del aviso. Cada vez que cambia el aviso, cambia también **changeKey**. Permite que Exchange aplique los cambios a la versión correcta del objeto.|
|eventEndTime|[DateTimeTimeZone](datetimetimezone.md)|Fecha, hora y zona horaria en que finaliza el evento.|
|eventId|Cadena|Identificador único del evento. Solo lectura.|
|eventLocation|[Ubicación](location.md)|Ubicación del evento.|
|eventStartTime|[DateTimeTimeZone](datetimetimezone.md)|Fecha, hora y zona horaria en que comienza el evento.|
|eventSubject|Cadena|Texto de la línea de asunto del evento.|
|eventWebLink|Cadena|Dirección URL para abrir el evento en Outlook en la web.<br/><br/>El evento se abrirá en el navegador si está conectado a su buzón mediante Outlook en la web. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.<br/><br/>Se puede acceder a esta dirección URL desde un iFrame.|
|reminderFireTime|[DateTimeTimeZone](datetimetimezone.md)|Fecha, hora y zona horaria en que se establece que se produzca el aviso.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.reminder"
}-->

```json
{
  "changeKey": "string",
  "eventEndTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "eventId": "string",
  "eventLocation": {"@odata.type": "microsoft.graph.location"},
  "eventStartTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "eventSubject": "string",
  "eventWebLink": "string",
  "reminderFireTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "reminder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->