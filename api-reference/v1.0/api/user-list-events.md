---
title: List events
description: 'Para obtener una lista de objetos de eventos en el buzón del usuario. La lista contiene único '
localization_priority: Priority
ms.openlocfilehash: a4766528e8a8e9ee71075377bccc5dfbeaaa4c06
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852041"
---
# <a name="list-events"></a><span data-ttu-id="4dfe1-104">List events</span><span class="sxs-lookup"><span data-stu-id="4dfe1-104">List events</span></span>

<span data-ttu-id="4dfe1-p102">Obtiene una lista de objetos [event](../resources/event.md) en el buzón del usuario. La lista contiene patrones de serie y reuniones de instancia única.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-p102">Get a list of [event](../resources/event.md) objects in the user's mailbox. The list contains single instance meetings and series masters.</span></span>

<span data-ttu-id="4dfe1-107">Para obtener instancias de evento de expansión, puede [obtener la vista de calendario](calendar-list-calendarview.md) o bien [obtener las instancias de un evento](event-list-instances.md).</span><span class="sxs-lookup"><span data-stu-id="4dfe1-107">To get expanded event instances, you can [get the calendar view](calendar-list-calendarview.md), or [get the instances of an event](event-list-instances.md).</span></span>

<span data-ttu-id="4dfe1-108">Actualmente, esta operación devuelve los cuerpos de los eventos solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-108">Currently, this operation returns event bodies in only HTML format.</span></span>

<span data-ttu-id="4dfe1-109">Hay dos escenarios donde una aplicación puede obtener eventos de calendario de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="4dfe1-109">There are two scenarios where an app can get events in another user's calendar:</span></span>

* <span data-ttu-id="4dfe1-110">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="4dfe1-110">If the app has application permissions, or,</span></span>
* <span data-ttu-id="4dfe1-111">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido un calendario con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-111">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a calendar with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="4dfe1-112">Consulte los [Detalles y un ejemplo](/graph/outlook-get-shared-events-calendars).</span><span class="sxs-lookup"><span data-stu-id="4dfe1-112">See [details and an example](/graph/outlook-get-shared-events-calendars).</span></span>

### <a name="support-various-time-zones"></a><span data-ttu-id="4dfe1-113">Compatibilidad con varias zonas horarias</span><span class="sxs-lookup"><span data-stu-id="4dfe1-113">Support various time zones</span></span>

<span data-ttu-id="4dfe1-114">Para todas las operaciones GET que devuelven eventos, puede usar el encabezado `Prefer: outlook.timezone` para especificar la zona horaria de las horas de inicio y finalización del evento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-114">For all GET operations that return events, you can use the `Prefer: outlook.timezone` header to specify the time zone for the event start and end times in the response.</span></span> 

<span data-ttu-id="4dfe1-115">Por ejemplo, el siguiente encabezado `Prefer: outlook.timezone` establece las horas de inicio y finalización en la respuesta en la hora estándar del Este.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-115">For example, the following `Prefer: outlook.timezone` header sets the start and end times in the response to Eastern Standard Time.</span></span>
```http
Prefer: outlook.timezone="Eastern Standard Time"
```

<span data-ttu-id="4dfe1-p104">Si el evento se ha creado en una zona horaria diferente, las horas de inicio y finalización se ajustarán a la zona horaria especificada en ese encabezado `Prefer`. Consulte esta [lista](../resources/datetimetimezone.md) para ver los nombres de zona horaria admitidos. Si no se especifica el encabezado `Prefer: outlook.timezone`, se devuelven las horas de inicio y finalización en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-p104">If the event was created in a different time zone, the start and end times will be adjusted to the time zone specified in that `Prefer` header. See this [list](../resources/datetimetimezone.md) for the supported time zone names. If the `Prefer: outlook.timezone` header is not specified, the start and end times are returned in UTC.</span></span>

<span data-ttu-id="4dfe1-119">Puede usar las propiedades **OriginalStartTimeZone** y **OriginalEndTimeZone** del recurso **event** para averiguar la zona horaria usada al crear el evento.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-119">You can use the **OriginalStartTimeZone** and **OriginalEndTimeZone** properties on the **event** resource to find out the time zone used when the event was created.</span></span>

