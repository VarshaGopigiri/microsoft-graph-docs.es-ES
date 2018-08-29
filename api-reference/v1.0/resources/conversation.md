# <a name="conversation-resource-type"></a><span data-ttu-id="cf876-101">Tipo de recurso conversation</span><span class="sxs-lookup"><span data-stu-id="cf876-101">conversation resource type</span></span>

<span data-ttu-id="cf876-p101">Una conversación es una colección de [hilos](conversationthread.md) y un hilo contiene publicaciones de ese hilo. Todos los hilos y publicaciones de una conversación comparten el mismo asunto.</span><span class="sxs-lookup"><span data-stu-id="cf876-p101">A conversation is a collection of [threads](conversationthread.md), and a thread contains posts to that thread. All threads and posts in a conversation share the same subject.</span></span>

## <a name="methods"></a><span data-ttu-id="cf876-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf876-104">Methods</span></span>

| <span data-ttu-id="cf876-105">Método</span><span class="sxs-lookup"><span data-stu-id="cf876-105">Method</span></span>       | <span data-ttu-id="cf876-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf876-106">Return Type</span></span>  |<span data-ttu-id="cf876-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf876-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="cf876-108">Enumerar conversaciones</span><span class="sxs-lookup"><span data-stu-id="cf876-108">List conversations</span></span>](../api/group_list_conversations.md) | <span data-ttu-id="cf876-109">Colección [conversation](conversation.md)</span><span class="sxs-lookup"><span data-stu-id="cf876-109">[conversation](conversation.md) collection</span></span> |<span data-ttu-id="cf876-110">Obtenga la lista de conversaciones en este grupo.</span><span class="sxs-lookup"><span data-stu-id="cf876-110">Get the list of conversations in this group.</span></span>|
|[<span data-ttu-id="cf876-111">Crear</span><span class="sxs-lookup"><span data-stu-id="cf876-111">Create</span></span>](../api/group_post_conversations.md) |[<span data-ttu-id="cf876-112">conversation</span><span class="sxs-lookup"><span data-stu-id="cf876-112">conversation</span></span>](conversation.md)| <span data-ttu-id="cf876-113">Cree una conversación al incluir un hilo y una publicación.</span><span class="sxs-lookup"><span data-stu-id="cf876-113">Create a new conversation by including a thread and a post.</span></span>|
|[<span data-ttu-id="cf876-114">Obtener conversación</span><span class="sxs-lookup"><span data-stu-id="cf876-114">Get conversation</span></span>](../api/conversation_get.md) | [<span data-ttu-id="cf876-115">conversation</span><span class="sxs-lookup"><span data-stu-id="cf876-115">conversation</span></span>](conversation.md) |<span data-ttu-id="cf876-116">Lea las propiedades y las relaciones del objeto de conversación.</span><span class="sxs-lookup"><span data-stu-id="cf876-116">Read properties and relationships of conversation object.</span></span>|
|[<span data-ttu-id="cf876-117">Eliminar</span><span class="sxs-lookup"><span data-stu-id="cf876-117">Delete</span></span>](../api/conversation_delete.md) | <span data-ttu-id="cf876-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cf876-118">None</span></span> |<span data-ttu-id="cf876-119">Elimine el objeto de conversación.</span><span class="sxs-lookup"><span data-stu-id="cf876-119">Delete conversation object.</span></span> |
|[<span data-ttu-id="cf876-120">Enumerar hilos de conversación</span><span class="sxs-lookup"><span data-stu-id="cf876-120">List conversation threads</span></span>](../api/conversation_list_threads.md) |<span data-ttu-id="cf876-121">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="cf876-121">[conversationThread](conversationthread.md) collection</span></span>| <span data-ttu-id="cf876-122">Obtenga todos los hilos de una conversación de grupo.</span><span class="sxs-lookup"><span data-stu-id="cf876-122">Get all the threads in a group conversation.</span></span>|
|[<span data-ttu-id="cf876-123">Crear hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="cf876-123">Create conversation thread</span></span>](../api/conversation_post_threads.md) |<span data-ttu-id="cf876-124">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="cf876-124">[conversationThread](conversationthread.md) collection</span></span>| <span data-ttu-id="cf876-125">Cree un hilo en la conversación especificada.</span><span class="sxs-lookup"><span data-stu-id="cf876-125">Create a thread in the specified conversation.</span></span>|

