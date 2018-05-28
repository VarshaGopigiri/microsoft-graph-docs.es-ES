# <a name="get-incremental-changes-to-events-in-a-calendar-view"></a>Obtener los cambios incrementales en los eventos en una vista de calendario 

Una vista de calendario es una colección de eventos en un intervalo de fecha y hora del calendario predeterminado (../me/calendarview) o algún otro calendario del usuario. Mediante la consulta de delta, puede obtener eventos nuevos, actualizados o eliminados en una vista de calendario. Los eventos devueltos pueden incluir las repeticiones y excepciones de una serie periódica e instancias únicas. Los datos de delta permiten mantener y sincronizar un almacén local de eventos de un usuario, sin tener que capturar cada vez todo el conjunto de eventos del usuario desde el servidor.

La consulta de delta admite la sincronización completa que recupera todos los eventos en la vista de calendario especificada y la sincronización incremental que recupera aquellos eventos que cambiaron en la vista de calendario desde la última sincronización. Normalmente, se debería realizar una sincronización completa inicial y, después, obtener los cambios incrementales en la vista de calendario de forma periódica. 

## <a name="track-event-changes-in-a-calendar-view"></a>Seguir los cambios de eventos en una vista de calendario

La consulta de delta para eventos es específica del calendario y el intervalo de fecha y hora que se especifique (por ejemplo, una vista de calendario). Para realizar el seguimiento de los cambios en varios calendarios, necesitará realizar el seguimiento de cada calendario individualmente. 

El seguimiento de los cambios de eventos en una vista de calendario normalmente es una ronda de una o varias solicitudes GET con la función [delta](../api-reference/v1.0/api/event_delta.md). La solicitud GET inicial es muy similar a la forma de [enumerar un objeto calendarView](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/calendar_list_calendarview), salvo que se incluye la función **delta**:

```
GET /me/calendarView/delta?startDateTime={start_datetime}&endDateTime={end_datetime}
```

Una solicitud GET con la función **delta** función devuelve:

- Un `nextLink` (que contiene una dirección URL con una llamada de función **delta** y un _skipToken_), o 
- Un `deltaLink` (que contiene una dirección URL con una llamada de función **delta** y un _deltaToken_).

