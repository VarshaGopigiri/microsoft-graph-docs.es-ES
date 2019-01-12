---
title: Obtener evento
description: Obtenga las propiedades y relaciones del objeto event especificado.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: c7dbada78ab4f8b345c0d125aad8a2844da175a0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980723"
---
# <a name="get-event"></a><span data-ttu-id="396b6-103">Obtener evento</span><span class="sxs-lookup"><span data-stu-id="396b6-103">Get event</span></span>

> <span data-ttu-id="396b6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="396b6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="396b6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="396b6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="396b6-106">Obtenga las propiedades y relaciones del objeto [event](../resources/event.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="396b6-106">Get the properties and relationships of the specified [event](../resources/event.md) object.</span></span>

<span data-ttu-id="396b6-107">Hay dos escenarios donde una aplicación puede obtener un evento en el calendario de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="396b6-107">There are two scenarios where an app can get an event in another user's calendar:</span></span>

* <span data-ttu-id="396b6-108">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="396b6-108">If the app has application permissions, or,</span></span>
* <span data-ttu-id="396b6-109">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido un calendario con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="396b6-109">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a calendar with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="396b6-110">Consulte los [Detalles y un ejemplo](/graph/outlook-get-shared-events-calendars).</span><span class="sxs-lookup"><span data-stu-id="396b6-110">See [details and an example](/graph/outlook-get-shared-events-calendars).</span></span>

<span data-ttu-id="396b6-111">Dado que el recurso **event** admite [extensiones](/graph/extensibility-overview), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia **event**.</span><span class="sxs-lookup"><span data-stu-id="396b6-111">Since the **event** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in an **event** instance.</span></span>


### <a name="support-various-time-zones"></a><span data-ttu-id="396b6-112">Compatibilidad con varias zonas horarias</span><span class="sxs-lookup"><span data-stu-id="396b6-112">Support various time zones</span></span>

<span data-ttu-id="396b6-113">Para todas las operaciones GET que devuelven eventos, puede usar el encabezado `Prefer: outlook.timezone` para especificar la zona horaria de las horas de inicio y finalización del evento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="396b6-113">For all GET operations that return events, you can use the `Prefer: outlook.timezone` header to specify the time zone for the event start and end times in the response.</span></span> 

<span data-ttu-id="396b6-114">Por ejemplo, el siguiente encabezado `Prefer: outlook.timezone` establece las horas de inicio y finalización en la respuesta en la hora estándar del Este.</span><span class="sxs-lookup"><span data-stu-id="396b6-114">For example, the following `Prefer: outlook.timezone` header sets the start and end times in the response to Eastern Standard Time.</span></span>
```http
Prefer: outlook.timezone="Eastern Standard Time"
```

<span data-ttu-id="396b6-p103">Si el evento se ha creado en una zona horaria diferente, las horas de inicio y finalización se ajustarán a la zona horaria especificada en ese encabezado `Prefer`. Consulte esta [lista](../resources/datetimetimezone.md) para ver los nombres de zona horaria admitidos. Si no se especifica el encabezado `Prefer: outlook.timezone`, se devuelven las horas de inicio y finalización en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="396b6-p103">If the event was created in a different time zone, the start and end times will be adjusted to the time zone specified in that `Prefer` header. See this [list](../resources/datetimetimezone.md) for the supported time zone names. If the `Prefer: outlook.timezone` header is not specified, the start and end times are returned in UTC.</span></span>

<span data-ttu-id="396b6-118">Puede usar las propiedades **OriginalStartTimeZone** y **OriginalEndTimeZone** del recurso **event** para averiguar la zona horaria usada al crear el evento.</span><span class="sxs-lookup"><span data-stu-id="396b6-118">You can use the **OriginalStartTimeZone** and **OriginalEndTimeZone** properties on the **event** resource to find out the time zone used when the event was created.</span></span>

## <a name="permissions"></a><span data-ttu-id="396b6-119">Permisos</span><span class="sxs-lookup"><span data-stu-id="396b6-119">Permissions</span></span>
<span data-ttu-id="396b6-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="396b6-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="396b6-122">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="396b6-122">Permission type</span></span>      | <span data-ttu-id="396b6-123">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="396b6-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="396b6-124">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="396b6-124">Delegated (work or school account)</span></span> | <span data-ttu-id="396b6-125">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="396b6-125">Calendars.Read</span></span>    |
|<span data-ttu-id="396b6-126">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="396b6-126">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="396b6-127">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="396b6-127">Calendars.Read</span></span>    |
|<span data-ttu-id="396b6-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="396b6-128">Application</span></span> | <span data-ttu-id="396b6-129">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="396b6-129">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="396b6-130">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="396b6-130">HTTP request</span></span>
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
## <a name="optional-query-parameters"></a><span data-ttu-id="396b6-131">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="396b6-131">Optional query parameters</span></span>
<span data-ttu-id="396b6-132">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="396b6-132">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="396b6-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="396b6-133">Request headers</span></span>
| <span data-ttu-id="396b6-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="396b6-134">Name</span></span>       | <span data-ttu-id="396b6-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="396b6-135">Type</span></span> | <span data-ttu-id="396b6-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="396b6-136">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="396b6-137">Autorización</span><span class="sxs-lookup"><span data-stu-id="396b6-137">Authorization</span></span>  | <span data-ttu-id="396b6-138">string</span><span class="sxs-lookup"><span data-stu-id="396b6-138">string</span></span>  | <span data-ttu-id="396b6-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="396b6-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="396b6-141">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="396b6-141">Prefer: outlook.timezone</span></span> | <span data-ttu-id="396b6-142">string</span><span class="sxs-lookup"><span data-stu-id="396b6-142">string</span></span> | <span data-ttu-id="396b6-143">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="396b6-143">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="396b6-144">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="396b6-144">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="396b6-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="396b6-145">Optional.</span></span> |
| <span data-ttu-id="396b6-146">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="396b6-146">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="396b6-147">string</span><span class="sxs-lookup"><span data-stu-id="396b6-147">string</span></span> | <span data-ttu-id="396b6-148">Formato de la propiedad **body** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="396b6-148">The format of the **body** property to be returned in.</span></span> <span data-ttu-id="396b6-149">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="396b6-149">Values can be "text" or "html".</span></span> <span data-ttu-id="396b6-150">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="396b6-150">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="396b6-151">Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="396b6-151">If the header is not specified, the **body** property is returned in HTML format.</span></span> <span data-ttu-id="396b6-152">Opcional.</span><span class="sxs-lookup"><span data-stu-id="396b6-152">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="396b6-153">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="396b6-153">Request body</span></span>
<span data-ttu-id="396b6-154">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="396b6-154">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="396b6-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="396b6-155">Response</span></span>

<span data-ttu-id="396b6-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="396b6-156">If successful, this method returns a `200 OK` response code and [event](../resources/event.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="396b6-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="396b6-157">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="396b6-158">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="396b6-158">Request 1</span></span>
<span data-ttu-id="396b6-p108">El primer ejemplo obtiene el evento especificado. Especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="396b6-p108">The first example gets the specified event. It specifies the following:</span></span>

- <span data-ttu-id="396b6-161">Un encabezado `Prefer: outlook.timezone` para obtener valores de fecha y hora devueltos en la hora estándar del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="396b6-161">A `Prefer: outlook.timezone` header to get date time values returned in Pacific Standard Time.</span></span> 
- <span data-ttu-id="396b6-p109">Un parámetro de consulta `$select` para devolver propiedades específicas. Sin ningún parámetro `$select`, se devolverán todas las propiedades de evento.</span><span class="sxs-lookup"><span data-stu-id="396b6-p109">A `$select` query parameter to return specific properties. Without a `$select` parameter, all of the event properties will be returned.</span></span>

<span data-ttu-id="396b6-164">La solicitud no especifica `Prefer: outlook.body-content-type` encabezado para indicar un formato específico para el cuerpo de evento devuelto.</span><span class="sxs-lookup"><span data-stu-id="396b6-164">The request does not specify any `Prefer: outlook.body-content-type` header to indicate a specific format for the returned event body.</span></span> 

<!-- {
  "blockType": "request",
  "name": "get_event"
}-->
```http
GET https://graph.microsoft.com/beta/me/events('AAMkAGIAAAoZDOFAAA=')?$select=subject,body,bodyPreview,organizer,attendees,start,end,location 
Prefer: outlook.timezone="Pacific Standard Time"
```
##### <a name="response-1"></a><span data-ttu-id="396b6-165">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="396b6-165">Response 1</span></span>
<span data-ttu-id="396b6-166">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="396b6-166">Here is an example of the response.</span></span> <span data-ttu-id="396b6-167">Debido a que no hay `Prefer: outlook.body-content-type` encabezado se ha especificado, se devuelve la propiedad **body** en el formato HTML de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="396b6-167">Because no `Prefer: outlook.body-content-type` header was specified, the **body** property is returned in the default HTML format.</span></span> 

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
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('cd209b0b-3f83-4c35-82d2-d88a61820480')/events(subject,body,bodyPreview,organizer,attendees,start,end,location)/$entity",
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

##### <a name="request-2"></a><span data-ttu-id="396b6-168">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="396b6-168">Request 2</span></span>
<span data-ttu-id="396b6-169">El segundo ejemplo muestra cómo usar un `Prefer: outlook.body-content-type="text"` encabezado para obtener la propiedad **body** del evento especificado en formato de texto.</span><span class="sxs-lookup"><span data-stu-id="396b6-169">The second example shows how to use a `Prefer: outlook.body-content-type="text"` header to get the **body** property of the specified event in text format.</span></span>

<span data-ttu-id="396b6-170">La solicitud también usa un `$select` parámetro para devolver propiedades específicas de la consulta.</span><span class="sxs-lookup"><span data-stu-id="396b6-170">The request also uses a `$select` query parameter to return specific properties.</span></span> <span data-ttu-id="396b6-171">Sin un `$select` parámetro, todas las propiedades de evento se devolverá.</span><span class="sxs-lookup"><span data-stu-id="396b6-171">Without a `$select` parameter, all of the event properties will be returned.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_event_in_text"
}-->
```http
GET https://graph.microsoft.com/beta/me/events('AAMkAGI1AAAoZDOFAAA=')?$select=subject,body,bodyPreview
Prefer: outlook.body-content-type="text"
```
##### <a name="response-2"></a><span data-ttu-id="396b6-172">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="396b6-172">Response 2</span></span>
<span data-ttu-id="396b6-173">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="396b6-173">Here is an example of the response.</span></span> <span data-ttu-id="396b6-174">La propiedad **body** se devuelve en formato de texto.</span><span class="sxs-lookup"><span data-stu-id="396b6-174">The **body** property is returned in text format.</span></span> 

