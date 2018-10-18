# <a name="list-events"></a><span data-ttu-id="bd94e-101">Listar eventos</span><span class="sxs-lookup"><span data-stu-id="bd94e-101">List events</span></span>

<span data-ttu-id="bd94e-p101">Obtiene una lista de objetos [event](../resources/event.md) en el buzón del usuario. La lista contiene patrones de serie y reuniones de instancia única.</span><span class="sxs-lookup"><span data-stu-id="bd94e-p101">Get a list of [event](../resources/event.md) objects in the user's mailbox. The list contains single instance meetings and series masters.</span></span>

<span data-ttu-id="bd94e-104">Para recibir instancias de eventos ampliados, puede [obtener la vista de calendario](calendar_list_calendarview.md) o bien [obtener las instancias de un evento](event_list_instances.md).</span><span class="sxs-lookup"><span data-stu-id="bd94e-104">To get expanded event instances, you can [get the calendar view](calendar_list_calendarview.md), or [get the instances of an event](event_list_instances.md).</span></span>

<span data-ttu-id="bd94e-105">Actualmente, esta operación devuelve los cuerpos de los eventos solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="bd94e-105">Currently, this operation returns event bodies in only HTML format.</span></span>

<span data-ttu-id="bd94e-106">Existen dos escenarios en los que una aplicación puede obtener eventos en el calendario de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="bd94e-106">There are two scenarios where an app can get events in another user's calendar:</span></span>

