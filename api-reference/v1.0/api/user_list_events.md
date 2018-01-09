# <a name="list-events"></a>List events

Obtiene una lista de objetos [event](../resources/event.md) en el buzón del usuario. La lista contiene patrones de serie y reuniones de instancia única.

Actualmente, esta operación devuelve los cuerpos de los eventos solo en formato HTML.

Para obtener instancias de evento de expansión, puede [obtener la vista de calendario](calendar_list_calendarview.md) o bien [obtener las instancias de un evento](event_list_instances.md).


### <a name="get-events-in-another-users-calendar"></a>Obtener los eventos del calendario de otro usuario

Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los eventos del calendario de otro usuario. Esta sección se centra en escenarios que implican permisos delegados.

Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John. Suponga que otro usuario, Garth, ha compartido un calendario con John. Puede obtener los eventos de dicho calendario compartido especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/events
```

Esta capacidad se aplica a todas las operaciones de eventos GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación. También se aplica si Garth ha delegado todo el buzón en John.

Si Garth no ha compartido su calendario con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error. En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener los eventos de los calendarios del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:

<!-- { "blockType": "ignored" } -->
```http
GET /me/events
```

Esta capacidad solo está disponible en las operaciones GET de:

- Uso compartido de carpetas de contactos, calendarios y carpetas de mensajes 
- Contactos, eventos y mensajes en carpetas compartidas
- Los recursos anteriores en buzones delegados

Esta capacidad no está disponible en otras operaciones de contactos, eventos, mensajes y sus carpetas.


### <a name="support-various-time-zones"></a>Compatibilidad con varias zonas horarias

Para todas las operaciones GET que devuelven eventos, puede usar el encabezado `Prefer: outlook.timezone` para especificar la zona horaria de las horas de inicio y finalización del evento en la respuesta. 

Por ejemplo, el siguiente encabezado `Prefer: outlook.timezone` establece las horas de inicio y finalización en la respuesta en la hora estándar del Este.
```http
Prefer: outlook.timezone="Eastern Standard Time"
```

Si el evento se ha creado en una zona horaria diferente, las horas de inicio y finalización se ajustarán a la zona horaria especificada en ese encabezado `Prefer`. Consulte esta [lista](../resources/datetimetimezone.md) para ver los nombres de zona horaria admitidos. Si no se especifica el encabezado `Prefer: outlook.timezone`, se devuelven las horas de inicio y finalización en hora UTC.

Puede usar las propiedades **OriginalStartTimeZone** y **OriginalEndTimeZone** del recurso **event** para averiguar la zona horaria usada al crear el evento.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Calendars.Read, Calendars.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | Calendars.Read, Calendars.ReadWrite    |
|Aplicación | Calendars.Read, Calendars.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /me/events
GET /users/{id | userPrincipalName}/events

GET /me/calendar/events
GET /users/{id | userPrincipalName}/calendar/events

GET /me/calendars/{id}/events
GET /users/{id | userPrincipalName}/calendars/{id}/events

GET /me/calendargroup/calendars/{id}/events
GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events

GET /me/calendargroups/{id}/calendars/{id}/events
GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events
```
## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) a modo de ayuda para personalizar la respuesta.
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción |
|:---------------|:--------|:--------|
| Authorization  | string | {token} de portador. Obligatorio.  |
| Prefer: outlook.timezone  | string | Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta. Si no se especifican, estos valores de hora se devuelven en UTC. Opcional. |
| Prefer: outlook.body-content-type | string | Formato de la propiedad **body** que se devolverá. Los valores pueden ser "text" o "html". Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`. Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML. Opcional. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [event](../resources/event.md) en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud. Especifica lo siguiente:

- Un encabezado `Prefer: outlook.timezone` para obtener valores de fecha y hora devueltos en la hora estándar del Pacífico. 
- Un parámetro de consulta `$select` para devolver propiedades específicas. Sin ningún parámetro `$select`, se devolverán todas las propiedades de evento.

<!-- {
  "blockType": "request",
  "name": "get_events"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events?$select=subject,body,bodyPreview,organizer,attendees,start,end,location
Prefer: outlook.timezone="Pacific Standard Time"
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Se devuelve la propiedad **body** en el formato HTML predeterminado.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Preference-Applied: outlook.timezone="Pacific Standard Time"
Content-length: 1932

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('cd209b0b-3f83-4c35-82d2-d88a61820480')/events(subject,body,bodyPreview,organizer,attendees,start,end,location)",
    "value":[
        {
            "@odata.etag":"W/\"ZlnW4RIAV06KYYwlrfNZvQAAKGWwbw==\"",
            "id":"AAMkAGIAAAoZDOFAAA=",
            "subject":"Orientation ",
            "bodyPreview":"Dana, this is the time you selected for our orientation. Please bring the notes I sent you.",
            "body":{
                "contentType":"html",
                "content":"<html><head></head><body><p>Dana, this is the time you selected for our orientation. Please bring the notes I sent you.</p></body></html>"
            },
            "start":{
                "dateTime":"2017-04-21T10:00:00.0000000",
                "timeZone":"Pacific Standard Time"
            },
            "end":{
                "dateTime":"2017-04-21T12:00:00.0000000",
                "timeZone":"Pacific Standard Time"
            },
            "location":{
                "displayName":"Assembly Hall"
            },
            "attendees":[
                {
                    "type":"required",
                    "status":{
                        "response":"none",
                        "time":"0001-01-01T00:00:00Z"
                    },
                    "emailAddress":{
                        "name":"Samantha Booth",
                        "address":"samanthab@a830edad905084922E17020313.onmicrosoft.com"
                    }
                },
                {
                    "type":"required",
                    "status":{
                        "response":"none",
                        "time":"0001-01-01T00:00:00Z"
                    },
                    "emailAddress":{
                        "name":"Dana Swope",
                        "address":"danas@a830edad905084922E17020313.onmicrosoft.com"
                    }
                }
            ],
            "organizer":{
                "emailAddress":{
                    "name":"Samantha Booth",
                    "address":"samanthab@a830edad905084922E17020313.onmicrosoft.com"
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
  "description": "List events",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
