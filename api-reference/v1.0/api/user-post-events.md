---
title: Crear evento
description: Cree un evento en el calendario predeterminado del usuario o en un calendario especificado.
localization_priority: Priority
ms.openlocfilehash: 178891392d32e97bb8f3db85f9f32acc43a177a6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836473"
---
# <a name="create-event"></a><span data-ttu-id="5d3de-103">Crear evento</span><span class="sxs-lookup"><span data-stu-id="5d3de-103">Create Event</span></span>

<span data-ttu-id="5d3de-104">Cree un [evento](../resources/event.md) en el calendario predeterminado del usuario o en un calendario especificado.</span><span class="sxs-lookup"><span data-stu-id="5d3de-104">Create an [event](../resources/event.md) in the user's default calendar or specified calendar.</span></span>

<span data-ttu-id="5d3de-105">Puede especificar la zona horaria de cada una de las horas de inicio y finalización del evento como parte de estos valores, ya que las propiedades **start** y **end** son del tipo [dateTimeTimeZone](../resources/datetimetimezone.md).</span><span class="sxs-lookup"><span data-stu-id="5d3de-105">You can specify the time zone for each of the start and end times of the event as part of these values, as the **start** and **end** properties are of [dateTimeTimeZone](../resources/datetimetimezone.md) type.</span></span> 

<span data-ttu-id="5d3de-106">Cuando se envía un evento, el servidor envía invitaciones a todos los asistentes.</span><span class="sxs-lookup"><span data-stu-id="5d3de-106">When an event is sent, the server sends invitations to all the attendees.</span></span>

<span data-ttu-id="5d3de-107">**Definir la ubicación de un evento**</span><span class="sxs-lookup"><span data-stu-id="5d3de-107">**Setting the location in an event**</span></span>

<span data-ttu-id="5d3de-108">Un administrador de Exchange puede configurar un buzón y una dirección de correo electrónico para un recurso, como una sala de reuniones, o equipamiento, como un proyector.</span><span class="sxs-lookup"><span data-stu-id="5d3de-108">An Exchange administrator can set up a mailbox and an email address for a resource such as a meeting room, or equipment like a projector.</span></span> <span data-ttu-id="5d3de-109">Los usuarios pueden luego invitar al recurso como asistente a una reunión.</span><span class="sxs-lookup"><span data-stu-id="5d3de-109">Users can then invite the resource as an attendee to a meeting.</span></span> <span data-ttu-id="5d3de-110">En nombre de recurso, el servidor acepta o rechaza la convocatoria de reunión en función de la programación de disponibilidad del recurso.</span><span class="sxs-lookup"><span data-stu-id="5d3de-110">On behalf of the resource, the server accepts or rejects the meeting request based on the free/busy schedule of the resource.</span></span> <span data-ttu-id="5d3de-111">Si el servidor acepta una reunión para el recurso, se crea un evento de la reunión en el calendario del recurso.</span><span class="sxs-lookup"><span data-stu-id="5d3de-111">If the server accepts a meeting for the resource, it creates an event for the meeting in the resource's calendar.</span></span> <span data-ttu-id="5d3de-112">Si se vuelve a programar la reunión, el servidor actualiza automáticamente el evento en el calendario del recurso.</span><span class="sxs-lookup"><span data-stu-id="5d3de-112">If the meeting is rescheduled, the server automatically updates the event in the resource's calendar.</span></span>

<span data-ttu-id="5d3de-113">Otra ventaja de configurar un buzón para un recurso es controlar la programación del recurso; por ejemplo, solo los ejecutivos o los delegados pueden reservar una sala de reuniones privadas.</span><span class="sxs-lookup"><span data-stu-id="5d3de-113">Another advantage of setting up a mailbox for a resource is to control scheduling of the resource, for example, only executives or their delegates can book a private meeting room.</span></span>

<span data-ttu-id="5d3de-114">Si se organiza un evento que implica una ubicación de la reunión:</span><span class="sxs-lookup"><span data-stu-id="5d3de-114">If you're organizing an event that involves a meeting location:</span></span>

1. <span data-ttu-id="5d3de-115">Configure la propiedad **location** del **evento** en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="5d3de-115">Set the **location** property of the **event** accordingly.</span></span> 
2. <span data-ttu-id="5d3de-116">Establezca la propiedad **locationEmailAddress** si la ubicación de la reunión tiene una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5d3de-116">Set the optional **locationEmailAddress** property if the meeting location has an email address.</span></span>

