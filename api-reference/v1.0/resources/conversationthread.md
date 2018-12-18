---
title: Tipo de recurso conversationThread
description: Un recurso conversationThread es una colección de posts.
author: dkershaw10
ms.openlocfilehash: 1456b32a26b279b917930740ca220025e8858590
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332175"
---
# <a name="conversationthread-resource-type"></a><span data-ttu-id="abbdc-103">Tipo de recurso conversationThread</span><span class="sxs-lookup"><span data-stu-id="abbdc-103">conversationThread resource type</span></span>
<span data-ttu-id="abbdc-104">Un recurso conversationThread es una colección de [posts](post.md).</span><span class="sxs-lookup"><span data-stu-id="abbdc-104">A conversationThread is a collection of [posts](post.md).</span></span>

<span data-ttu-id="abbdc-p101">La colección de destinatarios de la última publicación son los destinatarios agregados del hilo completo. Un hilo puede tener una colección creciente de destinatarios. Se crea un hilo al eliminar un destinatario del hilo.</span><span class="sxs-lookup"><span data-stu-id="abbdc-p101">The last post's recipients collection is the aggregated recipients of the entire thread. A thread can have a growing collection of recipients. A new thread is created when a recipient is removed from the thread.</span></span>

## <a name="methods"></a><span data-ttu-id="abbdc-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="abbdc-108">Methods</span></span>

| <span data-ttu-id="abbdc-109">Método</span><span class="sxs-lookup"><span data-stu-id="abbdc-109">Method</span></span>       | <span data-ttu-id="abbdc-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abbdc-110">Return Type</span></span>  |<span data-ttu-id="abbdc-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="abbdc-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="abbdc-112">Enumerar hilos</span><span class="sxs-lookup"><span data-stu-id="abbdc-112">List threads</span></span>](../api/group-list-threads.md) | <span data-ttu-id="abbdc-113">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="abbdc-113">[conversationThread](conversationthread.md) collection</span></span> |<span data-ttu-id="abbdc-114">Obtenga todos los hilos de un grupo.</span><span class="sxs-lookup"><span data-stu-id="abbdc-114">Get all the threads of a group.</span></span>|
|[<span data-ttu-id="abbdc-115">Crear hilo</span><span class="sxs-lookup"><span data-stu-id="abbdc-115">Create thread</span></span>](../api/group-post-threads.md) | [<span data-ttu-id="abbdc-116">conversationThread</span><span class="sxs-lookup"><span data-stu-id="abbdc-116">conversationThread</span></span>](conversationthread.md) |<span data-ttu-id="abbdc-p102">Inicie una nueva conversación creando primero un hilo. Se crean una conversación, un hilo de conversación y una publicación en el grupo.</span><span class="sxs-lookup"><span data-stu-id="abbdc-p102">Start a new conversation by first creating a thread. A new conversation, conversation thread, and post are created in the group.</span></span>|
|[<span data-ttu-id="abbdc-119">Obtener conversationThread</span><span class="sxs-lookup"><span data-stu-id="abbdc-119">Get conversationThread</span></span>](../api/conversationthread-get.md) | [<span data-ttu-id="abbdc-120">conversationThread</span><span class="sxs-lookup"><span data-stu-id="abbdc-120">conversationThread</span></span>](conversationthread.md) |<span data-ttu-id="abbdc-121">Obtenga un hilo específico que pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="abbdc-121">Get a specific thread that belongs to a group.</span></span> |
|[<span data-ttu-id="abbdc-122">Actualizar</span><span class="sxs-lookup"><span data-stu-id="abbdc-122">Update</span></span>](../api/conversationthread-update.md) | [<span data-ttu-id="abbdc-123">conversationThread</span><span class="sxs-lookup"><span data-stu-id="abbdc-123">conversationThread</span></span>](conversationthread.md)  |<span data-ttu-id="abbdc-124">Actualice el objeto conversationThread.</span><span class="sxs-lookup"><span data-stu-id="abbdc-124">Update conversationThread object.</span></span> |
|[<span data-ttu-id="abbdc-125">Eliminar</span><span class="sxs-lookup"><span data-stu-id="abbdc-125">Delete</span></span>](../api/conversationthread-delete.md) | <span data-ttu-id="abbdc-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="abbdc-126">None</span></span> |<span data-ttu-id="abbdc-127">Elimine el objeto conversationThread.</span><span class="sxs-lookup"><span data-stu-id="abbdc-127">Delete conversationThread object.</span></span> |
|[<span data-ttu-id="abbdc-128">Responder</span><span class="sxs-lookup"><span data-stu-id="abbdc-128">Reply</span></span>](../api/conversationthread-reply.md)|<span data-ttu-id="abbdc-129">Ninguno</span><span class="sxs-lookup"><span data-stu-id="abbdc-129">None</span></span>|<span data-ttu-id="abbdc-130">Responda a este hilo mediante la creación de una nueva entidad Post.</span><span class="sxs-lookup"><span data-stu-id="abbdc-130">Reply to this thread by creating a new Post entity.</span></span>|
|[<span data-ttu-id="abbdc-131">Enumerar publicaciones</span><span class="sxs-lookup"><span data-stu-id="abbdc-131">List Posts</span></span>](../api/conversationthread-list-posts.md) |<span data-ttu-id="abbdc-132">Colección [post](post.md)</span><span class="sxs-lookup"><span data-stu-id="abbdc-132">[post](post.md) collection</span></span>| <span data-ttu-id="abbdc-133">Obtenga las publicaciones del hilo especificado.</span><span class="sxs-lookup"><span data-stu-id="abbdc-133">Get the posts of the specified thread.</span></span> |

