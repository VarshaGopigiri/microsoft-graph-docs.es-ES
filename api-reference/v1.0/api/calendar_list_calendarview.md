# <a name="list-calendarview"></a><span data-ttu-id="d9d73-101">List calendarView</span><span class="sxs-lookup"><span data-stu-id="d9d73-101">List calendarView</span></span>

<span data-ttu-id="d9d73-102">Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado `(../me/calendarview)` de un usuario o grupo, o alguno de los otros calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="d9d73-102">Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the default calendar `(../me/calendarview)` of a user or group, or some other calendar of the user's.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d9d73-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d9d73-103">Prerequisites</span></span>
<span data-ttu-id="d9d73-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="d9d73-104">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="d9d73-105">Eventos en el calendario de un usuario: _Calendars.Read_ o _Calendars.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="d9d73-105">Events in a user's calendar: _Calendars.Read_ or _Calendars.ReadWrite_</span></span>
* <span data-ttu-id="d9d73-106">Eventos de un calendario de grupo: _Group.Read.All_ o _Group.ReadWrite.All_</span><span class="sxs-lookup"><span data-stu-id="d9d73-106">Events in a group calendar: _Group.Read.All_ or _Group.ReadWrite.All_</span></span>

## <a name="http-request"></a><span data-ttu-id="d9d73-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d9d73-107">HTTP request</span></span>

<span data-ttu-id="d9d73-108">[calendar](../resources/calendar.md) predeterminado de un usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="d9d73-108">A user's or group's default [calendar](../resources/calendar.md).</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /groups/{id}/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="d9d73-109">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d9d73-109">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="d9d73-110">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="d9d73-110">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

## <a name="query-parameters"></a><span data-ttu-id="d9d73-111">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="d9d73-111">Query parameters</span></span>

<span data-ttu-id="d9d73-112">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="d9d73-112">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="d9d73-113">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d9d73-113">Parameter</span></span>    | <span data-ttu-id="d9d73-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9d73-114">Type</span></span>   |<span data-ttu-id="d9d73-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9d73-115">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d9d73-116">startDateTime</span><span class="sxs-lookup"><span data-stu-id="d9d73-116">startDateTime</span></span>|<span data-ttu-id="d9d73-117">String</span><span class="sxs-lookup"><span data-stu-id="d9d73-117">String</span></span>|<span data-ttu-id="d9d73-p101">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="d9d73-p101">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="d9d73-120">endDateTime</span><span class="sxs-lookup"><span data-stu-id="d9d73-120">endDateTime</span></span>|<span data-ttu-id="d9d73-121">String</span><span class="sxs-lookup"><span data-stu-id="d9d73-121">String</span></span>|<span data-ttu-id="d9d73-p102">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="d9d73-p102">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="d9d73-124">Este método también admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9d73-124">This method also supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="d9d73-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d9d73-125">Request headers</span></span>
| <span data-ttu-id="d9d73-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9d73-126">Header</span></span>       | <span data-ttu-id="d9d73-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d9d73-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d9d73-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="d9d73-128">Authorization</span></span>  | <span data-ttu-id="d9d73-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d9d73-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="d9d73-131">Prefer</span><span class="sxs-lookup"><span data-stu-id="d9d73-131">Prefer</span></span>  | <span data-ttu-id="d9d73-p104">outlook.timezone="Hora estándar del Este". Opcional. Se usa para especificar la zona horaria en las horas de inicio y final en la respuesta. Si no se especifica, la respuesta se devuelve en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="d9d73-p104">outlook.timezone="Eastern Standard Time". Optional. Use this to specify the time zone for start and end times in the response. If not specified, the response are returned in UTC.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d9d73-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d9d73-136">Request body</span></span>
<span data-ttu-id="d9d73-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d9d73-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d9d73-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9d73-138">Response</span></span>

<span data-ttu-id="d9d73-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9d73-139">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d9d73-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d9d73-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d9d73-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d9d73-141">Request</span></span>
<span data-ttu-id="d9d73-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d9d73-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendar/calendarView?startDateTime=2017-01-01T19:00:00.0000000&endDateTime=2017-01-07T19:00:00.0000000
```
##### <a name="response"></a><span data-ttu-id="d9d73-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9d73-143">Response</span></span>
<span data-ttu-id="d9d73-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d9d73-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
        "response": "response-value",
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
  "description": "List calendarView",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
