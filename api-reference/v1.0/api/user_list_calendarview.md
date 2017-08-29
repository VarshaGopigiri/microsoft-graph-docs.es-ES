# <a name="list-calendarview"></a><span data-ttu-id="9a69d-101">List calendarView</span><span class="sxs-lookup"><span data-stu-id="9a69d-101">List calendarView</span></span>

<span data-ttu-id="9a69d-102">Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado de un usuario, o alguno de los otros calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="9a69d-102">Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the user's default calendar, or from some other calendar of the user's.</span></span>
## <a name="permissions"></a><span data-ttu-id="9a69d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9a69d-103">Permissions</span></span>
<span data-ttu-id="9a69d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9a69d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9a69d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9a69d-106">Permission type</span></span>      | <span data-ttu-id="9a69d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9a69d-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="9a69d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9a69d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9a69d-109">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9a69d-109">Calendars.Read, Calendars.ReadWrite</span></span>    | 
|<span data-ttu-id="9a69d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9a69d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9a69d-111">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9a69d-111">Calendars.Read, Calendars.ReadWrite</span></span>    | 
|<span data-ttu-id="9a69d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9a69d-112">Application</span></span> | <span data-ttu-id="9a69d-113">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9a69d-113">Calendars.Read, Calendars.ReadWrite</span></span> | 

## <a name="http-request"></a><span data-ttu-id="9a69d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9a69d-114">HTTP request</span></span>

<span data-ttu-id="9a69d-115">[calendar](../resources/calendar.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="9a69d-115">A user's default [calendar](../resources/calendar.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="9a69d-116">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9a69d-116">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="9a69d-117">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="9a69d-117">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

## <a name="query-parameters"></a><span data-ttu-id="9a69d-118">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="9a69d-118">Query parameters</span></span>

<span data-ttu-id="9a69d-119">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="9a69d-119">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="9a69d-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9a69d-120">Parameter</span></span>    | <span data-ttu-id="9a69d-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a69d-121">Type</span></span>   |<span data-ttu-id="9a69d-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a69d-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9a69d-123">startDateTime</span><span class="sxs-lookup"><span data-stu-id="9a69d-123">startDateTime</span></span>|<span data-ttu-id="9a69d-124">String</span><span class="sxs-lookup"><span data-stu-id="9a69d-124">String</span></span>|<span data-ttu-id="9a69d-p102">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="9a69d-p102">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="9a69d-127">endDateTime</span><span class="sxs-lookup"><span data-stu-id="9a69d-127">endDateTime</span></span>|<span data-ttu-id="9a69d-128">String</span><span class="sxs-lookup"><span data-stu-id="9a69d-128">String</span></span>|<span data-ttu-id="9a69d-p103">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="9a69d-p103">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="9a69d-131">Este método también admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a69d-131">This method also supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="9a69d-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9a69d-132">Request headers</span></span>
| <span data-ttu-id="9a69d-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="9a69d-133">Name</span></span>       | <span data-ttu-id="9a69d-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a69d-134">Type</span></span> | <span data-ttu-id="9a69d-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a69d-135">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9a69d-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="9a69d-136">Authorization</span></span>  | <span data-ttu-id="9a69d-137">string</span><span class="sxs-lookup"><span data-stu-id="9a69d-137">string</span></span>  | <span data-ttu-id="9a69d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a69d-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9a69d-140">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9a69d-140">Content-Type</span></span>   | <span data-ttu-id="9a69d-141">string</span><span class="sxs-lookup"><span data-stu-id="9a69d-141">string</span></span>  | <span data-ttu-id="9a69d-142">application/json</span><span class="sxs-lookup"><span data-stu-id="9a69d-142">application/json</span></span> | 
| <span data-ttu-id="9a69d-143">Prefer</span><span class="sxs-lookup"><span data-stu-id="9a69d-143">Prefer</span></span> | <span data-ttu-id="9a69d-144">string</span><span class="sxs-lookup"><span data-stu-id="9a69d-144">string</span></span> | <span data-ttu-id="9a69d-p105">outlook.timezone="Hora estándar del Este". Opcional. Se usa para especificar la zona horaria en las horas de inicio y final en la respuesta. Si no se especifica, la respuesta se devuelve en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="9a69d-p105">outlook.timezone="Eastern Standard Time". Optional. Use this to specify the time zone for start and end times in the response. If not specified, the response are returned in UTC.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9a69d-149">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9a69d-149">Request body</span></span>
<span data-ttu-id="9a69d-150">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9a69d-150">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9a69d-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a69d-151">Response</span></span>

<span data-ttu-id="9a69d-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a69d-152">If successful, this method returns a `200 OK` response code and collection of [Event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9a69d-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9a69d-153">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9a69d-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9a69d-154">Request</span></span>
<span data-ttu-id="9a69d-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a69d-155">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarView?startDateTime=2016-01-01T19:00:00.0000000&endDateTime=2016-10-01T19:00:00.0000000 
```
##### <a name="response"></a><span data-ttu-id="9a69d-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a69d-156">Response</span></span>
<span data-ttu-id="9a69d-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9a69d-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
