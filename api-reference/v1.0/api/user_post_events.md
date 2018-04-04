# <a name="create-event"></a><span data-ttu-id="b338a-101">Crear evento</span><span class="sxs-lookup"><span data-stu-id="b338a-101">Create Event</span></span>

<span data-ttu-id="b338a-102">Cree un [evento](../resources/event.md) en el calendario predeterminado del usuario o en un calendario especificado.</span><span class="sxs-lookup"><span data-stu-id="b338a-102">Create an [event](../resources/event.md) in the user's default calendar or specified calendar.</span></span>

<span data-ttu-id="b338a-103">Puede especificar la zona horaria de cada una de las horas de inicio y finalización del evento como parte de estos valores, ya que las propiedades **start** y **end** son del tipo [dateTimeTimeZone](../resources/datetimetimezone.md).</span><span class="sxs-lookup"><span data-stu-id="b338a-103">You can specify the time zone for each of the start and end times of the event as part of these values, as the **start** and **end** properties are of [dateTimeTimeZone](../resources/datetimetimezone.md) type.</span></span> 

<span data-ttu-id="b338a-104">Cuando se envía un evento, el servidor envía invitaciones a todos los asistentes.</span><span class="sxs-lookup"><span data-stu-id="b338a-104">When an event is sent, the server sends invitations to all the attendees.</span></span>

<span data-ttu-id="b338a-105">**Definir la ubicación de un evento**</span><span class="sxs-lookup"><span data-stu-id="b338a-105">**Setting the location in an event**</span></span>

<span data-ttu-id="b338a-106">Un administrador de Exchange puede configurar un buzón y una dirección de correo electrónico para un recurso, como una sala de reuniones, o equipamiento, como un proyector.</span><span class="sxs-lookup"><span data-stu-id="b338a-106">An Exchange administrator can set up a mailbox and an email address for a resource such as a meeting room, or equipment like a projector.</span></span> <span data-ttu-id="b338a-107">Los usuarios pueden luego invitar al recurso como asistente a una reunión.</span><span class="sxs-lookup"><span data-stu-id="b338a-107">Users can then invite the resource as an attendee to a meeting.</span></span> <span data-ttu-id="b338a-108">En nombre de recurso, el servidor acepta o rechaza la convocatoria de reunión en función de la programación de disponibilidad del recurso.</span><span class="sxs-lookup"><span data-stu-id="b338a-108">On behalf of the resource, the server accepts or rejects the meeting request based on the free/busy schedule of the resource.</span></span> <span data-ttu-id="b338a-109">Si el servidor acepta una reunión para el recurso, se crea un evento de la reunión en el calendario del recurso.</span><span class="sxs-lookup"><span data-stu-id="b338a-109">If the server accepts a meeting for the resource, it creates an event for the meeting in the resource's calendar.</span></span> <span data-ttu-id="b338a-110">Si se vuelve a programar la reunión, el servidor actualiza automáticamente el evento en el calendario del recurso.</span><span class="sxs-lookup"><span data-stu-id="b338a-110">If the meeting is rescheduled, the server automatically updates the event in the resource's calendar.</span></span>

<span data-ttu-id="b338a-111">Otra ventaja de configurar un buzón para un recurso es controlar la programación del recurso; por ejemplo, solo los ejecutivos o los delegados pueden reservar una sala de reuniones privadas.</span><span class="sxs-lookup"><span data-stu-id="b338a-111">Another advantage of setting up a mailbox for a resource is to control scheduling of the resource, for example, only executives or their delegates can book a private meeting room.</span></span>

<span data-ttu-id="b338a-112">Si se organiza un evento que implica una ubicación de la reunión:</span><span class="sxs-lookup"><span data-stu-id="b338a-112">If you're organizing an event that involves a meeting location:</span></span>

1. <span data-ttu-id="b338a-113">Configure la propiedad **location** del **evento** en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="b338a-113">Set the **location** property of the **event** accordingly.</span></span> 
2. <span data-ttu-id="b338a-114">Establezca la propiedad **locationEmailAddress** si la ubicación de la reunión tiene una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b338a-114">Set the optional **locationEmailAddress** property if the meeting location has an email address.</span></span>

