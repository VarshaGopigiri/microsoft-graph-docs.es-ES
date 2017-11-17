# <a name="conversationthread-resource-type"></a><span data-ttu-id="85c57-101">Tipo de recurso conversationThread</span><span class="sxs-lookup"><span data-stu-id="85c57-101">conversationThread resource type</span></span>
<span data-ttu-id="85c57-102">Un recurso conversationThread es una colección de [posts](post.md).</span><span class="sxs-lookup"><span data-stu-id="85c57-102">A conversationThread is a collection of [posts](post.md).</span></span>

<span data-ttu-id="85c57-p101">La colección de destinatarios de la última publicación son los destinatarios agregados del hilo completo. Un hilo puede tener una colección creciente de destinatarios. Se crea un hilo al eliminar un destinatario del hilo.</span><span class="sxs-lookup"><span data-stu-id="85c57-p101">The last post's recipients collection is the aggregated recipients of the entire thread. A thread can have a growing collection of recipients. A new thread is created when a recipient is removed from the thread.</span></span>

## <a name="methods"></a><span data-ttu-id="85c57-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="85c57-106">Methods</span></span>

| <span data-ttu-id="85c57-107">Método</span><span class="sxs-lookup"><span data-stu-id="85c57-107">Method</span></span>       | <span data-ttu-id="85c57-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85c57-108">Return Type</span></span>  |<span data-ttu-id="85c57-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="85c57-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="85c57-110">Enumerar hilos</span><span class="sxs-lookup"><span data-stu-id="85c57-110">List threads</span></span>](../api/group_list_threads.md) | <span data-ttu-id="85c57-111">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="85c57-111">[conversationThread](conversationthread.md) collection</span></span> |<span data-ttu-id="85c57-112">Obtenga todos los hilos de un grupo.</span><span class="sxs-lookup"><span data-stu-id="85c57-112">Get all the threads of a group.</span></span>|
|[<span data-ttu-id="85c57-113">Crear hilo</span><span class="sxs-lookup"><span data-stu-id="85c57-113">Create thread</span></span>](../api/group_post_threads.md) | [<span data-ttu-id="85c57-114">conversationThread</span><span class="sxs-lookup"><span data-stu-id="85c57-114">conversationThread</span></span>](conversationthread.md) |<span data-ttu-id="85c57-p102">Inicie una nueva conversación creando primero un hilo. Se crean una conversación, un hilo de conversación y una publicación en el grupo.</span><span class="sxs-lookup"><span data-stu-id="85c57-p102">Start a new conversation by first creating a thread. A new conversation, conversation thread, and post are created in the group.</span></span>|
|[<span data-ttu-id="85c57-117">Obtener conversationThread</span><span class="sxs-lookup"><span data-stu-id="85c57-117">Get conversationThread</span></span>](../api/conversationthread_get.md) | [<span data-ttu-id="85c57-118">conversationThread</span><span class="sxs-lookup"><span data-stu-id="85c57-118">conversationThread</span></span>](conversationthread.md) |<span data-ttu-id="85c57-119">Obtenga un hilo específico que pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="85c57-119">Get a specific thread that belongs to a group.</span></span> |
|[<span data-ttu-id="85c57-120">Actualizar</span><span class="sxs-lookup"><span data-stu-id="85c57-120">Update</span></span>](../api/conversationthread_update.md) | [<span data-ttu-id="85c57-121">conversationThread</span><span class="sxs-lookup"><span data-stu-id="85c57-121">conversationThread</span></span>](conversationthread.md)  |<span data-ttu-id="85c57-122">Actualice el objeto conversationThread.</span><span class="sxs-lookup"><span data-stu-id="85c57-122">Update conversationThread object.</span></span> |
|[<span data-ttu-id="85c57-123">Eliminar</span><span class="sxs-lookup"><span data-stu-id="85c57-123">Delete</span></span>](../api/conversationthread_delete.md) | <span data-ttu-id="85c57-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="85c57-124">None</span></span> |<span data-ttu-id="85c57-125">Elimine el objeto conversationThread.</span><span class="sxs-lookup"><span data-stu-id="85c57-125">Delete conversationThread object.</span></span> |
|[<span data-ttu-id="85c57-126">Responder</span><span class="sxs-lookup"><span data-stu-id="85c57-126">Reply</span></span>](../api/conversationthread_reply.md)|<span data-ttu-id="85c57-127">Ninguno</span><span class="sxs-lookup"><span data-stu-id="85c57-127">None</span></span>|<span data-ttu-id="85c57-128">Responda a este hilo mediante la creación de una nueva entidad Post.</span><span class="sxs-lookup"><span data-stu-id="85c57-128">Reply to this thread by creating a new Post entity.</span></span>|
|[<span data-ttu-id="85c57-129">Enumerar publicaciones</span><span class="sxs-lookup"><span data-stu-id="85c57-129">List Posts</span></span>](../api/conversationthread_list_posts.md) |<span data-ttu-id="85c57-130">Colección [post](post.md)</span><span class="sxs-lookup"><span data-stu-id="85c57-130">[post](post.md) collection</span></span>| <span data-ttu-id="85c57-131">Obtenga las publicaciones del hilo especificado.</span><span class="sxs-lookup"><span data-stu-id="85c57-131">Get the posts of the specified thread.</span></span> |