## <a name="permissions"></a><span data-ttu-id="4dfe1-120">Permisos</span><span class="sxs-lookup"><span data-stu-id="4dfe1-120">Permissions</span></span>
<span data-ttu-id="4dfe1-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4dfe1-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4dfe1-123">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4dfe1-123">Permission type</span></span>      | <span data-ttu-id="4dfe1-124">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4dfe1-124">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4dfe1-125">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4dfe1-125">Delegated (work or school account)</span></span> | <span data-ttu-id="4dfe1-126">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4dfe1-126">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="4dfe1-127">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4dfe1-127">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4dfe1-128">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4dfe1-128">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="4dfe1-129">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4dfe1-129">Application</span></span> | <span data-ttu-id="4dfe1-130">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4dfe1-130">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="4dfe1-131">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4dfe1-131">HTTP request</span></span>
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
## <a name="optional-query-parameters"></a><span data-ttu-id="4dfe1-132">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4dfe1-132">Optional query parameters</span></span>
<span data-ttu-id="4dfe1-133">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-133">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="4dfe1-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4dfe1-134">Request headers</span></span>
| <span data-ttu-id="4dfe1-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="4dfe1-135">Name</span></span>       | <span data-ttu-id="4dfe1-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="4dfe1-136">Type</span></span> | <span data-ttu-id="4dfe1-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="4dfe1-137">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="4dfe1-138">Autorización</span><span class="sxs-lookup"><span data-stu-id="4dfe1-138">Authorization</span></span>  | <span data-ttu-id="4dfe1-139">string</span><span class="sxs-lookup"><span data-stu-id="4dfe1-139">string</span></span> | <span data-ttu-id="4dfe1-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-p106">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="4dfe1-142">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="4dfe1-142">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="4dfe1-143">string</span><span class="sxs-lookup"><span data-stu-id="4dfe1-143">string</span></span> | <span data-ttu-id="4dfe1-144">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-144">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="4dfe1-145">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-145">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="4dfe1-146">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-146">Optional.</span></span> |
| <span data-ttu-id="4dfe1-147">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="4dfe1-147">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="4dfe1-148">string</span><span class="sxs-lookup"><span data-stu-id="4dfe1-148">string</span></span> | <span data-ttu-id="4dfe1-149">Formato de la propiedad **body** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-149">The format of the **body** property to be returned in.</span></span> <span data-ttu-id="4dfe1-150">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="4dfe1-150">Values can be "text" or "html".</span></span> <span data-ttu-id="4dfe1-151">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-151">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="4dfe1-152">Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-152">If the header is not specified, the **body** property is returned in HTML format.</span></span> <span data-ttu-id="4dfe1-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-153">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4dfe1-154">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4dfe1-154">Request body</span></span>
<span data-ttu-id="4dfe1-155">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-155">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4dfe1-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4dfe1-156">Response</span></span>

<span data-ttu-id="4dfe1-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-157">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4dfe1-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4dfe1-158">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4dfe1-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4dfe1-159">Request</span></span>
<span data-ttu-id="4dfe1-p109">Aquí tiene un ejemplo de la solicitud. Especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4dfe1-p109">Here is an example of the request. It specifies the following:</span></span>

- <span data-ttu-id="4dfe1-162">Un encabezado `Prefer: outlook.timezone` para obtener valores de fecha y hora devueltos en la hora estándar del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-162">A `Prefer: outlook.timezone` header to get date time values returned in Pacific Standard Time.</span></span> 
- <span data-ttu-id="4dfe1-p110">Un parámetro de consulta `$select` para devolver propiedades específicas. Sin ningún parámetro `$select`, se devolverán todas las propiedades de evento.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-p110">A `$select` query parameter to return specific properties. Without a `$select` parameter, all of the event properties will be returned.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_events"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events?$select=subject,body,bodyPreview,organizer,attendees,start,end,location
Prefer: outlook.timezone="Pacific Standard Time"
```
##### <a name="response"></a><span data-ttu-id="4dfe1-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4dfe1-165">Response</span></span>
<span data-ttu-id="4dfe1-p111">Aquí tiene un ejemplo de la respuesta. Se devuelve la propiedad **body** en el formato HTML predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4dfe1-p111">Here is an example of the response. The **body** property is returned in the default HTML format.</span></span>
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
