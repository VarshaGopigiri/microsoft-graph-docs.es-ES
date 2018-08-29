# <a name="post-resource-type"></a><span data-ttu-id="72e11-101">Tipo de recurso post</span><span class="sxs-lookup"><span data-stu-id="72e11-101">post resource type</span></span>
<span data-ttu-id="72e11-102">Representa un elemento Post individual dentro en una entidad [conversationThread](conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="72e11-102">Represents an individual Post item within a [conversationThread](conversationthread.md) entity.</span></span>

<span data-ttu-id="72e11-103">Incluso aunque no pueda crear una publicación de forma explícita, cualquiera de las siguientes acciones creará una publicación:</span><span class="sxs-lookup"><span data-stu-id="72e11-103">Even though you cannot explicitly create a post, doing any of the following would create a post:</span></span>

- [<span data-ttu-id="72e11-104">Responder a una publicación existente</span><span class="sxs-lookup"><span data-stu-id="72e11-104">Reply to an existing post</span></span>](../api/post_reply.md) 
- [<span data-ttu-id="72e11-105">Responder a un hilo existente</span><span class="sxs-lookup"><span data-stu-id="72e11-105">Reply to an existing thread</span></span>](../api/conversationthread_reply.md) 
- [<span data-ttu-id="72e11-106">Crear un hilo en una conversación nueva</span><span class="sxs-lookup"><span data-stu-id="72e11-106">Create a thread in a new conversation</span></span>](../api/group_post_threads.md)
- [<span data-ttu-id="72e11-107">Crear una conversación</span><span class="sxs-lookup"><span data-stu-id="72e11-107">Create a new conversation</span></span>](../api/group_post_conversations.md)

<span data-ttu-id="72e11-108">Este recurso le permite agregar sus propios datos a las propiedades personalizadas mediante [extensiones](../../../concepts/extensibility_overview.md).</span><span class="sxs-lookup"><span data-stu-id="72e11-108">This resource lets you add your own data to custom properties using [extensions](../../../concepts/extensibility_overview.md).</span></span>

## <a name="methods"></a><span data-ttu-id="72e11-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="72e11-109">Methods</span></span>

| <span data-ttu-id="72e11-110">Método</span><span class="sxs-lookup"><span data-stu-id="72e11-110">Method</span></span>       | <span data-ttu-id="72e11-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72e11-111">Return Type</span></span>  |<span data-ttu-id="72e11-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="72e11-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="72e11-113">Enumerar publicaciones</span><span class="sxs-lookup"><span data-stu-id="72e11-113">List posts</span></span>](../api/conversationthread_list_posts.md) | [<span data-ttu-id="72e11-114">post</span><span class="sxs-lookup"><span data-stu-id="72e11-114">post</span></span>](post.md) |<span data-ttu-id="72e11-115">Obtenga las publicaciones del hilo especificado.</span><span class="sxs-lookup"><span data-stu-id="72e11-115">Get the posts of the specified thread.</span></span> |
|[<span data-ttu-id="72e11-116">Obtener publicación</span><span class="sxs-lookup"><span data-stu-id="72e11-116">Get post</span></span>](../api/post_get.md) | [<span data-ttu-id="72e11-117">post</span><span class="sxs-lookup"><span data-stu-id="72e11-117">post</span></span>](post.md) |<span data-ttu-id="72e11-118">Obtenga las propiedades y relaciones de una publicación de un hilo determinado.</span><span class="sxs-lookup"><span data-stu-id="72e11-118">Get the properties and relationships of a post in a specified thread.</span></span>|
|[<span data-ttu-id="72e11-119">Responder</span><span class="sxs-lookup"><span data-stu-id="72e11-119">Reply</span></span>](../api/post_reply.md)|<span data-ttu-id="72e11-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="72e11-120">None</span></span>|<span data-ttu-id="72e11-121">Responda a una publicación y agregue una nueva publicación al hilo especificado de una conversación de grupo.</span><span class="sxs-lookup"><span data-stu-id="72e11-121">Reply to a post and add a new post to the specified thread in a group conversation.</span></span>|
|[<span data-ttu-id="72e11-122">Reenviar</span><span class="sxs-lookup"><span data-stu-id="72e11-122">Forward</span></span>](../api/post_forward.md)|<span data-ttu-id="72e11-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="72e11-123">None</span></span>|<span data-ttu-id="72e11-124">Reenvíe una publicación a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="72e11-124">Forward a post to a recipient.</span></span>|
|<span data-ttu-id="72e11-125">**Datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="72e11-125">**Attachments**</span></span>| | |
|[<span data-ttu-id="72e11-126">Enumerar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="72e11-126">List attachments</span></span>](../api/post_list_attachments.md) |<span data-ttu-id="72e11-127">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="72e11-127">[attachment](attachment.md) collection</span></span>| <span data-ttu-id="72e11-128">Obtener todos los datos adjuntos en una publicación.</span><span class="sxs-lookup"><span data-stu-id="72e11-128">Get all attachments on a post.</span></span>|
|[<span data-ttu-id="72e11-129">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="72e11-129">Add attachment</span></span>](../api/post_post_attachments.md) |[<span data-ttu-id="72e11-130">dato adjunto</span><span class="sxs-lookup"><span data-stu-id="72e11-130">attachment</span></span>](attachment.md)| <span data-ttu-id="72e11-131">Agrega datos adjuntos a una publicación.</span><span class="sxs-lookup"><span data-stu-id="72e11-131">Add an attachment to a post.</span></span> |
|<span data-ttu-id="72e11-132">**Extensiones abiertas**</span><span class="sxs-lookup"><span data-stu-id="72e11-132">**Open extensions**</span></span>| | |
|[<span data-ttu-id="72e11-133">Crear extensión abierta</span><span class="sxs-lookup"><span data-stu-id="72e11-133">Create open extension</span></span>](../api/opentypeextension_post_opentypeextension.md) |[<span data-ttu-id="72e11-134">openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="72e11-134">openTypeExtension</span></span>](opentypeextension.md)| <span data-ttu-id="72e11-135">Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o existente de un recurso.</span><span class="sxs-lookup"><span data-stu-id="72e11-135">Create an open extension and add custom properties in a new or existing instance of a resource.</span></span>|
|[<span data-ttu-id="72e11-136">Obtener extensión abierta</span><span class="sxs-lookup"><span data-stu-id="72e11-136">Get open extension</span></span>](../api/opentypeextension_get.md) |<span data-ttu-id="72e11-137">Colección [openTypeExtension](opentypeextension.md)</span><span class="sxs-lookup"><span data-stu-id="72e11-137">[openTypeExtension](opentypeextension.md) collection</span></span>| <span data-ttu-id="72e11-138">Obtenga un objeto u objetos de extensión abierta identificados por nombre o por nombre completo.</span><span class="sxs-lookup"><span data-stu-id="72e11-138">Get an open extension object or objects identified by name or fully qualified name.</span></span>|
|<span data-ttu-id="72e11-139">**Extensiones de esquema**</span><span class="sxs-lookup"><span data-stu-id="72e11-139">**Schema extensions**</span></span>| | |
|[<span data-ttu-id="72e11-140">Agregar valores de extensión de esquema</span><span class="sxs-lookup"><span data-stu-id="72e11-140">Add schema extension values</span></span>](../../../concepts/extensibility_schema_groups.md) || <span data-ttu-id="72e11-141">Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.</span><span class="sxs-lookup"><span data-stu-id="72e11-141">Create a schema extension definition and then use it to add custom typed data to a resource.</span></span>|
|<span data-ttu-id="72e11-142">**Propiedades extendidas**</span><span class="sxs-lookup"><span data-stu-id="72e11-142">**Extended properties**</span></span>| | |
|[<span data-ttu-id="72e11-143">Crear propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="72e11-143">Create single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) |[<span data-ttu-id="72e11-144">post</span><span class="sxs-lookup"><span data-stu-id="72e11-144">post</span></span>](post.md)  |<span data-ttu-id="72e11-145">Cree una o varias propiedades extendidas de valor único en una publicación nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="72e11-145">Create one or more single-value extended properties in a new or existing post.</span></span>   |
|[<span data-ttu-id="72e11-146">Obtener publicación con propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="72e11-146">Get post with single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty_get.md)  | [<span data-ttu-id="72e11-147">post</span><span class="sxs-lookup"><span data-stu-id="72e11-147">post</span></span>](post.md) | <span data-ttu-id="72e11-148">Obtenga publicaciones que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="72e11-148">Get posts that contain a single-value extended property by using `$expand` or `$filter`.</span></span> |
|[<span data-ttu-id="72e11-149">Crear propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="72e11-149">Create multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | [<span data-ttu-id="72e11-150">post</span><span class="sxs-lookup"><span data-stu-id="72e11-150">post</span></span>](post.md) | <span data-ttu-id="72e11-151">Cree una o varias propiedades extendidas de varios valores en una publicación nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="72e11-151">Create one or more multi-value extended properties in a new or existing post.</span></span>  |
|[<span data-ttu-id="72e11-152">Obtener publicación con propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="72e11-152">Get post with multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty_get.md)  | [<span data-ttu-id="72e11-153">post</span><span class="sxs-lookup"><span data-stu-id="72e11-153">post</span></span>](post.md) | <span data-ttu-id="72e11-154">Obtenga una publicación que contiene una propiedad extendida de varios valores mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="72e11-154">Get a post that contains a multi-value extended property by using `$expand`.</span></span> |

## <a name="properties"></a><span data-ttu-id="72e11-155">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72e11-155">Properties</span></span>
| <span data-ttu-id="72e11-156">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72e11-156">Property</span></span>     | <span data-ttu-id="72e11-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="72e11-157">Type</span></span>   |<span data-ttu-id="72e11-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="72e11-158">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="72e11-159">body</span><span class="sxs-lookup"><span data-stu-id="72e11-159">body</span></span>|[<span data-ttu-id="72e11-160">itemBody</span><span class="sxs-lookup"><span data-stu-id="72e11-160">itemBody</span></span>](itembody.md)|<span data-ttu-id="72e11-p101">Los contenidos de la publicación. Esta es la propiedad predeterminada. Esta propiedad puede ser null.</span><span class="sxs-lookup"><span data-stu-id="72e11-p101">The contents of the post. This is a default property. This property can be null.</span></span>|
|<span data-ttu-id="72e11-164">categories</span><span class="sxs-lookup"><span data-stu-id="72e11-164">categories</span></span>|<span data-ttu-id="72e11-165">Colección String</span><span class="sxs-lookup"><span data-stu-id="72e11-165">String collection</span></span>|<span data-ttu-id="72e11-166">Las categorías asociadas a la publicación.</span><span class="sxs-lookup"><span data-stu-id="72e11-166">The categories associated with the post.</span></span>|
|<span data-ttu-id="72e11-167">changeKey</span><span class="sxs-lookup"><span data-stu-id="72e11-167">changeKey</span></span>|<span data-ttu-id="72e11-168">String</span><span class="sxs-lookup"><span data-stu-id="72e11-168">String</span></span>|<span data-ttu-id="72e11-p102">Identifica la versión de la publicación. Cada vez que cambia la publicación, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto.</span><span class="sxs-lookup"><span data-stu-id="72e11-p102">Identifies the version of the post. Every time the post is changed, ChangeKey changes as well. This allows Exchange to apply changes to the correct version of the object.</span></span>|
|<span data-ttu-id="72e11-172">conversationId</span><span class="sxs-lookup"><span data-stu-id="72e11-172">conversationId</span></span>|<span data-ttu-id="72e11-173">String</span><span class="sxs-lookup"><span data-stu-id="72e11-173">String</span></span>|<span data-ttu-id="72e11-p103">El identificador único de la conversación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="72e11-p103">Unique ID of the conversation. Read-only.</span></span>|
|<span data-ttu-id="72e11-176">conversationThreadId</span><span class="sxs-lookup"><span data-stu-id="72e11-176">conversationThreadId</span></span>|<span data-ttu-id="72e11-177">String</span><span class="sxs-lookup"><span data-stu-id="72e11-177">String</span></span>|<span data-ttu-id="72e11-p104">El identificador único del hilo de la conversación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="72e11-p104">Unique ID of the conversation thread. Read-only.</span></span>|
|<span data-ttu-id="72e11-180">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="72e11-180">createdDateTime</span></span>|<span data-ttu-id="72e11-181">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="72e11-181">DateTimeOffset</span></span>|<span data-ttu-id="72e11-p105">Especifica cuándo se ha creado la publicación. El tipo DateTimeOffset representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="72e11-p105">Specifies when the post was created. The DateTimeOffset type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="72e11-185">from</span><span class="sxs-lookup"><span data-stu-id="72e11-185">from</span></span>|[<span data-ttu-id="72e11-186">recipient</span><span class="sxs-lookup"><span data-stu-id="72e11-186">recipient</span></span>](recipient.md)|<span data-ttu-id="72e11-p106">Se usa en escenarios de acceso delegado. Indica quién ha publicado el mensaje en nombre de otro usuario. Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="72e11-p106">Used in delegate access scenarios. Indicates who posted the message on behalf of another user. This is a default property.</span></span>|
|<span data-ttu-id="72e11-190">hasAttachments</span><span class="sxs-lookup"><span data-stu-id="72e11-190">hasAttachments</span></span>|<span data-ttu-id="72e11-191">Boolean</span><span class="sxs-lookup"><span data-stu-id="72e11-191">Boolean</span></span>|<span data-ttu-id="72e11-p107">Indica si la publicación tiene al menos un dato adjunto. Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="72e11-p107">Indicates whether the post has at least one attachment. This is a default property.</span></span>|
|<span data-ttu-id="72e11-194">id</span><span class="sxs-lookup"><span data-stu-id="72e11-194">id</span></span>|<span data-ttu-id="72e11-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="72e11-195">String</span></span>| <span data-ttu-id="72e11-196">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="72e11-196">Read-only.</span></span>|
|<span data-ttu-id="72e11-197">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="72e11-197">lastModifiedDateTime</span></span>|<span data-ttu-id="72e11-198">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="72e11-198">DateTimeOffset</span></span>|<span data-ttu-id="72e11-p108">Especifica cuándo se ha modificado por última vez la publicación. El tipo DateTimeOffset representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="72e11-p108">Specifies when the post was last modified. The DateTimeOffset type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="72e11-202">newParticipants</span><span class="sxs-lookup"><span data-stu-id="72e11-202">newParticipants</span></span>|<span data-ttu-id="72e11-203">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="72e11-203">[recipient](recipient.md) collection</span></span>|<span data-ttu-id="72e11-204">Participantes de la conversación que se han agregado al hilo como parte de esta publicación.</span><span class="sxs-lookup"><span data-stu-id="72e11-204">Conversation participants that were added to the thread as part of this post.</span></span>|
|<span data-ttu-id="72e11-205">receivedDateTime</span><span class="sxs-lookup"><span data-stu-id="72e11-205">receivedDateTime</span></span>|<span data-ttu-id="72e11-206">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="72e11-206">DateTimeOffset</span></span>|<span data-ttu-id="72e11-p109">Especifica cuándo se ha recibido la publicación. El tipo DateTimeOffset representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="72e11-p109">Specifies when the post was received. The DateTimeOffset type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="72e11-210">sender</span><span class="sxs-lookup"><span data-stu-id="72e11-210">sender</span></span>|[<span data-ttu-id="72e11-211">recipient</span><span class="sxs-lookup"><span data-stu-id="72e11-211">recipient</span></span>](recipient.md)|<span data-ttu-id="72e11-p110">Contiene la dirección del remitente. El valor de Sender se supone que es la dirección del usuario autenticado en el caso de que no se especifique ningún Sender. Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="72e11-p110">Contains the address of the sender. The value of Sender is assumed to be the address of the authenticated user in the case when Sender is not specified. This is a default property.</span></span>|

## <a name="relationships"></a><span data-ttu-id="72e11-215">Relaciones</span><span class="sxs-lookup"><span data-stu-id="72e11-215">Relationships</span></span>
| <span data-ttu-id="72e11-216">Relación</span><span class="sxs-lookup"><span data-stu-id="72e11-216">Relationship</span></span> | <span data-ttu-id="72e11-217">Tipo</span><span class="sxs-lookup"><span data-stu-id="72e11-217">Type</span></span>   |<span data-ttu-id="72e11-218">Descripción</span><span class="sxs-lookup"><span data-stu-id="72e11-218">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="72e11-219">attachments</span><span class="sxs-lookup"><span data-stu-id="72e11-219">attachments</span></span>|<span data-ttu-id="72e11-220">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="72e11-220">[Attachment](attachment.md) collection</span></span>| <span data-ttu-id="72e11-p111">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="72e11-p111">Read-only. Nullable.</span></span>|
|<span data-ttu-id="72e11-223">extensions</span><span class="sxs-lookup"><span data-stu-id="72e11-223">extensions</span></span>|<span data-ttu-id="72e11-224">Colección [Extension](extension.md)</span><span class="sxs-lookup"><span data-stu-id="72e11-224">[Extension](extension.md) collection</span></span>|<span data-ttu-id="72e11-p112">La colección de extensiones abiertas definidas para la publicación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="72e11-p112">The collection of open extensions defined for the post. Read-only. Nullable.</span></span>|
|<span data-ttu-id="72e11-228">inReplyTo</span><span class="sxs-lookup"><span data-stu-id="72e11-228">inReplyTo</span></span>|[<span data-ttu-id="72e11-229">post</span><span class="sxs-lookup"><span data-stu-id="72e11-229">post</span></span>](post.md)| <span data-ttu-id="72e11-230">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="72e11-230">Read-only.</span></span>|
|<span data-ttu-id="72e11-231">multiValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="72e11-231">multiValueExtendedProperties</span></span>|<span data-ttu-id="72e11-232">Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="72e11-232">[multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="72e11-p113">La colección de propiedades extendidas de varios valores definidas para la publicación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="72e11-p113">The collection of multi-value extended properties defined for the post. Read-only. Nullable.</span></span>|
|<span data-ttu-id="72e11-236">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="72e11-236">singleValueExtendedProperties</span></span>|<span data-ttu-id="72e11-237">Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="72e11-237">[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="72e11-p114">La colección de propiedades extendidas de valor único definidas para la publicación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="72e11-p114">The collection of single-value extended properties defined for the post. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="72e11-241">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="72e11-241">JSON representation</span></span>

<span data-ttu-id="72e11-242">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="72e11-242">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [
    "attachments",
    "inReplyTo",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "baseType": "microsoft.graph.outlookItem",
  "@odata.type": "microsoft.graph.post",
  "@odata.annotations": [
    {
      "property": "attachments",
      "capabilities": {
        "changeTracking": false,
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "extensions",
      "capabilities": {
        "changeTracking": false,
        "searchable": false
      }
    },
    {
      "property": "inReplyTo",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "insertable": false,
        "navigability": "single",
        "searchable": false,
        "updatable": false
      }
    }
  ]
}-->

```json
{
  "body": {"@odata.type": "microsoft.graph.itemBody"},
  "categories": ["string"],
  "changeKey": "string",
  "conversationId": "string",
  "conversationThreadId": "string",
  "createdDateTime": "String (timestamp)",
  "from": {"@odata.type": "microsoft.graph.recipient"},
  "hasAttachments": true,
  "id": "string (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "newParticipants": [{"@odata.type": "microsoft.graph.recipient"}],
  "receivedDateTime": "String (timestamp)",
  "sender": {"@odata.type": "microsoft.graph.recipient"}
}

```

## <a name="see-also"></a><span data-ttu-id="72e11-243">Vea también</span><span class="sxs-lookup"><span data-stu-id="72e11-243">See also</span></span>

- [<span data-ttu-id="72e11-244">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="72e11-244">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="72e11-245">Agregar datos personalizados a los usuarios mediante extensiones abiertas</span><span class="sxs-lookup"><span data-stu-id="72e11-245">Add custom data to users using open extensions</span></span>](../../../concepts/extensibility_open_users.md)
- [<span data-ttu-id="72e11-246">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="72e11-246">Add custom data to groups using schema extensions</span></span>](../../../concepts/extensibility_schema_groups.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "post resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
