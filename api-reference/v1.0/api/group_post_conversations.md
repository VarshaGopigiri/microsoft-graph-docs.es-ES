# <a name="create-conversation"></a><span data-ttu-id="7f699-101">Create Conversation</span><span class="sxs-lookup"><span data-stu-id="7f699-101">Create Conversation</span></span>

<span data-ttu-id="7f699-102">Crea una nueva conversación incluyendo un hilo y una publicación.</span><span class="sxs-lookup"><span data-stu-id="7f699-102">Create a new conversation by including a thread and a post.</span></span> 

<span data-ttu-id="7f699-103">Use [responder hilo](conversationthread_reply.md) o [responder publicación](post_reply.md) para agregar publicaciones a la conversación.</span><span class="sxs-lookup"><span data-stu-id="7f699-103">Use [reply thread](conversationthread_reply.md) or [reply post](post_reply.md) to further post to that conversation.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7f699-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7f699-104">Prerequisites</span></span>
<span data-ttu-id="7f699-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="7f699-105">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="7f699-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7f699-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/conversations
```
## <a name="request-headers"></a><span data-ttu-id="7f699-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7f699-107">Request headers</span></span>
| <span data-ttu-id="7f699-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f699-108">Header</span></span>       | <span data-ttu-id="7f699-109">Valor</span><span class="sxs-lookup"><span data-stu-id="7f699-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7f699-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="7f699-110">Authorization</span></span>  | <span data-ttu-id="7f699-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7f699-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="7f699-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7f699-113">Content-Type</span></span>  | <span data-ttu-id="7f699-114">application/json</span><span class="sxs-lookup"><span data-stu-id="7f699-114">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7f699-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7f699-115">Request body</span></span>
<span data-ttu-id="7f699-116">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [conversation](../resources/conversation.md) que contiene un [conversationThread](../resources/conversationThread.md) y un [post](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="7f699-116">In the request body, supply a JSON representation of [conversation](../resources/conversation.md) object containing a [conversationThread](../resources/conversationThread.md) and a [post](../resources/post.md).</span></span>

## <a name="response"></a><span data-ttu-id="7f699-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f699-117">Response</span></span>

<span data-ttu-id="7f699-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [conversation](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f699-118">If successful, this method returns `201, Created` response code and [conversation](../resources/conversation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7f699-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7f699-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7f699-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7f699-120">Request</span></span>
<span data-ttu-id="7f699-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7f699-121">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="7f699-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f699-122">Response</span></span>
<span data-ttu-id="7f699-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7f699-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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