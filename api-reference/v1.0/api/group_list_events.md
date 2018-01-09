# <a name="list-events"></a><span data-ttu-id="02ed1-101">List events</span><span class="sxs-lookup"><span data-stu-id="02ed1-101">List events</span></span>
<span data-ttu-id="02ed1-102">Recupera una lista de objetos [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="02ed1-102">Retrieve a list of [event](../resources/event.md) objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="02ed1-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="02ed1-103">Permissions</span></span>
<span data-ttu-id="02ed1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="02ed1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="02ed1-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="02ed1-106">Permission type</span></span>      | <span data-ttu-id="02ed1-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="02ed1-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="02ed1-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="02ed1-108">Delegated (work or school account)</span></span> | <span data-ttu-id="02ed1-109">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="02ed1-109">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="02ed1-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="02ed1-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="02ed1-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="02ed1-111">Not supported.</span></span>    |
|<span data-ttu-id="02ed1-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="02ed1-112">Application</span></span> | <span data-ttu-id="02ed1-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="02ed1-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="02ed1-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="02ed1-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/events
GET /groups/{id}/calendar/events
```

## <a name="optional-query-parameters"></a><span data-ttu-id="02ed1-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="02ed1-115">Optional query parameters</span></span>
<span data-ttu-id="02ed1-116">Este método admite los [parámetros de consulta de OData](../../../concepts/query_parameters.md) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="02ed1-116">This method supports the [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="02ed1-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="02ed1-117">Request headers</span></span>
| <span data-ttu-id="02ed1-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02ed1-118">Header</span></span>       | <span data-ttu-id="02ed1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="02ed1-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="02ed1-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="02ed1-120">Authorization</span></span>  | <span data-ttu-id="02ed1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="02ed1-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="02ed1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="02ed1-123">Request body</span></span>
<span data-ttu-id="02ed1-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="02ed1-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="02ed1-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="02ed1-125">Response</span></span>
<span data-ttu-id="02ed1-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos de [evento](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="02ed1-126">If successful, this method returns a `200 OK` response code and a collection of [Event](../resources/event.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="02ed1-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="02ed1-127">Example</span></span>
#### <a name="request"></a><span data-ttu-id="02ed1-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="02ed1-128">Request</span></span>
<span data-ttu-id="02ed1-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="02ed1-129">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group_events"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/events
```

#### <a name="response"></a><span data-ttu-id="02ed1-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="02ed1-130">Response</span></span>
<span data-ttu-id="02ed1-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="02ed1-131">Here is an example of the response.</span></span>
><span data-ttu-id="02ed1-132">**Nota:** Se puede reducir el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="02ed1-132">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="02ed1-133">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="02ed1-133">All the properties will be returned from an actual call.</span></span>
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
