# <a name="post-reply"></a><span data-ttu-id="ea1a5-101">post: reply</span><span class="sxs-lookup"><span data-stu-id="ea1a5-101">post: reply</span></span>

<span data-ttu-id="ea1a5-p101">Responde a una publicación y agrega una nueva publicación al hilo especificado de una conversación de grupo. Puede especificar la conversación y el hilo primarios en la solicitud, o bien, especificar solo el hilo primario sin la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="ea1a5-p101">Reply to a post and add a new post to the specified thread in a group conversation. You can specify both the parent conversation and thread in the request, or, you can specify just the parent thread without the parent conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="ea1a5-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="ea1a5-104">Permissions</span></span>
<span data-ttu-id="ea1a5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ea1a5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ea1a5-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea1a5-107">Permission type</span></span>      | <span data-ttu-id="ea1a5-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea1a5-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ea1a5-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea1a5-109">Delegated (work or school account)</span></span> | <span data-ttu-id="ea1a5-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea1a5-110">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ea1a5-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea1a5-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ea1a5-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea1a5-112">Not supported.</span></span>    |
|<span data-ttu-id="ea1a5-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea1a5-113">Application</span></span> | <span data-ttu-id="ea1a5-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea1a5-114">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ea1a5-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea1a5-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/posts/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/reply

```
## <a name="request-headers"></a><span data-ttu-id="ea1a5-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea1a5-116">Request headers</span></span>
| <span data-ttu-id="ea1a5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea1a5-117">Header</span></span>       | <span data-ttu-id="ea1a5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ea1a5-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ea1a5-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="ea1a5-119">Authorization</span></span>  | <span data-ttu-id="ea1a5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ea1a5-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ea1a5-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea1a5-122">Request body</span></span>
<span data-ttu-id="ea1a5-123">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="ea1a5-123">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="ea1a5-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ea1a5-124">Parameter</span></span>    | <span data-ttu-id="ea1a5-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea1a5-125">Type</span></span>   |<span data-ttu-id="ea1a5-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea1a5-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ea1a5-127">post</span><span class="sxs-lookup"><span data-stu-id="ea1a5-127">post</span></span>|[<span data-ttu-id="ea1a5-128">post</span><span class="sxs-lookup"><span data-stu-id="ea1a5-128">post</span></span>](../resources/post.md)|<span data-ttu-id="ea1a5-129">La nueva publicación con que se responde.</span><span class="sxs-lookup"><span data-stu-id="ea1a5-129">The new post that is being replied with.</span></span>|

## <a name="response"></a><span data-ttu-id="ea1a5-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea1a5-130">Response</span></span>

<span data-ttu-id="ea1a5-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea1a5-p104">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ea1a5-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea1a5-133">Example</span></span>
<span data-ttu-id="ea1a5-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ea1a5-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="ea1a5-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea1a5-135">Request</span></span>
<span data-ttu-id="ea1a5-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea1a5-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_reply"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}/reply
Content-type: application/json
Content-length: 1131

{
  "post": {
    "body": {
      "contentType": "",
      "content": "content-value"
    },
    "receivedDateTime": "datetime-value",
    "hasAttachments": true,
    "from": {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    },
    "sender": {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    },
    "conversationThreadId": "conversationThreadId-value",
    "newParticipants": [
      {
        "emailAddress": {
          "name": "name-value",
          "address": "address-value"
        }
      }
    ],
    "conversationId": "conversationId-value",
    "createdDateTime": "datetime-value",
    "lastModifiedDateTime": "datetime-value",
    "changeKey": "changeKey-value",
    "categories": [
      "categories-value"
    ],
    "id": "id-value",
    "inReplyTo": {
    },
    "attachments": [
      {
        "lastModifiedDateTime": "datetime-value",
        "name": "name-value",
        "contentType": "contentType-value",
        "size": 99,
        "isInline": true,
        "id": "id-value"
      }
    ]
  }
}
```

##### <a name="response"></a><span data-ttu-id="ea1a5-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea1a5-137">Response</span></span>
##### <a name="response"></a><span data-ttu-id="ea1a5-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea1a5-138">Response</span></span>
<span data-ttu-id="ea1a5-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea1a5-139">Here is an example of the response.</span></span>
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
  "description": "post: reply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
