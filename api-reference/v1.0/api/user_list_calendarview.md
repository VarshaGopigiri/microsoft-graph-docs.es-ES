# <a name="list-calendarview"></a><span data-ttu-id="522c8-101">List calendarView</span><span class="sxs-lookup"><span data-stu-id="522c8-101">List calendarView</span></span>

<span data-ttu-id="522c8-102">Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado de un usuario, o alguno de los otros calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="522c8-102">Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the user's default calendar, or from some other calendar of the user's.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="522c8-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="522c8-103">Prerequisites</span></span>
<span data-ttu-id="522c8-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.Read; Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="522c8-104">One of the following scopes is required to execute this API: Calendars.Read; Calendars.ReadWrite</span></span>
## <a name="http-request"></a><span data-ttu-id="522c8-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="522c8-105">HTTP request</span></span>

<span data-ttu-id="522c8-106">[calendar](../resources/calendar.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="522c8-106">A user's default [calendar](../resources/calendar.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="522c8-107">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="522c8-107">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="522c8-108">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="522c8-108">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

## <a name="query-parameters"></a><span data-ttu-id="522c8-109">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="522c8-109">Query parameters</span></span>

<span data-ttu-id="522c8-110">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="522c8-110">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="522c8-111">Parámetro</span><span class="sxs-lookup"><span data-stu-id="522c8-111">Parameter</span></span>    | <span data-ttu-id="522c8-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="522c8-112">Type</span></span>   |<span data-ttu-id="522c8-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="522c8-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="522c8-114">startDateTime</span><span class="sxs-lookup"><span data-stu-id="522c8-114">startDateTime</span></span>|<span data-ttu-id="522c8-115">String</span><span class="sxs-lookup"><span data-stu-id="522c8-115">String</span></span>|<span data-ttu-id="522c8-p101">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="522c8-p101">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="522c8-118">endDateTime</span><span class="sxs-lookup"><span data-stu-id="522c8-118">endDateTime</span></span>|<span data-ttu-id="522c8-119">String</span><span class="sxs-lookup"><span data-stu-id="522c8-119">String</span></span>|<span data-ttu-id="522c8-p102">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="522c8-p102">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="522c8-122">Este método también admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="522c8-122">This method also supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="522c8-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="522c8-123">Request headers</span></span>
| <span data-ttu-id="522c8-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="522c8-124">Name</span></span>       | <span data-ttu-id="522c8-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="522c8-125">Type</span></span> | <span data-ttu-id="522c8-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="522c8-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="522c8-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="522c8-127">Authorization</span></span>  | <span data-ttu-id="522c8-128">string</span><span class="sxs-lookup"><span data-stu-id="522c8-128">string</span></span>  | <span data-ttu-id="522c8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="522c8-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="522c8-131">Content-Type</span><span class="sxs-lookup"><span data-stu-id="522c8-131">Content-Type</span></span>   | <span data-ttu-id="522c8-132">string</span><span class="sxs-lookup"><span data-stu-id="522c8-132">string</span></span>  | <span data-ttu-id="522c8-133">application/json</span><span class="sxs-lookup"><span data-stu-id="522c8-133">application/json</span></span> | 
| <span data-ttu-id="522c8-134">Prefer</span><span class="sxs-lookup"><span data-stu-id="522c8-134">Prefer</span></span> | <span data-ttu-id="522c8-135">string</span><span class="sxs-lookup"><span data-stu-id="522c8-135">string</span></span> | <span data-ttu-id="522c8-p104">outlook.timezone="Hora estándar del Este". Opcional. Se usa para especificar la zona horaria en las horas de inicio y final en la respuesta. Si no se especifica, la respuesta se devuelve en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="522c8-p104">outlook.timezone="Eastern Standard Time". Optional. Use this to specify the time zone for start and end times in the response. If not specified, the response are returned in UTC.</span></span> |

## <a name="request-body"></a><span data-ttu-id="522c8-140">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="522c8-140">Request body</span></span>
<span data-ttu-id="522c8-141">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="522c8-141">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="522c8-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="522c8-142">Response</span></span>

<span data-ttu-id="522c8-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="522c8-143">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="522c8-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="522c8-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="522c8-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="522c8-145">Request</span></span>
<span data-ttu-id="522c8-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="522c8-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarView?startDateTime=2016-01-01T19:00:00.0000000&endDateTime=2016-10-01T19:00:00.0000000 
```
##### <a name="response"></a><span data-ttu-id="522c8-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="522c8-147">Response</span></span>
<span data-ttu-id="522c8-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="522c8-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List calendarView",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
