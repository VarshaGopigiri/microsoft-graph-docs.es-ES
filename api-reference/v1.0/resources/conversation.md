# <a name="conversation-resource-type"></a><span data-ttu-id="ee246-101">Tipo de recurso conversation</span><span class="sxs-lookup"><span data-stu-id="ee246-101">conversation resource type</span></span>

<span data-ttu-id="ee246-p101">Una conversación es una colección de [hilos](conversationthread.md) y un hilo contiene publicaciones de ese hilo. Todos los hilos y publicaciones de una conversación comparten el mismo asunto.</span><span class="sxs-lookup"><span data-stu-id="ee246-p101">A conversation is a collection of [threads](conversationthread.md), and a thread contains posts to that thread. All threads and posts in a conversation share the same subject.</span></span>

<span data-ttu-id="ee246-104">Este recurso es compatible con la suscripción a [las notificaciones de cambios](../../../concepts/webhooks.md).</span><span class="sxs-lookup"><span data-stu-id="ee246-104">This resource supports subscribing to [change notifications](../../../concepts/webhooks.md).</span></span>

## <a name="methods"></a><span data-ttu-id="ee246-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="ee246-105">Methods</span></span>

| <span data-ttu-id="ee246-106">Método</span><span class="sxs-lookup"><span data-stu-id="ee246-106">Method</span></span>       | <span data-ttu-id="ee246-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee246-107">Return Type</span></span>  |<span data-ttu-id="ee246-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee246-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ee246-109">Enumerar conversaciones</span><span class="sxs-lookup"><span data-stu-id="ee246-109">List conversations</span></span>](../api/group_list_conversations.md) | <span data-ttu-id="ee246-110">Colección [conversation](conversation.md)</span><span class="sxs-lookup"><span data-stu-id="ee246-110">[conversation](conversation.md) collection</span></span> |<span data-ttu-id="ee246-111">Obtenga la lista de conversaciones en este grupo.</span><span class="sxs-lookup"><span data-stu-id="ee246-111">Get the list of conversations in this group.</span></span>|
|[<span data-ttu-id="ee246-112">Crear</span><span class="sxs-lookup"><span data-stu-id="ee246-112">Create</span></span>](../api/group_post_conversations.md) |[<span data-ttu-id="ee246-113">conversation</span><span class="sxs-lookup"><span data-stu-id="ee246-113">conversation</span></span>](conversation.md)| <span data-ttu-id="ee246-114">Cree una conversación al incluir un hilo y una publicación.</span><span class="sxs-lookup"><span data-stu-id="ee246-114">Create a new conversation by including a thread and a post.</span></span>|
|[<span data-ttu-id="ee246-115">Obtener conversación</span><span class="sxs-lookup"><span data-stu-id="ee246-115">Get conversation</span></span>](../api/conversation_get.md) | [<span data-ttu-id="ee246-116">conversation</span><span class="sxs-lookup"><span data-stu-id="ee246-116">conversation</span></span>](conversation.md) |<span data-ttu-id="ee246-117">Lea las propiedades y las relaciones del objeto de conversación.</span><span class="sxs-lookup"><span data-stu-id="ee246-117">Read properties and relationships of conversation object.</span></span>|
|[<span data-ttu-id="ee246-118">Eliminar</span><span class="sxs-lookup"><span data-stu-id="ee246-118">Delete</span></span>](../api/conversation_delete.md) | <span data-ttu-id="ee246-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ee246-119">None</span></span> |<span data-ttu-id="ee246-120">Elimine el objeto de conversación.</span><span class="sxs-lookup"><span data-stu-id="ee246-120">Delete conversation object.</span></span> |
|[<span data-ttu-id="ee246-121">Enumerar hilos de conversación</span><span class="sxs-lookup"><span data-stu-id="ee246-121">List conversation threads</span></span>](../api/conversation_list_threads.md) |<span data-ttu-id="ee246-122">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="ee246-122">[conversationThread](conversationthread.md) collection</span></span>| <span data-ttu-id="ee246-123">Obtenga todos los hilos de una conversación de grupo.</span><span class="sxs-lookup"><span data-stu-id="ee246-123">Get all the threads in a group conversation.</span></span>|
|[<span data-ttu-id="ee246-124">Crear hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="ee246-124">Create conversation thread</span></span>](../api/conversation_post_threads.md) |<span data-ttu-id="ee246-125">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="ee246-125">[conversationThread](conversationthread.md) collection</span></span>| <span data-ttu-id="ee246-126">Cree un hilo en la conversación especificada.</span><span class="sxs-lookup"><span data-stu-id="ee246-126">Create a thread in the specified conversation.</span></span>|

