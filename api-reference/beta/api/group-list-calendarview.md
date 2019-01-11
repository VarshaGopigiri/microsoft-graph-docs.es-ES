---
title: List calendarView
description: Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado de un grupo.
localization_priority: Normal
ms.openlocfilehash: 651484045823c3c189d2c4b5a6ee9f3c19815e06
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843501"
---
# <a name="list-calendarview"></a><span data-ttu-id="2ca00-103">List calendarView</span><span class="sxs-lookup"><span data-stu-id="2ca00-103">List calendarView</span></span>

> <span data-ttu-id="2ca00-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2ca00-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2ca00-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2ca00-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2ca00-106">Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado de un grupo.</span><span class="sxs-lookup"><span data-stu-id="2ca00-106">Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the default calendar of a group.</span></span>

## <a name="permissions"></a><span data-ttu-id="2ca00-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2ca00-107">Permissions</span></span>
<span data-ttu-id="2ca00-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2ca00-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2ca00-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2ca00-110">Permission type</span></span>      | <span data-ttu-id="2ca00-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2ca00-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2ca00-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2ca00-112">Delegated (work or school account)</span></span> | <span data-ttu-id="2ca00-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2ca00-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="2ca00-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2ca00-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2ca00-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2ca00-115">Not supported.</span></span>    |
|<span data-ttu-id="2ca00-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2ca00-116">Application</span></span> | <span data-ttu-id="2ca00-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2ca00-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2ca00-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2ca00-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

## <a name="query-parameters"></a><span data-ttu-id="2ca00-119">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="2ca00-119">Query parameters</span></span>
<span data-ttu-id="2ca00-120">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="2ca00-120">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="2ca00-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2ca00-121">Parameter</span></span>    | <span data-ttu-id="2ca00-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ca00-122">Type</span></span>   |<span data-ttu-id="2ca00-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ca00-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2ca00-124">startDateTime</span><span class="sxs-lookup"><span data-stu-id="2ca00-124">startDateTime</span></span>|<span data-ttu-id="2ca00-125">String</span><span class="sxs-lookup"><span data-stu-id="2ca00-125">String</span></span>|<span data-ttu-id="2ca00-p103">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="2ca00-p103">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="2ca00-128">endDateTime</span><span class="sxs-lookup"><span data-stu-id="2ca00-128">endDateTime</span></span>|<span data-ttu-id="2ca00-129">String</span><span class="sxs-lookup"><span data-stu-id="2ca00-129">String</span></span>|<span data-ttu-id="2ca00-p104">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="2ca00-p104">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="2ca00-132">Este método también admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ca00-132">This method also supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2ca00-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2ca00-133">Request headers</span></span>
| <span data-ttu-id="2ca00-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ca00-134">Name</span></span>       | <span data-ttu-id="2ca00-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ca00-135">Type</span></span> | <span data-ttu-id="2ca00-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ca00-136">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="2ca00-137">Autorización</span><span class="sxs-lookup"><span data-stu-id="2ca00-137">Authorization</span></span>  | <span data-ttu-id="2ca00-138">string</span><span class="sxs-lookup"><span data-stu-id="2ca00-138">string</span></span> | <span data-ttu-id="2ca00-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2ca00-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="2ca00-141">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="2ca00-141">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="2ca00-142">string</span><span class="sxs-lookup"><span data-stu-id="2ca00-142">string</span></span> | <span data-ttu-id="2ca00-143">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ca00-143">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="2ca00-144">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="2ca00-144">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="2ca00-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2ca00-145">Optional.</span></span> |
| <span data-ttu-id="2ca00-146">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="2ca00-146">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="2ca00-147">string</span><span class="sxs-lookup"><span data-stu-id="2ca00-147">string</span></span> | <span data-ttu-id="2ca00-148">Formato de la propiedad **body** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="2ca00-148">The format of the **body** property to be returned in.</span></span> <span data-ttu-id="2ca00-149">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="2ca00-149">Values can be "text" or "html".</span></span> <span data-ttu-id="2ca00-150">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="2ca00-150">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="2ca00-151">Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="2ca00-151">If the header is not specified, the **body** property is returned in HTML format.</span></span> <span data-ttu-id="2ca00-152">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2ca00-152">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2ca00-153">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2ca00-153">Request body</span></span>
<span data-ttu-id="2ca00-154">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2ca00-154">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2ca00-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ca00-155">Response</span></span>
<span data-ttu-id="2ca00-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ca00-156">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2ca00-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2ca00-157">Example</span></span>
#### <a name="request"></a><span data-ttu-id="2ca00-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ca00-158">Request</span></span>
<span data-ttu-id="2ca00-159">En el ejemplo siguiente, se solicita la devolución de cuerpos de evento en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="2ca00-159">The following example requests event bodies to be returned in text format.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendarviews"
}-->
```http
GET https://graph.microsoft.com/beta/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/calendarView?startDateTime=2017-01-01T19:00:00.0000000&endDateTime=2017-10-01T19:00:00.00
Prefer: outlook.body-content-type="text"
```

