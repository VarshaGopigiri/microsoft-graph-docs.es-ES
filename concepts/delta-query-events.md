---
title: 'Obtener los cambios incrementales en los eventos en una vista de calendario '
description: 'Una vista de calendario es una colección de eventos en un intervalo de fecha y hora del calendario predeterminado (../me/calendarview). '
ms.openlocfilehash: 68e4053c29fd95f04ff0b031bf519301e63dc08a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092857"
---
# <a name="get-incremental-changes-to-events-in-a-calendar-view"></a><span data-ttu-id="41608-103">Obtener los cambios incrementales en los eventos en una vista de calendario</span><span class="sxs-lookup"><span data-stu-id="41608-103">Get incremental changes to events in a calendar view</span></span> 

<span data-ttu-id="41608-p101">Una vista de calendario es una colección de eventos en un intervalo de fecha y hora del calendario predeterminado (../me/calendarview) o algún otro calendario del usuario. Mediante la consulta de delta, puede obtener eventos nuevos, actualizados o eliminados en una vista de calendario. Los eventos devueltos pueden incluir las repeticiones y excepciones de una serie periódica e instancias únicas. Los datos de delta permiten mantener y sincronizar un almacén local de eventos de un usuario, sin tener que capturar cada vez todo el conjunto de eventos del usuario desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="41608-p101">A calendar view is a collection of events in a date/time range from the default calendar (../me/calendarview) or some other calendar of the user's. By using delta query, you can get new, updated, or deleted events in a calendar view. The returned events may include occurrences and exceptions of a recurring series, and single instances. The delta data enables you to maintain and synchronize a local store of a user's events, without having to fetch the entire set of the user's events from the server every time.</span></span>

<span data-ttu-id="41608-p102">La consulta de delta admite la sincronización completa que recupera todos los eventos en la vista de calendario especificada y la sincronización incremental que recupera aquellos eventos que cambiaron en la vista de calendario desde la última sincronización. Normalmente, se debería realizar una sincronización completa inicial y, después, obtener los cambios incrementales en la vista de calendario de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="41608-p102">Delta query supports both full synchronization that retrieves all the events in the specified calendar view, and incremental synchronization that retrieves those events that have changed in the calendar view since the last synchronization. Typically, you would do an initial full synchronization, and subsequently, get incremental changes to that calendar view periodically.</span></span> 

## <a name="track-event-changes-in-a-calendar-view"></a><span data-ttu-id="41608-110">Seguir los cambios de eventos en una vista de calendario</span><span class="sxs-lookup"><span data-stu-id="41608-110">Track event changes in a calendar view</span></span>

<span data-ttu-id="41608-p103">La consulta de delta para eventos es específica del calendario y el intervalo de fecha y hora que se especifique (por ejemplo, una vista de calendario). Para realizar el seguimiento de los cambios en varios calendarios, necesitará realizar el seguimiento de cada calendario individualmente.</span><span class="sxs-lookup"><span data-stu-id="41608-p103">Delta query for events is specific to a calendar and date/time range that you specify (i.e., a calendar view). To track the changes in multiple calendars, you need to track each calendar individually.</span></span> 

<span data-ttu-id="41608-p104">El seguimiento de los cambios de eventos en una vista de calendario normalmente es una ronda de una o varias solicitudes GET con la función [delta](/graph/api/event-delta?view=graph-rest-1.0). La solicitud GET inicial es muy similar a la forma de [enumerar un objeto calendarView](/graph/api/calendar-list-calendarview?view=graph-rest-1.0), salvo que se incluye la función **delta**:</span><span class="sxs-lookup"><span data-stu-id="41608-p104">Tracking event changes in a calendar view typically is a round of one or more GET requests with the [delta](/graph/api/event-delta?view=graph-rest-1.0) function. The initial GET request is very much like the way you [list a calendarView](/graph/api/calendar-list-calendarview?view=graph-rest-1.0), except that you include the **delta** function:</span></span>