<span data-ttu-id="5d3de-117">Además, si la ubicación de la reunión se ha configurado como recurso o el evento implica equipos que se han configurado como recurso:</span><span class="sxs-lookup"><span data-stu-id="5d3de-117">Additionally, if the meeting location has been set up as a resource, or if the event involves some equipment that has been set up as a resource:</span></span>

3. <span data-ttu-id="5d3de-118">Invite al recurso como [asistente](../resources/attendee.md).</span><span class="sxs-lookup"><span data-stu-id="5d3de-118">Invite the resource as an [attendee](../resources/attendee.md).</span></span>
4. <span data-ttu-id="5d3de-119">Establezca la propiedad **type** como `resource`.</span><span class="sxs-lookup"><span data-stu-id="5d3de-119">Set the attendee **type** property as `resource`.</span></span>
5. <span data-ttu-id="5d3de-120">Establezca la **emailAddress** del asistente como dirección de correo electrónico del recurso.</span><span class="sxs-lookup"><span data-stu-id="5d3de-120">Set the attendee **emailAddress** as the resource email address.</span></span>



## <a name="permissions"></a><span data-ttu-id="5d3de-121">Permisos</span><span class="sxs-lookup"><span data-stu-id="5d3de-121">Permissions</span></span>
<span data-ttu-id="5d3de-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5d3de-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5d3de-124">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5d3de-124">Permission type</span></span>      | <span data-ttu-id="5d3de-125">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5d3de-125">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5d3de-126">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5d3de-126">Delegated (work or school account)</span></span> | <span data-ttu-id="5d3de-127">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5d3de-127">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="5d3de-128">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5d3de-128">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5d3de-129">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5d3de-129">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="5d3de-130">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5d3de-130">Application</span></span> | <span data-ttu-id="5d3de-131">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5d3de-131">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="5d3de-132">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5d3de-132">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events
POST /users/{id | userPrincipalName}/events

POST /me/calendar/events
POST /users/{id | userPrincipalName}/calendar/events