<!-- {
  "blockType": "response",
  "name": "get_event_in_text",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Preference-Applied: outlook.body-content-type="text"
Content-length: 636

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('cd209b0b-3f83-4c35-82d2-d88a61820480')/events(subject,body,bodyPreview)/$entity",
    "@odata.etag":"W/\"ZlnW4RIAV06KYYwlrfNZvQAAKGWwbw==\"",
    "id":"AAMkAGI1AAAoZDOFAAA=",
    "subject":"Orientation ",
    "bodyPreview":"Dana, this is the time you selected for our orientation. Please bring the notes I sent you.",
    "body":{
        "contentType":"text",
        "content":"Dana, this is the time you selected for our orientation. Please bring the notes I sent you.\r\n"
    }
}
```


##### <a name="request-3"></a><span data-ttu-id="396b6-175">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="396b6-175">Request 3</span></span>

<span data-ttu-id="396b6-176">El tercer ejemplo muestra la obtención de un evento que especifica más de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="396b6-176">The third example shows getting an event that specifies more than one location.</span></span> <span data-ttu-id="396b6-177">La solicitud especifica un parámetro de consulta `$select` para devolver propiedades específicas.</span><span class="sxs-lookup"><span data-stu-id="396b6-177">The request specifies a `$select` query parameter to return specific properties.</span></span> 

<!-- {
  "blockType": "request",
  "name": "get_event_multiple_locations"
}-->
```http
GET https://graph.microsoft.com/beta/me/events('AAMkADAGAADDdm4NAAA=')?$select=subject,body,bodyPreview,organizer,attendees,start,end,location,locations
```
##### <a name="response-3"></a><span data-ttu-id="396b6-178">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="396b6-178">Response 3</span></span>
<span data-ttu-id="396b6-179">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="396b6-179">Here is an example of the response.</span></span> <span data-ttu-id="396b6-180">La propiedad **locations** incluye detalles de las tres ubicaciones en las que se organiza el evento.</span><span class="sxs-lookup"><span data-stu-id="396b6-180">The **locations** property includes details for the 3 locations that the event is organized for.</span></span> 

<span data-ttu-id="396b6-181">Debido a que la solicitud no especifica `Prefer: outlook.timezone` o `Prefer: outlook.body-content-type` las propiedades de encabezado, **start** y **end** se muestran en la zona de hora UTC de forma predeterminada, y el cuerpo está en el formato HTML predeterminado.</span><span class="sxs-lookup"><span data-stu-id="396b6-181">Because the request does not specify any `Prefer: outlook.timezone` or `Prefer: outlook.body-content-type` header, the **start** and **end** properties are displayed in the default UTC time zone, and the body is in the default HTML format.</span></span>  

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
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('d1a2fae9-db66-4cc9-8133-2184c77af1b8')/events(subject,body,bodyPreview,organizer,attendees,start,end,location,locations)/$entity",
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
        "type":"unknown",
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

## <a name="see-also"></a><span data-ttu-id="396b6-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="396b6-182">See also</span></span>

- [<span data-ttu-id="396b6-183">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="396b6-183">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="396b6-184">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="396b6-184">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="396b6-185">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="396b6-185">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