<span data-ttu-id="b338a-115">Además, si la ubicación de la reunión se ha configurado como recurso o el evento implica equipos que se han configurado como recurso:</span><span class="sxs-lookup"><span data-stu-id="b338a-115">Additionally, if the meeting location has been set up as a resource, or if the event involves some equipment that has been set up as a resource:</span></span>

3. <span data-ttu-id="b338a-116">Invite al recurso como [asistente](../resources/attendee.md).</span><span class="sxs-lookup"><span data-stu-id="b338a-116">Invite the resource as an [attendee](../resources/attendee.md).</span></span>
4. <span data-ttu-id="b338a-117">Establezca la propiedad **type** como `resource`.</span><span class="sxs-lookup"><span data-stu-id="b338a-117">Set the attendee **type** property as `resource`.</span></span>
5. <span data-ttu-id="b338a-118">Establezca la **emailAddress** del asistente como dirección de correo electrónico del recurso.</span><span class="sxs-lookup"><span data-stu-id="b338a-118">Set the attendee **emailAddress** as the resource email address.</span></span>



## <a name="permissions"></a><span data-ttu-id="b338a-119">Permisos</span><span class="sxs-lookup"><span data-stu-id="b338a-119">Permissions</span></span>
<span data-ttu-id="b338a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b338a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b338a-122">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b338a-122">Permission type</span></span>      | <span data-ttu-id="b338a-123">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b338a-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b338a-124">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b338a-124">Delegated (work or school account)</span></span> | <span data-ttu-id="b338a-125">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b338a-125">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="b338a-126">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b338a-126">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b338a-127">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b338a-127">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="b338a-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b338a-128">Application</span></span> | <span data-ttu-id="b338a-129">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b338a-129">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="b338a-130">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b338a-130">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events
POST /users/{id | userPrincipalName}/events

POST /me/calendar/events
POST /users/{id | userPrincipalName}/calendar/events

