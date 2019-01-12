---
title: Tipo de recurso conversationThread
description: Un recurso conversationThread es una colección de posts.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: a1a45f5ac6d26b58f1179616d3a6b9b76c6c1618
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912319"
---
# <a name="conversationthread-resource-type"></a><span data-ttu-id="01a42-103">Tipo de recurso conversationThread</span><span class="sxs-lookup"><span data-stu-id="01a42-103">conversationThread resource type</span></span>
<span data-ttu-id="01a42-104">Un recurso conversationThread es una colección de [posts](post.md).</span><span class="sxs-lookup"><span data-stu-id="01a42-104">A conversationThread is a collection of [posts](post.md).</span></span>

<span data-ttu-id="01a42-p101">La colección de destinatarios de la última publicación son los destinatarios agregados del hilo completo. Un hilo puede tener una colección creciente de destinatarios. Se crea un hilo al eliminar un destinatario del hilo.</span><span class="sxs-lookup"><span data-stu-id="01a42-p101">The last post's recipients collection is the aggregated recipients of the entire thread. A thread can have a growing collection of recipients. A new thread is created when a recipient is removed from the thread.</span></span>

## <a name="methods"></a><span data-ttu-id="01a42-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="01a42-108">Methods</span></span>

| <span data-ttu-id="01a42-109">Método</span><span class="sxs-lookup"><span data-stu-id="01a42-109">Method</span></span>       | <span data-ttu-id="01a42-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01a42-110">Return Type</span></span>  |<span data-ttu-id="01a42-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="01a42-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="01a42-112">Enumerar hilos</span><span class="sxs-lookup"><span data-stu-id="01a42-112">List threads</span></span>](../api/group-list-threads.md) | <span data-ttu-id="01a42-113">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="01a42-113">[conversationThread](conversationthread.md) collection</span></span> |<span data-ttu-id="01a42-114">Obtenga todos los hilos de un grupo.</span><span class="sxs-lookup"><span data-stu-id="01a42-114">Get all the threads of a group.</span></span>|
|[<span data-ttu-id="01a42-115">Crear hilo</span><span class="sxs-lookup"><span data-stu-id="01a42-115">Create thread</span></span>](../api/group-post-threads.md) | [<span data-ttu-id="01a42-116">conversationThread</span><span class="sxs-lookup"><span data-stu-id="01a42-116">conversationThread</span></span>](conversationthread.md) |<span data-ttu-id="01a42-p102">Inicie una nueva conversación creando primero un hilo. Se crean una conversación, un hilo de conversación y una publicación en el grupo.</span><span class="sxs-lookup"><span data-stu-id="01a42-p102">Start a new conversation by first creating a thread. A new conversation, conversation thread, and post are created in the group.</span></span>|
|[<span data-ttu-id="01a42-119">Obtener conversationThread</span><span class="sxs-lookup"><span data-stu-id="01a42-119">Get conversationThread</span></span>](../api/conversationthread-get.md) | [<span data-ttu-id="01a42-120">conversationThread</span><span class="sxs-lookup"><span data-stu-id="01a42-120">conversationThread</span></span>](conversationthread.md) |<span data-ttu-id="01a42-121">Obtenga un hilo específico que pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="01a42-121">Get a specific thread that belongs to a group.</span></span> |
|[<span data-ttu-id="01a42-122">Actualizar</span><span class="sxs-lookup"><span data-stu-id="01a42-122">Update</span></span>](../api/conversationthread-update.md) | [<span data-ttu-id="01a42-123">conversationThread</span><span class="sxs-lookup"><span data-stu-id="01a42-123">conversationThread</span></span>](conversationthread.md)  |<span data-ttu-id="01a42-124">Actualice el objeto conversationThread.</span><span class="sxs-lookup"><span data-stu-id="01a42-124">Update conversationThread object.</span></span> |
|[<span data-ttu-id="01a42-125">Eliminar</span><span class="sxs-lookup"><span data-stu-id="01a42-125">Delete</span></span>](../api/conversationthread-delete.md) | <span data-ttu-id="01a42-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="01a42-126">None</span></span> |<span data-ttu-id="01a42-127">Elimine el objeto conversationThread.</span><span class="sxs-lookup"><span data-stu-id="01a42-127">Delete conversationThread object.</span></span> |
|[<span data-ttu-id="01a42-128">Responder</span><span class="sxs-lookup"><span data-stu-id="01a42-128">Reply</span></span>](../api/conversationthread-reply.md)|<span data-ttu-id="01a42-129">Ninguno</span><span class="sxs-lookup"><span data-stu-id="01a42-129">None</span></span>|<span data-ttu-id="01a42-130">Responda a este hilo mediante la creación de una nueva entidad Post.</span><span class="sxs-lookup"><span data-stu-id="01a42-130">Reply to this thread by creating a new Post entity.</span></span>|
|[<span data-ttu-id="01a42-131">Enumerar publicaciones</span><span class="sxs-lookup"><span data-stu-id="01a42-131">List Posts</span></span>](../api/conversationthread-list-posts.md) |<span data-ttu-id="01a42-132">Colección [post](post.md)</span><span class="sxs-lookup"><span data-stu-id="01a42-132">[post](post.md) collection</span></span>| <span data-ttu-id="01a42-133">Obtenga las publicaciones del hilo especificado.</span><span class="sxs-lookup"><span data-stu-id="01a42-133">Get the posts of the specified thread.</span></span> |

