# <a name="list-events"></a><span data-ttu-id="83958-101">List events</span><span class="sxs-lookup"><span data-stu-id="83958-101">List events</span></span>

<span data-ttu-id="83958-p101">Obtiene una lista de objetos [event](../resources/event.md) en el buzón del usuario. La lista contiene patrones de serie y reuniones de instancia única.</span><span class="sxs-lookup"><span data-stu-id="83958-p101">Get a list of [event](../resources/event.md) objects in the user's mailbox. The list contains single instance meetings and series masters.</span></span>

<span data-ttu-id="83958-104">Actualmente, esta operación devuelve los cuerpos de los eventos solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="83958-104">Currently, this operation returns event bodies in only HTML format.</span></span>

<span data-ttu-id="83958-105">Para obtener instancias de evento de expansión, puede [obtener la vista de calendario](calendar_list_calendarview.md) o bien [obtener las instancias de un evento](event_list_instances.md).</span><span class="sxs-lookup"><span data-stu-id="83958-105">To get expanded event instances, you can [get the calendar view](calendar_list_calendarview.md), or [get the instances of an event](event_list_instances.md).</span></span>

### <a name="support-various-time-zones"></a><span data-ttu-id="83958-106">Compatibilidad con varias zonas horarias</span><span class="sxs-lookup"><span data-stu-id="83958-106">Support various time zones</span></span>

<span data-ttu-id="83958-107">Para todas las operaciones GET que devuelven eventos, puede usar el encabezado `Prefer: outlook.timezone` para especificar la zona horaria de las horas de inicio y finalización del evento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="83958-107">For all GET operations that return events, you can use the `Prefer: outlook.timezone` header to specify the time zone for the event start and end times in the response.</span></span> 

<span data-ttu-id="83958-108">Por ejemplo, el siguiente encabezado `Prefer: outlook.timezone` establece las horas de inicio y finalización en la respuesta en la hora estándar del Este.</span><span class="sxs-lookup"><span data-stu-id="83958-108">For example, the following `Prefer: outlook.timezone` header sets the start and end times in the response to Eastern Standard Time.</span></span>
```http
Prefer: outlook.timezone="Eastern Standard Time"
```

<span data-ttu-id="83958-p102">Si el evento se ha creado en una zona horaria diferente, las horas de inicio y finalización se ajustarán a la zona horaria especificada en ese encabezado `Prefer`. Consulte esta [lista](../resources/datetimetimezone.md) para ver los nombres de zona horaria admitidos. Si no se especifica el encabezado `Prefer: outlook.timezone`, se devuelven las horas de inicio y finalización en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="83958-p102">If the event was created in a different time zone, the start and end times will be adjusted to the time zone specified in that `Prefer` header. See this [list](../resources/datetimetimezone.md) for the supported time zone names. If the `Prefer: outlook.timezone` header is not specified, the start and end times are returned in UTC.</span></span>

<span data-ttu-id="83958-112">Puede usar las propiedades **OriginalStartTimeZone** y **OriginalEndTimeZone** del recurso **event** para averiguar la zona horaria usada al crear el evento.</span><span class="sxs-lookup"><span data-stu-id="83958-112">You can use the **OriginalStartTimeZone** and **OriginalEndTimeZone** properties on the **event** resource to find out the time zone used when the event was created.</span></span>

## <a name="permissions"></a><span data-ttu-id="83958-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="83958-113">Permissions</span></span>
<span data-ttu-id="83958-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="83958-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="83958-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="83958-116">Permission type</span></span>      | <span data-ttu-id="83958-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="83958-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="83958-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="83958-118">Delegated (work or school account)</span></span> | <span data-ttu-id="83958-119">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="83958-119">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="83958-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="83958-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="83958-121">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="83958-121">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="83958-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="83958-122">Application</span></span> | <span data-ttu-id="83958-123">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="83958-123">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="83958-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="83958-124">HTTP request</span></span>
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
## <a name="optional-query-parameters"></a><span data-ttu-id="83958-125">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="83958-125">Optional query parameters</span></span>
<span data-ttu-id="83958-126">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="83958-126">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="83958-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="83958-127">Request headers</span></span>
| <span data-ttu-id="83958-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="83958-128">Name</span></span>       | <span data-ttu-id="83958-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="83958-129">Type</span></span> | <span data-ttu-id="83958-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="83958-130">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="83958-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="83958-131">Authorization</span></span>  | <span data-ttu-id="83958-132">string</span><span class="sxs-lookup"><span data-stu-id="83958-132">string</span></span>  | <span data-ttu-id="83958-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="83958-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="83958-135">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="83958-135">Prefer: outlook.timezone</span></span> | <span data-ttu-id="83958-136">string</span><span class="sxs-lookup"><span data-stu-id="83958-136">string</span></span> | <span data-ttu-id="83958-p105">La zona horaria predeterminada para eventos en la respuesta. Opcional.</span><span class="sxs-lookup"><span data-stu-id="83958-p105">The default time zone for events in the response. Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="83958-139">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="83958-139">Request body</span></span>
<span data-ttu-id="83958-140">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="83958-140">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="83958-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="83958-141">Response</span></span>

<span data-ttu-id="83958-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="83958-142">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="83958-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="83958-143">Example</span></span>
##### <a name="request"></a><span data-ttu-id="83958-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="83958-144">Request</span></span>
<span data-ttu-id="83958-p106">Aquí tiene un ejemplo de la solicitud. Especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="83958-p106">Here is an example of the request. It specifies the following:</span></span>

- <span data-ttu-id="83958-147">Un encabezado `Prefer: outlook.timezone` para obtener valores de fecha y hora devueltos en la hora estándar del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="83958-147">A `Prefer: outlook.timezone` header to get date time values returned in Pacific Standard Time.</span></span> 
- <span data-ttu-id="83958-p107">Un parámetro de consulta `$select` para devolver propiedades específicas. Sin ningún parámetro `$select`, se devolverán todas las propiedades de evento.</span><span class="sxs-lookup"><span data-stu-id="83958-p107">A `$select` query parameter to return specific properties. Without a `$select` parameter, all of the event properties will be returned.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_events"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events?$select=subject,body,bodyPreview,organizer,attendees,start,end,location
Prefer: outlook.timezone="Pacific Standard Time"
```
##### <a name="response"></a><span data-ttu-id="83958-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="83958-150">Response</span></span>
<span data-ttu-id="83958-p108">Aquí tiene un ejemplo de la respuesta. Se devuelve la propiedad **body** en el formato HTML predeterminado.</span><span class="sxs-lookup"><span data-stu-id="83958-p108">Here is an example of the response. The **body** property is returned in the default HTML format.</span></span>
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
                        "name":"Fanny Downs",
                        "address":"fannyd@a830edad905084922E17020313.onmicrosoft.com"
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
                    "name":"Fanny Downs",
                    "address":"fannyd@a830edad905084922E17020313.onmicrosoft.com"
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
