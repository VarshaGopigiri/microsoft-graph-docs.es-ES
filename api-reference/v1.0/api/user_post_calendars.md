# <a name="create-calendar"></a><span data-ttu-id="52b52-101">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="52b52-101">Create Calendar</span></span>

<span data-ttu-id="52b52-102">Use esta API para crear un calendario.</span><span class="sxs-lookup"><span data-stu-id="52b52-102">Use this API to create a new calendar.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="52b52-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="52b52-103">Prerequisites</span></span>
<span data-ttu-id="52b52-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="52b52-104">One of the following **scopes** is required to execute this API: *Calendars.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="52b52-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52b52-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/calendars
```
## <a name="request-headers"></a><span data-ttu-id="52b52-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="52b52-106">Request headers</span></span>
| <span data-ttu-id="52b52-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52b52-107">Header</span></span>       | <span data-ttu-id="52b52-108">Valor</span><span class="sxs-lookup"><span data-stu-id="52b52-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="52b52-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="52b52-109">Authorization</span></span>  | <span data-ttu-id="52b52-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="52b52-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="52b52-112">Content-Type</span><span class="sxs-lookup"><span data-stu-id="52b52-112">Content-Type</span></span>  | <span data-ttu-id="52b52-113">application/json</span><span class="sxs-lookup"><span data-stu-id="52b52-113">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="52b52-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="52b52-114">Request body</span></span>
<span data-ttu-id="52b52-115">En el cuerpo de la solicitud, especifique una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="52b52-115">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="52b52-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52b52-116">Response</span></span>

<span data-ttu-id="52b52-117">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52b52-117">If successful, this method returns `201, Created` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="52b52-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52b52-118">Example</span></span>
##### <a name="request"></a><span data-ttu-id="52b52-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="52b52-119">Request</span></span>
<span data-ttu-id="52b52-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="52b52-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_calendar_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/calendars
Content-type: application/json

{
  "name": "Volunteer"
}
```
<span data-ttu-id="52b52-121">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="52b52-121">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="52b52-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52b52-122">Response</span></span>
<span data-ttu-id="52b52-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="52b52-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#me/calendars/$entity",
    "@odata.id":"https://graph.microsoft.com/v1.0/users('266efe5a-0fd7-4edd-877b-b2d1e561f193@ae01a323-3934-4475-a32d-af1274312bb0')/calendars('AAMkADJmMVAAA=')",
    "id":"AAMkADJmMVAAA=",
    "name":"Volunteer",
    "color":"auto",
    "changeKey":"DxYSthXJXEWwAQSYQnXvIgAAIxGttg==",
    "canShare":true,
    "canViewPrivateItems":true,
    "canEdit":true,
    "owner":{
        "name":"Fanny Downs",
        "address":"fannyd@adatum.onmicrosoft.com"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
