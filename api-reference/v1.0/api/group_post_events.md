# <a name="create-event"></a><span data-ttu-id="5c558-101">Create Event</span><span class="sxs-lookup"><span data-stu-id="5c558-101">Create Event</span></span>

<span data-ttu-id="5c558-102">Use esta API para crear un objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="5c558-102">Use this API to create a new [event](../resources/event.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5c558-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5c558-103">Prerequisites</span></span>
<span data-ttu-id="5c558-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="5c558-104">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="5c558-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5c558-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/events
POST /groups/{id}/calendar/events
```
## <a name="request-headers"></a><span data-ttu-id="5c558-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5c558-106">Request headers</span></span>
| <span data-ttu-id="5c558-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c558-107">Header</span></span>       | <span data-ttu-id="5c558-108">Valor</span><span class="sxs-lookup"><span data-stu-id="5c558-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5c558-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="5c558-109">Authorization</span></span>  | <span data-ttu-id="5c558-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5c558-p101">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5c558-112">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5c558-112">Request body</span></span>
<span data-ttu-id="5c558-113">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="5c558-113">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="5c558-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c558-114">Response</span></span>

<span data-ttu-id="5c558-115">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c558-115">If successful, this method returns `201, Created` response code and [event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5c558-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5c558-116">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5c558-117">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5c558-117">Request</span></span>
<span data-ttu-id="5c558-118">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c558-118">Here is an example of the request.</span></span>
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
<span data-ttu-id="5c558-119">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="5c558-119">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="5c558-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c558-120">Response</span></span>
<span data-ttu-id="5c558-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5c558-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
