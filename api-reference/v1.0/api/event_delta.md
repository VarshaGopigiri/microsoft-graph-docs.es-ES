# <a name="event-delta"></a>event: delta

Obtenga un conjunto de eventos que se han agregado, eliminado o actualizado en una **calendarView** (un intervalo de eventos) del calendario principal del usuario.

La llamada de una función **delta** para eventos funciona de forma similar a una solicitud `GET /calendarview` para un intervalo de fechas en el calendario principal del usuario, salvo que, al aplicar correctamente los [tokens de estado](../../../concepts/delta_query_overview.md) en al menos una de estas llamadas, pueda realizar una consulta para obtener los cambios incrementales en la vista del calendario. Esto permite mantener y sincronizar un almacén local de eventos de un usuario en el calendario principal, sin tener que capturar cada vez todos los eventos de ese calendario desde el servidor.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Calendars.Read    |
|Delegado (cuenta personal de Microsoft) | Calendars.Read    |
|Aplicación | Calendars.Read |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendarView/delta?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/<id>/calendarView/delta?startDateTime={start_datetime}&endDateTime={end_datetime}

```

### <a name="query-parameters"></a>Parámetros de consulta

El seguimiento de cambios en los eventos conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta. Solo debe especificar una vez por adelantado los parámetros de consulta deseados. En solicitudes posteriores, basta con copiar y aplicar la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.


| Parámetro de consulta      | Tipo   |Descripción|
|:---------------|:--------|:----------|
|startDateTime|String|La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".|
|endDateTime|String|La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".|
| $deltatoken | string | [Token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de usuarios. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de la vista del calendario.|
| $skiptoken | string | [Token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma vista del calendario. |

Al hacer una consulta delta en una vista del calendario, se espera obtener todas las propiedades que se obtendrían con normalidad de una solicitud `GET /calendarview`. `$select` no se admite en este caso. 


## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción |
|:---------------|:----------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |
| Content-Type  | string  | application/json. Obligatorio. |
| Prefer | string  | odata.maxpagesize={x}. Opcional. |
| Prefer | string | {Zona horaria}. Opcional, se supone la hora UTC si no se encuentra.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto de colección [event](../resources/event.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud

En el ejemplo siguiente se muestra cómo realizar una llamada de función **delta** única y limitar el número máximo de eventos en el cuerpo de la respuesta a 2.

Para realizar un seguimiento de la vista del calendario, debería realizar al menos una llamada de función **delta**, con unos [tokens de estado](../../../concepts/delta_query_overview.md) adecuados, para obtener el conjunto de cambios incrementales desde la última consulta delta. 

<!-- {
  "blockType": "request",
  "name": "event_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarview/delta?startdatetime={start_datetime}&enddatetime={end_datetime}

Prefer: odata.maxpagesize=2
```

##### <a name="response"></a>Respuesta
Si la solicitud es correcta, la respuesta debería incluir un token de estado, que puede ser un _skipToken_ (en un encabezado de respuesta _@odata.nextLink_) o un _deltaToken_ (en un encabezado de respuesta _@odata.deltaLink_). Respectivamente, indican si debe continuar con la ronda, o bien si ha terminado de obtener todos los cambios de la ronda.

La respuesta siguiente muestra un _skipToken_ en un encabezado de respuesta de _@odata.nextLink_.

Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 359

{
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/me/calendarview/delta?$skiptoken={_skipToken_}",
  "value": [
    {
      "originalStartTimeZone": "originalStartTimeZone-value",
      "originalEndTimeZone": "originalEndTimeZone-value",
      "responseStatus": {
        "response": "response-value",
        "time": "datetime-value"
      },
      "iCalUId": "iCalUId-value",
      "reminderMinutesBeforeStart": 99,
      "isReminderOn": true
    }
  ]
}
```

### <a name="see-also"></a>Recursos adicionales

- [Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph](../../../concepts/delta_query_overview.md)
- [Obtener los cambios incrementales en los eventos en un calendario](../../../concepts/delta_query_events.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "event: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->