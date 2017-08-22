# <a name="create-event"></a><span data-ttu-id="c18bc-101">Create Event</span><span class="sxs-lookup"><span data-stu-id="c18bc-101">Create Event</span></span>

<span data-ttu-id="c18bc-102">Use esta API para crear un objeto Event en el calendario especificado o el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c18bc-102">Use this API to create a new Event in the default or the specified calendar.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c18bc-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c18bc-103">Prerequisites</span></span>
<span data-ttu-id="c18bc-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="c18bc-104">One of the following **scopes** is required to execute this API: *Calendars.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="c18bc-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c18bc-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="c18bc-106">[calendar](../resources/calendar.md) predeterminado de un usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="c18bc-106">A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
POST /me/calendar/events
POST /users/{id | userPrincipalName}/calendar/events
POST /groups/{id}/calendar/events
```
<span data-ttu-id="c18bc-107">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c18bc-107">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
POST /me/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendars/{id}/events

POST /me/calendarGroup/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/events
```
<span data-ttu-id="c18bc-108">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="c18bc-108">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
POST /me/calendarGroups/{id}/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/events
```
## <a name="request-headers"></a><span data-ttu-id="c18bc-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c18bc-109">Request headers</span></span>
| <span data-ttu-id="c18bc-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c18bc-110">Header</span></span>       | <span data-ttu-id="c18bc-111">Valor</span><span class="sxs-lookup"><span data-stu-id="c18bc-111">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c18bc-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="c18bc-112">Authorization</span></span>  | <span data-ttu-id="c18bc-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c18bc-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c18bc-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c18bc-115">Content-Type</span></span>  | <span data-ttu-id="c18bc-p102">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c18bc-p102">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c18bc-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c18bc-118">Request body</span></span>
<span data-ttu-id="c18bc-119">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="c18bc-119">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="c18bc-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c18bc-120">Response</span></span>

<span data-ttu-id="c18bc-121">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c18bc-121">If successful, this method returns `201, Created` response code and [event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c18bc-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c18bc-122">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c18bc-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c18bc-123">Request</span></span>
<span data-ttu-id="c18bc-124">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c18bc-124">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_event_from_calendar"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/calendar/events
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "datetime-value"
  },
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```
<span data-ttu-id="c18bc-125">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="c18bc-125">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="c18bc-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c18bc-126">Response</span></span>
<span data-ttu-id="c18bc-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c18bc-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "datetime-value"
  },
  "iCalUId": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
