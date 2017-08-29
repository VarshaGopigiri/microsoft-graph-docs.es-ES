# <a name="get-event"></a><span data-ttu-id="2bb7e-101">Obtener evento</span><span class="sxs-lookup"><span data-stu-id="2bb7e-101">Get event</span></span>

<span data-ttu-id="2bb7e-102">Obtenga las propiedades y relaciones del objeto [event](../resources/event.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-102">Get the properties and relationships of the specified [event](../resources/event.md) object.</span></span>

<span data-ttu-id="2bb7e-103">Actualmente, esta operación devuelve los cuerpos de los eventos solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-103">Currently, this operation returns event bodies in only HTML format.</span></span>

<span data-ttu-id="2bb7e-104">Dado que el recurso **event** admite [extensiones](../../../concepts/extensibility_overview.md), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia **event**.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-104">Since the **event** resource supports [extensions](../../../concepts/extensibility_overview.md), you can also use the `GET` operation to get custom properties and extension data in an **event** instance.</span></span>

### <a name="support-various-time-zones"></a><span data-ttu-id="2bb7e-105">Compatibilidad con varias zonas horarias</span><span class="sxs-lookup"><span data-stu-id="2bb7e-105">Support various time zones</span></span>

<span data-ttu-id="2bb7e-106">Para todas las operaciones GET que devuelven eventos, puede usar el encabezado `Prefer: outlook.timezone` para especificar la zona horaria de las horas de inicio y finalización del evento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-106">For all GET operations that return events, you can use the `Prefer: outlook.timezone` header to specify the time zone for the event start and end times in the response.</span></span> 

<span data-ttu-id="2bb7e-107">Por ejemplo, el siguiente encabezado `Prefer: outlook.timezone` establece las horas de inicio y finalización en la respuesta en la hora estándar del Este.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-107">For example, the following `Prefer: outlook.timezone` header sets the start and end times in the response to Eastern Standard Time.</span></span>
```http
Prefer: outlook.timezone="Eastern Standard Time"
```

<span data-ttu-id="2bb7e-p101">Si el evento se ha creado en una zona horaria diferente, las horas de inicio y finalización se ajustarán a la zona horaria especificada en ese encabezado `Prefer`. Consulte esta [lista](../resources/datetimetimezone.md) para ver los nombres de zona horaria admitidos. Si no se especifica el encabezado `Prefer: outlook.timezone`, se devuelven las horas de inicio y finalización en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-p101">If the event was created in a different time zone, the start and end times will be adjusted to the time zone specified in that `Prefer` header. See this [list](../resources/datetimetimezone.md) for the supported time zone names. If the `Prefer: outlook.timezone` header is not specified, the start and end times are returned in UTC.</span></span>

<span data-ttu-id="2bb7e-111">Puede usar las propiedades **OriginalStartTimeZone** y **OriginalEndTimeZone** del recurso **event** para averiguar la zona horaria usada al crear el evento.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-111">You can use the **OriginalStartTimeZone** and **OriginalEndTimeZone** properties on the **event** resource to find out the time zone used when the event was created.</span></span>


## <a name="permissions"></a><span data-ttu-id="2bb7e-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="2bb7e-112">Permissions</span></span>
<span data-ttu-id="2bb7e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2bb7e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2bb7e-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2bb7e-115">Permission type</span></span>      | <span data-ttu-id="2bb7e-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2bb7e-116">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="2bb7e-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2bb7e-117">Delegated (work or school account)</span></span> | <span data-ttu-id="2bb7e-118">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="2bb7e-118">Calendars.Read</span></span>    | 
|<span data-ttu-id="2bb7e-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2bb7e-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2bb7e-120">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="2bb7e-120">Calendars.Read</span></span>    | 
|<span data-ttu-id="2bb7e-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2bb7e-121">Application</span></span> | <span data-ttu-id="2bb7e-122">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="2bb7e-122">Calendars.Read</span></span> | 

## <a name="http-request"></a><span data-ttu-id="2bb7e-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2bb7e-123">HTTP request</span></span>
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
## <a name="optional-query-parameters"></a><span data-ttu-id="2bb7e-124">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2bb7e-124">Optional query parameters</span></span>
<span data-ttu-id="2bb7e-125">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-125">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="2bb7e-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2bb7e-126">Request headers</span></span>
| <span data-ttu-id="2bb7e-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="2bb7e-127">Name</span></span>       | <span data-ttu-id="2bb7e-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="2bb7e-128">Type</span></span> | <span data-ttu-id="2bb7e-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bb7e-129">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="2bb7e-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="2bb7e-130">Authorization</span></span>  | <span data-ttu-id="2bb7e-131">string</span><span class="sxs-lookup"><span data-stu-id="2bb7e-131">string</span></span>  | <span data-ttu-id="2bb7e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2bb7e-134">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="2bb7e-134">Prefer: outlook.timezone</span></span> | <span data-ttu-id="2bb7e-135">string</span><span class="sxs-lookup"><span data-stu-id="2bb7e-135">string</span></span> | <span data-ttu-id="2bb7e-136">La zona horaria predeterminada para eventos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-136">The default time zone for events in the response.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2bb7e-137">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="2bb7e-137">Request body</span></span>
<span data-ttu-id="2bb7e-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2bb7e-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bb7e-139">Response</span></span>

<span data-ttu-id="2bb7e-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-140">If successful, this method returns a `200 OK` response code and [event](../resources/event.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2bb7e-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2bb7e-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2bb7e-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2bb7e-142">Request</span></span>
<span data-ttu-id="2bb7e-p104">El primer ejemplo obtiene el evento especificado. Especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2bb7e-p104">The first example gets the specified event. It specifies the following:</span></span>

- <span data-ttu-id="2bb7e-145">Un encabezado `Prefer: outlook.timezone` para obtener valores de fecha y hora devueltos en la hora estándar del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-145">A `Prefer: outlook.timezone` header to get date time values returned in Pacific Standard Time.</span></span> 
- <span data-ttu-id="2bb7e-p105">Un parámetro de consulta `$select` para devolver propiedades específicas. Sin ningún parámetro `$select`, se devolverán todas las propiedades de evento.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-p105">A `$select` query parameter to return specific properties. Without a `$select` parameter, all of the event properties will be returned.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_event"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/events('AAMkAGIAAAoZDOFAAA=')?$select=subject,body,bodyPreview,organizer,attendees,start,end,location 
Prefer: outlook.timezone="Pacific Standard Time"
```

##### <a name="response"></a><span data-ttu-id="2bb7e-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bb7e-148">Response</span></span>

<span data-ttu-id="2bb7e-p106">Aquí tiene un ejemplo de la respuesta. Se devuelve la propiedad **body** en el formato predeterminado de HTML.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-p106">Here is an example of the response. The **body** property is returned in the default format of HTML.</span></span>

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
```

## <a name="see-also"></a><span data-ttu-id="2bb7e-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2bb7e-151">See also</span></span>

- [<span data-ttu-id="2bb7e-152">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="2bb7e-152">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="2bb7e-153">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="2bb7e-153">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
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
