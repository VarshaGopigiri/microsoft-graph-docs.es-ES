---
title: Obtener evento
description: Obtiene un objeto de evento.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: cab66a0df10ee46737065d232834c5a7b6fe6a50
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27930631"
---
# <a name="get-event"></a><span data-ttu-id="f382b-103">Obtener evento</span><span class="sxs-lookup"><span data-stu-id="f382b-103">Get event</span></span>

> <span data-ttu-id="f382b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f382b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f382b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f382b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f382b-106">Obtiene un objeto de [evento](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="f382b-106">Get an [event](../resources/event.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="f382b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f382b-107">Permissions</span></span>
<span data-ttu-id="f382b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f382b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f382b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f382b-110">Permission type</span></span>      | <span data-ttu-id="f382b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f382b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f382b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f382b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f382b-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f382b-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="f382b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f382b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f382b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f382b-115">Not supported.</span></span>    |
|<span data-ttu-id="f382b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f382b-116">Application</span></span> | <span data-ttu-id="f382b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f382b-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f382b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f382b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/events/{id}
GET /groups/{id}/calendar/events/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f382b-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f382b-119">Optional query parameters</span></span>
<span data-ttu-id="f382b-120">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f382b-120">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f382b-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f382b-121">Request headers</span></span>
| <span data-ttu-id="f382b-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="f382b-122">Name</span></span>       | <span data-ttu-id="f382b-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="f382b-123">Type</span></span> | <span data-ttu-id="f382b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="f382b-124">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="f382b-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="f382b-125">Authorization</span></span>  | <span data-ttu-id="f382b-126">string</span><span class="sxs-lookup"><span data-stu-id="f382b-126">string</span></span> | <span data-ttu-id="f382b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f382b-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="f382b-129">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="f382b-129">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="f382b-130">string</span><span class="sxs-lookup"><span data-stu-id="f382b-130">string</span></span> | <span data-ttu-id="f382b-131">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f382b-131">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="f382b-132">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="f382b-132">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="f382b-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f382b-133">Optional.</span></span> |
| <span data-ttu-id="f382b-134">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="f382b-134">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="f382b-135">string</span><span class="sxs-lookup"><span data-stu-id="f382b-135">string</span></span> | <span data-ttu-id="f382b-136">Formato de la propiedad **body** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="f382b-136">The format of the **body** property to be returned in.</span></span> <span data-ttu-id="f382b-137">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="f382b-137">Values can be "text" or "html".</span></span> <span data-ttu-id="f382b-138">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="f382b-138">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="f382b-139">Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="f382b-139">If the header is not specified, the **body** property is returned in HTML format.</span></span> <span data-ttu-id="f382b-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f382b-140">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f382b-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f382b-141">Request body</span></span>
<span data-ttu-id="f382b-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f382b-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f382b-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f382b-143">Response</span></span>
<span data-ttu-id="f382b-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto de [evento](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f382b-144">If successful, this method returns a `200 OK` response code and an [event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f382b-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f382b-145">Example</span></span>
#### <a name="request"></a><span data-ttu-id="f382b-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f382b-146">Request</span></span>
<span data-ttu-id="f382b-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f382b-147">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group_event"
}-->
```http
GET https://graph.microsoft.com/beta/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/events/AQMkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NwAzZWYARgAAA_b2VnUAiWNLj0xeSOs499YHAMT2RdsuOqRIlQZ4vOzp66YAAAIBDQAAAMT2RdsuOqRIlQZ4vOzp66YAAAIJOgAAAA==
```

#### <a name="response"></a><span data-ttu-id="f382b-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f382b-148">Response</span></span>
<span data-ttu-id="f382b-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f382b-149">The following is an example of the response.</span></span>
><span data-ttu-id="f382b-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f382b-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1728

{
    "id": "AQMkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NwAzZWYARgAAA_b2VnUAiWNLj0xeSOs499YHAMT2RdsuOqRIlQZ4vOzp66YAAAIBDQAAAMT2RdsuOqRIlQZ4vOzp66YAAAIJOgAAAA==",
    "createdDateTime": "2017-07-31T18:58:31.011909Z",
    "lastModifiedDateTime": "2017-07-31T18:58:35.418473Z",
    "changeKey": "xPZF2y46pEiVBni87OnrpgAAAAAJTg==",
    "categories": [],
    "originalStartTimeZone": "Eastern Standard Time",
    "originalEndTimeZone": "Eastern Standard Time",
    "uid": "040000008200E00074C5B7101A82E00800000000B23663002F0AD301000000000000000010000000B7C936D4C2FEC749824EE24B2FD7DA62",
    "reminderMinutesBeforeStart": 15,
    "isReminderOn": true,
    "hasAttachments": false,
    "subject": "Continuing Education Sync",
    "bodyPreview": "Higher Education Planning.\r\n\r\n\r\n\r\nJoin Microsoft Teams Online Meeting<https://teams.microsoft.com/l/meetup-join/19%3acc89e82c01e349d4998655891d93e12e%40thread.skype/1501527510806?tenantId=dcd219dd-bc68-4b9b-bf0b-4a33a796be35>",
    "importance": "normal",
    "sensitivity": "normal",
    "isAllDay": false,
    "isCancelled": false,
    "isOrganizer": true,
    "responseRequested": true,
    "seriesMasterId": null,
    "showAs": "busy",
    "type": "seriesMaster",
    "webLink": "https://outlook.office365.com/owa/?itemid=AQMkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NwAzZWYARgAAA%2Bb2VnUAiWNLj0xeSOs499YHAMT2RdsuOqRIlQZ4vOzp66YAAAIBDQAAAMT2RdsuOqRIlQZ4vOzp66YAAAIJOgAAAA%3D%3D&exvsurl=1&path=/calendar/item",
    "onlineMeetingUrl": null,
    "responseStatus": {
        "response": "organizer",
        "time": "0001-01-01T00:00:00Z"
    },
    "body": {
        "contentType": "html",
        "content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\n<div>Higher Education Planning.</div>\r\n<div><br>\r\n<br>\r\n<br>\r\n<a href=\"https://teams.microsoft.com/l/meetup-join/19%3acc89e82c01e349d4998655891d93e12e%40thread.skype/1501527510806?tenantId=dcd219dd-bc68-4b9b-bf0b-4a33a796be35\">Join Microsoft Teams Online Meeting</a></div>\r\n</body>\r\n</html>\r\n"
    },
    "start": {
        "dateTime": "2017-08-15T14:30:00.0000000",
        "timeZone": "UTC"
    },
    "end": {
        "dateTime": "2017-08-15T15:30:00.0000000",
        "timeZone": "UTC"
    },
    "location": {
        "displayName": "HR Taskforce / Benefits"
    },
    "recurrence": {
        "pattern": {
            "type": "weekly",
            "interval": 1,
            "month": 0,
            "dayOfMonth": 0,
            "daysOfWeek": [
                "tuesday",
                "thursday"
            ],
            "firstDayOfWeek": "sunday",
            "index": "first"
        },
        "range": {
            "type": "noEnd",
            "startDate": "2017-08-15",
            "endDate": "0001-01-01",
            "recurrenceTimeZone": "Eastern Standard Time",
            "numberOfOccurrences": 0
        }
    },
    "attendees": [
        {
            "type": "required",
            "status": {
                "response": "accepted",
                "time": "2017-07-31T18:58:34.3298022Z"
            },
            "emailAddress": {
                "name": "Lidia Holloway",
                "address": "LidiaH@contoso.com"
            }
        },
        {
            "type": "required",
            "status": {
                "response": "none",
                "time": "0001-01-01T00:00:00Z"
            },
            "emailAddress": {
                "name": "HR Taskforce",
                "address": "HRTaskforce@contoso.com"
            }
        },
        {
            "type": "required",
            "status": {
                "response": "none",
                "time": "0001-01-01T00:00:00Z"
            },
            "emailAddress": {
                "name": "Diego Siciliani",
                "address": "DiegoS@contoso.com"
            }
        },
        {
            "type": "required",
            "status": {
                "response": "none",
                "time": "0001-01-01T00:00:00Z"
            },
            "emailAddress": {
                "name": "Johanna Lorenz",
                "address": "JohannaL@contoso.com"
            }
        },
        {
            "type": "required",
            "status": {
                "response": "none",
                "time": "0001-01-01T00:00:00Z"
            },
            "emailAddress": {
                "name": "Megan Bowen",
                "address": "MeganB@contoso.com"
            }
        }
    ],
    "organizer": {
        "emailAddress": {
            "name": "HR Taskforce",
            "address": "HRTaskforce@contoso.com"
        }
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