## <a name="properties"></a><span data-ttu-id="85c57-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85c57-132">Properties</span></span>
| <span data-ttu-id="85c57-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="85c57-133">Property</span></span>     | <span data-ttu-id="85c57-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="85c57-134">Type</span></span>   |<span data-ttu-id="85c57-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="85c57-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="85c57-136">id</span><span class="sxs-lookup"><span data-stu-id="85c57-136">id</span></span>|<span data-ttu-id="85c57-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="85c57-137">String</span></span>| <span data-ttu-id="85c57-138">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="85c57-138">Read-only.</span></span>|
|<span data-ttu-id="85c57-139">toRecipients</span><span class="sxs-lookup"><span data-stu-id="85c57-139">toRecipients</span></span>|<span data-ttu-id="85c57-140">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="85c57-140">[recipient](recipient.md) collection</span></span>|<span data-ttu-id="85c57-141">Los destinatarios Para: del hilo.</span><span class="sxs-lookup"><span data-stu-id="85c57-141">The To: recipients for the thread.</span></span>|
|<span data-ttu-id="85c57-142">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="85c57-142">ccRecipients</span></span>|<span data-ttu-id="85c57-143">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="85c57-143">[recipient](recipient.md) collection</span></span>|<span data-ttu-id="85c57-144">Los destinatarios CC: del hilo.</span><span class="sxs-lookup"><span data-stu-id="85c57-144">The Cc: recipients for the thread.</span></span>|
|<span data-ttu-id="85c57-145">topic</span><span class="sxs-lookup"><span data-stu-id="85c57-145">topic</span></span>|<span data-ttu-id="85c57-146">String</span><span class="sxs-lookup"><span data-stu-id="85c57-146">String</span></span>|<span data-ttu-id="85c57-p103">El tema de la conversación. Esta propiedad se puede establecer al crear la conversación, pero no se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="85c57-p103">The topic of the conversation. This property can be set when the conversation is created, but it cannot be updated.</span></span>||
|<span data-ttu-id="85c57-149">hasAttachments</span><span class="sxs-lookup"><span data-stu-id="85c57-149">hasAttachments</span></span>|<span data-ttu-id="85c57-150">Boolean</span><span class="sxs-lookup"><span data-stu-id="85c57-150">Boolean</span></span>|<span data-ttu-id="85c57-151">Indica si alguna de las publicaciones de este hilo tiene al menos un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="85c57-151">Indicates whether any of the posts within this thread has at least one attachment.</span></span>|
|<span data-ttu-id="85c57-152">lastDeliveredDateTime</span><span class="sxs-lookup"><span data-stu-id="85c57-152">lastDeliveredDateTime</span></span>|<span data-ttu-id="85c57-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="85c57-153">DateTimeOffset</span></span>|<span data-ttu-id="85c57-p104">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="85c57-p104">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="85c57-156">uniqueSenders</span><span class="sxs-lookup"><span data-stu-id="85c57-156">uniqueSenders</span></span>|<span data-ttu-id="85c57-157">Colección String</span><span class="sxs-lookup"><span data-stu-id="85c57-157">String collection</span></span>|<span data-ttu-id="85c57-158">Todos los usuarios que envían un mensaje a este hilo.</span><span class="sxs-lookup"><span data-stu-id="85c57-158">All the users that sent a message to this thread.</span></span>|
|<span data-ttu-id="85c57-159">preview</span><span class="sxs-lookup"><span data-stu-id="85c57-159">preview</span></span>|<span data-ttu-id="85c57-160">String</span><span class="sxs-lookup"><span data-stu-id="85c57-160">String</span></span>|<span data-ttu-id="85c57-161">Un breve resumen del cuerpo de la última publicación de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="85c57-161">A short summary from the body of the latest post in this converstaion.</span></span>|
|<span data-ttu-id="85c57-162">isLocked</span><span class="sxs-lookup"><span data-stu-id="85c57-162">isLocked</span></span>|<span data-ttu-id="85c57-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="85c57-163">Boolean</span></span>|<span data-ttu-id="85c57-164">Indica si el hilo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="85c57-164">Indicates if the thread is locked.</span></span>|

## <a name="relationships"></a><span data-ttu-id="85c57-165">Relaciones</span><span class="sxs-lookup"><span data-stu-id="85c57-165">Relationships</span></span>
| <span data-ttu-id="85c57-166">Relación</span><span class="sxs-lookup"><span data-stu-id="85c57-166">Relationship</span></span> | <span data-ttu-id="85c57-167">Tipo</span><span class="sxs-lookup"><span data-stu-id="85c57-167">Type</span></span>   |<span data-ttu-id="85c57-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="85c57-168">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="85c57-169">posts</span><span class="sxs-lookup"><span data-stu-id="85c57-169">posts</span></span>|<span data-ttu-id="85c57-170">Colección [post](post.md)</span><span class="sxs-lookup"><span data-stu-id="85c57-170">[post](post.md) collection</span></span>| <span data-ttu-id="85c57-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="85c57-p105">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="85c57-173">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="85c57-173">JSON representation</span></span>

<span data-ttu-id="85c57-174">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="85c57-174">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "posts"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.conversationThread"
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