## <a name="properties"></a><span data-ttu-id="abbdc-134">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abbdc-134">Properties</span></span>
| <span data-ttu-id="abbdc-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="abbdc-135">Property</span></span>     | <span data-ttu-id="abbdc-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="abbdc-136">Type</span></span>   |<span data-ttu-id="abbdc-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="abbdc-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="abbdc-138">id</span><span class="sxs-lookup"><span data-stu-id="abbdc-138">id</span></span>|<span data-ttu-id="abbdc-139">String</span><span class="sxs-lookup"><span data-stu-id="abbdc-139">String</span></span>| <span data-ttu-id="abbdc-140">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="abbdc-140">Read-only.</span></span>|
|<span data-ttu-id="abbdc-141">toRecipients</span><span class="sxs-lookup"><span data-stu-id="abbdc-141">toRecipients</span></span>|<span data-ttu-id="abbdc-142">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="abbdc-142">[recipient](recipient.md) collection</span></span>|<span data-ttu-id="abbdc-143">Los destinatarios Para: del hilo.</span><span class="sxs-lookup"><span data-stu-id="abbdc-143">The To: recipients for the thread.</span></span>|
|<span data-ttu-id="abbdc-144">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="abbdc-144">ccRecipients</span></span>|<span data-ttu-id="abbdc-145">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="abbdc-145">[recipient](recipient.md) collection</span></span>|<span data-ttu-id="abbdc-146">Los destinatarios CC: del hilo.</span><span class="sxs-lookup"><span data-stu-id="abbdc-146">The Cc: recipients for the thread.</span></span>|
|<span data-ttu-id="abbdc-147">topic</span><span class="sxs-lookup"><span data-stu-id="abbdc-147">topic</span></span>|<span data-ttu-id="abbdc-148">String</span><span class="sxs-lookup"><span data-stu-id="abbdc-148">String</span></span>|<span data-ttu-id="abbdc-p103">El tema de la conversación. Esta propiedad se puede establecer al crear la conversación, pero no se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="abbdc-p103">The topic of the conversation. This property can be set when the conversation is created, but it cannot be updated.</span></span>||
|<span data-ttu-id="abbdc-151">hasAttachments</span><span class="sxs-lookup"><span data-stu-id="abbdc-151">hasAttachments</span></span>|<span data-ttu-id="abbdc-152">Boolean</span><span class="sxs-lookup"><span data-stu-id="abbdc-152">Boolean</span></span>|<span data-ttu-id="abbdc-153">Indica si alguna de las publicaciones de este hilo tiene al menos un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="abbdc-153">Indicates whether any of the posts within this thread has at least one attachment.</span></span>|
|<span data-ttu-id="abbdc-154">lastDeliveredDateTime</span><span class="sxs-lookup"><span data-stu-id="abbdc-154">lastDeliveredDateTime</span></span>|<span data-ttu-id="abbdc-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="abbdc-155">DateTimeOffset</span></span>|<span data-ttu-id="abbdc-p104">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="abbdc-p104">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="abbdc-158">uniqueSenders</span><span class="sxs-lookup"><span data-stu-id="abbdc-158">uniqueSenders</span></span>|<span data-ttu-id="abbdc-159">Colección String</span><span class="sxs-lookup"><span data-stu-id="abbdc-159">String collection</span></span>|<span data-ttu-id="abbdc-160">Todos los usuarios que envían un mensaje a este hilo.</span><span class="sxs-lookup"><span data-stu-id="abbdc-160">All the users that sent a message to this thread.</span></span>|
|<span data-ttu-id="abbdc-161">preview</span><span class="sxs-lookup"><span data-stu-id="abbdc-161">preview</span></span>|<span data-ttu-id="abbdc-162">String</span><span class="sxs-lookup"><span data-stu-id="abbdc-162">String</span></span>|<span data-ttu-id="abbdc-163">Un breve resumen del cuerpo de la última publicación de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="abbdc-163">A short summary from the body of the latest post in this converstaion.</span></span>|
|<span data-ttu-id="abbdc-164">isLocked</span><span class="sxs-lookup"><span data-stu-id="abbdc-164">isLocked</span></span>|<span data-ttu-id="abbdc-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="abbdc-165">Boolean</span></span>|<span data-ttu-id="abbdc-166">Indica si el hilo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="abbdc-166">Indicates if the thread is locked.</span></span>|

## <a name="relationships"></a><span data-ttu-id="abbdc-167">Relaciones</span><span class="sxs-lookup"><span data-stu-id="abbdc-167">Relationships</span></span>
| <span data-ttu-id="abbdc-168">Relación</span><span class="sxs-lookup"><span data-stu-id="abbdc-168">Relationship</span></span> | <span data-ttu-id="abbdc-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="abbdc-169">Type</span></span>   |<span data-ttu-id="abbdc-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="abbdc-170">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="abbdc-171">posts</span><span class="sxs-lookup"><span data-stu-id="abbdc-171">posts</span></span>|<span data-ttu-id="abbdc-172">Colección [post](post.md)</span><span class="sxs-lookup"><span data-stu-id="abbdc-172">[post](post.md) collection</span></span>| <span data-ttu-id="abbdc-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="abbdc-p105">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="abbdc-175">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="abbdc-175">JSON representation</span></span>

<span data-ttu-id="abbdc-176">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="abbdc-176">Here is a JSON representation of the resource</span></span>

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
