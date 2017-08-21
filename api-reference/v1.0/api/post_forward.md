# <a name="post-forward"></a><span data-ttu-id="92b93-101">post: forward</span><span class="sxs-lookup"><span data-stu-id="92b93-101">post: forward</span></span>

<span data-ttu-id="92b93-p101">Reenvía una publicación a un destinatario. Puede especificar la conversación y el hilo primarios en la solicitud, o bien, especificar solo el hilo primario sin la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="92b93-p101">Forward a post to a recipient. You can specify both the parent conversation and thread in the request, or, you can specify just the parent thread without the parent conversation.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="92b93-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="92b93-104">Prerequisites</span></span>
<span data-ttu-id="92b93-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="92b93-105">One of the following **scopes** is required to execute this API:</span></span>

<span data-ttu-id="92b93-106">*Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="92b93-106">*Group.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="92b93-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="92b93-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/posts/{id}/forward
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/forward

```
## <a name="request-headers"></a><span data-ttu-id="92b93-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="92b93-108">Request headers</span></span>
| <span data-ttu-id="92b93-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92b93-109">Header</span></span>       | <span data-ttu-id="92b93-110">Valor</span><span class="sxs-lookup"><span data-stu-id="92b93-110">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="92b93-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="92b93-111">Authorization</span></span>  | <span data-ttu-id="92b93-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="92b93-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="92b93-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="92b93-114">Request body</span></span>
<span data-ttu-id="92b93-115">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="92b93-115">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="92b93-116">Parámetro</span><span class="sxs-lookup"><span data-stu-id="92b93-116">Parameter</span></span>    | <span data-ttu-id="92b93-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="92b93-117">Type</span></span>   |<span data-ttu-id="92b93-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="92b93-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="92b93-119">comment</span><span class="sxs-lookup"><span data-stu-id="92b93-119">comment</span></span>|<span data-ttu-id="92b93-120">String</span><span class="sxs-lookup"><span data-stu-id="92b93-120">String</span></span>|<span data-ttu-id="92b93-121">Comentario opcional que se envía junto con la publicación.</span><span class="sxs-lookup"><span data-stu-id="92b93-121">Optional comment that is forwarded together with the post.</span></span>|
|<span data-ttu-id="92b93-122">toRecipients</span><span class="sxs-lookup"><span data-stu-id="92b93-122">toRecipients</span></span>|<span data-ttu-id="92b93-123">Colección [recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="92b93-123">[recipient](../resources/recipient.md) collection</span></span>|<span data-ttu-id="92b93-124">Destinatarios a los que se ha reenviado el encadenado de hilos.</span><span class="sxs-lookup"><span data-stu-id="92b93-124">The recipients to whom the threaded is forwarded to.</span></span>|

## <a name="response"></a><span data-ttu-id="92b93-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="92b93-125">Response</span></span>

<span data-ttu-id="92b93-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="92b93-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="92b93-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="92b93-128">Example</span></span>
<span data-ttu-id="92b93-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="92b93-129">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="92b93-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="92b93-130">Request</span></span>
<span data-ttu-id="92b93-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="92b93-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_forward"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}/forward
Content-type: application/json
Content-length: 166

{
  "comment": "comment-value",
  "toRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="92b93-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="92b93-132">Response</span></span>
<span data-ttu-id="92b93-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="92b93-133">Here is an example of the response.</span></span>
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
  "description": "post: forward",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