## <a name="properties"></a><span data-ttu-id="ee246-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ee246-127">Properties</span></span>
| <span data-ttu-id="ee246-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ee246-128">Property</span></span>     | <span data-ttu-id="ee246-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee246-129">Type</span></span>   |<span data-ttu-id="ee246-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee246-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ee246-131">hasAttachments</span><span class="sxs-lookup"><span data-stu-id="ee246-131">hasAttachments</span></span>|<span data-ttu-id="ee246-132">Booleano</span><span class="sxs-lookup"><span data-stu-id="ee246-132">Boolean</span></span>|<span data-ttu-id="ee246-133">Indica si alguna de las publicaciones de esta conversación tiene al menos un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="ee246-133">Indicates whether any of the posts within this Conversation has at least one attachment.</span></span>|
|<span data-ttu-id="ee246-134">id</span><span class="sxs-lookup"><span data-stu-id="ee246-134">id</span></span>|<span data-ttu-id="ee246-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="ee246-135">String</span></span>|<span data-ttu-id="ee246-p102">El identificador único de las conversaciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ee246-p102">The conversations's unique identifier. Read-only.</span></span>|
|<span data-ttu-id="ee246-138">lastDeliveredDateTime</span><span class="sxs-lookup"><span data-stu-id="ee246-138">lastDeliveredDateTime</span></span>|<span data-ttu-id="ee246-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ee246-139">DateTimeOffset</span></span>|<span data-ttu-id="ee246-p103">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="ee246-p103">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="ee246-142">preview</span><span class="sxs-lookup"><span data-stu-id="ee246-142">preview</span></span>|<span data-ttu-id="ee246-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="ee246-143">String</span></span>|<span data-ttu-id="ee246-144">Un breve resumen del cuerpo de la última publicación de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="ee246-144">A short summary from the body of the latest post in this converstaion.</span></span>|
|<span data-ttu-id="ee246-145">topic</span><span class="sxs-lookup"><span data-stu-id="ee246-145">topic</span></span>|<span data-ttu-id="ee246-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="ee246-146">String</span></span>|<span data-ttu-id="ee246-p104">El tema de la conversación. Esta propiedad se puede establecer al crear la conversación, pero no se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="ee246-p104">The topic of the conversation. This property can be set when the conversation is created, but it cannot be updated.</span></span>|
|<span data-ttu-id="ee246-149">uniqueSenders</span><span class="sxs-lookup"><span data-stu-id="ee246-149">uniqueSenders</span></span>|<span data-ttu-id="ee246-150">Colección String</span><span class="sxs-lookup"><span data-stu-id="ee246-150">String collection</span></span>|<span data-ttu-id="ee246-151">Todos los usuarios que envían un mensaje a esta conversación.</span><span class="sxs-lookup"><span data-stu-id="ee246-151">All the users that sent a message to this Conversation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ee246-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ee246-152">Relationships</span></span>
| <span data-ttu-id="ee246-153">Relación</span><span class="sxs-lookup"><span data-stu-id="ee246-153">Relationship</span></span> | <span data-ttu-id="ee246-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee246-154">Type</span></span>   |<span data-ttu-id="ee246-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee246-155">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ee246-156">threads</span><span class="sxs-lookup"><span data-stu-id="ee246-156">threads</span></span>|<span data-ttu-id="ee246-157">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="ee246-157">[conversationThread](conversationthread.md) collection</span></span>|<span data-ttu-id="ee246-p105">Una colección de todos los hilos de la conversación. Una propiedad de navegación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="ee246-p105">A collection of all the conversation threads in the conversation. A navigation property. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ee246-162">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ee246-162">JSON representation</span></span>

<span data-ttu-id="ee246-163">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ee246-163">Here is a JSON representation of the resource</span></span>

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
