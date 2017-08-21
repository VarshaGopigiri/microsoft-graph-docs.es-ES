# <a name="create-thread"></a><span data-ttu-id="54c99-101">Crear hilo</span><span class="sxs-lookup"><span data-stu-id="54c99-101">Create thread</span></span>

<span data-ttu-id="54c99-102">Cree un nuevo hilo en la conversación especificada.</span><span class="sxs-lookup"><span data-stu-id="54c99-102">Create a new thread in the specified conversation.</span></span> 

<span data-ttu-id="54c99-p101">Se crean un hilo y una publicación como se ha especificado. Use [responder hilo](conversationthread_reply.md) para agregar publicaciones al hilo. O, si tiene el identificador de la publicación, también puede [responder](post_reply.md) a esa publicación en ese hilo.</span><span class="sxs-lookup"><span data-stu-id="54c99-p101">A thread and post are created as specified. Use [reply thread](conversationthread_reply.md) to further post to that thread. Or, if you get the post ID, you can also [reply](post_reply.md) to that post in that thread.</span></span>

<span data-ttu-id="54c99-106">Nota: También puede [crear primero un hilo para iniciar una nueva conversación](group_post_threads.md).</span><span class="sxs-lookup"><span data-stu-id="54c99-106">Note: You can also [start a new conversation by first creating a thread](group_post_threads.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="54c99-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="54c99-107">Prerequisites</span></span>
<span data-ttu-id="54c99-108">Se requieren los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="54c99-108">The following **scopes** are required to execute this API: *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="54c99-109">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54c99-109">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/conversations/{id}/threads
```
## <a name="request-headers"></a><span data-ttu-id="54c99-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="54c99-110">Request headers</span></span>
| <span data-ttu-id="54c99-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="54c99-111">Name</span></span>       | <span data-ttu-id="54c99-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="54c99-112">Type</span></span> | <span data-ttu-id="54c99-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="54c99-113">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="54c99-114">Authorization</span><span class="sxs-lookup"><span data-stu-id="54c99-114">Authorization</span></span>  | <span data-ttu-id="54c99-115">string</span><span class="sxs-lookup"><span data-stu-id="54c99-115">string</span></span>  | <span data-ttu-id="54c99-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="54c99-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="54c99-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54c99-118">Request body</span></span>
<span data-ttu-id="54c99-119">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ConversationThread](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="54c99-119">In the request body, supply a JSON representation of [ConversationThread](../resources/conversationthread.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="54c99-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54c99-120">Response</span></span>

<span data-ttu-id="54c99-121">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [ConversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54c99-121">If successful, this method returns `201, Created` response code and [conversationThread](../resources/conversationthread.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="54c99-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54c99-122">Example</span></span>
##### <a name="request"></a><span data-ttu-id="54c99-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54c99-123">Request</span></span>
<span data-ttu-id="54c99-124">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54c99-124">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_conversationthread_from_conversation"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/conversations/{id}/threads
Content-type: application/json

{
  "topic": "topic-value",
  "posts": [{
      "body": {
        "contentType": "html",
        "content": "this is body content"
      }
  }]
}
```
<span data-ttu-id="54c99-125">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [conversationThread](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="54c99-125">In the request body, supply a JSON representation of [conversationThread](../resources/conversationthread.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="54c99-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54c99-126">Response</span></span>

<span data-ttu-id="54c99-p103">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el `id` del nuevo hilo en el cuerpo de la respuesta. Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54c99-p103">If successful, this method returns `201, Created` response code and the `id` of the new thread in the response body. Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 346

{
  "id": "thread-id-value"
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
