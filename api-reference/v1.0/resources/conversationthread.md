# <a name="conversationthread-resource-type"></a><span data-ttu-id="e7f6a-101">Tipo de recurso conversationThread</span><span class="sxs-lookup"><span data-stu-id="e7f6a-101">conversationThread resource type</span></span>
<span data-ttu-id="e7f6a-102">Un recurso conversationThread es una colección de [posts](post.md).</span><span class="sxs-lookup"><span data-stu-id="e7f6a-102">A conversationThread is a collection of [posts](post.md).</span></span>

<span data-ttu-id="e7f6a-p101">La colección de destinatarios de la última publicación son los destinatarios agregados del hilo completo. Un hilo puede tener una colección creciente de destinatarios. Se crea un hilo al eliminar un destinatario del hilo.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-p101">The last post's recipients collection is the aggregated recipients of the entire thread. A thread can have a growing collection of recipients. A new thread is created when a recipient is removed from the thread.</span></span>

## <a name="methods"></a><span data-ttu-id="e7f6a-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="e7f6a-106">Methods</span></span>

| <span data-ttu-id="e7f6a-107">Método</span><span class="sxs-lookup"><span data-stu-id="e7f6a-107">Method</span></span>       | <span data-ttu-id="e7f6a-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7f6a-108">Return Type</span></span>  |<span data-ttu-id="e7f6a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7f6a-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e7f6a-110">Enumerar hilos</span><span class="sxs-lookup"><span data-stu-id="e7f6a-110">List threads</span></span>](../api/group_list_threads.md) | <span data-ttu-id="e7f6a-111">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="e7f6a-111">[conversationThread](conversationthread.md) collection</span></span> |<span data-ttu-id="e7f6a-112">Obtenga todos los hilos de un grupo.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-112">Get all the threads of a group.</span></span>|
|[<span data-ttu-id="e7f6a-113">Crear hilo</span><span class="sxs-lookup"><span data-stu-id="e7f6a-113">Create thread</span></span>](../api/group_post_threads.md) | [<span data-ttu-id="e7f6a-114">conversationThread</span><span class="sxs-lookup"><span data-stu-id="e7f6a-114">conversationThread</span></span>](conversationthread.md) |<span data-ttu-id="e7f6a-p102">Inicie una nueva conversación creando primero un hilo. Se crean una conversación, un hilo de conversación y una publicación en el grupo.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-p102">Start a new conversation by first creating a thread. A new conversation, conversation thread, and post are created in the group.</span></span>|
|[<span data-ttu-id="e7f6a-117">Obtener conversationThread</span><span class="sxs-lookup"><span data-stu-id="e7f6a-117">Get conversationThread</span></span>](../api/conversationthread_get.md) | [<span data-ttu-id="e7f6a-118">conversationThread</span><span class="sxs-lookup"><span data-stu-id="e7f6a-118">conversationThread</span></span>](conversationthread.md) |<span data-ttu-id="e7f6a-119">Obtenga un hilo específico que pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-119">Get a specific thread that belongs to a group.</span></span> |
|[<span data-ttu-id="e7f6a-120">Actualizar</span><span class="sxs-lookup"><span data-stu-id="e7f6a-120">Update</span></span>](../api/conversationthread_update.md) | [<span data-ttu-id="e7f6a-121">conversationThread</span><span class="sxs-lookup"><span data-stu-id="e7f6a-121">conversationThread</span></span>](conversationthread.md)  |<span data-ttu-id="e7f6a-122">Actualice el objeto conversationThread.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-122">Update conversationThread object.</span></span> |
|[<span data-ttu-id="e7f6a-123">Eliminar</span><span class="sxs-lookup"><span data-stu-id="e7f6a-123">Delete</span></span>](../api/conversationthread_delete.md) | <span data-ttu-id="e7f6a-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e7f6a-124">None</span></span> |<span data-ttu-id="e7f6a-125">Elimine el objeto conversationThread.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-125">Delete conversationThread object.</span></span> |
|[<span data-ttu-id="e7f6a-126">Responder</span><span class="sxs-lookup"><span data-stu-id="e7f6a-126">Reply</span></span>](../api/conversationthread_reply.md)|<span data-ttu-id="e7f6a-127">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e7f6a-127">None</span></span>|<span data-ttu-id="e7f6a-128">Responda a este hilo mediante la creación de una nueva entidad Post.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-128">Reply to this thread by creating a new Post entity.</span></span>|
|[<span data-ttu-id="e7f6a-129">Enumerar publicaciones</span><span class="sxs-lookup"><span data-stu-id="e7f6a-129">List Posts</span></span>](../api/conversationthread_list_posts.md) |<span data-ttu-id="e7f6a-130">Colección [post](post.md)</span><span class="sxs-lookup"><span data-stu-id="e7f6a-130">[post](post.md) collection</span></span>| <span data-ttu-id="e7f6a-131">Obtenga las publicaciones del hilo especificado.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-131">Get the posts of the specified thread.</span></span> |

