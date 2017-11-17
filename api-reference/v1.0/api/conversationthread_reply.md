# <a name="conversationthread-reply"></a><span data-ttu-id="60697-101">conversationThread: reply</span><span class="sxs-lookup"><span data-stu-id="60697-101">conversationThread: reply</span></span>

<span data-ttu-id="60697-p101">Responde a un hilo de una conversación de grupo y agrega una nueva publicación a la misma. Puede especificar la conversación primaria en la solicitud, o bien, especificar solo el hilo sin la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="60697-p101">Reply to a thread in a group conversation and add a new post to it. You can specify the parent conversation in the request, or, you can specify just the thread without the parent conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="60697-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="60697-104">Permissions</span></span>
<span data-ttu-id="60697-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="60697-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="60697-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="60697-107">Permission type</span></span>      | <span data-ttu-id="60697-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="60697-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="60697-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="60697-109">Delegated (work or school account)</span></span> | <span data-ttu-id="60697-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="60697-110">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="60697-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="60697-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="60697-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="60697-112">Not supported.</span></span>    |
|<span data-ttu-id="60697-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="60697-113">Application</span></span> | <span data-ttu-id="60697-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="60697-114">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="60697-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="60697-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/reply
```
## <a name="request-headers"></a><span data-ttu-id="60697-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="60697-116">Request headers</span></span>
| <span data-ttu-id="60697-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60697-117">Header</span></span>       | <span data-ttu-id="60697-118">Valor</span><span class="sxs-lookup"><span data-stu-id="60697-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="60697-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="60697-119">Authorization</span></span>  | <span data-ttu-id="60697-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="60697-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="60697-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="60697-122">Content-Type</span></span>  | <span data-ttu-id="60697-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="60697-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="60697-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="60697-125">Request body</span></span>
<span data-ttu-id="60697-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="60697-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="60697-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="60697-127">Parameter</span></span>    | <span data-ttu-id="60697-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="60697-128">Type</span></span>   |<span data-ttu-id="60697-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="60697-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="60697-130">post</span><span class="sxs-lookup"><span data-stu-id="60697-130">post</span></span>|[<span data-ttu-id="60697-131">post</span><span class="sxs-lookup"><span data-stu-id="60697-131">post</span></span>](../resources/post.md)|<span data-ttu-id="60697-132">La nueva publicación con que se responde.</span><span class="sxs-lookup"><span data-stu-id="60697-132">The new post that is being replied with.</span></span>|

## <a name="response"></a><span data-ttu-id="60697-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60697-133">Response</span></span>

<span data-ttu-id="60697-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60697-p105">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="60697-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="60697-136">Example</span></span>
<span data-ttu-id="60697-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="60697-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="60697-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="60697-138">Request</span></span>
<span data-ttu-id="60697-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="60697-139">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="60697-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60697-140">Response</span></span>
<span data-ttu-id="60697-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60697-141">Here is an example of the response.</span></span>
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
