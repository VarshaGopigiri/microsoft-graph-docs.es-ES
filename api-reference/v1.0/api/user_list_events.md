# <a name="list-events"></a><span data-ttu-id="f5adb-101">List events</span><span class="sxs-lookup"><span data-stu-id="f5adb-101">List events</span></span>

<span data-ttu-id="f5adb-p101">Obtiene una lista de objetos [event](../resources/event.md) en el buzón del usuario. La lista contiene patrones de serie y reuniones de instancia única.</span><span class="sxs-lookup"><span data-stu-id="f5adb-p101">Get a list of [event](../resources/event.md) objects in the user's mailbox. The list contains single instance meetings and series masters.</span></span>

<span data-ttu-id="f5adb-104">Actualmente, esta operación devuelve los cuerpos de los eventos solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="f5adb-104">Currently, this operation returns event bodies in only HTML format.</span></span>

<span data-ttu-id="f5adb-105">Para obtener instancias de evento de expansión, puede [obtener la vista de calendario](calendar_list_calendarview.md) o bien [obtener las instancias de un evento](event_list_instances.md).</span><span class="sxs-lookup"><span data-stu-id="f5adb-105">To get expanded event instances, you can [get the calendar view](calendar_list_calendarview.md), or [get the instances of an event](event_list_instances.md).</span></span>


### <a name="get-events-in-another-users-calendar"></a><span data-ttu-id="f5adb-106">Obtener los eventos del calendario de otro usuario</span><span class="sxs-lookup"><span data-stu-id="f5adb-106">Get events in another user's calendar</span></span>

<span data-ttu-id="f5adb-107">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los eventos del calendario de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="f5adb-107">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get events from another user's calendar.</span></span> <span data-ttu-id="f5adb-108">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="f5adb-108">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="f5adb-109">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="f5adb-109">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="f5adb-110">Suponga que otro usuario, Garth, ha compartido un calendario con John.</span><span class="sxs-lookup"><span data-stu-id="f5adb-110">Suppose another user, Garth, has shared a calendar with John.</span></span> <span data-ttu-id="f5adb-111">Puede obtener los eventos de dicho calendario compartido especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="f5adb-111">You can get the events in that shared calendar by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/events
```

<span data-ttu-id="f5adb-112">Esta capacidad se aplica a todas las operaciones de eventos GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="f5adb-112">This capability applies to all the supported GET events operations for an individual user, as listed in the [HTTP request](#http-request) section below.</span></span> <span data-ttu-id="f5adb-113">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="f5adb-113">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="f5adb-114">Si Garth no ha compartido su calendario con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="f5adb-114">If Garth has not shared his calendar with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="f5adb-115">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener los eventos de los calendarios del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="f5adb-115">In such cases, specifying a user ID or user principal name only works for getting events in the signed-in user’s own calendars, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/events
```

<span data-ttu-id="f5adb-116">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="f5adb-116">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="f5adb-117">Carpetas de contactos compartidas</span><span class="sxs-lookup"><span data-stu-id="f5adb-117">Shared contact folders</span></span>
- <span data-ttu-id="f5adb-118">Calendarios compartidos</span><span class="sxs-lookup"><span data-stu-id="f5adb-118">Shared calendars</span></span>
- <span data-ttu-id="f5adb-119">Contactos y eventos en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="f5adb-119">Contacts and events in shared folders</span></span>
- <span data-ttu-id="f5adb-120">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="f5adb-120">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="f5adb-121">Esta capacidad no está disponible en otras operaciones de contactos, eventos y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="f5adb-121">This capability is not available in other operations for contacts, events, and their folders.</span></span>


### <a name="support-various-time-zones"></a><span data-ttu-id="f5adb-122">Compatibilidad con varias zonas horarias</span><span class="sxs-lookup"><span data-stu-id="f5adb-122">Support various time zones</span></span>

<span data-ttu-id="f5adb-123">Para todas las operaciones GET que devuelven eventos, puede usar el encabezado `Prefer: outlook.timezone` para especificar la zona horaria de las horas de inicio y finalización del evento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5adb-123">For all GET operations that return events, you can use the `Prefer: outlook.timezone` header to specify the time zone for the event start and end times in the response.</span></span> 

<span data-ttu-id="f5adb-124">Por ejemplo, el siguiente encabezado `Prefer: outlook.timezone` establece las horas de inicio y finalización en la respuesta en la hora estándar del Este.</span><span class="sxs-lookup"><span data-stu-id="f5adb-124">For example, the following `Prefer: outlook.timezone` header sets the start and end times in the response to Eastern Standard Time.</span></span>
```http
Prefer: outlook.timezone="Eastern Standard Time"
```