## <a name="properties"></a><span data-ttu-id="e7f6a-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7f6a-132">Properties</span></span>
| <span data-ttu-id="e7f6a-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7f6a-133">Property</span></span>     | <span data-ttu-id="e7f6a-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7f6a-134">Type</span></span>   |<span data-ttu-id="e7f6a-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7f6a-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e7f6a-136">id</span><span class="sxs-lookup"><span data-stu-id="e7f6a-136">id</span></span>|<span data-ttu-id="e7f6a-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="e7f6a-137">String</span></span>| <span data-ttu-id="e7f6a-138">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-138">Read-only.</span></span>|
|<span data-ttu-id="e7f6a-139">toRecipients</span><span class="sxs-lookup"><span data-stu-id="e7f6a-139">toRecipients</span></span>|<span data-ttu-id="e7f6a-140">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="e7f6a-140">[recipient](recipient.md) collection</span></span>|<span data-ttu-id="e7f6a-141">Los destinatarios Para: del hilo.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-141">The To: recipients for the thread.</span></span>|
|<span data-ttu-id="e7f6a-142">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="e7f6a-142">ccRecipients</span></span>|<span data-ttu-id="e7f6a-143">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="e7f6a-143">[recipient](recipient.md) collection</span></span>|<span data-ttu-id="e7f6a-144">Los destinatarios CC: del hilo.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-144">The Cc: recipients for the thread.</span></span>|
|<span data-ttu-id="e7f6a-145">topic</span><span class="sxs-lookup"><span data-stu-id="e7f6a-145">topic</span></span>|<span data-ttu-id="e7f6a-146">String</span><span class="sxs-lookup"><span data-stu-id="e7f6a-146">String</span></span>|<span data-ttu-id="e7f6a-p103">El tema de la conversación. Esta propiedad se puede establecer al crear la conversación, pero no se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-p103">The topic of the conversation. This property can be set when the conversation is created, but it cannot be updated.</span></span>||
|<span data-ttu-id="e7f6a-149">hasAttachments</span><span class="sxs-lookup"><span data-stu-id="e7f6a-149">hasAttachments</span></span>|<span data-ttu-id="e7f6a-150">Boolean</span><span class="sxs-lookup"><span data-stu-id="e7f6a-150">Boolean</span></span>|<span data-ttu-id="e7f6a-151">Indica si alguna de las publicaciones de este hilo tiene al menos un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-151">Indicates whether any of the posts within this thread has at least one attachment.</span></span>|
|<span data-ttu-id="e7f6a-152">lastDeliveredDateTime</span><span class="sxs-lookup"><span data-stu-id="e7f6a-152">lastDeliveredDateTime</span></span>|<span data-ttu-id="e7f6a-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e7f6a-153">DateTimeOffset</span></span>|<span data-ttu-id="e7f6a-p104">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="e7f6a-p104">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="e7f6a-156">uniqueSenders</span><span class="sxs-lookup"><span data-stu-id="e7f6a-156">uniqueSenders</span></span>|<span data-ttu-id="e7f6a-157">Colección String</span><span class="sxs-lookup"><span data-stu-id="e7f6a-157">String collection</span></span>|<span data-ttu-id="e7f6a-158">Todos los usuarios que envían un mensaje a este hilo.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-158">All the users that sent a message to this thread.</span></span>|
|<span data-ttu-id="e7f6a-159">preview</span><span class="sxs-lookup"><span data-stu-id="e7f6a-159">preview</span></span>|<span data-ttu-id="e7f6a-160">String</span><span class="sxs-lookup"><span data-stu-id="e7f6a-160">String</span></span>|<span data-ttu-id="e7f6a-161">Un breve resumen del cuerpo de la última publicación de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-161">A short summary from the body of the latest post in this converstaion.</span></span>|
|<span data-ttu-id="e7f6a-162">isLocked</span><span class="sxs-lookup"><span data-stu-id="e7f6a-162">isLocked</span></span>|<span data-ttu-id="e7f6a-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="e7f6a-163">Boolean</span></span>|<span data-ttu-id="e7f6a-164">Indica si el hilo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-164">Indicates if the thread is locked.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e7f6a-165">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e7f6a-165">Relationships</span></span>
| <span data-ttu-id="e7f6a-166">Relación</span><span class="sxs-lookup"><span data-stu-id="e7f6a-166">Relationship</span></span> | <span data-ttu-id="e7f6a-167">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7f6a-167">Type</span></span>   |<span data-ttu-id="e7f6a-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7f6a-168">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e7f6a-169">posts</span><span class="sxs-lookup"><span data-stu-id="e7f6a-169">posts</span></span>|<span data-ttu-id="e7f6a-170">Colección [post](post.md)</span><span class="sxs-lookup"><span data-stu-id="e7f6a-170">[post](post.md) collection</span></span>| <span data-ttu-id="e7f6a-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-p105">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e7f6a-173">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e7f6a-173">JSON representation</span></span>

<span data-ttu-id="e7f6a-174">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e7f6a-174">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "posts"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.conversationThread",
  "@odata.annotations": [
    {
      "property": "posts",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "insertable": false,
        "searchable": false,
        "updatable": false
      }
    }
  ]
}-->

```json
{
  "ccRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "hasAttachments": true,
  "id": "string (identifier)",
  "isLocked": true,
  "lastDeliveredDateTime": "String (timestamp)",
  "preview": "string",
  "toRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "topic": "string",
  "uniqueSenders": ["string"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conversationThread resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