```
GET /me/calendarView/delta?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="41608-115">Una solicitud GET con la función **delta** función devuelve:</span><span class="sxs-lookup"><span data-stu-id="41608-115">A GET request with the **delta** function returns either:</span></span>

- <span data-ttu-id="41608-116">Un `nextLink` (que contiene una dirección URL con una llamada de función **delta** y un _skipToken_), o</span><span class="sxs-lookup"><span data-stu-id="41608-116">A `nextLink` (that contains a URL with a **delta** function call and a _skipToken_), or</span></span> 
- <span data-ttu-id="41608-117">Un `deltaLink` (que contiene una dirección URL con una llamada de función **delta** y un _deltaToken_).</span><span class="sxs-lookup"><span data-stu-id="41608-117">A `deltaLink` (that contains a URL with a **delta** function call and _deltaToken_).</span></span>

<span data-ttu-id="41608-118">Estos tokens son [tokens de estado](delta-query-overview.md#state-tokens) que codifican los parámetros refs/remotes/microsoftgraph/master _startDateTime_ y _endDateTime_, y cualquier otro parámetro de consulta en la solicitud GET de la consulta de delta inicial.</span><span class="sxs-lookup"><span data-stu-id="41608-118">These tokens are [state tokens](delta-query-overview.md#state-tokens) which encode the refs/remotes/microsoftgraph/master _startDateTime_ and _endDateTime_ parameters, and any other query parameter in your initial delta query GET request.</span></span> 

<span data-ttu-id="41608-p105">Los tokens de estado son totalmente opacos para el cliente. Para continuar con una ronda de seguimiento de cambios, basta con copiar y aplicar la dirección URL `nextLink` o `deltaLink` devuelta desde la última solicitud GET a la siguiente llamada de función**delta** para la mismo vista de calendario. Un `deltaLink` devuelto en una respuesta significa que la ronda actual de seguimiento de cambios está completa. Se puede guardar y usar la dirección URL `deltaLink` cuando se inicia la siguiente ronda.</span><span class="sxs-lookup"><span data-stu-id="41608-p105">State tokens are completely opaque to the client. To proceed with a round of change tracking, simply copy and apply the `nextLink` or `deltaLink` URL returned from the last GET request to the next **delta** function call for that same calendar view. A `deltaLink` returned in a response signifies that the current round of change tracking is complete. You can save and use the `deltaLink` URL when you begin the next round.</span></span>

<span data-ttu-id="41608-123">Vea el [ejemplo](#example-to-synchronize-events-in-a-calendar-view) siguiente para obtener información sobre cómo usar estas direcciones URL `nextLink` y `deltaLink`.</span><span class="sxs-lookup"><span data-stu-id="41608-123">See the [example](#example-to-synchronize-events-in-a-calendar-view) below to learn how to use these `nextLink` and `deltaLink` URLs.</span></span>

### <a name="use-query-parameters-in-a-delta-query-for-calendar-view"></a><span data-ttu-id="41608-124">Usar parámetros de consulta en una consulta de delta para la vista de calendario</span><span class="sxs-lookup"><span data-stu-id="41608-124">Use query parameters in a delta query for calendar view</span></span>

- <span data-ttu-id="41608-125">Incluya los parámetros _startDateTime_ y _endDateTime_ para definir un intervalo de fecha y hora para la vista de calendario.</span><span class="sxs-lookup"><span data-stu-id="41608-125">Include the _startDateTime_ and _endDateTime_ parameters to define a date/time range for your calendar view.</span></span>
- <span data-ttu-id="41608-126">`$select` no es compatible.</span><span class="sxs-lookup"><span data-stu-id="41608-126">`$select` is not supported.</span></span>


### <a name="optional-request-header"></a><span data-ttu-id="41608-127">Encabezado de solicitud opcional</span><span class="sxs-lookup"><span data-stu-id="41608-127">Optional request header</span></span>

<span data-ttu-id="41608-128">Cada solicitud GET de la consulta delta devuelve una colección de uno o más eventos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41608-128">Each delta query GET request returns a collection of one or more events in the response.</span></span> <span data-ttu-id="41608-129">Opcionalmente se puede especificar el encabezado de solicitud, `Prefer: odata.maxpagesize={x}`, para establecer el número máximo de eventos en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="41608-129">You can optionally specify the request header, `Prefer: odata.maxpagesize={x}`, to set the maximum number of events in a response.</span></span>


## <a name="example-to-synchronize-events-in-a-calendar-view"></a><span data-ttu-id="41608-130">Ejemplo para sincronizar los eventos en una vista de calendario</span><span class="sxs-lookup"><span data-stu-id="41608-130">Example to synchronize events in a calendar view</span></span>

<span data-ttu-id="41608-p107">En el ejemplo siguiente se muestra una serie de tres solicitudes para sincronizar el calendario predeterminado del usuario en un intervalo de tiempo específico. En esa vista de calendario hay cinco eventos.</span><span class="sxs-lookup"><span data-stu-id="41608-p107">The following example shows a series of 3 requests to synchronize the user's default calendar in a specific time range. There are 5 events in that calendar view.</span></span>

- <span data-ttu-id="41608-133">[Paso 1: solicitud inicial de ejemplo](#step-1-sample-initial-request) y [respuesta](#sample-initial-response)</span><span class="sxs-lookup"><span data-stu-id="41608-133">[Step 1: sample initial request](#step-1-sample-initial-request) and [response](#sample-initial-response)</span></span>
- <span data-ttu-id="41608-134">[Paso 2: segunda solicitud de ejemplo](#step-2-sample-second-request) y [respuesta](#sample-second-response)</span><span class="sxs-lookup"><span data-stu-id="41608-134">[Step 2: sample second request](#step-2-sample-second-request) and [response](#sample-second-response)</span></span>
- <span data-ttu-id="41608-135">[Paso 2: tercera solicitud de ejemplo](#step-3-sample-third-request) y [respuesta final](#sample-third-and-final-response)</span><span class="sxs-lookup"><span data-stu-id="41608-135">[Step 3: sample third request](#step-3-sample-third-request) and [final response](#sample-third-and-final-response)</span></span>

<span data-ttu-id="41608-p108">Para mayor brevedad, las respuestas de ejemplo muestran solo un subconjunto de las propiedades de un evento. En una llamada real, se devuelve la mayoría de las propiedades de evento .</span><span class="sxs-lookup"><span data-stu-id="41608-p108">For brevity, the sample responses show only a subset of the properties for an event. In an actual call, most event properties are returned.</span></span> 

<span data-ttu-id="41608-138">Vea también lo que hará la [siguiente ronda](#the-next-round-sample-first-response).</span><span class="sxs-lookup"><span data-stu-id="41608-138">See also what you'll do in the [next round](#the-next-round-sample-first-response).</span></span>


### <a name="step-1-sample-initial-request"></a><span data-ttu-id="41608-139">Paso 1: solicitud inicial de ejemplo</span><span class="sxs-lookup"><span data-stu-id="41608-139">Step 1: sample initial request</span></span>

<span data-ttu-id="41608-p109">En este ejemplo, se sincroniza por primera vez la vista de calendario especificada, por lo que la solicitud de sincronización inicial no incluye ningún token de estado. Esa ronda devolverá todos los eventos de esa vista de calendario.</span><span class="sxs-lookup"><span data-stu-id="41608-p109">In this example, the specified calendar view is being synchronized for the first time, so the initial sync request does not include any state token. This round will return all the events in that calendar view.</span></span>

<span data-ttu-id="41608-142">La primera solicitud especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="41608-142">The first request specifies the following:</span></span>

- <span data-ttu-id="41608-143">Valores de fecha u hora para los parámetros _startDateTime_ y _endDateTime_.</span><span class="sxs-lookup"><span data-stu-id="41608-143">Date/time values for the _startDateTime_ and _endDateTime_ parameters.</span></span>
- <span data-ttu-id="41608-144">El [encabezado de solicitud opcional](#optional-request-header), _odata.maxpagesize_, que devuelve dos eventos a la vez.</span><span class="sxs-lookup"><span data-stu-id="41608-144">The [optional request header](#optional-request-header), _odata.maxpagesize_, returning 2 events at a time.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_calendarview_delta_1"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarView/delta?startdatetime=2016-12-01T00:00:00Z&enddatetime=2016-12-30T00:00:00Z HTTP/1.1
Prefer: odata.maxpagesize=2
```


