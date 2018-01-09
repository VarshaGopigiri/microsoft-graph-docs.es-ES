# <a name="list-calendarview"></a><span data-ttu-id="615b0-101">List calendarView</span><span class="sxs-lookup"><span data-stu-id="615b0-101">List calendarView</span></span>

<span data-ttu-id="615b0-102">Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado `(../me/calendarview)` de un usuario o grupo, o alguno de los otros calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="615b0-102">Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the default calendar `(../me/calendarview)` of a user or group, or some other calendar of the user's.</span></span>

## <a name="permissions"></a><span data-ttu-id="615b0-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="615b0-103">Permissions</span></span>
<span data-ttu-id="615b0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="615b0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

* <span data-ttu-id="615b0-106">Eventos en el calendario de un usuario: Calendars.Read o Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="615b0-106">Events in a user's calendar: Calendars.Read or Calendars.ReadWrite</span></span>
* <span data-ttu-id="615b0-107">Eventos de un calendario de grupo: Group.Read.All o Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="615b0-107">Events in a group calendar: Group.Read.All or Group.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="615b0-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="615b0-108">HTTP request</span></span>

<span data-ttu-id="615b0-109">[calendar](../resources/calendar.md) predeterminado de un usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="615b0-109">A user's or group's default [calendar](../resources/calendar.md).</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /groups/{id}/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="615b0-110">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="615b0-110">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="615b0-111">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="615b0-111">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

## <a name="query-parameters"></a><span data-ttu-id="615b0-112">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="615b0-112">Query parameters</span></span>

<span data-ttu-id="615b0-113">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="615b0-113">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="615b0-114">Parámetro</span><span class="sxs-lookup"><span data-stu-id="615b0-114">Parameter</span></span>    | <span data-ttu-id="615b0-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="615b0-115">Type</span></span>   |<span data-ttu-id="615b0-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="615b0-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="615b0-117">startDateTime</span><span class="sxs-lookup"><span data-stu-id="615b0-117">startDateTime</span></span>|<span data-ttu-id="615b0-118">String</span><span class="sxs-lookup"><span data-stu-id="615b0-118">String</span></span>|<span data-ttu-id="615b0-p102">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="615b0-p102">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="615b0-121">endDateTime</span><span class="sxs-lookup"><span data-stu-id="615b0-121">endDateTime</span></span>|<span data-ttu-id="615b0-122">String</span><span class="sxs-lookup"><span data-stu-id="615b0-122">String</span></span>|<span data-ttu-id="615b0-p103">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="615b0-p103">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="615b0-125">Este método también admite los [parámetros de consulta de OData]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="615b0-125">This method also supports the [OData Query Parameters]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="615b0-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="615b0-126">Request headers</span></span>
| <span data-ttu-id="615b0-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="615b0-127">Name</span></span>       | <span data-ttu-id="615b0-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="615b0-128">Type</span></span> | <span data-ttu-id="615b0-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="615b0-129">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="615b0-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="615b0-130">Authorization</span></span>  | <span data-ttu-id="615b0-131">string</span><span class="sxs-lookup"><span data-stu-id="615b0-131">string</span></span> | <span data-ttu-id="615b0-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="615b0-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="615b0-134">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="615b0-134">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="615b0-135">string</span><span class="sxs-lookup"><span data-stu-id="615b0-135">string</span></span> | <span data-ttu-id="615b0-136">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="615b0-136">outlook.timezone="Eastern Standard Time". Optional. Use this to specify the time zone for start and end times in the response. If not specified, the response are returned in UTC.</span></span> <span data-ttu-id="615b0-137">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="615b0-137">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="615b0-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="615b0-138">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="615b0-139">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="615b0-139">Request body</span></span>
<span data-ttu-id="615b0-140">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="615b0-140">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="615b0-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="615b0-141">Response</span></span>

<span data-ttu-id="615b0-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="615b0-142">If successful, this method returns a `200 OK` response code and collection of [Event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="615b0-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="615b0-143">Example</span></span>
##### <a name="request"></a><span data-ttu-id="615b0-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="615b0-144">Request</span></span>
<span data-ttu-id="615b0-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="615b0-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendar/calendarView?startDateTime=2017-01-01T19:00:00.0000000&endDateTime=2017-01-07T19:00:00.0000000
```
##### <a name="response"></a><span data-ttu-id="615b0-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="615b0-146">Response</span></span>
<span data-ttu-id="615b0-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="615b0-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
