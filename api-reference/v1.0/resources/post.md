---
title: Tipo de recurso post
description: Representa un elemento Post individual dentro en una entidad conversationThread.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 585d823a7a3e4b6814f06c1613cac66a82a93e65
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851194"
---
# <a name="post-resource-type"></a><span data-ttu-id="4403b-103">Tipo de recurso post</span><span class="sxs-lookup"><span data-stu-id="4403b-103">post resource type</span></span>
<span data-ttu-id="4403b-104">Representa un elemento Post individual dentro en una entidad [conversationThread](conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="4403b-104">Represents an individual Post item within a [conversationThread](conversationthread.md) entity.</span></span>

<span data-ttu-id="4403b-105">Incluso aunque no pueda crear una publicación de forma explícita, cualquiera de las siguientes acciones creará una publicación:</span><span class="sxs-lookup"><span data-stu-id="4403b-105">Even though you cannot explicitly create a post, doing any of the following would create a post:</span></span>

- [<span data-ttu-id="4403b-106">Responder a una publicación existente</span><span class="sxs-lookup"><span data-stu-id="4403b-106">Reply to an existing post</span></span>](../api/post-reply.md) 
- [<span data-ttu-id="4403b-107">Responder a un hilo existente</span><span class="sxs-lookup"><span data-stu-id="4403b-107">Reply to an existing thread</span></span>](../api/conversationthread-reply.md) 
- [<span data-ttu-id="4403b-108">Crear un hilo en una conversación nueva</span><span class="sxs-lookup"><span data-stu-id="4403b-108">Create a thread in a new conversation</span></span>](../api/group-post-threads.md)
- [<span data-ttu-id="4403b-109">Crear una conversación</span><span class="sxs-lookup"><span data-stu-id="4403b-109">Create a new conversation</span></span>](../api/group-post-conversations.md)

<span data-ttu-id="4403b-110">Este recurso le permite agregar sus propios datos a las propiedades personalizadas mediante [extensiones](/graph/extensibility-overview).</span><span class="sxs-lookup"><span data-stu-id="4403b-110">This resource lets you add your own data to custom properties using [extensions](/graph/extensibility-overview).</span></span>

## <a name="methods"></a><span data-ttu-id="4403b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4403b-111">Methods</span></span>

| <span data-ttu-id="4403b-112">Método</span><span class="sxs-lookup"><span data-stu-id="4403b-112">Method</span></span>       | <span data-ttu-id="4403b-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4403b-113">Return Type</span></span>  |<span data-ttu-id="4403b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4403b-114">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="4403b-115">Enumerar publicaciones</span><span class="sxs-lookup"><span data-stu-id="4403b-115">List posts</span></span>](../api/conversationthread-list-posts.md) | [<span data-ttu-id="4403b-116">post</span><span class="sxs-lookup"><span data-stu-id="4403b-116">post</span></span>](post.md) |<span data-ttu-id="4403b-117">Obtenga las publicaciones del hilo especificado.</span><span class="sxs-lookup"><span data-stu-id="4403b-117">Get the posts of the specified thread.</span></span> |
|[<span data-ttu-id="4403b-118">Obtener publicación</span><span class="sxs-lookup"><span data-stu-id="4403b-118">Get post</span></span>](../api/post-get.md) | [<span data-ttu-id="4403b-119">post</span><span class="sxs-lookup"><span data-stu-id="4403b-119">post</span></span>](post.md) |<span data-ttu-id="4403b-120">Obtenga las propiedades y relaciones de una publicación de un hilo determinado.</span><span class="sxs-lookup"><span data-stu-id="4403b-120">Get the properties and relationships of a post in a specified thread.</span></span>|
|[<span data-ttu-id="4403b-121">Responder</span><span class="sxs-lookup"><span data-stu-id="4403b-121">Reply</span></span>](../api/post-reply.md)|<span data-ttu-id="4403b-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4403b-122">None</span></span>|<span data-ttu-id="4403b-123">Responda a una publicación y agregue una nueva publicación al hilo especificado de una conversación de grupo.</span><span class="sxs-lookup"><span data-stu-id="4403b-123">Reply to a post and add a new post to the specified thread in a group conversation.</span></span>|
|[<span data-ttu-id="4403b-124">Reenviar</span><span class="sxs-lookup"><span data-stu-id="4403b-124">Forward</span></span>](../api/post-forward.md)|<span data-ttu-id="4403b-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4403b-125">None</span></span>|<span data-ttu-id="4403b-126">Reenvíe una publicación a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="4403b-126">Forward a post to a recipient.</span></span>|
|<span data-ttu-id="4403b-127">**Datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="4403b-127">**Attachments**</span></span>| | |
|[<span data-ttu-id="4403b-128">Enumerar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="4403b-128">List attachments</span></span>](../api/post-list-attachments.md) |<span data-ttu-id="4403b-129">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="4403b-129">[attachment](attachment.md) collection</span></span>| <span data-ttu-id="4403b-130">Obtener todos los datos adjuntos en una publicación.</span><span class="sxs-lookup"><span data-stu-id="4403b-130">Get all attachments on a post.</span></span>|
|[<span data-ttu-id="4403b-131">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="4403b-131">Add attachment</span></span>](../api/post-post-attachments.md) |[<span data-ttu-id="4403b-132">dato adjunto</span><span class="sxs-lookup"><span data-stu-id="4403b-132">attachment</span></span>](attachment.md)| <span data-ttu-id="4403b-133">Agrega datos adjuntos a una publicación.</span><span class="sxs-lookup"><span data-stu-id="4403b-133">Add an attachment to a post.</span></span> |
|<span data-ttu-id="4403b-134">**Extensiones abiertas**</span><span class="sxs-lookup"><span data-stu-id="4403b-134">**Open extensions**</span></span>| | |
|[<span data-ttu-id="4403b-135">Crear extensión abierta</span><span class="sxs-lookup"><span data-stu-id="4403b-135">Create open extension</span></span>](../api/opentypeextension-post-opentypeextension.md) |[<span data-ttu-id="4403b-136">openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="4403b-136">openTypeExtension</span></span>](opentypeextension.md)| <span data-ttu-id="4403b-137">Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o existente de un recurso.</span><span class="sxs-lookup"><span data-stu-id="4403b-137">Create an open extension and add custom properties in a new or existing instance of a resource.</span></span>|
|[<span data-ttu-id="4403b-138">Obtener extensión abierta</span><span class="sxs-lookup"><span data-stu-id="4403b-138">Get open extension</span></span>](../api/opentypeextension-get.md) |<span data-ttu-id="4403b-139">Colección [openTypeExtension](opentypeextension.md)</span><span class="sxs-lookup"><span data-stu-id="4403b-139">[openTypeExtension](opentypeextension.md) collection</span></span>| <span data-ttu-id="4403b-140">Obtenga un objeto u objetos de extensión abierta identificados por nombre o por nombre completo.</span><span class="sxs-lookup"><span data-stu-id="4403b-140">Get an open extension object or objects identified by name or fully qualified name.</span></span>|
|<span data-ttu-id="4403b-141">**Extensiones de esquema**</span><span class="sxs-lookup"><span data-stu-id="4403b-141">**Schema extensions**</span></span>| | |
|[<span data-ttu-id="4403b-142">Agregar valores de extensión de esquema</span><span class="sxs-lookup"><span data-stu-id="4403b-142">Add schema extension values</span></span>](/graph/extensibility-schema-groups) || <span data-ttu-id="4403b-143">Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.</span><span class="sxs-lookup"><span data-stu-id="4403b-143">Create a schema extension definition and then use it to add custom typed data to a resource.</span></span>|
|<span data-ttu-id="4403b-144">**Propiedades extendidas**</span><span class="sxs-lookup"><span data-stu-id="4403b-144">**Extended properties**</span></span>| | |
|[<span data-ttu-id="4403b-145">Crear propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="4403b-145">Create single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[<span data-ttu-id="4403b-146">post</span><span class="sxs-lookup"><span data-stu-id="4403b-146">post</span></span>](post.md)  |<span data-ttu-id="4403b-147">Cree una o varias propiedades extendidas de valor único en una publicación nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="4403b-147">Create one or more single-value extended properties in a new or existing post.</span></span>   |
|[<span data-ttu-id="4403b-148">Obtener publicación con propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="4403b-148">Get post with single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="4403b-149">post</span><span class="sxs-lookup"><span data-stu-id="4403b-149">post</span></span>](post.md) | <span data-ttu-id="4403b-150">Obtenga publicaciones que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="4403b-150">Get posts that contain a single-value extended property by using `$expand` or `$filter`.</span></span> |
|[<span data-ttu-id="4403b-151">Crear propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="4403b-151">Create multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [<span data-ttu-id="4403b-152">post</span><span class="sxs-lookup"><span data-stu-id="4403b-152">post</span></span>](post.md) | <span data-ttu-id="4403b-153">Cree una o varias propiedades extendidas de varios valores en una publicación nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="4403b-153">Create one or more multi-value extended properties in a new or existing post.</span></span>  |
|[<span data-ttu-id="4403b-154">Obtener publicación con propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="4403b-154">Get post with multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="4403b-155">post</span><span class="sxs-lookup"><span data-stu-id="4403b-155">post</span></span>](post.md) | <span data-ttu-id="4403b-156">Obtenga una publicación que contiene una propiedad extendida de varios valores mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="4403b-156">Get a post that contains a multi-value extended property by using `$expand`.</span></span> |

## <a name="properties"></a><span data-ttu-id="4403b-157">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4403b-157">Properties</span></span>
| <span data-ttu-id="4403b-158">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4403b-158">Property</span></span>     | <span data-ttu-id="4403b-159">Tipo</span><span class="sxs-lookup"><span data-stu-id="4403b-159">Type</span></span>   |<span data-ttu-id="4403b-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="4403b-160">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4403b-161">body</span><span class="sxs-lookup"><span data-stu-id="4403b-161">body</span></span>|[<span data-ttu-id="4403b-162">itemBody</span><span class="sxs-lookup"><span data-stu-id="4403b-162">itemBody</span></span>](itembody.md)|<span data-ttu-id="4403b-p101">Los contenidos de la publicación. Esta es la propiedad predeterminada. Esta propiedad puede ser null.</span><span class="sxs-lookup"><span data-stu-id="4403b-p101">The contents of the post. This is a default property. This property can be null.</span></span>|
|<span data-ttu-id="4403b-166">categories</span><span class="sxs-lookup"><span data-stu-id="4403b-166">categories</span></span>|<span data-ttu-id="4403b-167">Colección String</span><span class="sxs-lookup"><span data-stu-id="4403b-167">String collection</span></span>|<span data-ttu-id="4403b-168">Las categorías asociadas a la publicación.</span><span class="sxs-lookup"><span data-stu-id="4403b-168">The categories associated with the post.</span></span>|
|<span data-ttu-id="4403b-169">changeKey</span><span class="sxs-lookup"><span data-stu-id="4403b-169">changeKey</span></span>|<span data-ttu-id="4403b-170">String</span><span class="sxs-lookup"><span data-stu-id="4403b-170">String</span></span>|<span data-ttu-id="4403b-p102">Identifica la versión de la publicación. Cada vez que cambia la publicación, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto.</span><span class="sxs-lookup"><span data-stu-id="4403b-p102">Identifies the version of the post. Every time the post is changed, ChangeKey changes as well. This allows Exchange to apply changes to the correct version of the object.</span></span>|
|<span data-ttu-id="4403b-174">conversationId</span><span class="sxs-lookup"><span data-stu-id="4403b-174">conversationId</span></span>|<span data-ttu-id="4403b-175">String</span><span class="sxs-lookup"><span data-stu-id="4403b-175">String</span></span>|<span data-ttu-id="4403b-p103">El identificador único de la conversación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4403b-p103">Unique ID of the conversation. Read-only.</span></span>|
|<span data-ttu-id="4403b-178">conversationThreadId</span><span class="sxs-lookup"><span data-stu-id="4403b-178">conversationThreadId</span></span>|<span data-ttu-id="4403b-179">String</span><span class="sxs-lookup"><span data-stu-id="4403b-179">String</span></span>|<span data-ttu-id="4403b-p104">El identificador único del hilo de la conversación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4403b-p104">Unique ID of the conversation thread. Read-only.</span></span>|
|<span data-ttu-id="4403b-182">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4403b-182">createdDateTime</span></span>|<span data-ttu-id="4403b-183">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4403b-183">DateTimeOffset</span></span>|<span data-ttu-id="4403b-p105">Especifica cuándo se ha creado la publicación. El tipo DateTimeOffset representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="4403b-p105">Specifies when the post was created. The DateTimeOffset type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="4403b-187">from</span><span class="sxs-lookup"><span data-stu-id="4403b-187">from</span></span>|[<span data-ttu-id="4403b-188">recipient</span><span class="sxs-lookup"><span data-stu-id="4403b-188">recipient</span></span>](recipient.md)|<span data-ttu-id="4403b-p106">Se usa en escenarios de acceso delegado. Indica quién ha publicado el mensaje en nombre de otro usuario. Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4403b-p106">Used in delegate access scenarios. Indicates who posted the message on behalf of another user. This is a default property.</span></span>|
|<span data-ttu-id="4403b-192">hasAttachments</span><span class="sxs-lookup"><span data-stu-id="4403b-192">hasAttachments</span></span>|<span data-ttu-id="4403b-193">Boolean</span><span class="sxs-lookup"><span data-stu-id="4403b-193">Boolean</span></span>|<span data-ttu-id="4403b-p107">Indica si la publicación tiene al menos un dato adjunto. Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4403b-p107">Indicates whether the post has at least one attachment. This is a default property.</span></span>|
|<span data-ttu-id="4403b-196">id</span><span class="sxs-lookup"><span data-stu-id="4403b-196">id</span></span>|<span data-ttu-id="4403b-197">Cadena</span><span class="sxs-lookup"><span data-stu-id="4403b-197">String</span></span>| <span data-ttu-id="4403b-198">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4403b-198">Read-only.</span></span>|
|<span data-ttu-id="4403b-199">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4403b-199">lastModifiedDateTime</span></span>|<span data-ttu-id="4403b-200">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4403b-200">DateTimeOffset</span></span>|<span data-ttu-id="4403b-p108">Especifica cuándo se ha modificado por última vez la publicación. El tipo DateTimeOffset representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="4403b-p108">Specifies when the post was last modified. The DateTimeOffset type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="4403b-204">newParticipants</span><span class="sxs-lookup"><span data-stu-id="4403b-204">newParticipants</span></span>|<span data-ttu-id="4403b-205">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="4403b-205">[recipient](recipient.md) collection</span></span>|<span data-ttu-id="4403b-206">Participantes de la conversación que se han agregado al hilo como parte de esta publicación.</span><span class="sxs-lookup"><span data-stu-id="4403b-206">Conversation participants that were added to the thread as part of this post.</span></span>|
|<span data-ttu-id="4403b-207">receivedDateTime</span><span class="sxs-lookup"><span data-stu-id="4403b-207">receivedDateTime</span></span>|<span data-ttu-id="4403b-208">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4403b-208">DateTimeOffset</span></span>|<span data-ttu-id="4403b-p109">Especifica cuándo se ha recibido la publicación. El tipo DateTimeOffset representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="4403b-p109">Specifies when the post was received. The DateTimeOffset type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="4403b-212">sender</span><span class="sxs-lookup"><span data-stu-id="4403b-212">sender</span></span>|[<span data-ttu-id="4403b-213">recipient</span><span class="sxs-lookup"><span data-stu-id="4403b-213">recipient</span></span>](recipient.md)|<span data-ttu-id="4403b-p110">Contiene la dirección del remitente. El valor de Sender se supone que es la dirección del usuario autenticado en el caso de que no se especifique ningún Sender. Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4403b-p110">Contains the address of the sender. The value of Sender is assumed to be the address of the authenticated user in the case when Sender is not specified. This is a default property.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4403b-217">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4403b-217">Relationships</span></span>
| <span data-ttu-id="4403b-218">Relación</span><span class="sxs-lookup"><span data-stu-id="4403b-218">Relationship</span></span> | <span data-ttu-id="4403b-219">Tipo</span><span class="sxs-lookup"><span data-stu-id="4403b-219">Type</span></span>   |<span data-ttu-id="4403b-220">Descripción</span><span class="sxs-lookup"><span data-stu-id="4403b-220">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4403b-221">attachments</span><span class="sxs-lookup"><span data-stu-id="4403b-221">attachments</span></span>|<span data-ttu-id="4403b-222">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="4403b-222">[Attachment](attachment.md) collection</span></span>| <span data-ttu-id="4403b-p111">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="4403b-p111">Read-only. Nullable.</span></span>|
|<span data-ttu-id="4403b-225">extensions</span><span class="sxs-lookup"><span data-stu-id="4403b-225">extensions</span></span>|<span data-ttu-id="4403b-226">Colección [Extension](extension.md)</span><span class="sxs-lookup"><span data-stu-id="4403b-226">[Extension](extension.md) collection</span></span>|<span data-ttu-id="4403b-p112">La colección de extensiones abiertas definidas para la publicación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="4403b-p112">The collection of open extensions defined for the post. Read-only. Nullable.</span></span>|
|<span data-ttu-id="4403b-230">inReplyTo</span><span class="sxs-lookup"><span data-stu-id="4403b-230">inReplyTo</span></span>|[<span data-ttu-id="4403b-231">post</span><span class="sxs-lookup"><span data-stu-id="4403b-231">post</span></span>](post.md)| <span data-ttu-id="4403b-232">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4403b-232">Read-only.</span></span>|
|<span data-ttu-id="4403b-233">multiValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="4403b-233">multiValueExtendedProperties</span></span>|<span data-ttu-id="4403b-234">Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="4403b-234">[multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="4403b-p113">La colección de propiedades extendidas de varios valores definidas para la publicación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="4403b-p113">The collection of multi-value extended properties defined for the post. Read-only. Nullable.</span></span>|
|<span data-ttu-id="4403b-238">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="4403b-238">singleValueExtendedProperties</span></span>|<span data-ttu-id="4403b-239">Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="4403b-239">[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="4403b-p114">La colección de propiedades extendidas de valor único definidas para la publicación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="4403b-p114">The collection of single-value extended properties defined for the post. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4403b-243">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4403b-243">JSON representation</span></span>

<span data-ttu-id="4403b-244">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4403b-244">Here is a JSON representation of the resource</span></span>

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

## <a name="see-also"></a><span data-ttu-id="4403b-245">Vea también</span><span class="sxs-lookup"><span data-stu-id="4403b-245">See also</span></span>

- [<span data-ttu-id="4403b-246">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="4403b-246">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="4403b-247">Agregar datos personalizados a los usuarios mediante extensiones abiertas</span><span class="sxs-lookup"><span data-stu-id="4403b-247">Add custom data to users using open extensions</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="4403b-248">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="4403b-248">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "post resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
