# <a name="list-calendarview"></a><span data-ttu-id="4a81c-101">List calendarView</span><span class="sxs-lookup"><span data-stu-id="4a81c-101">List calendarView</span></span>

<span data-ttu-id="4a81c-102">Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado de un grupo.</span><span class="sxs-lookup"><span data-stu-id="4a81c-102">Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the default calendar of a group.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4a81c-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4a81c-103">Prerequisites</span></span>
<span data-ttu-id="4a81c-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.Read.All* o *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="4a81c-104">One of the following **scopes** is required to execute this API: *Group.Read.All* or *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="4a81c-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a81c-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```
## <a name="query-parameters"></a><span data-ttu-id="4a81c-106">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="4a81c-106">Query parameters</span></span>

<span data-ttu-id="4a81c-107">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="4a81c-107">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="4a81c-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4a81c-108">Parameter</span></span>    | <span data-ttu-id="4a81c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a81c-109">Type</span></span>   |<span data-ttu-id="4a81c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a81c-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4a81c-111">startDateTime</span><span class="sxs-lookup"><span data-stu-id="4a81c-111">startDateTime</span></span>|<span data-ttu-id="4a81c-112">String</span><span class="sxs-lookup"><span data-stu-id="4a81c-112">String</span></span>|<span data-ttu-id="4a81c-p101">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="4a81c-p101">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="4a81c-115">endDateTime</span><span class="sxs-lookup"><span data-stu-id="4a81c-115">endDateTime</span></span>|<span data-ttu-id="4a81c-116">String</span><span class="sxs-lookup"><span data-stu-id="4a81c-116">String</span></span>|<span data-ttu-id="4a81c-p102">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="4a81c-p102">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="4a81c-119">Este método también admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a81c-119">This method also supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="4a81c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4a81c-120">Request headers</span></span>
| <span data-ttu-id="4a81c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a81c-121">Header</span></span>       | <span data-ttu-id="4a81c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4a81c-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4a81c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="4a81c-123">Authorization</span></span>  | <span data-ttu-id="4a81c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4a81c-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="4a81c-126">Prefer</span><span class="sxs-lookup"><span data-stu-id="4a81c-126">Prefer</span></span> | <span data-ttu-id="4a81c-127">string</span><span class="sxs-lookup"><span data-stu-id="4a81c-127">string</span></span> | <span data-ttu-id="4a81c-p104">outlook.timezone="Hora estándar del Este". Opcional. Se usa para especificar la zona horaria en las horas de inicio y final en la respuesta. Si no se especifica, la respuesta se devuelve en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="4a81c-p104">outlook.timezone="Eastern Standard Time". Optional. Use this to specify the time zone for start and end times in the response. If not specified, the response are returned in UTC.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4a81c-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4a81c-132">Request body</span></span>
<span data-ttu-id="4a81c-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4a81c-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4a81c-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a81c-134">Response</span></span>

<span data-ttu-id="4a81c-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a81c-135">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4a81c-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a81c-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4a81c-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4a81c-137">Request</span></span>
<span data-ttu-id="4a81c-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4a81c-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/calendarView
```
##### <a name="response"></a><span data-ttu-id="4a81c-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a81c-139">Response</span></span>
<span data-ttu-id="4a81c-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4a81c-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
