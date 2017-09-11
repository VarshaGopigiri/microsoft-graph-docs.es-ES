# <a name="create-event"></a><span data-ttu-id="b0071-101">Crear evento</span><span class="sxs-lookup"><span data-stu-id="b0071-101">Create Event</span></span>

<span data-ttu-id="b0071-102">Cree un [evento](../resources/event.md) en el calendario predeterminado del usuario o en un calendario especificado.</span><span class="sxs-lookup"><span data-stu-id="b0071-102">Create an [event](../resources/event.md) in the user's default calendar or specified calendar.</span></span>

<span data-ttu-id="b0071-103">Puede especificar la zona horaria de cada una de las horas de inicio y finalización del evento como parte de estos valores, ya que las propiedades **start** y **end** son del tipo [dateTimeTimeZone](../resources/datetimetimezone.md).</span><span class="sxs-lookup"><span data-stu-id="b0071-103">You can specify the time zone for each of the start and end times of the event as part of these values, as the **start** and **end** properties are of [dateTimeTimeZone](../resources/datetimetimezone.md) type.</span></span> 

<span data-ttu-id="b0071-104">Cuando se crea el evento, el servidor envía invitaciones a todos los asistentes.</span><span class="sxs-lookup"><span data-stu-id="b0071-104">When the event is created, the server send invitations to all attendees.</span></span>


## <a name="permissions"></a><span data-ttu-id="b0071-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b0071-105">Permissions</span></span>
<span data-ttu-id="b0071-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b0071-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b0071-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b0071-108">Permission type</span></span>      | <span data-ttu-id="b0071-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b0071-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b0071-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b0071-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b0071-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b0071-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="b0071-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b0071-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b0071-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b0071-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="b0071-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b0071-114">Application</span></span> | <span data-ttu-id="b0071-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b0071-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="b0071-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b0071-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events
POST /users/{id | userPrincipalName}/events

POST /me/calendar/events
POST /users/{id | userPrincipalName}/calendar/events

POST /me/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendars/{id}/events
```
## <a name="request-headers"></a><span data-ttu-id="b0071-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b0071-117">Request headers</span></span>
| <span data-ttu-id="b0071-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0071-118">Header</span></span>       | <span data-ttu-id="b0071-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b0071-119">Value</span></span> |
|:-----------|:------|
| <span data-ttu-id="b0071-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="b0071-120">Authorization</span></span>  | <span data-ttu-id="b0071-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b0071-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="b0071-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b0071-123">Content-Type</span></span>  | <span data-ttu-id="b0071-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b0071-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b0071-126">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="b0071-126">Request body</span></span>
<span data-ttu-id="b0071-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="b0071-127">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>

<span data-ttu-id="b0071-128">Dado que el recurso **event** admite [extensiones](../../../concepts/extensibility_overview.md), puede utilizar la operación `POST` y agregar propiedades personalizadas con sus propios datos al evento al crearla.</span><span class="sxs-lookup"><span data-stu-id="b0071-128">Since the **event** resource supports [extensions](../../../concepts/extensibility_overview.md), you can use the `POST` operation and add custom properties with your own data to the event while creating it.</span></span>

## <a name="response"></a><span data-ttu-id="b0071-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b0071-129">Response</span></span>

<span data-ttu-id="b0071-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b0071-130">If successful, this method returns `201, Created` response code and [event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b0071-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b0071-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b0071-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b0071-132">Request</span></span>
<span data-ttu-id="b0071-p104">Aquí tiene un ejemplo de la solicitud. Usa el encabezado de solicitud `Prefer: outlook.timezone` para especificar que las horas de **inicio** y **finalización** en la respuesta deben usar esa zona horaria.</span><span class="sxs-lookup"><span data-stu-id="b0071-p104">Here is an example of the request. It uses the `Prefer: outlook.timezone` request header to specify the **start** and **end** times in the response should use that time zone.</span></span>
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
<span data-ttu-id="b0071-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="b0071-135">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="b0071-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b0071-136">Response</span></span>
<span data-ttu-id="b0071-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b0071-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
## <a name="see-also"></a><span data-ttu-id="b0071-140">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b0071-140">See also</span></span>

- [<span data-ttu-id="b0071-141">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="b0071-141">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="b0071-142">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="b0071-142">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
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
