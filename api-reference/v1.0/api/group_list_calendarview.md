# <a name="list-calendarview"></a><span data-ttu-id="c58bc-101">List calendarView</span><span class="sxs-lookup"><span data-stu-id="c58bc-101">List calendarView</span></span>
<span data-ttu-id="c58bc-102">Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado de un grupo.</span><span class="sxs-lookup"><span data-stu-id="c58bc-102">Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the default calendar of a group.</span></span>

## <a name="permissions"></a><span data-ttu-id="c58bc-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c58bc-103">Permissions</span></span>
<span data-ttu-id="c58bc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c58bc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c58bc-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c58bc-106">Permission type</span></span>      | <span data-ttu-id="c58bc-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c58bc-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c58bc-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c58bc-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c58bc-109">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c58bc-109">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="c58bc-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c58bc-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c58bc-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c58bc-111">Not supported.</span></span>    |
|<span data-ttu-id="c58bc-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c58bc-112">Application</span></span> | <span data-ttu-id="c58bc-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c58bc-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c58bc-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c58bc-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

## <a name="query-parameters"></a><span data-ttu-id="c58bc-115">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="c58bc-115">Query parameters</span></span>
<span data-ttu-id="c58bc-116">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="c58bc-116">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="c58bc-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c58bc-117">Parameter</span></span>    | <span data-ttu-id="c58bc-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="c58bc-118">Type</span></span>   |<span data-ttu-id="c58bc-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c58bc-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c58bc-120">startDateTime</span><span class="sxs-lookup"><span data-stu-id="c58bc-120">startDateTime</span></span>|<span data-ttu-id="c58bc-121">String</span><span class="sxs-lookup"><span data-stu-id="c58bc-121">String</span></span>|<span data-ttu-id="c58bc-p102">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="c58bc-p102">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="c58bc-124">endDateTime</span><span class="sxs-lookup"><span data-stu-id="c58bc-124">endDateTime</span></span>|<span data-ttu-id="c58bc-125">String</span><span class="sxs-lookup"><span data-stu-id="c58bc-125">String</span></span>|<span data-ttu-id="c58bc-p103">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="c58bc-p103">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="c58bc-128">Este método también admite los [parámetros de consulta de OData](../../../concepts/query_parameters.md) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c58bc-128">This method also supports the [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c58bc-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c58bc-129">Request headers</span></span>
| <span data-ttu-id="c58bc-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c58bc-130">Header</span></span>       | <span data-ttu-id="c58bc-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c58bc-131">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c58bc-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="c58bc-132">Authorization</span></span>  | <span data-ttu-id="c58bc-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c58bc-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c58bc-135">Prefer</span><span class="sxs-lookup"><span data-stu-id="c58bc-135">Prefer</span></span> | <span data-ttu-id="c58bc-136">string</span><span class="sxs-lookup"><span data-stu-id="c58bc-136">string</span></span> | <span data-ttu-id="c58bc-p105">outlook.timezone="Hora estándar del Este". Opcional. Se usa para especificar la zona horaria en las horas de inicio y final en la respuesta. Si no se especifica, la respuesta se devuelve en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="c58bc-p105">outlook.timezone="Eastern Standard Time". Optional. Use this to specify the time zone for start and end times in the response. If not specified, the response are returned in UTC.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c58bc-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c58bc-141">Request body</span></span>
<span data-ttu-id="c58bc-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c58bc-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c58bc-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c58bc-143">Response</span></span>
<span data-ttu-id="c58bc-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c58bc-144">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c58bc-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c58bc-145">Example</span></span>
#### <a name="request"></a><span data-ttu-id="c58bc-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c58bc-146">Request</span></span>
<span data-ttu-id="c58bc-147">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c58bc-147">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/calendarView
```

#### <a name="response"></a><span data-ttu-id="c58bc-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c58bc-148">Response</span></span>
<span data-ttu-id="c58bc-149">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c58bc-149">Here is an example of the response.</span></span>
><span data-ttu-id="c58bc-150">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c58bc-150">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="c58bc-151">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c58bc-151">All the properties will be returned from an actual call.</span></span>
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
