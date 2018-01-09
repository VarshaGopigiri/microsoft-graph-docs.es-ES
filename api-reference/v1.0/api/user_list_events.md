# <a name="list-events"></a><span data-ttu-id="c89f6-101">List events</span><span class="sxs-lookup"><span data-stu-id="c89f6-101">List events</span></span>

<span data-ttu-id="c89f6-p101">Obtiene una lista de objetos [event](../resources/event.md) en el buzón del usuario. La lista contiene patrones de serie y reuniones de instancia única.</span><span class="sxs-lookup"><span data-stu-id="c89f6-p101">Get a list of [event](../resources/event.md) objects in the user's mailbox. The list contains single instance meetings and series masters.</span></span>

<span data-ttu-id="c89f6-104">Actualmente, esta operación devuelve los cuerpos de los eventos solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="c89f6-104">Currently, this operation returns event bodies in only HTML format.</span></span>

<span data-ttu-id="c89f6-105">Para obtener instancias de evento de expansión, puede [obtener la vista de calendario](calendar_list_calendarview.md) o bien [obtener las instancias de un evento](event_list_instances.md).</span><span class="sxs-lookup"><span data-stu-id="c89f6-105">To get expanded event instances, you can [get the calendar view](calendar_list_calendarview.md), or [get the instances of an event](event_list_instances.md).</span></span>


### <a name="get-events-in-another-users-calendar"></a><span data-ttu-id="c89f6-106">Obtener los eventos del calendario de otro usuario</span><span class="sxs-lookup"><span data-stu-id="c89f6-106">Get events in another user's calendar</span></span>

<span data-ttu-id="c89f6-107">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los eventos del calendario de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="c89f6-107">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get events from another user's calendar.</span></span> <span data-ttu-id="c89f6-108">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="c89f6-108">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="c89f6-109">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="c89f6-109">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="c89f6-110">Suponga que otro usuario, Garth, ha compartido un calendario con John.</span><span class="sxs-lookup"><span data-stu-id="c89f6-110">Suppose another user, Garth, has shared a calendar with John.</span></span> <span data-ttu-id="c89f6-111">Puede obtener los eventos de dicho calendario compartido especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="c89f6-111">You can get the events in that shared calendar by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/events
```

<span data-ttu-id="c89f6-112">Esta capacidad se aplica a todas las operaciones de eventos GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="c89f6-112">This capability applies to all the supported GET events operations for an individual user, as listed in the [HTTP request](#http-request) section below.</span></span> <span data-ttu-id="c89f6-113">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="c89f6-113">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="c89f6-114">Si Garth no ha compartido su calendario con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="c89f6-114">If Garth has not shared his calendar with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="c89f6-115">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener los eventos de los calendarios del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="c89f6-115">In such cases, specifying a user ID or user principal name only works for getting events in the signed-in user’s own calendars, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/events
```

<span data-ttu-id="c89f6-116">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="c89f6-116">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="c89f6-117">Uso compartido de carpetas de contactos, calendarios y carpetas de mensajes</span><span class="sxs-lookup"><span data-stu-id="c89f6-117">Shared contact folders, calendars, and message folders</span></span> 
- <span data-ttu-id="c89f6-118">Contactos, eventos y mensajes en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="c89f6-118">Contacts, events, and messages in shared folders</span></span>
- <span data-ttu-id="c89f6-119">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="c89f6-119">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="c89f6-120">Esta capacidad no está disponible en otras operaciones de contactos, eventos, mensajes y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="c89f6-120">This capability is not available in other operations for contacts, events, messages, and their folders.</span></span>


### <a name="support-various-time-zones"></a><span data-ttu-id="c89f6-121">Compatibilidad con varias zonas horarias</span><span class="sxs-lookup"><span data-stu-id="c89f6-121">Support various time zones</span></span>

<span data-ttu-id="c89f6-122">Para todas las operaciones GET que devuelven eventos, puede usar el encabezado `Prefer: outlook.timezone` para especificar la zona horaria de las horas de inicio y finalización del evento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c89f6-122">For all GET operations that return events, you can use the `Prefer: outlook.timezone` header to specify the time zone for the event start and end times in the response.</span></span> 

<span data-ttu-id="c89f6-123">Por ejemplo, el siguiente encabezado `Prefer: outlook.timezone` establece las horas de inicio y finalización en la respuesta en la hora estándar del Este.</span><span class="sxs-lookup"><span data-stu-id="c89f6-123">For example, the following `Prefer: outlook.timezone` header sets the start and end times in the response to Eastern Standard Time.</span></span>
```http
Prefer: outlook.timezone="Eastern Standard Time"
```

<span data-ttu-id="c89f6-p106">Si el evento se ha creado en una zona horaria diferente, las horas de inicio y finalización se ajustarán a la zona horaria especificada en ese encabezado `Prefer`. Consulte esta [lista](../resources/datetimetimezone.md) para ver los nombres de zona horaria admitidos. Si no se especifica el encabezado `Prefer: outlook.timezone`, se devuelven las horas de inicio y finalización en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="c89f6-p106">If the event was created in a different time zone, the start and end times will be adjusted to the time zone specified in that `Prefer` header. See this [list](../resources/datetimetimezone.md) for the supported time zone names. If the `Prefer: outlook.timezone` header is not specified, the start and end times are returned in UTC.</span></span>

