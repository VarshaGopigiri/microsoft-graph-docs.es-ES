# <a name="create-thread"></a><span data-ttu-id="9e92b-101">Crear hilo</span><span class="sxs-lookup"><span data-stu-id="9e92b-101">Create thread</span></span>

<span data-ttu-id="9e92b-102">Cree un nuevo hilo en la conversación especificada.</span><span class="sxs-lookup"><span data-stu-id="9e92b-102">Create a new thread in the specified conversation.</span></span> 

<span data-ttu-id="9e92b-p101">Se crean un hilo y una publicación como se ha especificado. Use [responder hilo](conversationthread_reply.md) para agregar publicaciones al hilo. O, si tiene el identificador de la publicación, también puede [responder](post_reply.md) a esa publicación en ese hilo.</span><span class="sxs-lookup"><span data-stu-id="9e92b-p101">A thread and post are created as specified. Use [reply thread](conversationthread_reply.md) to further post to that thread. Or, if you get the post ID, you can also [reply](post_reply.md) to that post in that thread.</span></span>

<span data-ttu-id="9e92b-106">Nota: También puede [crear primero un hilo para iniciar una nueva conversación](group_post_threads.md).</span><span class="sxs-lookup"><span data-stu-id="9e92b-106">Note: You can also [start a new conversation by first creating a thread](group_post_threads.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="9e92b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9e92b-107">Permissions</span></span>
<span data-ttu-id="9e92b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9e92b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9e92b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9e92b-110">Permission type</span></span>      | <span data-ttu-id="9e92b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9e92b-111">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="9e92b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9e92b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9e92b-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9e92b-113">Group.ReadWrite.All</span></span>    | 
|<span data-ttu-id="9e92b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9e92b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9e92b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9e92b-115">Not supported.</span></span>    | 
|<span data-ttu-id="9e92b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9e92b-116">Application</span></span> | <span data-ttu-id="9e92b-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9e92b-117">Group.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="9e92b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9e92b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/conversations/{id}/threads
```
## <a name="request-headers"></a><span data-ttu-id="9e92b-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9e92b-119">Request headers</span></span>
| <span data-ttu-id="9e92b-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="9e92b-120">Name</span></span>       | <span data-ttu-id="9e92b-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="9e92b-121">Type</span></span> | <span data-ttu-id="9e92b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e92b-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="9e92b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9e92b-123">Authorization</span></span>  | <span data-ttu-id="9e92b-124">string</span><span class="sxs-lookup"><span data-stu-id="9e92b-124">string</span></span>  | <span data-ttu-id="9e92b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9e92b-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9e92b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9e92b-127">Request body</span></span>
<span data-ttu-id="9e92b-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ConversationThread](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="9e92b-128">In the request body, supply a JSON representation of [ConversationThread](../resources/conversationthread.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="9e92b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9e92b-129">Response</span></span>

<span data-ttu-id="9e92b-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [ConversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9e92b-130">If successful, this method returns `201, Created` response code and [conversationThread](../resources/conversationthread.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9e92b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9e92b-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9e92b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9e92b-132">Request</span></span>
<span data-ttu-id="9e92b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9e92b-133">Here is an example of the request.</span></span>
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
<span data-ttu-id="9e92b-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [conversationThread](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="9e92b-134">In the request body, supply a JSON representation of [conversationThread](../resources/conversationthread.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="9e92b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9e92b-135">Response</span></span>

<span data-ttu-id="9e92b-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el `id` del nuevo hilo en el cuerpo de la respuesta. Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9e92b-p104">If successful, this method returns `201, Created` response code and the `id` of the new thread in the response body. Here is an example of the response.</span></span> 
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