Estos tokens son [tokens de estado](delta_query_overview.md#state-tokens) que codifican los parámetros refs/remotes/microsoftgraph/master _startDateTime_ y _endDateTime_, y cualquier otro parámetro de consulta en la solicitud GET de la consulta de delta inicial. 

Los tokens de estado son totalmente opacos para el cliente. Para continuar con una ronda de seguimiento de cambios, basta con copiar y aplicar la dirección URL `nextLink` o `deltaLink` devuelta desde la última solicitud GET a la siguiente llamada de función**delta** para la mismo vista de calendario. Un `deltaLink` devuelto en una respuesta significa que la ronda actual de seguimiento de cambios está completa. Se puede guardar y usar la dirección URL `deltaLink` cuando se inicia la siguiente ronda.

Vea el [ejemplo](#example-to-synchronize-events-in-a-calendar-view) siguiente para obtener información sobre cómo usar estas direcciones URL `nextLink` y `deltaLink`.

### <a name="use-query-parameters-in-a-delta-query-for-calendar-view"></a>Usar parámetros de consulta en una consulta de delta para la vista de calendario

- Incluya los parámetros _startDateTime_ y _endDateTime_ para definir un intervalo de fecha y hora para la vista de calendario.
- `$select` no es compatible.


### <a name="optional-request-header"></a>Encabezado de solicitud opcional

Cada solicitud GET de la consulta delta devuelve una colección de uno o más eventos en la respuesta. Opcionalmente se puede especificar el encabezado de solicitud, `Prefer: odata.maxpagesize={x}`, para establecer el número máximo de eventos en una respuesta.


## <a name="example-to-synchronize-events-in-a-calendar-view"></a>Ejemplo para sincronizar los eventos en una vista de calendario

En el ejemplo siguiente se muestra una serie de tres solicitudes para sincronizar el calendario predeterminado del usuario en un intervalo de tiempo específico. En esa vista de calendario hay cinco eventos.

- [Paso 1: solicitud inicial de ejemplo](#step-1-sample-initial-request) y [respuesta](#sample-initial-response)
- [Paso 2: segunda solicitud de ejemplo](#step-2-sample-second-request) y [respuesta](#sample-second-response)
- [Paso 2: tercera solicitud de ejemplo](#step-3-sample-third-request) y [respuesta final](#sample-third-and-final-response)

Para mayor brevedad, las respuestas de ejemplo muestran solo un subconjunto de las propiedades de un evento. En una llamada real, se devuelve la mayoría de las propiedades de evento . 

Vea también lo que hará la [siguiente ronda](#the-next-round-sample-first-response).


### <a name="step-1-sample-initial-request"></a>Paso 1: solicitud inicial de ejemplo

En este ejemplo, se sincroniza por primera vez la vista de calendario especificada, por lo que la solicitud de sincronización inicial no incluye ningún token de estado. Esa ronda devolverá todos los eventos de esa vista de calendario.

La primera solicitud especifica lo siguiente:

- Valores de fecha u hora para los parámetros _startDateTime_ y _endDateTime_.
- El [encabezado de solicitud opcional](#optional-request-header), _odata.maxpagesize_, que devuelve dos eventos a la vez.

<!-- {
  "blockType": "request",
  "name": "get_calendarview_delta_1"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarview/delta?startdatetime=2016-12-01T00:00:00Z&enddatetime=2016-12-30T00:00:00Z HTTP/1.1
Prefer: odata.maxpagesize=2
```


### <a name="sample-initial-response"></a>Respuesta inicial de ejemplo

La respuesta incluye dos eventos y un encabezado de respuesta `@odata.nextLink` con un `skipToken`. La dirección URL `nextLink` indica que hay más eventos para obtener en la vista de calendario.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Collection(event)",
    "@odata.nextLink":"https://graph.microsoft.com/v1.0/me/calendarview/delta?$skiptoken=R0usmcCM996atia_s",
    "value":[
        {
            "@odata.type":"#microsoft.graph.event",
            "@odata.etag":"W/\"EZ9r3czxY0m2jz8c45czkwAAFXcvIQ==\"",
            "subject":"Plan shopping list",
            "body":{
                "contentType":"html",
                "content":""
            },
            "start":{
                "dateTime":"2016-12-09T20:30:00.0000000",
                "timeZone":"UTC"
            },
            "end":{
                "dateTime":"2016-12-09T22:00:00.0000000",
                "timeZone":"UTC"
            },
            "attendees":[

            ],
            "organizer":{
                "emailAddress":{
                    "name":"Samantha Booth",
                    "address":"samanthab@contoso.onmicrosoft.com"
                }
            },      
            "id":"AAMkADNVxRAAA="
        },
        {
            "@odata.type":"#microsoft.graph.event",
            "@odata.etag":"W/\"EZ9r3czxY0m2jz8c45czkwAAFXcvIg==\"",
            "subject":"Pick up car",
            "body":{
                "contentType":"html",
                "content":""
            },
            "start":{
                "dateTime":"2016-12-10T01:00:00.0000000",
                "timeZone":"UTC"
            },
            "end":{
                "dateTime":"2016-12-10T02:00:00.0000000",
                "timeZone":"UTC"
            },
            "attendees":[

            ],
            "organizer":{
                "emailAddress":{
                    "name":"Samantha Booth",
                    "address":"samanthab@contoso.onmicrosoft.com"
                }
            },
            "id":"AAMkADVxSAAA="
        }
    ]
}
```

### <a name="step-2-sample-second-request"></a>Paso 2: segunda solicitud de ejemplo

La segunda solicitud especifica la dirección URL `nextLink` devuelta de la respuesta anterior. Observe que ya no tiene que especificar los mismos parámetros _startDateTime_ y _endDateTime_ como en la solicitud inicial, dado que el `skipToken` en la dirección URL `nextLink` los codifica y los incluye.

<!-- {
  "blockType": "request",
  "name": "get_calendarview_delta_2"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarview/delta?$skiptoken=R0usmcCM996atia_s HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="sample-second-response"></a>Segunda respuesta de ejemplo 

La segunda respuesta devuelve los dos siguientes eventos próximos en la vista de calendario y otro `nextLink`, para indicar que hay más eventos para obtener desde la vista de calendario.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Collection(event)",
    "@odata.nextLink":"https://graph.microsoft.com/v1.0/me/calendarview/delta?$skiptoken=R0usmci39OQxqJrxK4",
    "value":[
        {
            "@odata.type":"#microsoft.graph.event",
            "@odata.etag":"W/\"EZ9r3czxY0m2jz8c45czkwAAFXcvIw==\"",
            "subject":"Get food",
            "body":{
                "contentType":"html",
                "content":""
            },
            "start":{
                "dateTime":"2016-12-10T19:30:00.0000000",
                "timeZone":"UTC"
            },
            "end":{
                "dateTime":"2016-12-10T21:30:00.0000000",
                "timeZone":"UTC"
            },
            "attendees":[

            ],
            "organizer":{
                "emailAddress":{
                    "name":"Samantha Booth",
                    "address":"samanthab@contoso.onmicrosoft.com"
                }
            },
            "id":"AAMkADVxTAAA="
        },
        {
            "@odata.type":"#microsoft.graph.event",
            "@odata.etag":"W/\"EZ9r3czxY0m2jz8c45czkwAAFXcvJA==\"",
            "subject":"Prepare food",
            "body":{
                "contentType":"html",
                "content":""
            },
            "start":{
                "dateTime":"2016-12-10T22:00:00.0000000",
                "timeZone":"UTC"
            },
            "end":{
                "dateTime":"2016-12-11T00:00:00.0000000",
                "timeZone":"UTC"
            },
            "attendees":[

            ],
            "organizer":{
                "emailAddress":{
                    "name":"Samantha Booth",
                    "address":"samanthab@contoso.onmicrosoft.com"
                }
            },
            "id":"AAMkADVxUAAA="
        }
    ]
}
```


### <a name="step-3-sample-third-request"></a>Paso 3: tercera solicitud de ejemplo

La tercera solicitud continúa usando el último `nextLink` devuelto desde la última solicitud de sincronización. 
 

<!-- {
  "blockType": "request",
  "name": "get_calendarview_delta_3"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarview/delta?$skiptoken=R0usmci39OQxqJrxK4 HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="sample-third-and-final-response"></a>Tercera y última respuesta de ejemplo

La tercera respuesta devuelve el único evento restante en la vista de calendario y una dirección URL `deltaLink` que indica que la sincronización se completó para esta vista de calendario. Guarde y use la dirección URL `deltaLink` para [sincronizar la vista de calendario en la siguiente ronda](#the-next-round-sample-first-request).


<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Collection(event)",
    "@odata.deltaLink":"https://graph.microsoft.com/v1.0/me/calendarview/delta?$deltatoken=R0usmcMDNGg0J1E",
    "value":[
        {
            "@odata.type":"#microsoft.graph.event",
            "@odata.etag":"W/\"EZ9r3czxY0m2jz8c45czkwAALZu97g==\"",
            "subject":"Rest!",
            "body":{
                "contentType":"html",
                "content":""
            },
            "start":{
                "dateTime":"2016-12-12T02:00:00.0000000",
                "timeZone":"UTC"
            },
            "end":{
                "dateTime":"2016-12-12T07:30:00.0000000",
                "timeZone":"UTC"
            },
            "location":{
                "displayName":"Home"
            },
            "attendees":[

            ],
            "organizer":{
                "emailAddress":{
                    "name":"Samantha Booth",
                    "address":"samanthab@contoso.onmicrosoft.com"
                }
            },
            "id":"AAMkADj1HuAAA="
        }
    ]
}
```


### <a name="the-next-round-sample-first-request"></a>La siguiente ronda: primera solicitud de ejemplo

Con el `deltaLink` de la [última solicitud](#step-3-sample-third-request) de la última ronda, solo se podrán obtener aquellos eventos que cambiaron (que se agregaron, eliminaron o actualizaron) en esa vista de calendario desde entonces. La primera solicitud de la ronda siguiente será similar a la mostrada a continuación, suponiendo que prefiere mantener el mismo tamaño de página máximo en la respuesta:

<!-- {
  "blockType": "request",
  "name": "get_calendarview_delta_next"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarview/delta?$deltatoken=R0usmcMDNGg0J1E HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="the-next-round-sample-first-response"></a>La siguiente ronda: primera respuesta de ejemplo

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Collection(event)",
    "@odata.deltaLink":"https://graph.microsoft.com/v1.0/me/calendarview/delta?$deltatoken=R0usmcFuQtZdtpk4",
    "value":[
        {
            "@odata.type": "#microsoft.graph.event",
            "id": "AAMkADk0MGFkODE3LWE4MmYtNDRhOS04OGQLkRkXbBznTvAADb6ytyAAA=",
            "@removed": {
                "reason": "deleted"
            }
        },
        {
            "@odata.type":"#microsoft.graph.event",
            "@odata.etag":"W/\"EZ9r3czxY0m2jz8c45czkwAALZu97w==\"",
            "subject":"Attend service",
            "body":{
                "contentType":"html",
                "content":""
            },
            "start":{
                "dateTime":"2016-12-25T06:00:00.0000000",
                "timeZone":"UTC"
            },
            "end":{
                "dateTime":"2016-12-25T07:30:00.0000000",
                "timeZone":"UTC"
            },
            "location":{
                "displayName":"Chapel of Saint Ignatius",
                "address":{
                    "type":"unknown",
                    "street":"900 Broadway",
                    "city":"Seattle",
                    "state":"WA",
                    "countryOrRegion":"United States",
                    "postalCode":""
                },
                "coordinates":{
                    "latitude":47.6105,
                    "longitude":-122.321
                }
            },
            "attendees":[

            ],
            "organizer":{
                "emailAddress":{
                    "name":"Samantha Booth",
                    "address":"samanthab@contoso.onmicrosoft.com"
                }
            },
            "id":"AAMkADj1HvAAA="
        }
    ]
}
```

## <a name="see-also"></a>Vea también

- [Consulta delta de Microsoft Graph](../Concepts/delta_query_overview.md)
- [Obtener los cambios incrementales en los mensajes](../Concepts/delta_query_messages.md)
- [Obtener los cambios incrementales en los grupos](../Concepts/delta_query_groups.md)
- [Obtener los cambios incrementales en los usuarios](../Concepts/delta_query_users.md)
