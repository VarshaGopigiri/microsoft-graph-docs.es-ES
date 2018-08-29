# <a name="get-event"></a><span data-ttu-id="cf873-101">Obtener evento</span><span class="sxs-lookup"><span data-stu-id="cf873-101">Get event</span></span>

<span data-ttu-id="cf873-102">Obtenga las propiedades y relaciones del objeto [event](../resources/event.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="cf873-102">Get the properties and relationships of the specified [event](../resources/event.md) object.</span></span>

<span data-ttu-id="cf873-103">Actualmente, esta operación devuelve los cuerpos de los eventos solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="cf873-103">Currently, this operation returns event bodies in only HTML format.</span></span>

<span data-ttu-id="cf873-104">Dado que el recurso **event** admite [extensiones](../../../concepts/extensibility_overview.md), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia **event**.</span><span class="sxs-lookup"><span data-stu-id="cf873-104">Since the **event** resource supports [extensions](../../../concepts/extensibility_overview.md), you can also use the `GET` operation to get custom properties and extension data in an **event** instance.</span></span>


### <a name="get-events-in-another-users-calendar"></a><span data-ttu-id="cf873-105">Obtener los eventos del calendario de otro usuario</span><span class="sxs-lookup"><span data-stu-id="cf873-105">Get events in another user's calendar</span></span>

<span data-ttu-id="cf873-106">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los eventos del calendario de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="cf873-106">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get events from another user's calendar.</span></span> <span data-ttu-id="cf873-107">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="cf873-107">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="cf873-108">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="cf873-108">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="cf873-109">Suponga que otro usuario, Garth, ha compartido un calendario con John.</span><span class="sxs-lookup"><span data-stu-id="cf873-109">Suppose another user, Garth, has shared a calendar with John.</span></span> <span data-ttu-id="cf873-110">Puede obtener un evento de dicho calendario compartido especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="cf873-110">You can get an event in that shared calendar by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/events/{id}
```

<span data-ttu-id="cf873-111">Esta capacidad se aplica a todas las operaciones de eventos GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="cf873-111">This capability applies to all the supported GET events operations for an individual user, as listed in the [HTTP request](#http-request) section below .</span></span> <span data-ttu-id="cf873-112">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="cf873-112">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="cf873-113">Si Garth no ha compartido su calendario con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="cf873-113">If Garth has not shared his calendar with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="cf873-114">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener un evento de los calendarios del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="cf873-114">In such cases, specifying a user ID or user principal name only works for getting an event in the signed-in user’s own calendars, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/events/{id}
```

<span data-ttu-id="cf873-115">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="cf873-115">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="cf873-116">Uso compartido de carpetas de contactos, calendarios y carpetas de mensajes</span><span class="sxs-lookup"><span data-stu-id="cf873-116">Shared contact folders, calendars, and message folders</span></span> 
- <span data-ttu-id="cf873-117">Contactos, eventos y mensajes en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="cf873-117">Contacts, events, and messages in shared folders</span></span>
- <span data-ttu-id="cf873-118">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="cf873-118">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="cf873-119">Esta capacidad no está disponible en otras operaciones de contactos, eventos, mensajes y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="cf873-119">This capability is not available in other operations for contacts, events, messages, and their folders.</span></span>


### <a name="support-various-time-zones"></a><span data-ttu-id="cf873-120">Compatibilidad con varias zonas horarias</span><span class="sxs-lookup"><span data-stu-id="cf873-120">Support various time zones</span></span>

<span data-ttu-id="cf873-121">Para todas las operaciones GET que devuelven eventos, puede usar el encabezado `Prefer: outlook.timezone` para especificar la zona horaria de las horas de inicio y finalización del evento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf873-121">For all GET operations that return events, you can use the `Prefer: outlook.timezone` header to specify the time zone for the event start and end times in the response.</span></span> 

<span data-ttu-id="cf873-122">Por ejemplo, el siguiente encabezado `Prefer: outlook.timezone` establece las horas de inicio y finalización en la respuesta en la hora estándar del Este.</span><span class="sxs-lookup"><span data-stu-id="cf873-122">For example, the following `Prefer: outlook.timezone` header sets the start and end times in the response to Eastern Standard Time.</span></span>
```http
Prefer: outlook.timezone="Eastern Standard Time"
```

<span data-ttu-id="cf873-p105">Si el evento se ha creado en una zona horaria diferente, las horas de inicio y finalización se ajustarán a la zona horaria especificada en ese encabezado `Prefer`. Consulte esta [lista](../resources/datetimetimezone.md) para ver los nombres de zona horaria admitidos. Si no se especifica el encabezado `Prefer: outlook.timezone`, se devuelven las horas de inicio y finalización en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="cf873-p105">If the event was created in a different time zone, the start and end times will be adjusted to the time zone specified in that `Prefer` header. See this [list](../resources/datetimetimezone.md) for the supported time zone names. If the `Prefer: outlook.timezone` header is not specified, the start and end times are returned in UTC.</span></span>

<span data-ttu-id="cf873-126">Puede usar las propiedades **OriginalStartTimeZone** y **OriginalEndTimeZone** del recurso **event** para averiguar la zona horaria usada al crear el evento.</span><span class="sxs-lookup"><span data-stu-id="cf873-126">You can use the **OriginalStartTimeZone** and **OriginalEndTimeZone** properties on the **event** resource to find out the time zone used when the event was created.</span></span>


## <a name="permissions"></a><span data-ttu-id="cf873-127">Permisos</span><span class="sxs-lookup"><span data-stu-id="cf873-127">Permissions</span></span>
<span data-ttu-id="cf873-p106">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cf873-p106">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="cf873-130">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cf873-130">Permission type</span></span>      | <span data-ttu-id="cf873-131">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cf873-131">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cf873-132">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cf873-132">Delegated (work or school account)</span></span> | <span data-ttu-id="cf873-133">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="cf873-133">Calendars.Read</span></span>    |
|<span data-ttu-id="cf873-134">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cf873-134">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cf873-135">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="cf873-135">Calendars.Read</span></span>    |
|<span data-ttu-id="cf873-136">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cf873-136">Application</span></span> | <span data-ttu-id="cf873-137">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="cf873-137">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="cf873-138">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cf873-138">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/events/{id}
GET /users/{id | userPrincipalName}/events/{id}
GET /groups/{id}/events/{id}

GET /me/calendar/events/{id}
GET /users/{id | userPrincipalName}/calendar/events/{id}
GET /groups/{id}/calendar/events/{id}

GET /me/calendars/{id}/events/{id}
GET /users/{id | userPrincipalName}/calendars/{id}/events/{id}

GET /me/calendargroup/calendars/{id}/events/{id}
GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}