### <a name="sample-initial-response"></a><span data-ttu-id="41608-145">Respuesta inicial de ejemplo</span><span class="sxs-lookup"><span data-stu-id="41608-145">Sample initial response</span></span>

<span data-ttu-id="41608-p110">La respuesta incluye dos eventos y un encabezado de respuesta `@odata.nextLink` con un `skipToken`. La dirección URL `nextLink` indica que hay más eventos para obtener en la vista de calendario.</span><span class="sxs-lookup"><span data-stu-id="41608-p110">The response includes two events and a `@odata.nextLink` response header with a `skipToken`. The `nextLink` URL indicates there are more events in the calendar view to get.</span></span>

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
    "@odata.nextLink":"https://graph.microsoft.com/v1.0/me/calendarView/delta?$skiptoken=R0usmcCM996atia_s",
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

### <a name="step-2-sample-second-request"></a><span data-ttu-id="41608-148">Paso 2: segunda solicitud de ejemplo</span><span class="sxs-lookup"><span data-stu-id="41608-148">Step 2: sample second request</span></span>

<span data-ttu-id="41608-p111">La segunda solicitud especifica la dirección URL `nextLink` devuelta de la respuesta anterior. Observe que ya no tiene que especificar los mismos parámetros _startDateTime_ y _endDateTime_ como en la solicitud inicial, dado que el `skipToken` en la dirección URL `nextLink` los codifica y los incluye.</span><span class="sxs-lookup"><span data-stu-id="41608-p111">The second request specifies the `nextLink` URL returned from the previous response. Notice that it no longer has to specify the same _startDateTime_ and _endDateTime_ parameters as in the initial request, as the `skipToken` in the `nextLink` URL encodes and includes them.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_calendarview_delta_2"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarView/delta?$skiptoken=R0usmcCM996atia_s HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="sample-second-response"></a><span data-ttu-id="41608-151">Segunda respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="41608-151">Sample second response</span></span> 