POST /me/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendars/{id}/events
```
## <a name="request-headers"></a><span data-ttu-id="5d3de-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5d3de-133">Request headers</span></span>
| <span data-ttu-id="5d3de-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d3de-134">Header</span></span>       | <span data-ttu-id="5d3de-135">Valor</span><span class="sxs-lookup"><span data-stu-id="5d3de-135">Value</span></span> |
|:-----------|:------|
| <span data-ttu-id="5d3de-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="5d3de-136">Authorization</span></span>  | <span data-ttu-id="5d3de-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5d3de-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="5d3de-139">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5d3de-139">Content-Type</span></span>  | <span data-ttu-id="5d3de-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5d3de-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5d3de-142">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5d3de-142">Request body</span></span>
<span data-ttu-id="5d3de-143">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="5d3de-143">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>

<span data-ttu-id="5d3de-144">Dado que el recurso **event** admite [extensiones](/graph/extensibility-overview), puede utilizar la operación `POST` y agregar propiedades personalizadas con sus propios datos al evento al crearla.</span><span class="sxs-lookup"><span data-stu-id="5d3de-144">Since the **event** resource supports [extensions](/graph/extensibility-overview), you can use the `POST` operation and add custom properties with your own data to the event while creating it.</span></span>

## <a name="response"></a><span data-ttu-id="5d3de-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d3de-145">Response</span></span>

<span data-ttu-id="5d3de-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d3de-146">If successful, this method returns `201 Created` response code and [event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5d3de-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5d3de-147">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="5d3de-148">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="5d3de-148">Request 1</span></span>
<span data-ttu-id="5d3de-149">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d3de-149">Here is an example of the request.</span></span> <span data-ttu-id="5d3de-150">Usa el encabezado de solicitud `Prefer: outlook.timezone` para especificar la zona horaria de las horas de **inicio** y **finalización** en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d3de-150">It uses the `Prefer: outlook.timezone` request header to specify the time zone for the **start** and **end** times in the response.</span></span>
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
<span data-ttu-id="5d3de-151">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="5d3de-151">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>
##### <a name="response-1"></a><span data-ttu-id="5d3de-152">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="5d3de-152">Response 1</span></span>
<span data-ttu-id="5d3de-153">Este es un ejemplo de la respuesta, que muestra las propiedades **start** y **end** que usan la zona horaria especificada en el encabezado `Prefer: outlook.timezone`.</span><span class="sxs-lookup"><span data-stu-id="5d3de-153">Here is an example of the response, which shows the **start** and **end** properties use the time zone specified in the `Prefer: outlook.timezone` header.</span></span> <span data-ttu-id="5d3de-154">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="5d3de-154">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="5d3de-155">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5d3de-155">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "name": "create_event_from_user",
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
    "location": {
        "displayName": "Harry's Bar",
        "locationType": "default",
        "uniqueId": "Harry's Bar",
        "uniqueIdType": "private"
    },
    "locations": [
        {
            "displayName": "Harry's Bar",
            "locationType": "default",
            "uniqueIdType": "unknown"
        }
    ],
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


##### <a name="request-2"></a><span data-ttu-id="5d3de-156">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="5d3de-156">Request 2</span></span>
<span data-ttu-id="5d3de-157">En el siguiente ejemplo de solicitud se especifican tres ubicaciones en donde el organizador y los asistentes pueden asistir a la reunión.</span><span class="sxs-lookup"><span data-stu-id="5d3de-157">The next example request specifies 3 locations where the organizer and attendees can attend the meeting from.</span></span>

<span data-ttu-id="5d3de-158">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="5d3de-158">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_event_from_user_multiple_locations"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events
Prefer: outlook.timezone="Pacific Standard Time"
Content-type: application/json
Content-length: 1390

{
  "subject": "Plan summer company picnic",
  "body": {
    "contentType": "HTML",
    "content": "Let's kick-start this event planning!"
  },
  "start": {
      "dateTime": "2017-08-30T11:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "end": {
      "dateTime": "2017-08-30T12:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "attendees": [
    {
      "emailAddress": {
        "address": "DanaS@contoso.onmicrosoft.com",
        "name": "Dana Swope"
      },
      "type": "Required"
    },
    {
      "emailAddress": {
        "address": "AlexW@contoso.onmicrosoft.com",
        "name": "Alex Wilber"
      },
      "type": "Required"
    }
  ],
  "location": {
    "displayName": "Conf Room 3; Fourth Coffee; Home Office",
    "locationType": "Default"
  },
  "locations": [
    {
      "displayName": "Conf Room 3"
    },
    {
      "displayName": "Fourth Coffee",
      "address": {
        "street": "4567 Main St",
        "city": "Redmond",
        "state": "WA",
        "countryOrRegion": "US",
        "postalCode": "32008"
      },
      "coordinates": {
        "latitude": 47.672,
        "longitude": -102.103
      }
    },
    {
      "displayName": "Home Office"
    }
  ]

}
```