* <span data-ttu-id="bd94e-107">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="bd94e-107">If the app has application permissions, or,</span></span>
* <span data-ttu-id="bd94e-108">si la aplicación tiene los correspondientes [permisos](#permissions) delegados de un usuario, y otro usuario ha compartido un calendario con ese usuario, o se le ha concedido acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="bd94e-108">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a calendar with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="bd94e-109">Consulte los [detalles y un ejemplo](../../../concepts/outlook-get-shared-events-calendars.md).</span><span class="sxs-lookup"><span data-stu-id="bd94e-109">See [details and an example](../../../concepts/outlook-get-shared-events-calendars.md).</span></span>

### <a name="support-various-time-zones"></a><span data-ttu-id="bd94e-110">Compatibilidad con varias zonas horarias</span><span class="sxs-lookup"><span data-stu-id="bd94e-110">Support various time zones</span></span>

<span data-ttu-id="bd94e-111">Para todas las operaciones GET que devuelven eventos, puede usar el encabezado `Prefer: outlook.timezone` para especificar la zona horaria de las horas de inicio y finalización del evento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd94e-111">For all GET operations that return events, you can use the `Prefer: outlook.timezone` header to specify the time zone for the event start and end times in the response.</span></span> 

<span data-ttu-id="bd94e-112">Por ejemplo, el siguiente encabezado `Prefer: outlook.timezone` establece las horas de inicio y finalización en la respuesta en la hora estándar del Este.</span><span class="sxs-lookup"><span data-stu-id="bd94e-112">For example, the following `Prefer: outlook.timezone` header sets the start and end times in the response to Eastern Standard Time.</span></span>
```http
Prefer: outlook.timezone="Eastern Standard Time"
```

<span data-ttu-id="bd94e-p103">Si el evento se ha creado en una zona horaria diferente, las horas de inicio y finalización se ajustarán a la zona horaria especificada en ese encabezado `Prefer`. Consulte esta [lista](../resources/datetimetimezone.md) para ver los nombres de zona horaria admitidos. Si no se especifica el encabezado `Prefer: outlook.timezone`, se devuelven las horas de inicio y finalización en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="bd94e-p103">If the event was created in a different time zone, the start and end times will be adjusted to the time zone specified in that `Prefer` header. See this [list](../resources/datetimetimezone.md) for the supported time zone names. If the `Prefer: outlook.timezone` header is not specified, the start and end times are returned in UTC.</span></span>

<span data-ttu-id="bd94e-116">Puede usar las propiedades **OriginalStartTimeZone** y **OriginalEndTimeZone** del recurso **event** para averiguar la zona horaria usada al crear el evento.</span><span class="sxs-lookup"><span data-stu-id="bd94e-116">You can use the **OriginalStartTimeZone** and **OriginalEndTimeZone** properties on the **event** resource to find out the time zone used when the event was created.</span></span>

## <a name="permissions"></a><span data-ttu-id="bd94e-117">Permisos</span><span class="sxs-lookup"><span data-stu-id="bd94e-117">Permissions</span></span>
<span data-ttu-id="bd94e-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bd94e-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bd94e-120">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bd94e-120">Permission type</span></span>      | <span data-ttu-id="bd94e-121">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bd94e-121">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bd94e-122">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bd94e-122">Delegated (work or school account)</span></span> | <span data-ttu-id="bd94e-123">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bd94e-123">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="bd94e-124">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bd94e-124">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bd94e-125">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bd94e-125">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="bd94e-126">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bd94e-126">Application</span></span> | <span data-ttu-id="bd94e-127">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bd94e-127">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="bd94e-128">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bd94e-128">HTTP request</span></span>
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
## <a name="optional-query-parameters"></a><span data-ttu-id="bd94e-129">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bd94e-129">Optional query parameters</span></span>
<span data-ttu-id="bd94e-130">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd94e-130">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bd94e-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bd94e-131">Request headers</span></span>
| <span data-ttu-id="bd94e-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="bd94e-132">Name</span></span>       | <span data-ttu-id="bd94e-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="bd94e-133">Type</span></span> | <span data-ttu-id="bd94e-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd94e-134">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="bd94e-135">Autorización</span><span class="sxs-lookup"><span data-stu-id="bd94e-135">Authorization</span></span>  | <span data-ttu-id="bd94e-136">cadena</span><span class="sxs-lookup"><span data-stu-id="bd94e-136">string</span></span> | <span data-ttu-id="bd94e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bd94e-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="bd94e-139">Preferido: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="bd94e-139">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="bd94e-140">cadena</span><span class="sxs-lookup"><span data-stu-id="bd94e-140">string</span></span> | <span data-ttu-id="bd94e-141">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd94e-141">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="bd94e-142">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="bd94e-142">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="bd94e-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bd94e-143">Optional.</span></span> |
| <span data-ttu-id="bd94e-144">Preferido: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="bd94e-144">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="bd94e-145">cadena</span><span class="sxs-lookup"><span data-stu-id="bd94e-145">string</span></span> | <span data-ttu-id="bd94e-146">Formato de la propiedad **body** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="bd94e-146">The format of the **body** property to be returned in.</span></span> <span data-ttu-id="bd94e-147">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="bd94e-147">Values can be "text" or "html".</span></span> <span data-ttu-id="bd94e-148">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="bd94e-148">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="bd94e-149">Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="bd94e-149">If the header is not specified, the **body** property is returned in HTML format.</span></span> <span data-ttu-id="bd94e-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bd94e-150">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bd94e-151">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bd94e-151">Request body</span></span>
<span data-ttu-id="bd94e-152">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bd94e-152">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bd94e-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd94e-153">Response</span></span>

<span data-ttu-id="bd94e-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd94e-154">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bd94e-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd94e-155">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bd94e-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bd94e-156">Request</span></span>
<span data-ttu-id="bd94e-p108">Aquí tiene un ejemplo de la solicitud. Especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bd94e-p108">Here is an example of the request. It specifies the following:</span></span>

- <span data-ttu-id="bd94e-159">Un encabezado `Prefer: outlook.timezone` para obtener valores de fecha y hora devueltos en la hora estándar del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="bd94e-159">A `Prefer: outlook.timezone` header to get date time values returned in Pacific Standard Time.</span></span> 
- <span data-ttu-id="bd94e-p109">Un parámetro de consulta `$select` para devolver propiedades específicas. Sin ningún parámetro `$select`, se devolverán todas las propiedades de evento.</span><span class="sxs-lookup"><span data-stu-id="bd94e-p109">A `$select` query parameter to return specific properties. Without a `$select` parameter, all of the event properties will be returned.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_events"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events?$select=subject,body,bodyPreview,organizer,attendees,start,end,location
Prefer: outlook.timezone="Pacific Standard Time"
```
##### <a name="response"></a><span data-ttu-id="bd94e-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd94e-162">Response</span></span>
<span data-ttu-id="bd94e-p110">Aquí tiene un ejemplo de la respuesta. Se devuelve la propiedad **body** en el formato HTML predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bd94e-p110">Here is an example of the response. The **body** property is returned in the default HTML format.</span></span>
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
            "location": {
                "displayName": "Assembly Hall",
                "locationType": "default",
                "uniqueId": "Assembly Hall",
                "uniqueIdType": "private"
            },
            "locations": [
                {
                    "displayName": "Assembly Hall",
                    "locationType": "default",
                    "uniqueIdType": "unknown"
                }
            ],
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
