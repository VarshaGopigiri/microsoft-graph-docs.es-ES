---
title: List events
description: Recupera una lista de objetos event.
ms.openlocfilehash: ec91a899dc8ffb36ca06a0e3554be46f33c72ed0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029566"
---
# <a name="list-events"></a><span data-ttu-id="a3b62-103">List events</span><span class="sxs-lookup"><span data-stu-id="a3b62-103">List events</span></span>
<span data-ttu-id="a3b62-104">Recupera una lista de objetos [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="a3b62-104">Retrieve a list of [event](../resources/event.md) objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="a3b62-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a3b62-105">Permissions</span></span>
<span data-ttu-id="a3b62-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a3b62-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a3b62-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a3b62-108">Permission type</span></span>      | <span data-ttu-id="a3b62-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a3b62-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a3b62-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a3b62-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a3b62-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a3b62-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="a3b62-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a3b62-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a3b62-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a3b62-113">Not supported.</span></span>    |
|<span data-ttu-id="a3b62-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a3b62-114">Application</span></span> | <span data-ttu-id="a3b62-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a3b62-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a3b62-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a3b62-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/events
GET /groups/{id}/calendar/events
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a3b62-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a3b62-117">Optional query parameters</span></span>
<span data-ttu-id="a3b62-118">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3b62-118">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a3b62-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a3b62-119">Request headers</span></span>
| <span data-ttu-id="a3b62-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="a3b62-120">Name</span></span>       | <span data-ttu-id="a3b62-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="a3b62-121">Type</span></span> | <span data-ttu-id="a3b62-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3b62-122">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="a3b62-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a3b62-123">Authorization</span></span>  | <span data-ttu-id="a3b62-124">string</span><span class="sxs-lookup"><span data-stu-id="a3b62-124">string</span></span> | <span data-ttu-id="a3b62-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a3b62-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a3b62-127">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="a3b62-127">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="a3b62-128">string</span><span class="sxs-lookup"><span data-stu-id="a3b62-128">string</span></span> | <span data-ttu-id="a3b62-129">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3b62-129">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="a3b62-130">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="a3b62-130">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="a3b62-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a3b62-131">Optional.</span></span> |
| <span data-ttu-id="a3b62-132">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="a3b62-132">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="a3b62-133">string</span><span class="sxs-lookup"><span data-stu-id="a3b62-133">string</span></span> | <span data-ttu-id="a3b62-134">Formato de la propiedad **body** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="a3b62-134">The format of the **body** property to be returned in.</span></span> <span data-ttu-id="a3b62-135">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="a3b62-135">Values can be "text" or "html".</span></span> <span data-ttu-id="a3b62-136">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="a3b62-136">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="a3b62-137">Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="a3b62-137">If the header is not specified, the **body** property is returned in HTML format.</span></span> <span data-ttu-id="a3b62-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a3b62-138">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a3b62-139">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a3b62-139">Request body</span></span>
<span data-ttu-id="a3b62-140">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a3b62-140">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a3b62-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3b62-141">Response</span></span>
<span data-ttu-id="a3b62-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos de [evento](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3b62-142">If successful, this method returns a `200 OK` response code and a collection of [event](../resources/event.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a3b62-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3b62-143">Example</span></span>
#### <a name="request"></a><span data-ttu-id="a3b62-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a3b62-144">Request</span></span>
<span data-ttu-id="a3b62-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3b62-145">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["02bd9fd6-8f93-4758-87c3-1fb73740a315"],
  "name": "get_group_events"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/events
```

#### <a name="response"></a><span data-ttu-id="a3b62-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3b62-146">Response</span></span>
<span data-ttu-id="a3b62-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3b62-147">The following is an example of the response.</span></span>
><span data-ttu-id="a3b62-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a3b62-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 354

{
  "value": [
    {
      "id": "AQMkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NwAzZWYARgAAA_b2VnUAiWNLj0xeSOs499YHAMT2RdsuOqRIlQZ4vOzp66YAAAIBDQAAAMT2RdsuOqRIlQZ4vOzp66YAAAIJOwAAAA==",
      "createdDateTime": "2017-07-31T18:59:01.982289Z",
      "lastModifiedDateTime": "2017-09-06T04:29:38.6647687Z",
      "changeKey": "xPZF2y46pEiVBni87OnrpgAAFq78Xw==",
      "categories": [],
      "originalStartTimeZone": "Eastern Standard Time",
      "originalEndTimeZone": "Eastern Standard Time",
      "iCalUId": "040000008200E00074C5B7101A82E00800000000824DDB122F0AD301000000000000000010000000824A8905B038D54AA7735F117B3442ED",
      "reminderMinutesBeforeStart": 15,
      "isReminderOn": true,
      "hasAttachments": false,
      "subject": "New Training Plans",
      "bodyPreview": "Meeting to plan new trainings.\r\n\r\n\r\n\r\nJoin Microsoft Teams Online Meeting<https://teams.microsoft.com/l/meetup-join/19%3a900876baa3134907b0dcb41a0d220e31%40thread.skype/1501527539926?tenantId=dcd219dd-bc68-4b9b-bf0b-4a33a796be35>",
      "importance": "normal",
      "sensitivity": "normal",
      "isAllDay": false,
      "isCancelled": false,
      "isOrganizer": true,
      "responseRequested": true,
      "seriesMasterId": null,
      "showAs": "busy",
      "type": "seriesMaster",
      "webLink": "https://outlook.office365.com/owa/?itemid=AQMkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NwAzZWYARgAAA%2Bb2VnUAiWNLj0xeSOs499YHAMT2RdsuOqRIlQZ4vOzp66YAAAIBDQAAAMT2RdsuOqRIlQZ4vOzp66YAAAIJOwAAAA%3D%3D&exvsurl=1&path=/calendar/item",
      "onlineMeetingUrl": null,
      "responseStatus": {
          "response": "organizer",
          "time": "0001-01-01T00:00:00Z"
      },
      "body": {
          "contentType": "html",
          "content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\n<div>Meeting to plan new trainings.</div>\r\n<div><br>\r\n<br>\r\n<br>\r\n<a href=\"https://teams.microsoft.com/l/meetup-join/19%3a900876baa3134907b0dcb41a0d220e31%40thread.skype/1501527539926?tenantId=dcd219dd-bc68-4b9b-bf0b-4a33a796be35\">Join Microsoft Teams Online Meeting</a></div>\r\n</body>\r\n</html>\r\n"
      },
      "start": {
          "dateTime": "2017-08-14T21:00:00.0000000",
          "timeZone": "UTC"
      },
      "end": {
          "dateTime": "2017-08-14T22:00:00.0000000",
          "timeZone": "UTC"
      },
      "location": {
          "displayName": "HR Taskforce / Facilities"
      },
      "recurrence": {
          "pattern": {
              "type": "weekly",
              "interval": 1,
              "month": 0,
              "dayOfMonth": 0,
              "daysOfWeek": [
                  "monday",
                  "wednesday",
                  "friday"
              ],
              "firstDayOfWeek": "sunday",
              "index": "first"
          },
          "range": {
              "type": "noEnd",
              "startDate": "2017-08-14",
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
                  "time": "2017-07-31T18:59:06.4180028Z"
              },
              "emailAddress": {
                  "name": "Joni Sherman",
                  "address": "JoniS@contoso.onmicrosoft.com"
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
                  "address": "HRTaskforce@contoso.onmicrosoft.com"
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
                  "address": "MeganB@contoso.onmicrosoft.com"
              }
          },
          {
              "type": "required",
              "status": {
                  "response": "none",
                  "time": "0001-01-01T00:00:00Z"
              },
              "emailAddress": {
                  "name": "Lidia Holloway",
                  "address": "LidiaH@contoso.onmicrosoft.com"
              }
          },
          {
              "type": "required",
              "status": {
                  "response": "none",
                  "time": "0001-01-01T00:00:00Z"
              },
              "emailAddress": {
                  "name": "Emily Braun",
                  "address": "EmilyB@contoso.onmicrosoft.com"
              }
          }
      ],
      "organizer": {
          "emailAddress": {
              "name": "HR Taskforce",
              "address": "HRTaskforce@contoso.onmicrosoft.com"
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