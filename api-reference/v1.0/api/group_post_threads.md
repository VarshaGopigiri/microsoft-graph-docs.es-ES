# <a name="create-conversation-thread"></a><span data-ttu-id="aaf5b-101">Crear hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="aaf5b-101">Create conversation thread</span></span>

<span data-ttu-id="aaf5b-102">Inicie una nueva conversación de grupo creando primero un hilo de conversación.</span><span class="sxs-lookup"><span data-stu-id="aaf5b-102">Start a new group conversation by first creating a thread.</span></span> 

<span data-ttu-id="aaf5b-p101">Se crea una conversación, un hilo de conversación y una publicación en el grupo. Use [responder hilo](conversationthread_reply.md) o [responder publicación](post_reply.md) para agregar publicaciones al hilo.</span><span class="sxs-lookup"><span data-stu-id="aaf5b-p101">A new conversation, conversation thread, and post are created in the group. Use [reply thread](conversationthread_reply.md) or [reply post](post_reply.md) to further post to that thread.</span></span>

<span data-ttu-id="aaf5b-105">Nota: También puede [iniciar un nuevo hilo en una conversación ya existente](conversation_post_threads.md).</span><span class="sxs-lookup"><span data-stu-id="aaf5b-105">Note: You can also [start a new thread in an existing conversation](conversation_post_threads.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="aaf5b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aaf5b-106">Prerequisites</span></span>
<span data-ttu-id="aaf5b-107">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="aaf5b-107">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="aaf5b-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aaf5b-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads
```
## <a name="request-headers"></a><span data-ttu-id="aaf5b-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aaf5b-109">Request headers</span></span>
| <span data-ttu-id="aaf5b-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aaf5b-110">Header</span></span>       | <span data-ttu-id="aaf5b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="aaf5b-111">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="aaf5b-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="aaf5b-112">Authorization</span></span>  | <span data-ttu-id="aaf5b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aaf5b-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="aaf5b-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="aaf5b-115">Content-Type</span></span>  | <span data-ttu-id="aaf5b-116">application/json</span><span class="sxs-lookup"><span data-stu-id="aaf5b-116">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="aaf5b-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aaf5b-117">Request body</span></span>
<span data-ttu-id="aaf5b-118">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [conversationThread](../resources/conversationthread.md) que contiene un [post](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="aaf5b-118">In the request body, supply a JSON representation of [conversationThread](../resources/conversationthread.md) object containing a [post](../resources/post.md).</span></span>

## <a name="response"></a><span data-ttu-id="aaf5b-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aaf5b-119">Response</span></span>

<span data-ttu-id="aaf5b-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [conversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aaf5b-120">If successful, this method returns `201, Created` response code and [conversationThread](../resources/conversationthread.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="aaf5b-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aaf5b-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="aaf5b-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aaf5b-122">Request</span></span>
<span data-ttu-id="aaf5b-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aaf5b-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_conversationthread_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads
Content-type: application/json

{
  "topic": "New Conversation Thread Topic",
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
}
```
##### <a name="response"></a><span data-ttu-id="aaf5b-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aaf5b-124">Response</span></span>
<span data-ttu-id="aaf5b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aaf5b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread"
} -->
```http
HTTP/1.1 201 OK
Content-type: application/json
Content-length: 419

{
  "toRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ],
  "topic": "topic-value",
  "hasAttachments": true,
  "lastDeliveredDateTime": "datetime-value",
  "uniqueSenders": [
    "uniqueSenders-value"
  ],
  "ccRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create thread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
