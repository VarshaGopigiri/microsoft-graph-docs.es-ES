# <a name="create-calendargroup"></a><span data-ttu-id="b8eee-101">Create CalendarGroup</span><span class="sxs-lookup"><span data-stu-id="b8eee-101">Create CalendarGroup</span></span>

<span data-ttu-id="b8eee-102">Use esta API para crear un objeto CalendarGroup.</span><span class="sxs-lookup"><span data-stu-id="b8eee-102">Use this API to create a new CalendarGroup.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b8eee-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b8eee-103">Prerequisites</span></span>
<span data-ttu-id="b8eee-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="b8eee-104">One of the following **scopes** is required to execute this API: *Calendars.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="b8eee-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b8eee-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/calendarGroups
```
## <a name="request-headers"></a><span data-ttu-id="b8eee-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b8eee-106">Request headers</span></span>
| <span data-ttu-id="b8eee-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8eee-107">Header</span></span>       | <span data-ttu-id="b8eee-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b8eee-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b8eee-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="b8eee-109">Authorization</span></span>  | <span data-ttu-id="b8eee-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b8eee-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="b8eee-112">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b8eee-112">Content-Type</span></span>  | <span data-ttu-id="b8eee-113">application/json</span><span class="sxs-lookup"><span data-stu-id="b8eee-113">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b8eee-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b8eee-114">Request body</span></span>
<span data-ttu-id="b8eee-115">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [CalendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="b8eee-115">In the request body, supply a JSON representation of [CalendarGroup](../resources/calendargroup.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="b8eee-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8eee-116">Response</span></span>

<span data-ttu-id="b8eee-117">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [CalendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8eee-117">If successful, this method returns `201, Created` response code and [CalendarGroup](../resources/calendargroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b8eee-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b8eee-118">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b8eee-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b8eee-119">Request</span></span>
<span data-ttu-id="b8eee-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b8eee-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_calendargroup_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/calendarGroups
Content-type: application/json
Content-length: 90

{
  "name": "name-value",
  "classId": "classId-value",
  "changeKey": "changeKey-value"
}
```
<span data-ttu-id="b8eee-121">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="b8eee-121">In the request body, supply a JSON representation of [calendarGroup](../resources/calendargroup.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="b8eee-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8eee-122">Response</span></span>
<span data-ttu-id="b8eee-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b8eee-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarGroup"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 110

{
  "name": "name-value",
  "classId": "classId-value",
  "changeKey": "changeKey-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create CalendarGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
