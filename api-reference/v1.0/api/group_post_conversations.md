# <a name="create-conversation"></a><span data-ttu-id="f57b1-101">Create Conversation</span><span class="sxs-lookup"><span data-stu-id="f57b1-101">Create Conversation</span></span>

<span data-ttu-id="f57b1-102">Crea una nueva conversación incluyendo un hilo y una publicación.</span><span class="sxs-lookup"><span data-stu-id="f57b1-102">Create a new conversation by including a thread and a post.</span></span> 

<span data-ttu-id="f57b1-103">Use [responder hilo](conversationthread_reply.md) o [responder publicación](post_reply.md) para agregar publicaciones a la conversación.</span><span class="sxs-lookup"><span data-stu-id="f57b1-103">Use [reply thread](conversationthread_reply.md) or [reply post](post_reply.md) to further post to that conversation.</span></span>
## <a name="permissions"></a><span data-ttu-id="f57b1-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="f57b1-104">Permissions</span></span>
<span data-ttu-id="f57b1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f57b1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f57b1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f57b1-107">Permission type</span></span>      | <span data-ttu-id="f57b1-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f57b1-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f57b1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f57b1-109">Delegated (work or school account)</span></span> | <span data-ttu-id="f57b1-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f57b1-110">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="f57b1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f57b1-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f57b1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f57b1-112">Not supported.</span></span>    |
|<span data-ttu-id="f57b1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f57b1-113">Application</span></span> | <span data-ttu-id="f57b1-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f57b1-114">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f57b1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f57b1-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/conversations
```
## <a name="request-headers"></a><span data-ttu-id="f57b1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f57b1-116">Request headers</span></span>
| <span data-ttu-id="f57b1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f57b1-117">Header</span></span>       | <span data-ttu-id="f57b1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f57b1-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="f57b1-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="f57b1-119">Authorization</span></span>  | <span data-ttu-id="f57b1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f57b1-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="f57b1-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f57b1-122">Content-Type</span></span>  | <span data-ttu-id="f57b1-123">application/json</span><span class="sxs-lookup"><span data-stu-id="f57b1-123">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="f57b1-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f57b1-124">Request body</span></span>
<span data-ttu-id="f57b1-125">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [conversation](../resources/conversation.md) que contiene un [conversationThread](../resources/conversationThread.md) y un [post](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="f57b1-125">In the request body, supply a JSON representation of [conversation](../resources/conversation.md) object containing a [conversationThread](../resources/conversationThread.md) and a [post](../resources/post.md).</span></span>

## <a name="response"></a><span data-ttu-id="f57b1-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f57b1-126">Response</span></span>

<span data-ttu-id="f57b1-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [conversation](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f57b1-127">If successful, this method returns `201 Created` response code and [conversation](../resources/conversation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f57b1-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f57b1-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f57b1-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f57b1-129">Request</span></span>
<span data-ttu-id="f57b1-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f57b1-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_conversation_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/conversations
Content-type: application/json

{
  "topic": "New Conversation Topic",
  "threads": [{
    "posts": [{
      "body": {
        "contentType": "html",
        "content": "this is body content"
      },
      "newParticipants": [{
        "emailAddress": {
          "name": "Alex Darrow",
          "address": "alexd@contoso.com"
        }
      }]
    }]
  }]
}
```
##### <a name="response"></a><span data-ttu-id="f57b1-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f57b1-131">Response</span></span>
<span data-ttu-id="f57b1-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f57b1-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
  "topic": "topic-value",
  "hasAttachments": true,
  "lastDeliveredDateTime": "datetime-value",
  "uniqueSenders": [
    "uniqueSenders-value"
  ],
  "preview": "preview-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Conversation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->