POST /me/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendars/{id}/events
```
## <a name="request-headers"></a><span data-ttu-id="b338a-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b338a-131">Request headers</span></span>
| <span data-ttu-id="b338a-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b338a-132">Header</span></span>       | <span data-ttu-id="b338a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b338a-133">Value</span></span> |
|:-----------|:------|
| <span data-ttu-id="b338a-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="b338a-134">Authorization</span></span>  | <span data-ttu-id="b338a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b338a-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="b338a-137">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b338a-137">Content-Type</span></span>  | <span data-ttu-id="b338a-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b338a-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b338a-140">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="b338a-140">Request body</span></span>
<span data-ttu-id="b338a-141">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="b338a-141">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>

<span data-ttu-id="b338a-142">Dado que el recurso **event** admite [extensiones](../../../concepts/extensibility_overview.md), puede utilizar la operación `POST` y agregar propiedades personalizadas con sus propios datos al evento al crearla.</span><span class="sxs-lookup"><span data-stu-id="b338a-142">Since the **event** resource supports [extensions](../../../concepts/extensibility_overview.md), you can use the `POST` operation and add custom properties with your own data to the event while creating it.</span></span>

## <a name="response"></a><span data-ttu-id="b338a-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b338a-143">Response</span></span>

<span data-ttu-id="b338a-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b338a-144">If successful, this method returns `201 Created` response code and [event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b338a-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b338a-145">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="b338a-146">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="b338a-146">Request 1</span></span>
<span data-ttu-id="b338a-147">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b338a-147">Here is an example of the request.</span></span> <span data-ttu-id="b338a-148">Usa el encabezado de solicitud `Prefer: outlook.timezone` para especificar la zona horaria de las horas de **inicio** y **finalización** en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b338a-148">It uses the `Prefer: outlook.timezone` request header to specify the time zone for the **start** and **end** times in the response.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_event_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events
Prefer: outlook.timezone="Pacific Standard Time"
Content-type: application/json
Content-length: 600

{
  "subject": "Let's go for lunch",
  "body": {
    "contentType": "HTML",
    "content": "Does late morning work for you?"
  },
  "start": {
      "dateTime": "2017-04-15T12:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "end": {
      "dateTime": "2017-04-15T14:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "location":{
      "displayName":"Harry's Bar"
  },
  "attendees": [
    {
      "emailAddress": {
        "address":"samanthab@contoso.onmicrosoft.com",
        "name": "Samantha Booth"
      },
      "type": "required"
    }
  ]
}
```
<span data-ttu-id="b338a-149">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="b338a-149">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>
##### <a name="response-1"></a><span data-ttu-id="b338a-150">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="b338a-150">Response 1</span></span>
<span data-ttu-id="b338a-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b338a-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 2197

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('cd209b0b-3f83-4c35-82d2-d88a61820480')/events/$entity",
    "@odata.etag":"W/\"ZlnW4RIAV06KYYwlrfNZvQAALfZeRQ==\"",
    "id":"AAMkAGI1AAAt9AHjAAA=",
    "createdDateTime":"2017-04-15T03:00:50.7579581Z",
    "lastModifiedDateTime":"2017-04-15T03:00:51.245372Z",
    "changeKey":"ZlnW4RIAV06KYYwlrfNZvQAALfZeRQ==",
    "categories":[

    ],
    "originalStartTimeZone":"Pacific Standard Time",
    "originalEndTimeZone":"Pacific Standard Time",
    "iCalUId":"040000008200E00074C5B7101A82E00800000000DA2B357D94B5D201000000000000000010000000EC4597557F0CB34EA4CC2887EA7B17C3",
    "reminderMinutesBeforeStart":15,
    "isReminderOn":true,
    "hasAttachments":false,
    "subject":"Let's go brunch",
    "bodyPreview":"Does late morning work for you?",
    "importance":"normal",
    "sensitivity":"normal",
    "isAllDay":false,
    "isCancelled":false,
    "isOrganizer":true,
    "responseRequested":true,
    "seriesMasterId":null,
    "showAs":"busy",
    "type":"singleInstance",
    "webLink":"https://outlook.office365.com/owa/?itemid=AAMkAGI1AAAt9AHjAAA%3D&exvsurl=1&path=/calendar/item",
    "onlineMeetingUrl":null,
    "responseStatus":{
        "response":"organizer",
        "time":"0001-01-01T00:00:00Z"
    },
    "body":{
        "contentType":"html",
        "content":"<html><head></head><body>Does late morning work for you?</body></html>"
    },
    "start":{
        "dateTime":"2017-04-15T11:00:00.0000000",
        "timeZone":"Pacific Standard Time"
    },
    "end":{
        "dateTime":"2017-04-15T12:00:00.0000000",
        "timeZone":"Pacific Standard Time"
    },
    "location":{
        "displayName":"Harry's Bar"
    },
    "recurrence":null,
    "attendees":[
        {
            "type":"required",
            "status":{
                "response":"none",
                "time":"0001-01-01T00:00:00Z"
            },
            "emailAddress":{
                "name":"Samantha Booth",
                "address":"samanthab@contoso.onmicrosoft.com"
            }
        }
    ],
    "organizer":{
        "emailAddress":{
            "name":"Dana Swope",
            "address":"danas@contoso.onmicrosoft.com"
        }
    }
}
```

##### <a name="request-2"></a><span data-ttu-id="b338a-154">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="b338a-154">Request 2</span></span>
<span data-ttu-id="b338a-155">En el segundo ejemplo se muestra cómo crear un evento periódico.</span><span class="sxs-lookup"><span data-stu-id="b338a-155">The second example shows how to create a recurring event.</span></span> <span data-ttu-id="b338a-156">El evento se produce de las 10:00 a. m. a las 11:00 a. m., todos los lunes a partir del 4 de septiembre de 2017 hasta el final del año.</span><span class="sxs-lookup"><span data-stu-id="b338a-156">The event occurs from 10:00am to 11:00am, every Monday starting September 4, 2017, through the end of the year.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_event_recurring"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events
Content-type: application/json

{
  "subject": "Let's go for coffee",
  "body": {
    "contentType": "HTML",
    "content": "Does late morning work for you?"
  },
  "start": {
      "dateTime": "2017-09-04T10:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "end": {
      "dateTime": "2017-09-04T11:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "recurrence": {
    "pattern": {
      "type": "weekly",
      "interval": 1,
      "daysOfWeek": [ "Monday" ]
    },
    "range": {
      "type": "endDate",
      "startDate": "2017-09-04",
      "endDate": "2017-12-31"
    }
  },
  "location":{
      "displayName":"Harry's Bar"
  },
  "attendees": [
    {
      "emailAddress": {
        "address":"AdeleV@contoso.onmicrosoft.com",
        "name": "Adele Vance"
      },
      "type": "required"
    }
  ]
}
```
<span data-ttu-id="b338a-157">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="b338a-157">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>
##### <a name="response-2"></a><span data-ttu-id="b338a-158">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="b338a-158">Response 2</span></span>
<span data-ttu-id="b338a-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b338a-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "name": "create_event_recurring",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('919717da-0460-4cca-a6be-d25382429896')/events/$entity",
    "@odata.etag":"W/\"+T8RDneHMkKe2BGYEaQZ4wAA7WsvGQ==\"",
    "id":"AAMkADQwMDI5YT",
    "createdDateTime":"2017-10-14T07:37:39.0083072Z",
    "lastModifiedDateTime":"2017-10-14T07:37:40.0239406Z",
    "changeKey":"+T8RDneHMkKe2BGYEaQZ4wAA7WsvGQ==",
    "categories":[

    ],
    "originalStartTimeZone":"Pacific Standard Time",
    "originalEndTimeZone":"Pacific Standard Time",
    "iCalUId":"040000008200E00074C5B7101A82E008000000000068AD4FBF44D301000000000000000010000000CA802EEBDE19CB4AB552714F48C7EEFB",
    "reminderMinutesBeforeStart":15,
    "isReminderOn":true,
    "hasAttachments":false,
    "subject":"Let's go for coffee",
    "bodyPreview":"Does late morning work for you?",
    "importance":"normal",
    "sensitivity":"normal",
    "isAllDay":false,
    "isCancelled":false,
    "isOrganizer":true,
    "responseRequested":true,
    "seriesMasterId":null,
    "showAs":"busy",
    "type":"seriesMaster",
    "webLink":"https://outlook.office365.com/owa/?itemid=AAMkADQwMDI5YT&exvsurl=1&path=/calendar/item",
    "onlineMeetingUrl":null,
    "responseStatus":{
        "response":"organizer",
        "time":"0001-01-01T00:00:00Z"
    },
    "body":{
        "contentType":"html",
        "content":"<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<meta content=\"text/html; charset=us-ascii\">\r\n</head>\r\n<body>\r\nDoes late morning work for you?\r\n</body>\r\n</html>\r\n"
    },
    "start":{
        "dateTime":"2017-09-04T10:00:00.0000000",
        "timeZone":"Pacific Standard Time"
    },
    "end":{
        "dateTime":"2017-09-04T11:00:00.0000000",
        "timeZone":"Pacific Standard Time"
    },
    "location":{
        "displayName":"Harry's Bar"
    },
    "recurrence":{
        "pattern":{
            "type":"weekly",
            "interval":1,
            "month":0,
            "dayOfMonth":0,
            "daysOfWeek":[
                "monday"
            ],
            "firstDayOfWeek":"sunday",
            "index":"first"
        },
        "range":{
            "type":"endDate",
            "startDate":"2017-09-04",
            "endDate":"2017-12-31",
            "recurrenceTimeZone":"Pacific Standard Time",
            "numberOfOccurrences":0
        }
    },
    "attendees":[
        {
            "type":"required",
            "status":{
                "response":"none",
                "time":"0001-01-01T00:00:00Z"
            },
            "emailAddress":{
                "name":"Adele Vance",
                "address":"AdeleV@contoso.onmicrosoft.com"
            }
        }
    ],
    "organizer":{
        "emailAddress":{
            "name":"Alex Wilber",
            "address":"AlexW@contoso.onmicrosoft.com"
        }
    }
}
```


## <a name="see-also"></a><span data-ttu-id="b338a-162">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b338a-162">See also</span></span>

- [<span data-ttu-id="b338a-163">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="b338a-163">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="b338a-164">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="b338a-164">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
<!--
- [Add custom data to groups using schema extensions (preview)](../../../concepts/extensibility_schema_groups.md)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