##### <a name="response-2"></a><span data-ttu-id="5d3de-159">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="5d3de-159">Response 2</span></span>
<span data-ttu-id="5d3de-160">La respuesta del ejemplo siguiente muestra el evento creado que especifica la información de las tres ubicaciones para la reunión.</span><span class="sxs-lookup"><span data-stu-id="5d3de-160">The following example response shows the created event that specifies information for the 3 locations for the meeting.</span></span> <span data-ttu-id="5d3de-161">Debido al encabezado de solicitud `Prefer: outlook.timezone="Pacific Standard Time"`, las propiedades **start** y **end** se expresan en el archivo PST.</span><span class="sxs-lookup"><span data-stu-id="5d3de-161">Because of the `Prefer: outlook.timezone="Pacific Standard Time"` request header, the **start** and **end** properties are expressed in PST.</span></span>
<span data-ttu-id="5d3de-162">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="5d3de-162">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="5d3de-163">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5d3de-163">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "name": "create_event_from_user_multiple_locations",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 2985

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('d1a2fae9-db66-4cc9-8133-2184c77af1b8')/events/$entity",
  "@odata.etag":"W/\"y53lbKh6jkaxHzFwGhgyxgAAw5zhug==\"",
  "id":"AAMkADAGAADDdm4NAAA=",
  "createdDateTime":"2017-08-30T07:06:33.8673345Z",
  "lastModifiedDateTime":"2017-08-30T07:06:34.5079772Z",
  "changeKey":"y53lbKh6jkaxHzFwGhgyxgAAz3IKMA==",
  "categories":[

  ],
  "originalStartTimeZone":"Pacific Standard Time",
  "originalEndTimeZone":"Pacific Standard Time",
  "iCalUId":"04000000820089190544",
  "reminderMinutesBeforeStart":15,
  "isReminderOn":true,
  "hasAttachments":false,
  "subject":"Plan summer company picnic",
  "bodyPreview":"Let's kick-start this event planning!",
  "importance":"normal",
  "sensitivity":"normal",
  "isAllDay":false,
  "isCancelled":false,
  "isOrganizer":true,
  "responseRequested":true,
  "seriesMasterId":null,
  "showAs":"busy",
  "type":"singleInstance",
  "webLink":"https://outlook.office365.com/owa/?itemid=AAMkADAGAADDdm4NAAA%3D&exvsurl=1&path=/calendar/item",
  "onlineMeetingUrl":null,
  "responseStatus":{
    "response":"organizer",
    "time":"0001-01-01T00:00:00Z"
  },
  "body":{
    "contentType":"html",
    "content":"<html>\r\n<head>\r\n</head>\r\n<body>\r\nLet's kick-start this event planning!\r\n</body>\r\n</html>\r\n"
  },
  "start":{
    "dateTime":"2017-08-30T11:00:00.0000000",
    "timeZone":"Pacific Standard Time"
  },
  "end":{
    "dateTime":"2017-08-30T12:00:00.0000000",
    "timeZone":"Pacific Standard Time"
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
  "recurrence":null,
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


##### <a name="request-3"></a><span data-ttu-id="5d3de-164">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="5d3de-164">Request 3</span></span>
<span data-ttu-id="5d3de-165">En el tercer ejemplo se muestra cómo crear un evento periódico.</span><span class="sxs-lookup"><span data-stu-id="5d3de-165">The third example shows how to create a recurring event.</span></span> <span data-ttu-id="5d3de-166">El evento se produce de las 12:00 a las 14:00, todos los lunes a partir del 4 de septiembre de 2017 hasta el final del año.</span><span class="sxs-lookup"><span data-stu-id="5d3de-166">The event occurs from 12:00pm to 2:00pm, every Monday starting September 4, 2017, through the end of the year.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_event_recurring"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events
Content-type: application/json

{
  "subject": "Let's go for lunch",
  "body": {
    "contentType": "HTML",
    "content": "Does noon time work for you?"
  },
  "start": {
      "dateTime": "2017-09-04T12:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "end": {
      "dateTime": "2017-09-04T14:00:00",
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
<span data-ttu-id="5d3de-167">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="5d3de-167">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>
##### <a name="response-3"></a><span data-ttu-id="5d3de-168">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="5d3de-168">Response 3</span></span>
<span data-ttu-id="5d3de-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5d3de-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.etag":"W/\"+T8RDneHMkKe2BGYEaQZ4wAA5a9Acw==\"",
    "id":"AAMkADQwMD",
    "createdDateTime":"2017-10-07T04:59:12.9698856Z",
    "lastModifiedDateTime":"2017-10-07T04:59:13.8136423Z",
    "changeKey":"+T8RDneHMkKe2BGYEaQZ4wAA5a9Acw==",
    "categories":[

    ],
    "originalStartTimeZone":"Pacific Standard Time",
    "originalEndTimeZone":"Pacific Standard Time",
    "iCalUId":"040000008200E00074C5B7101A82E0080000000028CEBE04293FD3010000000000000000100000009F85AB8AF8ED4D4FAC777FA89954BDB7",
    "reminderMinutesBeforeStart":15,
    "isReminderOn":true,
    "hasAttachments":false,
    "subject":"Let's go for lunch",
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
    "webLink":"https://outlook.office365.com/owa/?itemid=AAMkADQwMD&exvsurl=1&path=/calendar/item",
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
        "dateTime":"2017-09-04T12:00:00.0000000",
        "timeZone":"Pacific Standard Time"
    },
    "end":{
        "dateTime":"2017-09-04T14:00:00.0000000",
        "timeZone":"Pacific Standard Time"
    },
    "location":{
        "displayName":"Harry's Bar",
        "locationType":"default",
        "uniqueId":"Harry's Bar",
        "uniqueIdType":"private"
    },
    "locations":[
        {
            "displayName":"Harry's Bar",
            "locationType":"default",
            "uniqueIdType":"unknown"
        }
    ],
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
    },
    "OnlineMeeting":null
}
```


## <a name="see-also"></a><span data-ttu-id="5d3de-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d3de-172">See also</span></span>

- [<span data-ttu-id="5d3de-173">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="5d3de-173">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="5d3de-174">Agregar datos personalizados a los usuarios mediante extensiones abiertas</span><span class="sxs-lookup"><span data-stu-id="5d3de-174">Add custom data to users using open extensions</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="5d3de-175">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="5d3de-175">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
