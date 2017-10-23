# <a name="create-event"></a><span data-ttu-id="04ad8-101">Create Event</span><span class="sxs-lookup"><span data-stu-id="04ad8-101">Create Event</span></span>

<span data-ttu-id="04ad8-102">Use esta API para crear un objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="04ad8-102">Use this API to create a new [event](../resources/event.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="04ad8-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="04ad8-103">Permissions</span></span>
<span data-ttu-id="04ad8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="04ad8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="04ad8-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="04ad8-106">Permission type</span></span>      | <span data-ttu-id="04ad8-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="04ad8-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="04ad8-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="04ad8-108">Delegated (work or school account)</span></span> | <span data-ttu-id="04ad8-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="04ad8-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="04ad8-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="04ad8-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="04ad8-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04ad8-111">Not supported.</span></span>    |
|<span data-ttu-id="04ad8-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="04ad8-112">Application</span></span> | <span data-ttu-id="04ad8-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="04ad8-113">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="04ad8-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="04ad8-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/events
POST /groups/{id}/calendar/events
```
## <a name="request-headers"></a><span data-ttu-id="04ad8-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="04ad8-115">Request headers</span></span>
| <span data-ttu-id="04ad8-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04ad8-116">Header</span></span>       | <span data-ttu-id="04ad8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="04ad8-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="04ad8-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="04ad8-118">Authorization</span></span>  | <span data-ttu-id="04ad8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="04ad8-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="04ad8-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="04ad8-121">Request body</span></span>
<span data-ttu-id="04ad8-122">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="04ad8-122">In the request body, supply a JSON representation of [Event](../resources/event.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="04ad8-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04ad8-123">Response</span></span>

<span data-ttu-id="04ad8-124">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04ad8-124">If successful, this method returns `201 Created` response code and [Event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="04ad8-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04ad8-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="04ad8-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="04ad8-126">Request</span></span>
<span data-ttu-id="04ad8-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="04ad8-127">Here is an example of the request.</span></span>
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
<span data-ttu-id="04ad8-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="04ad8-128">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="04ad8-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04ad8-129">Response</span></span>
<span data-ttu-id="04ad8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="04ad8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