<span data-ttu-id="f5adb-p106">Si el evento se ha creado en una zona horaria diferente, las horas de inicio y finalización se ajustarán a la zona horaria especificada en ese encabezado `Prefer`. Consulte esta [lista](../resources/datetimetimezone.md) para ver los nombres de zona horaria admitidos. Si no se especifica el encabezado `Prefer: outlook.timezone`, se devuelven las horas de inicio y finalización en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="f5adb-p106">If the event was created in a different time zone, the start and end times will be adjusted to the time zone specified in that `Prefer` header. See this [list](../resources/datetimetimezone.md) for the supported time zone names. If the `Prefer: outlook.timezone` header is not specified, the start and end times are returned in UTC.</span></span>

<span data-ttu-id="f5adb-128">Puede usar las propiedades **OriginalStartTimeZone** y **OriginalEndTimeZone** del recurso **event** para averiguar la zona horaria usada al crear el evento.</span><span class="sxs-lookup"><span data-stu-id="f5adb-128">You can use the **OriginalStartTimeZone** and **OriginalEndTimeZone** properties on the **event** resource to find out the time zone used when the event was created.</span></span>

## <a name="permissions"></a><span data-ttu-id="f5adb-129">Permisos</span><span class="sxs-lookup"><span data-stu-id="f5adb-129">Permissions</span></span>
<span data-ttu-id="f5adb-p107">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f5adb-p107">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f5adb-132">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f5adb-132">Permission type</span></span>      | <span data-ttu-id="f5adb-133">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f5adb-133">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f5adb-134">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f5adb-134">Delegated (work or school account)</span></span> | <span data-ttu-id="f5adb-135">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5adb-135">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="f5adb-136">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f5adb-136">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f5adb-137">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5adb-137">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="f5adb-138">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f5adb-138">Application</span></span> | <span data-ttu-id="f5adb-139">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f5adb-139">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="f5adb-140">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f5adb-140">HTTP request</span></span>
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
## <a name="optional-query-parameters"></a><span data-ttu-id="f5adb-141">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f5adb-141">Optional query parameters</span></span>
<span data-ttu-id="f5adb-142">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5adb-142">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f5adb-143">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f5adb-143">Request headers</span></span>
| <span data-ttu-id="f5adb-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="f5adb-144">Name</span></span>       | <span data-ttu-id="f5adb-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5adb-145">Type</span></span> | <span data-ttu-id="f5adb-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5adb-146">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="f5adb-147">Authorization</span><span class="sxs-lookup"><span data-stu-id="f5adb-147">Authorization</span></span>  | <span data-ttu-id="f5adb-148">string</span><span class="sxs-lookup"><span data-stu-id="f5adb-148">string</span></span>  | <span data-ttu-id="f5adb-p108">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f5adb-p108">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f5adb-151">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="f5adb-151">Prefer: outlook.timezone</span></span> | <span data-ttu-id="f5adb-152">string</span><span class="sxs-lookup"><span data-stu-id="f5adb-152">string</span></span> | <span data-ttu-id="f5adb-p109">La zona horaria predeterminada para eventos en la respuesta. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f5adb-p109">The default time zone for events in the response. Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f5adb-155">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5adb-155">Request body</span></span>
<span data-ttu-id="f5adb-156">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f5adb-156">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f5adb-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5adb-157">Response</span></span>

<span data-ttu-id="f5adb-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5adb-158">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f5adb-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5adb-159">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f5adb-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f5adb-160">Request</span></span>
<span data-ttu-id="f5adb-p110">Aquí tiene un ejemplo de la solicitud. Especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f5adb-p110">Here is an example of the request. It specifies the following:</span></span>

- <span data-ttu-id="f5adb-163">Un encabezado `Prefer: outlook.timezone` para obtener valores de fecha y hora devueltos en la hora estándar del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="f5adb-163">A `Prefer: outlook.timezone` header to get date time values returned in Pacific Standard Time.</span></span> 
- <span data-ttu-id="f5adb-p111">Un parámetro de consulta `$select` para devolver propiedades específicas. Sin ningún parámetro `$select`, se devolverán todas las propiedades de evento.</span><span class="sxs-lookup"><span data-stu-id="f5adb-p111">A `$select` query parameter to return specific properties. Without a `$select` parameter, all of the event properties will be returned.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_events"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events?$select=subject,body,bodyPreview,organizer,attendees,start,end,location
Prefer: outlook.timezone="Pacific Standard Time"
```
##### <a name="response"></a><span data-ttu-id="f5adb-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5adb-166">Response</span></span>
<span data-ttu-id="f5adb-p112">Aquí tiene un ejemplo de la respuesta. Se devuelve la propiedad **body** en el formato HTML predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f5adb-p112">Here is an example of the response. The **body** property is returned in the default HTML format.</span></span>
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