#### <a name="response"></a><span data-ttu-id="2ca00-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ca00-160">Response</span></span>
<span data-ttu-id="2ca00-161">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ca00-161">The following is an example of the response.</span></span>
><span data-ttu-id="2ca00-162">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="2ca00-162">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="2ca00-163">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2ca00-163">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1354
Preference-Applied: outlook.body-content-type="text"

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#groups('02bd9fd6-8f93-4758-87c3-1fb73740a315')/calendarView",
    "@odata.nextLink":"https://graph.microsoft.com/beta/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/calendarView?startDateTime=2017-01-01T19%3a00%3a00.0000000&endDateTime=2017-10-01T19%3a00%3a00.00&$skip=10",
    "value":[
        {
            "@odata.etag":"W/\"xPZF2y46pEiVBni87OnrpgAAFq78Xw==\"",
            "id":"AAMkAGI5MWYJOwAAEA==",
            "createdDateTime":"2017-07-31T18:59:01.982289Z",
            "lastModifiedDateTime":"2017-09-06T04:29:38.6647687Z",
            "changeKey":"xPZF2y46pEiVBni87OnrpgAAFq78Xw==",
            "categories":[

            ],
            "originalStartTimeZone":"Eastern Standard Time",
            "originalEndTimeZone":"Eastern Standard Time",
            "uid":"040000008200E00074C5B7101A82E00807E1080E824DDB122F0AD301000000000000000010000000824A8905B038D54AA7735F117B3442ED",
            "reminderMinutesBeforeStart":15,
            "isReminderOn":true,
            "hasAttachments":false,
            "subject":"New Training Plans",
            "bodyPreview":"Meeting to plan new trainings.\r\n\r\n\r\n\r\nJoin Microsoft Teams Online Meeting<https://teams.microsoft.com/l/meetup-join/19%3a900876baa3134907b0dcb41a0d220e31%40thread.skype/1501527539926?tenantId=dcd219dd-bc68-4b9b-bf0b-4a33a796be35>",
            "importance":"normal",
            "sensitivity":"normal",
            "isAllDay":false,
            "isCancelled":false,
            "isOrganizer":true,
            "responseRequested":true,
            "seriesMasterId":null,
            "showAs":"busy",
            "type":"singleInstance",
            "webLink":"https://outlook.office365.com/owa/?itemid=AAMkAGI5MWYJOwAAEA%3D%3D&exvsurl=1&path=/calendar/item",
            "onlineMeetingUrl":null,
            "responseStatus":{
                "response":"organizer",
                "time":"0001-01-01T00:00:00Z"
            },
            "body":{
                "contentType":"text",
                "content":"Meeting to plan new trainings.\r\n\r\n\r\n\r\nJoin Microsoft Teams Online Meeting<https://teams.microsoft.com/l/meetup-join/19%3a900876baa3134907b0dcb41a0d220e31%40thread.skype/1501527539926?tenantId=dcd219dd-bc68-4b9b-bf0b-4a33a796be35>\r\n"
            },
            "start":{
                "dateTime":"2017-08-14T21:00:00.0000000",
                "timeZone":"UTC"
            },
            "end":{
                "dateTime":"2017-08-14T22:00:00.0000000",
                "timeZone":"UTC"
            },
            "location":{
                "displayName":"HR Taskforce / Facilities"
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
                        "name":"HR Taskforce",
                        "address":"HRTaskforce@contoso.onmicrosoft.com"
                    }
                },
                {
                    "type":"required",
                    "status":{
                        "response":"none",
                        "time":"0001-01-01T00:00:00Z"
                    },
                    "emailAddress":{
                        "name":"Megan Bowen",
                        "address":"MeganB@contoso.onmicrosoft.com"
                    }
                }
             ],
            "organizer":{
                "emailAddress":{
                    "name":"HR Taskforce",
                    "address":"HRTaskforce@contoso.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.etag":"W/\"xPZF2y46pEiVBni87OnrpgAAFq78Xw==\"",
            "id":"AAMkAGI5MWYJOwAAEA==",
            "createdDateTime":"2017-07-31T18:59:01.982289Z",
            "lastModifiedDateTime":"2017-09-06T04:29:38.6647687Z",
            "changeKey":"xPZF2y46pEiVBni87OnrpgAAFq78Xw==",
            "categories":[

            ],
            "originalStartTimeZone":"Eastern Standard Time",
            "originalEndTimeZone":"Eastern Standard Time",
            "uid":"040000008200E00074C5B7101A82E00807E10810824DDB122F0AD301000000000000000010000000824A8905B038D54AA7735F117B3442ED",
            "reminderMinutesBeforeStart":15,
            "isReminderOn":true,
            "hasAttachments":false,
            "subject":"New Training Plans",
            "bodyPreview":"Follow-up meeting to plan new trainings.\r\n\r\n\r\n\r\nJoin Microsoft Teams Online Meeting<https://teams.microsoft.com/l/meetup-join/19%3a900876baa3134907b0dcb41a0d220e31%40thread.skype/1501527539926?tenantId=dcd219dd-bc68-4b9b-bf0b-4a33a796be35>",
            "importance":"normal",
            "sensitivity":"normal",
            "isAllDay":false,
            "isCancelled":false,
            "isOrganizer":true,
            "responseRequested":true,
            "seriesMasterId":null,
            "showAs":"busy",
            "type":"singleInstance",
            "webLink":"https://outlook.office365.com/owa/?itemid=AAMkAGI5MWYJOwAAEA%3D%3D&exvsurl=1&path=/calendar/item",
            "onlineMeetingUrl":null,
            "responseStatus":{
                "response":"organizer",
                "time":"0001-01-01T00:00:00Z"
            },
            "body":{
                "contentType":"text",
                "content":"Meeting to plan new trainings.\r\n\r\n\r\n\r\nJoin Microsoft Teams Online Meeting<https://teams.microsoft.com/l/meetup-join/19%3a900876baa3134907b0dcb41a0d220e31%40thread.skype/1501527539926?tenantId=dcd219dd-bc68-4b9b-bf0b-4a33a796be35>\r\n"
            },
            "start":{
                "dateTime":"2017-08-16T21:00:00.0000000",
                "timeZone":"UTC"
            },
            "end":{
                "dateTime":"2017-08-16T22:00:00.0000000",
                "timeZone":"UTC"
            },
            "location":{
                "displayName":"HR Taskforce / Facilities"
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
                        "name":"HR Taskforce",
                        "address":"HRTaskforce@contoso.onmicrosoft.com"
                    }
                },
                {
                    "type":"required",
                    "status":{
                        "response":"none",
                        "time":"0001-01-01T00:00:00Z"
                    },
                    "emailAddress":{
                        "name":"Megan Bowen",
                        "address":"MeganB@contoso.onmicrosoft.com"
                    }
                }
            ],
            "organizer":{
                "emailAddress":{
                    "name":"HR Taskforce",
                    "address":"HRTaskforce@contoso.onmicrosoft.com"
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
  "description": "List calendarView",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