GET /me/calendargroups/{id}/calendars/{id}/events/{id}
GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="cf873-139">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="cf873-139">Optional query parameters</span></span>
<span data-ttu-id="cf873-140">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf873-140">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="cf873-141">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf873-141">Request headers</span></span>
| <span data-ttu-id="cf873-142">Nombre</span><span class="sxs-lookup"><span data-stu-id="cf873-142">Name</span></span>       | <span data-ttu-id="cf873-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf873-143">Type</span></span> | <span data-ttu-id="cf873-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf873-144">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="cf873-145">Authorization</span><span class="sxs-lookup"><span data-stu-id="cf873-145">Authorization</span></span>  | <span data-ttu-id="cf873-146">cadena</span><span class="sxs-lookup"><span data-stu-id="cf873-146">string</span></span> | <span data-ttu-id="cf873-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cf873-p107">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="cf873-149">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="cf873-149">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="cf873-150">string</span><span class="sxs-lookup"><span data-stu-id="cf873-150">string</span></span> | <span data-ttu-id="cf873-151">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf873-151">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="cf873-152">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="cf873-152">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="cf873-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cf873-153">Optional.</span></span> |
| <span data-ttu-id="cf873-154">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="cf873-154">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="cf873-155">string</span><span class="sxs-lookup"><span data-stu-id="cf873-155">string</span></span> | <span data-ttu-id="cf873-156">Formato de la propiedad **body** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="cf873-156">The format of the **body** property to be returned in.</span></span> <span data-ttu-id="cf873-157">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="cf873-157">Values can be "text" or "html".</span></span> <span data-ttu-id="cf873-158">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="cf873-158">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="cf873-159">Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="cf873-159">If the header is not specified, the **body** property is returned in HTML format.</span></span> <span data-ttu-id="cf873-160">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cf873-160">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cf873-161">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cf873-161">Request body</span></span>
<span data-ttu-id="cf873-162">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cf873-162">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cf873-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf873-163">Response</span></span>

