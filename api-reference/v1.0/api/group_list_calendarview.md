# <a name="list-calendarview"></a>List calendarView

Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado de un grupo.
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.Read.All* o *Group.ReadWrite.All*
## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```
## <a name="query-parameters"></a>Parámetros de consulta

En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|startDateTime|String|La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".|
|endDateTime|String|La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".|

Este método también admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |
| Prefer | string | <Time zone>. Opcional, se supone hora UTC si no se encuentra.|

## <a name="request-body"></a>Cuerpo de solicitud
No proporcione un cuerpo de solicitud para este método.
## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [event](../resources/event.md) en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/calendarView
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 354

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List calendarView",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