## <a name="properties"></a><span data-ttu-id="cf876-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf876-126">Properties</span></span>
| <span data-ttu-id="cf876-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf876-127">Property</span></span>     | <span data-ttu-id="cf876-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf876-128">Type</span></span>   |<span data-ttu-id="cf876-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf876-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cf876-130">hasAttachments</span><span class="sxs-lookup"><span data-stu-id="cf876-130">hasAttachments</span></span>|<span data-ttu-id="cf876-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="cf876-131">Boolean</span></span>|<span data-ttu-id="cf876-132">Indica si alguna de las publicaciones de esta conversación tiene al menos un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="cf876-132">Indicates whether any of the posts within this Conversation has at least one attachment.</span></span>|
|<span data-ttu-id="cf876-133">id</span><span class="sxs-lookup"><span data-stu-id="cf876-133">id</span></span>|<span data-ttu-id="cf876-134">String</span><span class="sxs-lookup"><span data-stu-id="cf876-134">String</span></span>|<span data-ttu-id="cf876-p102">El identificador único de las conversaciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cf876-p102">The conversations's unique identifier. Read-only.</span></span>|
|<span data-ttu-id="cf876-137">lastDeliveredDateTime</span><span class="sxs-lookup"><span data-stu-id="cf876-137">lastDeliveredDateTime</span></span>|<span data-ttu-id="cf876-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf876-138">DateTimeOffset</span></span>|<span data-ttu-id="cf876-p103">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="cf876-p103">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="cf876-141">preview</span><span class="sxs-lookup"><span data-stu-id="cf876-141">preview</span></span>|<span data-ttu-id="cf876-142">String</span><span class="sxs-lookup"><span data-stu-id="cf876-142">String</span></span>|<span data-ttu-id="cf876-143">Un breve resumen del cuerpo de la última publicación de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="cf876-143">A short summary from the body of the latest post in this converstaion.</span></span>|
|<span data-ttu-id="cf876-144">topic</span><span class="sxs-lookup"><span data-stu-id="cf876-144">topic</span></span>|<span data-ttu-id="cf876-145">String</span><span class="sxs-lookup"><span data-stu-id="cf876-145">String</span></span>|<span data-ttu-id="cf876-p104">El tema de la conversación. Esta propiedad se puede establecer al crear la conversación, pero no se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="cf876-p104">The topic of the conversation. This property can be set when the conversation is created, but it cannot be updated.</span></span>|
|<span data-ttu-id="cf876-148">uniqueSenders</span><span class="sxs-lookup"><span data-stu-id="cf876-148">uniqueSenders</span></span>|<span data-ttu-id="cf876-149">Colección String</span><span class="sxs-lookup"><span data-stu-id="cf876-149">String collection</span></span>|<span data-ttu-id="cf876-150">Todos los usuarios que envían un mensaje a esta conversación.</span><span class="sxs-lookup"><span data-stu-id="cf876-150">All the users that sent a message to this Conversation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="cf876-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cf876-151">Relationships</span></span>
| <span data-ttu-id="cf876-152">Relación</span><span class="sxs-lookup"><span data-stu-id="cf876-152">Relationship</span></span> | <span data-ttu-id="cf876-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf876-153">Type</span></span>   |<span data-ttu-id="cf876-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf876-154">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cf876-155">threads</span><span class="sxs-lookup"><span data-stu-id="cf876-155">threads</span></span>|<span data-ttu-id="cf876-156">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="cf876-156">[conversationThread](conversationthread.md) collection</span></span>|<span data-ttu-id="cf876-p105">Una colección de todos los hilos de la conversación. Una propiedad de navegación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="cf876-p105">A collection of all the conversation threads in the conversation. A navigation property. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="cf876-161">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cf876-161">JSON representation</span></span>

<span data-ttu-id="cf876-162">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="cf876-162">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "threads"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.conversation",
  "@odata.annotations": [
    {
      "property": "threads",
      "capabilities": {
        "changeTracking": false,
        "searchable": false
      }
    }
  ]
}-->

```json
{
  "hasAttachments": true,
  "id": "string (identifier)",
  "lastDeliveredDateTime": "String (timestamp)",
  "preview": "string",
  "topic": "string",
  "uniqueSenders": ["string"],

  "threads": [{"@odata.type": "microsoft.graph.conversationThread"}]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conversation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
