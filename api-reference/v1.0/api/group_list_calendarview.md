# <a name="list-calendarview"></a><span data-ttu-id="50845-101">List calendarView</span><span class="sxs-lookup"><span data-stu-id="50845-101">List calendarView</span></span>

<span data-ttu-id="50845-102">Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado de un grupo.</span><span class="sxs-lookup"><span data-stu-id="50845-102">Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the default calendar of a group.</span></span>
## <a name="permissions"></a><span data-ttu-id="50845-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="50845-103">Permissions</span></span>
<span data-ttu-id="50845-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="50845-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="50845-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="50845-106">Permission type</span></span>      | <span data-ttu-id="50845-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="50845-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="50845-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="50845-108">Delegated (work or school account)</span></span> | <span data-ttu-id="50845-109">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="50845-109">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="50845-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="50845-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="50845-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50845-111">Not supported.</span></span>    |
|<span data-ttu-id="50845-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="50845-112">Application</span></span> | <span data-ttu-id="50845-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="50845-113">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="50845-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="50845-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```
## <a name="query-parameters"></a><span data-ttu-id="50845-115">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="50845-115">Query parameters</span></span>

<span data-ttu-id="50845-116">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="50845-116">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="50845-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="50845-117">Parameter</span></span>    | <span data-ttu-id="50845-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="50845-118">Type</span></span>   |<span data-ttu-id="50845-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="50845-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="50845-120">startDateTime</span><span class="sxs-lookup"><span data-stu-id="50845-120">startDateTime</span></span>|<span data-ttu-id="50845-121">String</span><span class="sxs-lookup"><span data-stu-id="50845-121">String</span></span>|<span data-ttu-id="50845-p102">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="50845-p102">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="50845-124">endDateTime</span><span class="sxs-lookup"><span data-stu-id="50845-124">endDateTime</span></span>|<span data-ttu-id="50845-125">String</span><span class="sxs-lookup"><span data-stu-id="50845-125">String</span></span>|<span data-ttu-id="50845-p103">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="50845-p103">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="50845-128">Este método también admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50845-128">This method also supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="50845-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="50845-129">Request headers</span></span>
| <span data-ttu-id="50845-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50845-130">Header</span></span>       | <span data-ttu-id="50845-131">Valor</span><span class="sxs-lookup"><span data-stu-id="50845-131">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="50845-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="50845-132">Authorization</span></span>  | <span data-ttu-id="50845-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="50845-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="50845-135">Prefer</span><span class="sxs-lookup"><span data-stu-id="50845-135">Prefer</span></span> | <span data-ttu-id="50845-136">string</span><span class="sxs-lookup"><span data-stu-id="50845-136">string</span></span> | <span data-ttu-id="50845-p105">outlook.timezone="Hora estándar del Este". Opcional. Se usa para especificar la zona horaria en las horas de inicio y final en la respuesta. Si no se especifica, la respuesta se devuelve en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="50845-p105">outlook.timezone="Eastern Standard Time". Optional. Use this to specify the time zone for start and end times in the response. If not specified, the response are returned in UTC.</span></span> |

## <a name="request-body"></a><span data-ttu-id="50845-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="50845-141">Request body</span></span>
<span data-ttu-id="50845-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="50845-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="50845-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50845-143">Response</span></span>

<span data-ttu-id="50845-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50845-144">If successful, this method returns a `200 OK` response code and collection of [event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="50845-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="50845-145">Example</span></span>
##### <a name="request"></a><span data-ttu-id="50845-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="50845-146">Request</span></span>
<span data-ttu-id="50845-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="50845-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/calendarView
```
##### <a name="response"></a><span data-ttu-id="50845-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50845-148">Response</span></span>
<span data-ttu-id="50845-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="50845-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