<span data-ttu-id="41608-152">La segunda respuesta devuelve los dos siguientes eventos próximos en la vista de calendario y otro `nextLink`, para indicar que hay más eventos para obtener desde la vista de calendario.</span><span class="sxs-lookup"><span data-stu-id="41608-152">The second response returns the next 2 events in the calendar view and another `nextLink`, indicating there are more events to get from the calendar view.</span></span>

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
    "@odata.nextLink":"https://graph.microsoft.com/v1.0/me/calendarView/delta?$skiptoken=R0usmci39OQxqJrxK4",
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


### <a name="step-3-sample-third-request"></a><span data-ttu-id="41608-153">Paso 3: tercera solicitud de ejemplo</span><span class="sxs-lookup"><span data-stu-id="41608-153">Step 3: sample third request</span></span>

<span data-ttu-id="41608-154">La tercera solicitud continúa usando el último `nextLink` devuelto desde la última solicitud de sincronización.</span><span class="sxs-lookup"><span data-stu-id="41608-154">The third request continues to use the latest `nextLink` returned from the last sync request.</span></span> 
 

<!-- {
  "blockType": "request",
  "name": "get_calendarview_delta_3"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarView/delta?$skiptoken=R0usmci39OQxqJrxK4 HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="sample-third-and-final-response"></a><span data-ttu-id="41608-155">Tercera y última respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="41608-155">Sample third and final response</span></span>

<span data-ttu-id="41608-p112">La tercera respuesta devuelve el único evento restante en la vista de calendario y una dirección URL `deltaLink` que indica que la sincronización se completó para esta vista de calendario. Guarde y use la dirección URL `deltaLink` para [sincronizar la vista de calendario en la siguiente ronda](#the-next-round-sample-first-request).</span><span class="sxs-lookup"><span data-stu-id="41608-p112">The third response returns the only remaining event in the calendar view, and a `deltaLink` URL which indicates synchronization is complete for this calendar view. Save and use the `deltaLink` URL to [synchronize that calendar view in the next round](#the-next-round-sample-first-request).</span></span>


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
    "@odata.deltaLink":"https://graph.microsoft.com/v1.0/me/calendarView/delta?$deltatoken=R0usmcMDNGg0J1E",
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


### <a name="the-next-round-sample-first-request"></a><span data-ttu-id="41608-158">La siguiente ronda: primera solicitud de ejemplo</span><span class="sxs-lookup"><span data-stu-id="41608-158">The next round: sample first request</span></span>

<span data-ttu-id="41608-p113">Con el `deltaLink` de la [última solicitud](#step-3-sample-third-request) de la última ronda, solo se podrán obtener aquellos eventos que cambiaron (que se agregaron, eliminaron o actualizaron) en esa vista de calendario desde entonces. La primera solicitud de la ronda siguiente será similar a la mostrada a continuación, suponiendo que prefiere mantener el mismo tamaño de página máximo en la respuesta:</span><span class="sxs-lookup"><span data-stu-id="41608-p113">Using the `deltaLink` from the [last request](#step-3-sample-third-request) in the last round, you will be able to get only those events that have changed (by being added, deleted, or updated) in that calendar view since then. Your first request in the next round will look like the following, assuming you prefer to keep the same maximum page size in the response:</span></span>

<!-- {
  "blockType": "request",
  "name": "get_calendarview_delta_next"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarView/delta?$deltatoken=R0usmcMDNGg0J1E HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="the-next-round-sample-first-response"></a><span data-ttu-id="41608-161">La siguiente ronda: primera respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="41608-161">The next round: sample first response</span></span>

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
    "@odata.deltaLink":"https://graph.microsoft.com/v1.0/me/calendarView/delta?$deltatoken=R0usmcFuQtZdtpk4",
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

## <a name="see-also"></a><span data-ttu-id="41608-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="41608-162">See also</span></span>

- [<span data-ttu-id="41608-163">Consulta delta de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="41608-163">Microsoft Graph delta query</span></span>](delta-query-overview.md)
- [<span data-ttu-id="41608-164">Obtener los cambios incrementales en los mensajes</span><span class="sxs-lookup"><span data-stu-id="41608-164">Get incremental changes to messages</span></span>](delta-query-messages.md)
- [<span data-ttu-id="41608-165">Obtener los cambios incrementales en los grupos</span><span class="sxs-lookup"><span data-stu-id="41608-165">Get incremental changes to groups</span></span>](delta-query-groups.md)
- [<span data-ttu-id="41608-166">Obtener los cambios incrementales en los usuarios</span><span class="sxs-lookup"><span data-stu-id="41608-166">Get incremental changes to users</span></span>](delta-query-users.md)
