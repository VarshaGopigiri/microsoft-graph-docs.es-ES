# <a name="conversationthread-reply"></a><span data-ttu-id="d76ed-101">conversationThread: reply</span><span class="sxs-lookup"><span data-stu-id="d76ed-101">conversationThread: reply</span></span>

<span data-ttu-id="d76ed-p101">Responde a un hilo de una conversación de grupo y agrega una nueva publicación a la misma. Puede especificar la conversación primaria en la solicitud, o bien, especificar solo el hilo sin la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="d76ed-p101">Reply to a thread in a group conversation and add a new post to it. You can specify the parent conversation in the request, or, you can specify just the thread without the parent conversation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d76ed-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d76ed-104">Prerequisites</span></span>
<span data-ttu-id="d76ed-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="d76ed-105">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="d76ed-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d76ed-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/reply
```
## <a name="request-headers"></a><span data-ttu-id="d76ed-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d76ed-107">Request headers</span></span>
| <span data-ttu-id="d76ed-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d76ed-108">Header</span></span>       | <span data-ttu-id="d76ed-109">Valor</span><span class="sxs-lookup"><span data-stu-id="d76ed-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d76ed-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="d76ed-110">Authorization</span></span>  | <span data-ttu-id="d76ed-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d76ed-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="d76ed-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d76ed-113">Content-Type</span></span>  | <span data-ttu-id="d76ed-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d76ed-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d76ed-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d76ed-116">Request body</span></span>
<span data-ttu-id="d76ed-117">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d76ed-117">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d76ed-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d76ed-118">Parameter</span></span>    | <span data-ttu-id="d76ed-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="d76ed-119">Type</span></span>   |<span data-ttu-id="d76ed-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d76ed-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d76ed-121">post</span><span class="sxs-lookup"><span data-stu-id="d76ed-121">post</span></span>|[<span data-ttu-id="d76ed-122">post</span><span class="sxs-lookup"><span data-stu-id="d76ed-122">post</span></span>](../resources/post.md)|<span data-ttu-id="d76ed-123">La nueva publicación con que se responde.</span><span class="sxs-lookup"><span data-stu-id="d76ed-123">The new post that is being replied with.</span></span>|

## <a name="response"></a><span data-ttu-id="d76ed-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d76ed-124">Response</span></span>

<span data-ttu-id="d76ed-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d76ed-p104">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d76ed-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d76ed-127">Example</span></span>
<span data-ttu-id="d76ed-128">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d76ed-128">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d76ed-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d76ed-129">Request</span></span>
<span data-ttu-id="d76ed-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d76ed-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "conversationthread_reply"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/reply
Content-type: application/json
Content-length: 1131

{
  "post": {
    "body": {
      "contentType": "",
      "content": "content-value"
    }
  }
}
```

##### <a name="response"></a><span data-ttu-id="d76ed-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d76ed-131">Response</span></span>
<span data-ttu-id="d76ed-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d76ed-132">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conversationThread: reply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
