# <a name="create-event"></a>Create Event

Use esta API para crear un objeto Event en el calendario especificado o el predeterminado.
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*
## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
[calendar](../resources/calendar.md) predeterminado de un usuario o grupo.
```http
POST /me/calendar/events
POST /users/{id | userPrincipalName}/calendar/events
POST /groups/{id}/calendar/events
```
[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.
```http
POST /me/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendars/{id}/events

POST /me/calendarGroup/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/events
```
[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.
```http
POST /me/calendarGroups/{id}/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/events
```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |
| Tipo de contenido  | application/json. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Event](../resources/event.md).


## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Event](../resources/event.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_event_from_calendar"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/calendar/events
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "datetime-value"
  },
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```
En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "datetime-value"
  },
  "iCalUId": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