## <a name="properties"></a><span data-ttu-id="01a42-134">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01a42-134">Properties</span></span>
| <span data-ttu-id="01a42-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01a42-135">Property</span></span>     | <span data-ttu-id="01a42-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="01a42-136">Type</span></span>   |<span data-ttu-id="01a42-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="01a42-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="01a42-138">id</span><span class="sxs-lookup"><span data-stu-id="01a42-138">id</span></span>|<span data-ttu-id="01a42-139">String</span><span class="sxs-lookup"><span data-stu-id="01a42-139">String</span></span>| <span data-ttu-id="01a42-140">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01a42-140">Read-only.</span></span>|
|<span data-ttu-id="01a42-141">toRecipients</span><span class="sxs-lookup"><span data-stu-id="01a42-141">toRecipients</span></span>|<span data-ttu-id="01a42-142">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="01a42-142">[recipient](recipient.md) collection</span></span>|<span data-ttu-id="01a42-143">Los destinatarios Para: del hilo.</span><span class="sxs-lookup"><span data-stu-id="01a42-143">The To: recipients for the thread.</span></span>|
|<span data-ttu-id="01a42-144">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="01a42-144">ccRecipients</span></span>|<span data-ttu-id="01a42-145">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="01a42-145">[recipient](recipient.md) collection</span></span>|<span data-ttu-id="01a42-146">Los destinatarios CC: del hilo.</span><span class="sxs-lookup"><span data-stu-id="01a42-146">The Cc: recipients for the thread.</span></span>|
|<span data-ttu-id="01a42-147">topic</span><span class="sxs-lookup"><span data-stu-id="01a42-147">topic</span></span>|<span data-ttu-id="01a42-148">String</span><span class="sxs-lookup"><span data-stu-id="01a42-148">String</span></span>|<span data-ttu-id="01a42-p103">El tema de la conversación. Esta propiedad se puede establecer al crear la conversación, pero no se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="01a42-p103">The topic of the conversation. This property can be set when the conversation is created, but it cannot be updated.</span></span>||
|<span data-ttu-id="01a42-151">hasAttachments</span><span class="sxs-lookup"><span data-stu-id="01a42-151">hasAttachments</span></span>|<span data-ttu-id="01a42-152">Boolean</span><span class="sxs-lookup"><span data-stu-id="01a42-152">Boolean</span></span>|<span data-ttu-id="01a42-153">Indica si alguna de las publicaciones de este hilo tiene al menos un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="01a42-153">Indicates whether any of the posts within this thread has at least one attachment.</span></span>|
|<span data-ttu-id="01a42-154">lastDeliveredDateTime</span><span class="sxs-lookup"><span data-stu-id="01a42-154">lastDeliveredDateTime</span></span>|<span data-ttu-id="01a42-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="01a42-155">DateTimeOffset</span></span>|<span data-ttu-id="01a42-p104">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="01a42-p104">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="01a42-158">uniqueSenders</span><span class="sxs-lookup"><span data-stu-id="01a42-158">uniqueSenders</span></span>|<span data-ttu-id="01a42-159">Colección String</span><span class="sxs-lookup"><span data-stu-id="01a42-159">String collection</span></span>|<span data-ttu-id="01a42-160">Todos los usuarios que envían un mensaje a este hilo.</span><span class="sxs-lookup"><span data-stu-id="01a42-160">All the users that sent a message to this thread.</span></span>|
|<span data-ttu-id="01a42-161">preview</span><span class="sxs-lookup"><span data-stu-id="01a42-161">preview</span></span>|<span data-ttu-id="01a42-162">String</span><span class="sxs-lookup"><span data-stu-id="01a42-162">String</span></span>|<span data-ttu-id="01a42-163">Un breve resumen del cuerpo de la última publicación de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="01a42-163">A short summary from the body of the latest post in this converstaion.</span></span>|
|<span data-ttu-id="01a42-164">isLocked</span><span class="sxs-lookup"><span data-stu-id="01a42-164">isLocked</span></span>|<span data-ttu-id="01a42-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="01a42-165">Boolean</span></span>|<span data-ttu-id="01a42-166">Indica si el hilo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="01a42-166">Indicates if the thread is locked.</span></span>|

## <a name="relationships"></a><span data-ttu-id="01a42-167">Relaciones</span><span class="sxs-lookup"><span data-stu-id="01a42-167">Relationships</span></span>
| <span data-ttu-id="01a42-168">Relación</span><span class="sxs-lookup"><span data-stu-id="01a42-168">Relationship</span></span> | <span data-ttu-id="01a42-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="01a42-169">Type</span></span>   |<span data-ttu-id="01a42-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="01a42-170">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="01a42-171">posts</span><span class="sxs-lookup"><span data-stu-id="01a42-171">posts</span></span>|<span data-ttu-id="01a42-172">Colección [post](post.md)</span><span class="sxs-lookup"><span data-stu-id="01a42-172">[post](post.md) collection</span></span>| <span data-ttu-id="01a42-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="01a42-p105">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="01a42-175">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="01a42-175">JSON representation</span></span>

<span data-ttu-id="01a42-176">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="01a42-176">Here is a JSON representation of the resource</span></span>

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
