# <a name="list-events"></a><span data-ttu-id="c5625-101">List events</span><span class="sxs-lookup"><span data-stu-id="c5625-101">List events</span></span>

<span data-ttu-id="c5625-p101">Recupera una lista de eventos de un calendario.  La lista contiene patrones de serie y reuniones de instancia única.</span><span class="sxs-lookup"><span data-stu-id="c5625-p101">Retrieve a list of events in a calendar.  The list contains single instance meetings and series masters.</span></span>

<span data-ttu-id="c5625-104">Para obtener instancias de evento de expansión, puede [obtener la vista de calendario](calendar_list_calendarview.md) o bien [obtener las instancias de un evento](event_list_instances.md).</span><span class="sxs-lookup"><span data-stu-id="c5625-104">To get expanded event instances, you can [get the calendar view](calendar_list_calendarview.md), or [get the instances of an event](event_list_instances.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c5625-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c5625-105">Prerequisites</span></span>
<span data-ttu-id="c5625-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.Read*</span><span class="sxs-lookup"><span data-stu-id="c5625-106">One of the following **scopes** is required to execute this API: *Calendars.Read*</span></span>
## <a name="http-request"></a><span data-ttu-id="c5625-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c5625-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="c5625-108">[calendar](../resources/calendar.md) predeterminado de un usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="c5625-108">A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
GET /me/calendar/events
GET /users/{id | userPrincipalName}/calendar/events
GET /groups/{id}/calendar/events
```
<span data-ttu-id="c5625-109">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c5625-109">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendars/{id}/events
GET /users/{id | userPrincipalName}/calendars/{id}/events

GET /me/calendarGroup/calendars/{id}/events
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/events
```
<span data-ttu-id="c5625-110">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="c5625-110">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendarGroups/{id}/calendars/{id}/events
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/events
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c5625-111">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c5625-111">Optional query parameters</span></span>
<span data-ttu-id="c5625-112">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5625-112">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c5625-113">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c5625-113">Request headers</span></span>
| <span data-ttu-id="c5625-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5625-114">Header</span></span>       | <span data-ttu-id="c5625-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c5625-115">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c5625-116">Authorization</span><span class="sxs-lookup"><span data-stu-id="c5625-116">Authorization</span></span>  | <span data-ttu-id="c5625-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c5625-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c5625-119">Prefer</span><span class="sxs-lookup"><span data-stu-id="c5625-119">Prefer</span></span>  | <span data-ttu-id="c5625-p103">outlook.timezone="Hora estándar del Este". Opcional. Se usa para especificar la zona horaria en las horas de inicio y final en la respuesta. Si no se especifica, la respuesta se devuelve en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="c5625-p103">outlook.timezone="Eastern Standard Time". Optional. Use this to specify the time zone for start and end times in the response. If not specified, the response are returned in UTC.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c5625-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c5625-124">Request body</span></span>
<span data-ttu-id="c5625-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c5625-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c5625-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5625-126">Response</span></span>

<span data-ttu-id="c5625-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5625-127">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c5625-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c5625-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c5625-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c5625-129">Request</span></span>
<span data-ttu-id="c5625-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c5625-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_events"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendar/events
```
##### <a name="response"></a><span data-ttu-id="c5625-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5625-131">Response</span></span>
<span data-ttu-id="c5625-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c5625-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
