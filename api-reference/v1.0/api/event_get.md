# <a name="get-event"></a><span data-ttu-id="e1459-101">Obtener evento</span><span class="sxs-lookup"><span data-stu-id="e1459-101">Get event</span></span>

<span data-ttu-id="e1459-102">Obtenga las propiedades y relaciones del objeto [event](../resources/event.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="e1459-102">Get the properties and relationships of the specified [event](../resources/event.md) object.</span></span>

<span data-ttu-id="e1459-103">Actualmente, esta operación devuelve los cuerpos de los eventos solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="e1459-103">Currently, this operation returns event bodies in only HTML format.</span></span>

<span data-ttu-id="e1459-104">Dado que el recurso **event** admite [extensiones](../../../concepts/extensibility_overview.md), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia **event**.</span><span class="sxs-lookup"><span data-stu-id="e1459-104">Since the **event** resource supports [extensions](../../../concepts/extensibility_overview.md), you can also use the `GET` operation to get custom properties and extension data in an **event** instance.</span></span>


### <a name="get-events-in-another-users-calendar"></a><span data-ttu-id="e1459-105">Obtener los eventos del calendario de otro usuario</span><span class="sxs-lookup"><span data-stu-id="e1459-105">Get events in another user's calendar</span></span>

<span data-ttu-id="e1459-106">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los eventos del calendario de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="e1459-106">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get events from another user's calendar.</span></span> <span data-ttu-id="e1459-107">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="e1459-107">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="e1459-108">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="e1459-108">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="e1459-109">Suponga que otro usuario, Garth, ha compartido un calendario con John.</span><span class="sxs-lookup"><span data-stu-id="e1459-109">Suppose another user, Garth, has shared a calendar with John.</span></span> <span data-ttu-id="e1459-110">Puede obtener un evento de dicho calendario compartido especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="e1459-110">You can get an event in that shared calendar by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/events/{id}
```

<span data-ttu-id="e1459-111">Esta capacidad se aplica a todas las operaciones de eventos GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="e1459-111">This capability applies to all the supported GET events operations for an individual user, as listed in the [HTTP request](#http-request) section below .</span></span> <span data-ttu-id="e1459-112">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="e1459-112">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="e1459-113">Si Garth no ha compartido su calendario con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="e1459-113">If Garth has not shared his calendar with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="e1459-114">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener un evento de los calendarios del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="e1459-114">In such cases, specifying a user ID or user principal name only works for getting an event in the signed-in user’s own calendars, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/events/{id}
```

<span data-ttu-id="e1459-115">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="e1459-115">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="e1459-116">Uso compartido de carpetas de contactos, calendarios y carpetas de mensajes</span><span class="sxs-lookup"><span data-stu-id="e1459-116">Shared contact folders, calendars, and message folders</span></span> 
- <span data-ttu-id="e1459-117">Contactos, eventos y mensajes en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="e1459-117">Contacts, events, and messages in shared folders</span></span>
- <span data-ttu-id="e1459-118">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="e1459-118">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="e1459-119">Esta capacidad no está disponible en otras operaciones de contactos, eventos, mensajes y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="e1459-119">This capability is not available in other operations for contacts, events, messages, and their folders.</span></span>


### <a name="support-various-time-zones"></a><span data-ttu-id="e1459-120">Compatibilidad con varias zonas horarias</span><span class="sxs-lookup"><span data-stu-id="e1459-120">Support various time zones</span></span>

<span data-ttu-id="e1459-121">Para todas las operaciones GET que devuelven eventos, puede usar el encabezado `Prefer: outlook.timezone` para especificar la zona horaria de las horas de inicio y finalización del evento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1459-121">For all GET operations that return events, you can use the `Prefer: outlook.timezone` header to specify the time zone for the event start and end times in the response.</span></span> 

<span data-ttu-id="e1459-122">Por ejemplo, el siguiente encabezado `Prefer: outlook.timezone` establece las horas de inicio y finalización en la respuesta en la hora estándar del Este.</span><span class="sxs-lookup"><span data-stu-id="e1459-122">For example, the following `Prefer: outlook.timezone` header sets the start and end times in the response to Eastern Standard Time.</span></span>
```http
Prefer: outlook.timezone="Eastern Standard Time"
```

<span data-ttu-id="e1459-p105">Si el evento se ha creado en una zona horaria diferente, las horas de inicio y finalización se ajustarán a la zona horaria especificada en ese encabezado `Prefer`. Consulte esta [lista](../resources/datetimetimezone.md) para ver los nombres de zona horaria admitidos. Si no se especifica el encabezado `Prefer: outlook.timezone`, se devuelven las horas de inicio y finalización en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="e1459-p105">If the event was created in a different time zone, the start and end times will be adjusted to the time zone specified in that `Prefer` header. See this [list](../resources/datetimetimezone.md) for the supported time zone names. If the `Prefer: outlook.timezone` header is not specified, the start and end times are returned in UTC.</span></span>

<span data-ttu-id="e1459-126">Puede usar las propiedades **OriginalStartTimeZone** y **OriginalEndTimeZone** del recurso **event** para averiguar la zona horaria usada al crear el evento.</span><span class="sxs-lookup"><span data-stu-id="e1459-126">You can use the **OriginalStartTimeZone** and **OriginalEndTimeZone** properties on the **event** resource to find out the time zone used when the event was created.</span></span>


## <a name="permissions"></a><span data-ttu-id="e1459-127">Permisos</span><span class="sxs-lookup"><span data-stu-id="e1459-127">Permissions</span></span>
<span data-ttu-id="e1459-p106">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e1459-p106">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e1459-130">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e1459-130">Permission type</span></span>      | <span data-ttu-id="e1459-131">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e1459-131">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e1459-132">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e1459-132">Delegated (work or school account)</span></span> | <span data-ttu-id="e1459-133">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="e1459-133">Calendars.Read</span></span>    |
|<span data-ttu-id="e1459-134">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e1459-134">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e1459-135">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="e1459-135">Calendars.Read</span></span>    |
|<span data-ttu-id="e1459-136">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e1459-136">Application</span></span> | <span data-ttu-id="e1459-137">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="e1459-137">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="e1459-138">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e1459-138">HTTP request</span></span>
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
## <a name="optional-query-parameters"></a><span data-ttu-id="e1459-139">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e1459-139">Optional query parameters</span></span>
<span data-ttu-id="e1459-140">Este método admite los [parámetros de consulta de OData]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1459-140">This method supports the [OData Query Parameters]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="e1459-141">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e1459-141">Request headers</span></span>
| <span data-ttu-id="e1459-142">Nombre</span><span class="sxs-lookup"><span data-stu-id="e1459-142">Name</span></span>       | <span data-ttu-id="e1459-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1459-143">Type</span></span> | <span data-ttu-id="e1459-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1459-144">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="e1459-145">Authorization</span><span class="sxs-lookup"><span data-stu-id="e1459-145">Authorization</span></span>  | <span data-ttu-id="e1459-146">string</span><span class="sxs-lookup"><span data-stu-id="e1459-146">string</span></span> | <span data-ttu-id="e1459-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e1459-p107">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="e1459-149">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="e1459-149">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="e1459-150">string</span><span class="sxs-lookup"><span data-stu-id="e1459-150">string</span></span> | <span data-ttu-id="e1459-151">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1459-151">outlook.timezone="Eastern Standard Time". Optional. Use this to specify the time zone for start and end times in the response. If not specified, the response are returned in UTC.</span></span> <span data-ttu-id="e1459-152">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="e1459-152">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="e1459-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e1459-153">Optional.</span></span> |
| <span data-ttu-id="e1459-154">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="e1459-154">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="e1459-155">string</span><span class="sxs-lookup"><span data-stu-id="e1459-155">string</span></span> | <span data-ttu-id="e1459-156">Formato de la propiedad **body** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="e1459-156">The format of the **body** property to be returned in.</span></span> <span data-ttu-id="e1459-157">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="e1459-157">Values can be "text" or "html".</span></span> <span data-ttu-id="e1459-158">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="e1459-158">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="e1459-159">Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="e1459-159">If the header is not specified, the **body** property is returned in HTML format.</span></span> <span data-ttu-id="e1459-160">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e1459-160">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e1459-161">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e1459-161">Request body</span></span>
<span data-ttu-id="e1459-162">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e1459-162">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e1459-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1459-163">Response</span></span>

<span data-ttu-id="e1459-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1459-164">If successful, this method returns a `200 OK` response code and [event](../resources/event.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e1459-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1459-165">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e1459-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e1459-166">Request</span></span>
<span data-ttu-id="e1459-p110">El primer ejemplo obtiene el evento especificado. Especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e1459-p110">The first example gets the specified event. It specifies the following:</span></span>

- <span data-ttu-id="e1459-169">Un encabezado `Prefer: outlook.timezone` para obtener valores de fecha y hora devueltos en la hora estándar del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="e1459-169">A `Prefer: outlook.timezone` header to get date time values returned in Pacific Standard Time.</span></span> 
- <span data-ttu-id="e1459-p111">Un parámetro de consulta `$select` para devolver propiedades específicas. Sin ningún parámetro `$select`, se devolverán todas las propiedades de evento.</span><span class="sxs-lookup"><span data-stu-id="e1459-p111">A `$select` query parameter to return specific properties. Without a `$select` parameter, all of the event properties will be returned.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_event"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/events('AAMkAGIAAAoZDOFAAA=')?$select=subject,body,bodyPreview,organizer,attendees,start,end,location 
Prefer: outlook.timezone="Pacific Standard Time"
```

##### <a name="response"></a><span data-ttu-id="e1459-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1459-172">Response</span></span>

<span data-ttu-id="e1459-p112">Aquí tiene un ejemplo de la respuesta. Se devuelve la propiedad **body** en el formato predeterminado de HTML.</span><span class="sxs-lookup"><span data-stu-id="e1459-p112">Here is an example of the response. The **body** property is returned in the default format of HTML.</span></span>

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
```

## <a name="see-also"></a><span data-ttu-id="e1459-175">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e1459-175">See also</span></span>

- [<span data-ttu-id="e1459-176">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="e1459-176">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="e1459-177">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="e1459-177">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
<!--
- [Add custom data to groups using schema extensions (preview)](../../../concepts/extensibility_schema_groups.md)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