<span data-ttu-id="cf873-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf873-164">If successful, this method returns a `200 OK` response code and [event](../resources/event.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="cf873-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf873-165">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="cf873-166">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="cf873-166">Request 1</span></span>
<span data-ttu-id="cf873-p110">El primer ejemplo obtiene el evento especificado. Especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cf873-p110">The first example gets the specified event. It specifies the following:</span></span>

- <span data-ttu-id="cf873-169">Un encabezado `Prefer: outlook.timezone` para obtener valores de fecha y hora devueltos en la hora estándar del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="cf873-169">A `Prefer: outlook.timezone` header to get date time values returned in Pacific Standard Time.</span></span> 
- <span data-ttu-id="cf873-p111">Un parámetro de consulta `$select` para devolver propiedades específicas. Sin ningún parámetro `$select`, se devolverán todas las propiedades de evento.</span><span class="sxs-lookup"><span data-stu-id="cf873-p111">A `$select` query parameter to return specific properties. Without a `$select` parameter, all of the event properties will be returned.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkAGIAAAoZDOFAAA="],
  "name": "get_event"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/events/AAMkAGIAAAoZDOFAAA=?$select=subject,body,bodyPreview,organizer,attendees,start,end,location 
Prefer: outlook.timezone="Pacific Standard Time"
```

##### <a name="response-1"></a><span data-ttu-id="cf873-172">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="cf873-172">Response 1</span></span>

<span data-ttu-id="cf873-p112">Aquí tiene un ejemplo de la respuesta. Se devuelve la propiedad **body** en el formato predeterminado de HTML.</span><span class="sxs-lookup"><span data-stu-id="cf873-p112">Here is an example of the response. The **body** property is returned in the default format of HTML.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Preference-Applied: outlook.timezone="Pacific Standard Time"
Content-length: 1928

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('cd209b0b-3f83-4c35-82d2-d88a61820480')/events(subject,body,bodyPreview,organizer,attendees,start,end,location)/$entity",
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
```


##### <a name="request-2"></a><span data-ttu-id="cf873-175">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="cf873-175">Request 2</span></span>

<span data-ttu-id="cf873-176">En el segundo ejemplo se muestra la obtención de un evento que especifica más de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="cf873-176">The second example shows getting an event that specifies more than one location.</span></span> <span data-ttu-id="cf873-177">La solicitud especifica un parámetro de consulta `$select` para devolver propiedades específicas.</span><span class="sxs-lookup"><span data-stu-id="cf873-177">The request specifies a `$select` query parameter to return specific properties.</span></span> 

<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADAGAADDdm4NAAA="],
  "name": "get_event_multiple_locations"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events/AAMkADAGAADDdm4NAAA=?$select=subject,body,bodyPreview,organizer,attendees,start,end,location,locations
```
##### <a name="response-2"></a><span data-ttu-id="cf873-178">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="cf873-178">Response 2</span></span>
<span data-ttu-id="cf873-179">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf873-179">Here is an example of the response.</span></span> <span data-ttu-id="cf873-180">La propiedad **locations** incluye detalles de las tres ubicaciones en las que se organiza el evento.</span><span class="sxs-lookup"><span data-stu-id="cf873-180">The **locations** property includes details for the 3 locations that the event is organized for.</span></span> 

<span data-ttu-id="cf873-181">Dado que la solicitud no especifica ningún encabezado `Prefer: outlook.timezone`, las propiedades **start** y **end** se muestran en la zona horaria UTC predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cf873-181">Because the request does not specify any `Prefer: outlook.timezone` header, the **start** and **end** properties are displayed in the default UTC time zone.</span></span> 

<span data-ttu-id="cf873-182">El cuerpo del evento está en el formato HTML predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cf873-182">The event body is in the default HTML format.</span></span>  

<!-- {
  "blockType": "response",
  "name": "get_event_multiple_locations",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1992

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('d1a2fae9-db66-4cc9-8133-2184c77af1b8')/events(subject,body,bodyPreview,organizer,attendees,start,end,location,locations)/$entity",
  "@odata.etag":"W/\"y53lbKh6jkaxHzFwGhgyxgAAw5zhug==\"",
  "id":"AAMkADAGAADDdm4NAAA=",
  "subject":"Plan summer company picnic",
  "bodyPreview":"Let's kick-start this event planning!",
  "body":{
    "contentType":"html",
    "content":"<html>\r\n<head>\r\n</head>\r\n<body>\r\nLet's kick-start this event planning!\r\n</body>\r\n</html>\r\n"
  },
  "start":{
    "dateTime":"2017-08-30T11:00:00.0000000",
    "timeZone":"UTC"
  },
  "end":{
    "dateTime":"2017-08-30T12:00:00.0000000",
    "timeZone":"UTC"
  },
  "location":{
    "displayName":"Conf Room 3; Fourth Coffee; Home Office",
    "locationType":"default",
    "uniqueId":"Conf Room 3; Fourth Coffee; Home Office",
    "uniqueIdType":"private"
  },
  "locations":[
    {
      "displayName":"Conf Room 3",
      "locationType":"default",
      "uniqueIdType":"unknown"
    },
    {
      "displayName":"Fourth Coffee",
      "locationType":"default",
      "uniqueId":"Fourth Coffee",
      "uniqueIdType":"private",
      "address":{
        "street":"4567 Main St",
        "city":"Redmond",
        "state":"WA",
        "countryOrRegion":"US",
        "postalCode":"32008"
      },
      "coordinates":{
        "latitude":47.672,
        "longitude":-102.103
      }
    },
    {
      "displayName":"Home Office",
      "locationType":"default",
      "uniqueIdType":"unknown"
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
        "name":"Dana Swope",
        "address":"DanaS@contoso.onmicrosoft.com"
      }
    },
    {
      "type":"required",
      "status":{
        "response":"none",
        "time":"0001-01-01T00:00:00Z"
      },
      "emailAddress":{
        "name":"Alex Wilber",
        "address":"AlexW@contoso.onmicrosoft.com"
      }
    }
  ],
  "organizer":{
    "emailAddress":{
      "name":"Adele Vance",
      "address":"AdeleV@contoso.onmicrosoft.com"
    }
  }
}
```



## <a name="see-also"></a><span data-ttu-id="cf873-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf873-183">See also</span></span>

- [<span data-ttu-id="cf873-184">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="cf873-184">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="cf873-185">Agregar datos personalizados a los usuarios mediante extensiones abiertas</span><span class="sxs-lookup"><span data-stu-id="cf873-185">Add custom data to users using open extensions</span></span>](../../../concepts/extensibility_open_users.md)
- [<span data-ttu-id="cf873-186">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="cf873-186">Add custom data to groups using schema extensions</span></span>](../../../concepts/extensibility_schema_groups.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
