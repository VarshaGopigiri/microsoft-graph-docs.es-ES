# <a name="list-instances"></a><span data-ttu-id="bf48f-101">List instances</span><span class="sxs-lookup"><span data-stu-id="bf48f-101">List instances</span></span>

<span data-ttu-id="bf48f-p101">Obtiene las instancias (repeticiones) de un evento durante un intervalo de tiempo especificado. Si el evento es de tipo `SeriesMaster`, devuelve las repeticiones y excepciones del evento en el intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="bf48f-p101">Get the instances (occurrences) of an event for a specified time range. If the event is a `SeriesMaster` type, this returns the occurrences and exceptions of the event in the specified time range.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bf48f-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bf48f-104">Prerequisites</span></span>
<span data-ttu-id="bf48f-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.Read*</span><span class="sxs-lookup"><span data-stu-id="bf48f-105">One of the following **scopes** is required to execute this API: *Calendars.Read*</span></span>
## <a name="http-request"></a><span data-ttu-id="bf48f-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf48f-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /groups/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendar/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendar/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /groups/{id}/calendar/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendars/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendars/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendargroup/calendars/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendargroups/{id}/calendars/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
```
## <a name="query-parameters"></a><span data-ttu-id="bf48f-107">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="bf48f-107">Query parameters</span></span>

<span data-ttu-id="bf48f-108">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="bf48f-108">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="bf48f-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bf48f-109">Parameter</span></span>    | <span data-ttu-id="bf48f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf48f-110">Type</span></span>   |<span data-ttu-id="bf48f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf48f-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bf48f-112">startDateTime</span><span class="sxs-lookup"><span data-stu-id="bf48f-112">startDateTime</span></span>|<span data-ttu-id="bf48f-113">String</span><span class="sxs-lookup"><span data-stu-id="bf48f-113">String</span></span>|<span data-ttu-id="bf48f-p102">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="bf48f-p102">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="bf48f-116">endDateTime</span><span class="sxs-lookup"><span data-stu-id="bf48f-116">endDateTime</span></span>|<span data-ttu-id="bf48f-117">String</span><span class="sxs-lookup"><span data-stu-id="bf48f-117">String</span></span>|<span data-ttu-id="bf48f-p103">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="bf48f-p103">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="bf48f-120">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf48f-120">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bf48f-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf48f-121">Request headers</span></span>
| <span data-ttu-id="bf48f-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="bf48f-122">Name</span></span>       | <span data-ttu-id="bf48f-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf48f-123">Type</span></span> | <span data-ttu-id="bf48f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf48f-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bf48f-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="bf48f-125">Authorization</span></span>  | <span data-ttu-id="bf48f-126">string</span><span class="sxs-lookup"><span data-stu-id="bf48f-126">string</span></span>  | <span data-ttu-id="bf48f-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf48f-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bf48f-129">Prefer</span><span class="sxs-lookup"><span data-stu-id="bf48f-129">Prefer</span></span> | <span data-ttu-id="bf48f-130">string</span><span class="sxs-lookup"><span data-stu-id="bf48f-130">string</span></span> | <span data-ttu-id="bf48f-p105">outlook.timezone="Hora estándar del Este". Opcional. Se usa para especificar la zona horaria en las horas de inicio y final en la respuesta. Si no se especifica, la respuesta se devuelve en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="bf48f-p105">outlook.timezone="Eastern Standard Time". Optional. Use this to specify the time zone for start and end times in the response. If not specified, the response are returned in UTC.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bf48f-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bf48f-135">Request body</span></span>
<span data-ttu-id="bf48f-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bf48f-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bf48f-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf48f-137">Response</span></span>

<span data-ttu-id="bf48f-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf48f-138">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bf48f-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf48f-139">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bf48f-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bf48f-140">Request</span></span>
<span data-ttu-id="bf48f-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf48f-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_instances"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events/{id}/instances
```
##### <a name="response"></a><span data-ttu-id="bf48f-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf48f-142">Response</span></span>
<span data-ttu-id="bf48f-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf48f-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List instances",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
