---
title: Tipo de recurso conversationThread
description: Un recurso conversationThread es una colección de posts.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: d541d4ac47272c2825602b28526b2b7c9d5f3fcb
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933557"
---
# <a name="conversationthread-resource-type"></a><span data-ttu-id="42e3f-103">Tipo de recurso conversationThread</span><span class="sxs-lookup"><span data-stu-id="42e3f-103">conversationThread resource type</span></span>

> <span data-ttu-id="42e3f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="42e3f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="42e3f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="42e3f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="42e3f-106">Un recurso conversationThread es una colección de [posts](post.md).</span><span class="sxs-lookup"><span data-stu-id="42e3f-106">A conversationThread is a collection of [posts](post.md).</span></span>

<span data-ttu-id="42e3f-p102">La colección de destinatarios de la última publicación son los destinatarios agregados del hilo completo. Un hilo puede tener una colección creciente de destinatarios. Se crea un hilo al eliminar un destinatario del hilo.</span><span class="sxs-lookup"><span data-stu-id="42e3f-p102">The last post's recipients collection is the aggregated recipients of the entire thread. A thread can have a growing collection of recipients. A new thread is created when a recipient is removed from the thread.</span></span>

## <a name="methods"></a><span data-ttu-id="42e3f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="42e3f-110">Methods</span></span>

| <span data-ttu-id="42e3f-111">Método</span><span class="sxs-lookup"><span data-stu-id="42e3f-111">Method</span></span>       | <span data-ttu-id="42e3f-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42e3f-112">Return Type</span></span>  |<span data-ttu-id="42e3f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="42e3f-113">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="42e3f-114">Enumerar hilos</span><span class="sxs-lookup"><span data-stu-id="42e3f-114">List threads</span></span>](../api/group-list-threads.md) | <span data-ttu-id="42e3f-115">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="42e3f-115">[conversationThread](conversationthread.md) collection</span></span> |<span data-ttu-id="42e3f-116">Obtenga todos los hilos de un grupo.</span><span class="sxs-lookup"><span data-stu-id="42e3f-116">Get all the threads of a group.</span></span>|
|[<span data-ttu-id="42e3f-117">Crear hilo</span><span class="sxs-lookup"><span data-stu-id="42e3f-117">Create thread</span></span>](../api/group-post-threads.md) | [<span data-ttu-id="42e3f-118">conversationThread</span><span class="sxs-lookup"><span data-stu-id="42e3f-118">conversationThread</span></span>](conversationthread.md) |<span data-ttu-id="42e3f-p103">Inicie una nueva conversación creando primero un hilo. Se crean una conversación, un hilo de conversación y una publicación en el grupo.</span><span class="sxs-lookup"><span data-stu-id="42e3f-p103">Start a new conversation by first creating a thread. A new conversation, conversation thread, and post are created in the group.</span></span>|
|[<span data-ttu-id="42e3f-121">Obtener conversationThread</span><span class="sxs-lookup"><span data-stu-id="42e3f-121">Get conversationThread</span></span>](../api/conversationthread-get.md) | [<span data-ttu-id="42e3f-122">conversationThread</span><span class="sxs-lookup"><span data-stu-id="42e3f-122">conversationThread</span></span>](conversationthread.md) |<span data-ttu-id="42e3f-123">Obtenga un hilo específico que pertenece a un grupo.</span><span class="sxs-lookup"><span data-stu-id="42e3f-123">Get a specific thread that belongs to a group.</span></span> |
|[<span data-ttu-id="42e3f-124">Actualizar</span><span class="sxs-lookup"><span data-stu-id="42e3f-124">Update</span></span>](../api/conversationthread-update.md) | [<span data-ttu-id="42e3f-125">conversationThread</span><span class="sxs-lookup"><span data-stu-id="42e3f-125">conversationThread</span></span>](conversationthread.md)  |<span data-ttu-id="42e3f-126">Actualice el objeto conversationThread.</span><span class="sxs-lookup"><span data-stu-id="42e3f-126">Update conversationThread object.</span></span> |
|[<span data-ttu-id="42e3f-127">Eliminar</span><span class="sxs-lookup"><span data-stu-id="42e3f-127">Delete</span></span>](../api/conversationthread-delete.md) | <span data-ttu-id="42e3f-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="42e3f-128">None</span></span> |<span data-ttu-id="42e3f-129">Elimine el objeto conversationThread.</span><span class="sxs-lookup"><span data-stu-id="42e3f-129">Delete conversationThread object.</span></span> |
|[<span data-ttu-id="42e3f-130">reply</span><span class="sxs-lookup"><span data-stu-id="42e3f-130">reply</span></span>](../api/conversationthread-reply.md)|<span data-ttu-id="42e3f-131">Ninguno</span><span class="sxs-lookup"><span data-stu-id="42e3f-131">None</span></span>|<span data-ttu-id="42e3f-132">Responda a este hilo mediante la creación de una nueva entidad Post.</span><span class="sxs-lookup"><span data-stu-id="42e3f-132">Reply to this thread by creating a new Post entity.</span></span>|
|[<span data-ttu-id="42e3f-133">Enumerar publicaciones</span><span class="sxs-lookup"><span data-stu-id="42e3f-133">List Posts</span></span>](../api/conversationthread-list-posts.md) |<span data-ttu-id="42e3f-134">Colección [post](post.md)</span><span class="sxs-lookup"><span data-stu-id="42e3f-134">[post](post.md) collection</span></span>| <span data-ttu-id="42e3f-135">Obtenga las publicaciones del hilo especificado.</span><span class="sxs-lookup"><span data-stu-id="42e3f-135">Get the posts of the specified thread.</span></span> |

