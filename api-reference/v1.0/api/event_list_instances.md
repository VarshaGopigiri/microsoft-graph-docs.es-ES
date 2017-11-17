# <a name="list-instances"></a><span data-ttu-id="7e40c-101">List instances</span><span class="sxs-lookup"><span data-stu-id="7e40c-101">List instances</span></span>

<span data-ttu-id="7e40c-p101">Obtiene las instancias (repeticiones) de un evento durante un intervalo de tiempo especificado. Si el evento es de tipo `SeriesMaster`, devuelve las repeticiones y excepciones del evento en el intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="7e40c-p101">Get the instances (occurrences) of an event for a specified time range. If the event is a `SeriesMaster` type, this returns the occurrences and exceptions of the event in the specified time range.</span></span>

## <a name="permissions"></a><span data-ttu-id="7e40c-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="7e40c-104">Permissions</span></span>
<span data-ttu-id="7e40c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7e40c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7e40c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7e40c-107">Permission type</span></span>      | <span data-ttu-id="7e40c-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7e40c-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7e40c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7e40c-109">Delegated (work or school account)</span></span> | <span data-ttu-id="7e40c-110">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="7e40c-110">Calendars.Read</span></span>    |
|<span data-ttu-id="7e40c-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7e40c-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7e40c-112">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="7e40c-112">Calendars.Read</span></span>    |
|<span data-ttu-id="7e40c-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7e40c-113">Application</span></span> | <span data-ttu-id="7e40c-114">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="7e40c-114">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="7e40c-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7e40c-115">HTTP request</span></span>
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
## <a name="query-parameters"></a><span data-ttu-id="7e40c-116">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="7e40c-116">Query parameters</span></span>

<span data-ttu-id="7e40c-117">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="7e40c-117">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="7e40c-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7e40c-118">Parameter</span></span>    | <span data-ttu-id="7e40c-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e40c-119">Type</span></span>   |<span data-ttu-id="7e40c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e40c-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7e40c-121">startDateTime</span><span class="sxs-lookup"><span data-stu-id="7e40c-121">startDateTime</span></span>|<span data-ttu-id="7e40c-122">String</span><span class="sxs-lookup"><span data-stu-id="7e40c-122">String</span></span>|<span data-ttu-id="7e40c-p103">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="7e40c-p103">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="7e40c-125">endDateTime</span><span class="sxs-lookup"><span data-stu-id="7e40c-125">endDateTime</span></span>|<span data-ttu-id="7e40c-126">String</span><span class="sxs-lookup"><span data-stu-id="7e40c-126">String</span></span>|<span data-ttu-id="7e40c-p104">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="7e40c-p104">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="7e40c-129">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e40c-129">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="7e40c-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7e40c-130">Request headers</span></span>
| <span data-ttu-id="7e40c-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="7e40c-131">Name</span></span>       | <span data-ttu-id="7e40c-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e40c-132">Type</span></span> | <span data-ttu-id="7e40c-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e40c-133">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="7e40c-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="7e40c-134">Authorization</span></span>  | <span data-ttu-id="7e40c-135">string</span><span class="sxs-lookup"><span data-stu-id="7e40c-135">string</span></span>  | <span data-ttu-id="7e40c-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7e40c-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7e40c-138">Prefer</span><span class="sxs-lookup"><span data-stu-id="7e40c-138">Prefer</span></span> | <span data-ttu-id="7e40c-139">string</span><span class="sxs-lookup"><span data-stu-id="7e40c-139">string</span></span> | <span data-ttu-id="7e40c-p106">outlook.timezone="Hora estándar del Este". Opcional. Se usa para especificar la zona horaria en las horas de inicio y final en la respuesta. Si no se especifica, la respuesta se devuelve en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="7e40c-p106">outlook.timezone="Eastern Standard Time". Optional. Use this to specify the time zone for start and end times in the response. If not specified, the response are returned in UTC.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7e40c-144">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7e40c-144">Request body</span></span>
<span data-ttu-id="7e40c-145">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7e40c-145">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7e40c-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e40c-146">Response</span></span>

<span data-ttu-id="7e40c-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e40c-147">If successful, this method returns a `200 OK` response code and collection of [Event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7e40c-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7e40c-148">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7e40c-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7e40c-149">Request</span></span>
<span data-ttu-id="7e40c-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7e40c-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_instances"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events/{id}/instances
```
##### <a name="response"></a><span data-ttu-id="7e40c-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e40c-151">Response</span></span>
<span data-ttu-id="7e40c-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7e40c-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
