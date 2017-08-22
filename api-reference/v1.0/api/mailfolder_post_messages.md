# <a name="create-message"></a><span data-ttu-id="20182-101">Create Message</span><span class="sxs-lookup"><span data-stu-id="20182-101">Create Message</span></span>

<span data-ttu-id="20182-102">Use esta API para crear un objeto Message en una mailfolder.</span><span class="sxs-lookup"><span data-stu-id="20182-102">Use this API to create a new Message in a mailfolder.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="20182-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="20182-103">Prerequisites</span></span>
<span data-ttu-id="20182-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="20182-104">One of the following **scopes** is required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="20182-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="20182-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/{id}/messages
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages
```
## <a name="request-headers"></a><span data-ttu-id="20182-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="20182-106">Request headers</span></span>
| <span data-ttu-id="20182-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20182-107">Header</span></span>       | <span data-ttu-id="20182-108">Valor</span><span class="sxs-lookup"><span data-stu-id="20182-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="20182-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="20182-109">Authorization</span></span>  | <span data-ttu-id="20182-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="20182-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="20182-112">Content-Type</span><span class="sxs-lookup"><span data-stu-id="20182-112">Content-Type</span></span>  | <span data-ttu-id="20182-p102">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="20182-p102">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="20182-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="20182-115">Request body</span></span>
<span data-ttu-id="20182-116">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="20182-116">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="20182-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="20182-117">Response</span></span>

<span data-ttu-id="20182-118">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="20182-118">If successful, this method returns `201, Created` response code and [message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="20182-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="20182-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="20182-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="20182-120">Request</span></span>
<span data-ttu-id="20182-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="20182-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_message_from_mailfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/{id}/messages
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```
<span data-ttu-id="20182-122">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="20182-122">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="20182-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="20182-123">Response</span></span>
<span data-ttu-id="20182-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="20182-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
