# <a name="user-reminderview"></a>user: reminderView
Devolver una lista de los avisos de calendario entre las horas de inicio y finalización especificadas. 

## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.Read; Calendars.ReadWrite*
## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/reminderView(startDateTime=startDateTime-value,endDateTime=endDateTime-value)
```

## <a name="function-parameters"></a>Parámetros de función
En la dirección URL de la solicitud, proporcione los siguientes parámetros de función con valores.

| Parámetro       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|startDateTime|String|Fecha y hora de inicio del evento para el que se configura el aviso. El valor se representa en formato ISO 8601, por ejemplo, "2015-11-08T19:00:00.0000000".|
|endDateTime|String|Fecha y hora de finalización del evento para el que se configura el aviso. El valor se representa en formato ISO 8601, por ejemplo, "2015-11-08T20:00:00.0000000".|


## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor|
|:-----------|:------|
| Autorización  | Portador de <token>. Necesario.  |
| Content-Type   | application/json |
| Prefer | <Zona horaria>. Opcional, se supone hora UTC si no se encuentra.| 

## <a name="request-body"></a>Cuerpo de solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto de colección [reminder](../resources/reminder.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
Aquí tiene un ejemplo de cómo llamar a esta API.
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "user_reminderview"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/reminderView?startDateTime=startDateTime-value&endDateTime=endDateTime-value
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.reminder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 673

{
  "value": [
    {
      "eventId": "eventId-value",
      "eventStartTime": {
        "dateTime": "dateTime-value",
        "timeZone": "timeZone-value"
      },
      "eventEndTime": {
        "dateTime": "dateTime-value",
        "timeZone": "timeZone-value"
      },
      "changeKey": "changeKey-value",
      "eventSubject": "eventSubject-value",
      "eventLocation": {
        "displayName": "displayName-value",
        "address": {
          "street": "street-value",
          "city": "city-value",
          "state": "state-value",
          "countryOrRegion": "countryOrRegion-value",
          "postalCode": "postalCode-value"
        }
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: reminderView",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
