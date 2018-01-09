# <a name="create-event"></a><span data-ttu-id="729dd-101">Crear evento</span><span class="sxs-lookup"><span data-stu-id="729dd-101">Create Event</span></span>
<span data-ttu-id="729dd-102">Use esta API para crear un objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="729dd-102">Use this API to create a new [event](../resources/event.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="729dd-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="729dd-103">Permissions</span></span>
<span data-ttu-id="729dd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="729dd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="729dd-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="729dd-106">Permission type</span></span>      | <span data-ttu-id="729dd-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="729dd-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="729dd-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="729dd-108">Delegated (work or school account)</span></span> | <span data-ttu-id="729dd-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="729dd-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="729dd-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="729dd-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="729dd-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="729dd-111">Not supported.</span></span>    |
|<span data-ttu-id="729dd-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="729dd-112">Application</span></span> | <span data-ttu-id="729dd-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="729dd-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="729dd-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="729dd-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/events
POST /groups/{id}/calendar/events
```

## <a name="request-headers"></a><span data-ttu-id="729dd-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="729dd-115">Request headers</span></span>
| <span data-ttu-id="729dd-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="729dd-116">Header</span></span>       | <span data-ttu-id="729dd-117">Valor</span><span class="sxs-lookup"><span data-stu-id="729dd-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="729dd-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="729dd-118">Authorization</span></span>  | <span data-ttu-id="729dd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="729dd-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="729dd-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="729dd-121">Request body</span></span>
<span data-ttu-id="729dd-122">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="729dd-122">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="729dd-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="729dd-123">Response</span></span>
<span data-ttu-id="729dd-124">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="729dd-124">If successful, this method returns `201 Created` response code and [event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="729dd-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="729dd-125">Example</span></span>
#### <a name="request"></a><span data-ttu-id="729dd-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="729dd-126">Request</span></span>
<span data-ttu-id="729dd-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="729dd-127">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "create_event_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/events
Content-type: application/json
Content-length: 285

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
```
<span data-ttu-id="729dd-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="729dd-128">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>

#### <a name="response"></a><span data-ttu-id="729dd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="729dd-129">Response</span></span>
<span data-ttu-id="729dd-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="729dd-130">Here is an example of the response.</span></span>
><span data-ttu-id="729dd-131">**Nota:** Se puede reducir el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="729dd-131">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="729dd-132">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="729dd-132">All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 285

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
