# <a name="message-send"></a><span data-ttu-id="37a69-101">message: send</span><span class="sxs-lookup"><span data-stu-id="37a69-101">message: send</span></span>

<span data-ttu-id="37a69-p101">Envía un mensaje de la carpeta Borrador. El borrador del mensaje puede ser un borrador de mensaje nuevo, un borrador de respuesta, un borrador de respuesta a todos o un borrador de reenvío. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="37a69-p101">Send a message in the draft folder. The draft message can be a new message draft, reply draft, reply-all draft, or a forward draft. The message is then saved in the Sent Items folder.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="37a69-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="37a69-105">Prerequisites</span></span>
<span data-ttu-id="37a69-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.Send*</span><span class="sxs-lookup"><span data-stu-id="37a69-106">One of the following **scopes** is required to execute this API: *Mail.Send*</span></span>
## <a name="http-request"></a><span data-ttu-id="37a69-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="37a69-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/send
POST /users/{id | userPrincipalName}/messages/{id}/send
```
## <a name="request-headers"></a><span data-ttu-id="37a69-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="37a69-108">Request headers</span></span>
| <span data-ttu-id="37a69-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="37a69-109">Name</span></span>       | <span data-ttu-id="37a69-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="37a69-110">Type</span></span> | <span data-ttu-id="37a69-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="37a69-111">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="37a69-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="37a69-112">Authorization</span></span>  | <span data-ttu-id="37a69-113">string</span><span class="sxs-lookup"><span data-stu-id="37a69-113">string</span></span>  | <span data-ttu-id="37a69-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="37a69-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="37a69-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37a69-116">Request body</span></span>

## <a name="response"></a><span data-ttu-id="37a69-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37a69-117">Response</span></span>

<span data-ttu-id="37a69-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37a69-p103">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="37a69-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37a69-120">Example</span></span>
<span data-ttu-id="37a69-121">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="37a69-121">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="37a69-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="37a69-122">Request</span></span>
<span data-ttu-id="37a69-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37a69-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_send"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/send
```

##### <a name="response"></a><span data-ttu-id="37a69-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37a69-124">Response</span></span>
##### <a name="response"></a><span data-ttu-id="37a69-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37a69-125">Response</span></span>
<span data-ttu-id="37a69-126">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37a69-126">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: send",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