<span data-ttu-id="c89f6-127">Puede usar las propiedades **OriginalStartTimeZone** y **OriginalEndTimeZone** del recurso **event** para averiguar la zona horaria usada al crear el evento.</span><span class="sxs-lookup"><span data-stu-id="c89f6-127">You can use the **OriginalStartTimeZone** and **OriginalEndTimeZone** properties on the **event** resource to find out the time zone used when the event was created.</span></span>

## <a name="permissions"></a><span data-ttu-id="c89f6-128">Permisos</span><span class="sxs-lookup"><span data-stu-id="c89f6-128">Permissions</span></span>
<span data-ttu-id="c89f6-p107">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c89f6-p107">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c89f6-131">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c89f6-131">Permission type</span></span>      | <span data-ttu-id="c89f6-132">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c89f6-132">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c89f6-133">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c89f6-133">Delegated (work or school account)</span></span> | <span data-ttu-id="c89f6-134">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c89f6-134">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="c89f6-135">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c89f6-135">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c89f6-136">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c89f6-136">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="c89f6-137">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c89f6-137">Application</span></span> | <span data-ttu-id="c89f6-138">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c89f6-138">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c89f6-139">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c89f6-139">HTTP request</span></span>
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
## <a name="optional-query-parameters"></a><span data-ttu-id="c89f6-140">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c89f6-140">Optional query parameters</span></span>
<span data-ttu-id="c89f6-141">Este método admite los [parámetros de consulta de OData]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c89f6-141">This method supports the [OData Query Parameters]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c89f6-142">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c89f6-142">Request headers</span></span>
| <span data-ttu-id="c89f6-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="c89f6-143">Name</span></span>       | <span data-ttu-id="c89f6-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="c89f6-144">Type</span></span> | <span data-ttu-id="c89f6-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="c89f6-145">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="c89f6-146">Authorization</span><span class="sxs-lookup"><span data-stu-id="c89f6-146">Authorization</span></span>  | <span data-ttu-id="c89f6-147">string</span><span class="sxs-lookup"><span data-stu-id="c89f6-147">string</span></span> | <span data-ttu-id="c89f6-p108">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c89f6-p108">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c89f6-150">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="c89f6-150">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="c89f6-151">string</span><span class="sxs-lookup"><span data-stu-id="c89f6-151">string</span></span> | <span data-ttu-id="c89f6-152">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c89f6-152">outlook.timezone="Eastern Standard Time". Optional. Use this to specify the time zone for start and end times in the response. If not specified, the response are returned in UTC.</span></span> <span data-ttu-id="c89f6-153">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="c89f6-153">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="c89f6-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c89f6-154">Optional.</span></span> |
| <span data-ttu-id="c89f6-155">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="c89f6-155">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="c89f6-156">string</span><span class="sxs-lookup"><span data-stu-id="c89f6-156">string</span></span> | <span data-ttu-id="c89f6-157">Formato de la propiedad **body** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="c89f6-157">The format of the **body** property to be returned in.</span></span> <span data-ttu-id="c89f6-158">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="c89f6-158">Values can be "text" or "html".</span></span> <span data-ttu-id="c89f6-159">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="c89f6-159">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="c89f6-160">Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="c89f6-160">If the header is not specified, the **body** property is returned in HTML format.</span></span> <span data-ttu-id="c89f6-161">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c89f6-161">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c89f6-162">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c89f6-162">Request body</span></span>
<span data-ttu-id="c89f6-163">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c89f6-163">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c89f6-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c89f6-164">Response</span></span>

<span data-ttu-id="c89f6-165">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c89f6-165">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c89f6-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c89f6-166">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c89f6-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c89f6-167">Request</span></span>
<span data-ttu-id="c89f6-p111">Aquí tiene un ejemplo de la solicitud. Especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c89f6-p111">Here is an example of the request. It specifies the following:</span></span>

- <span data-ttu-id="c89f6-170">Un encabezado `Prefer: outlook.timezone` para obtener valores de fecha y hora devueltos en la hora estándar del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="c89f6-170">A `Prefer: outlook.timezone` header to get date time values returned in Pacific Standard Time.</span></span> 
- <span data-ttu-id="c89f6-p112">Un parámetro de consulta `$select` para devolver propiedades específicas. Sin ningún parámetro `$select`, se devolverán todas las propiedades de evento.</span><span class="sxs-lookup"><span data-stu-id="c89f6-p112">A `$select` query parameter to return specific properties. Without a `$select` parameter, all of the event properties will be returned.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_events"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events?$select=subject,body,bodyPreview,organizer,attendees,start,end,location
Prefer: outlook.timezone="Pacific Standard Time"
```
##### <a name="response"></a><span data-ttu-id="c89f6-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c89f6-173">Response</span></span>
<span data-ttu-id="c89f6-p113">Aquí tiene un ejemplo de la respuesta. Se devuelve la propiedad **body** en el formato HTML predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c89f6-p113">Here is an example of the response. The **body** property is returned in the default HTML format.</span></span>
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