## <a name="properties"></a><span data-ttu-id="42e3f-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42e3f-136">Properties</span></span>
| <span data-ttu-id="42e3f-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="42e3f-137">Property</span></span>     | <span data-ttu-id="42e3f-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="42e3f-138">Type</span></span>   |<span data-ttu-id="42e3f-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="42e3f-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="42e3f-140">id</span><span class="sxs-lookup"><span data-stu-id="42e3f-140">id</span></span>|<span data-ttu-id="42e3f-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="42e3f-141">String</span></span>| <span data-ttu-id="42e3f-142">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="42e3f-142">Read-only.</span></span>|
|<span data-ttu-id="42e3f-143">toRecipients</span><span class="sxs-lookup"><span data-stu-id="42e3f-143">toRecipients</span></span>|<span data-ttu-id="42e3f-144">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="42e3f-144">[recipient](recipient.md) collection</span></span>|<span data-ttu-id="42e3f-145">Los destinatarios Para: del hilo.</span><span class="sxs-lookup"><span data-stu-id="42e3f-145">The To: recipients for the thread.</span></span>|
|<span data-ttu-id="42e3f-146">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="42e3f-146">ccRecipients</span></span>|<span data-ttu-id="42e3f-147">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="42e3f-147">[recipient](recipient.md) collection</span></span>|<span data-ttu-id="42e3f-148">Los destinatarios CC: del hilo.</span><span class="sxs-lookup"><span data-stu-id="42e3f-148">The Cc: recipients for the thread.</span></span>|
|<span data-ttu-id="42e3f-149">topic</span><span class="sxs-lookup"><span data-stu-id="42e3f-149">topic</span></span>|<span data-ttu-id="42e3f-150">String</span><span class="sxs-lookup"><span data-stu-id="42e3f-150">String</span></span>|<span data-ttu-id="42e3f-p104">El tema de la conversación. Esta propiedad se puede establecer al crear la conversación, pero no se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="42e3f-p104">The topic of the conversation. This property can be set when the conversation is created, but it cannot be updated.</span></span>||
|<span data-ttu-id="42e3f-153">hasAttachments</span><span class="sxs-lookup"><span data-stu-id="42e3f-153">hasAttachments</span></span>|<span data-ttu-id="42e3f-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="42e3f-154">Boolean</span></span>|<span data-ttu-id="42e3f-155">Indica si alguna de las publicaciones de este hilo tiene al menos un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="42e3f-155">Indicates whether any of the posts within this thread has at least one attachment.</span></span>|
|<span data-ttu-id="42e3f-156">lastDeliveredDateTime</span><span class="sxs-lookup"><span data-stu-id="42e3f-156">lastDeliveredDateTime</span></span>|<span data-ttu-id="42e3f-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="42e3f-157">DateTimeOffset</span></span>|<span data-ttu-id="42e3f-p105">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="42e3f-p105">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="42e3f-160">uniqueSenders</span><span class="sxs-lookup"><span data-stu-id="42e3f-160">uniqueSenders</span></span>|<span data-ttu-id="42e3f-161">Colección String</span><span class="sxs-lookup"><span data-stu-id="42e3f-161">String collection</span></span>|<span data-ttu-id="42e3f-162">Todos los usuarios que envían un mensaje a este hilo.</span><span class="sxs-lookup"><span data-stu-id="42e3f-162">All the users that sent a message to this thread.</span></span>|
|<span data-ttu-id="42e3f-163">preview</span><span class="sxs-lookup"><span data-stu-id="42e3f-163">preview</span></span>|<span data-ttu-id="42e3f-164">String</span><span class="sxs-lookup"><span data-stu-id="42e3f-164">String</span></span>|<span data-ttu-id="42e3f-165">Un breve resumen del cuerpo de la última publicación de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="42e3f-165">A short summary from the body of the latest post in this converstaion.</span></span>|
|<span data-ttu-id="42e3f-166">isLocked</span><span class="sxs-lookup"><span data-stu-id="42e3f-166">isLocked</span></span>|<span data-ttu-id="42e3f-167">Boolean</span><span class="sxs-lookup"><span data-stu-id="42e3f-167">Boolean</span></span>|<span data-ttu-id="42e3f-168">Indica si el hilo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="42e3f-168">Indicates if the thread is locked.</span></span>|

## <a name="relationships"></a><span data-ttu-id="42e3f-169">Relaciones</span><span class="sxs-lookup"><span data-stu-id="42e3f-169">Relationships</span></span>
| <span data-ttu-id="42e3f-170">Relación</span><span class="sxs-lookup"><span data-stu-id="42e3f-170">Relationship</span></span> | <span data-ttu-id="42e3f-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="42e3f-171">Type</span></span>   |<span data-ttu-id="42e3f-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="42e3f-172">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="42e3f-173">posts</span><span class="sxs-lookup"><span data-stu-id="42e3f-173">posts</span></span>|<span data-ttu-id="42e3f-174">Colección [post](post.md)</span><span class="sxs-lookup"><span data-stu-id="42e3f-174">[post](post.md) collection</span></span>| <span data-ttu-id="42e3f-p106">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="42e3f-p106">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="42e3f-177">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="42e3f-177">JSON representation</span></span>

<span data-ttu-id="42e3f-178">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="42e3f-178">Here is a JSON representation of the resource</span></span>

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
