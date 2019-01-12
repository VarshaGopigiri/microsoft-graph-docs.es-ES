---
title: Tipo de recurso conversation
description: Una conversación es una colección de hilos y un hilo contiene publicaciones de ese hilo. Todos los hilos y publicaciones de una conversación comparten el mismo asunto.
localization_priority: Normal
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: 5cacad2b9539c398251ffd07899df7beb3c2f378
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991443"
---
# <a name="conversation-resource-type"></a><span data-ttu-id="9c3f9-104">Tipo de recurso conversation</span><span class="sxs-lookup"><span data-stu-id="9c3f9-104">conversation resource type</span></span>

> <span data-ttu-id="9c3f9-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9c3f9-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9c3f9-p103">Una conversación es una colección de [hilos](conversationthread.md) y un hilo contiene publicaciones de ese hilo. Todos los hilos y publicaciones de una conversación comparten el mismo asunto.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-p103">A conversation is a collection of [threads](conversationthread.md), and a thread contains posts to that thread. All threads and posts in a conversation share the same subject.</span></span>

<span data-ttu-id="9c3f9-109">Este recurso es compatible con la suscripción a [las notificaciones de cambios](/graph/webhooks).</span><span class="sxs-lookup"><span data-stu-id="9c3f9-109">This resource supports subscribing to [change notifications](/graph/webhooks).</span></span>

## <a name="methods"></a><span data-ttu-id="9c3f9-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c3f9-110">Methods</span></span>

| <span data-ttu-id="9c3f9-111">Método</span><span class="sxs-lookup"><span data-stu-id="9c3f9-111">Method</span></span>       | <span data-ttu-id="9c3f9-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c3f9-112">Return Type</span></span>  |<span data-ttu-id="9c3f9-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c3f9-113">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9c3f9-114">Enumerar conversaciones</span><span class="sxs-lookup"><span data-stu-id="9c3f9-114">List conversations</span></span>](../api/group-list-conversations.md) | <span data-ttu-id="9c3f9-115">Colección [conversation](conversation.md)</span><span class="sxs-lookup"><span data-stu-id="9c3f9-115">[conversation](conversation.md) collection</span></span> |<span data-ttu-id="9c3f9-116">Obtenga la lista de conversaciones en este grupo.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-116">Get the list of conversations in this group.</span></span>|
|[<span data-ttu-id="9c3f9-117">Crear</span><span class="sxs-lookup"><span data-stu-id="9c3f9-117">Create</span></span>](../api/group-post-conversations.md) |[<span data-ttu-id="9c3f9-118">conversation</span><span class="sxs-lookup"><span data-stu-id="9c3f9-118">conversation</span></span>](conversation.md)| <span data-ttu-id="9c3f9-119">Cree una conversación al incluir un hilo y una publicación.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-119">Create a new conversation by including a thread and a post.</span></span>|
|[<span data-ttu-id="9c3f9-120">Obtener conversación</span><span class="sxs-lookup"><span data-stu-id="9c3f9-120">Get conversation</span></span>](../api/conversation-get.md) | [<span data-ttu-id="9c3f9-121">conversation</span><span class="sxs-lookup"><span data-stu-id="9c3f9-121">conversation</span></span>](conversation.md) |<span data-ttu-id="9c3f9-122">Lea las propiedades y las relaciones del objeto de conversación.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-122">Read properties and relationships of conversation object.</span></span>|
|[<span data-ttu-id="9c3f9-123">Eliminar</span><span class="sxs-lookup"><span data-stu-id="9c3f9-123">Delete</span></span>](../api/conversation-delete.md) | <span data-ttu-id="9c3f9-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9c3f9-124">None</span></span> |<span data-ttu-id="9c3f9-125">Elimine el objeto de conversación.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-125">Delete conversation object.</span></span> |
|[<span data-ttu-id="9c3f9-126">Enumerar hilos de conversación</span><span class="sxs-lookup"><span data-stu-id="9c3f9-126">List conversation threads</span></span>](../api/conversation-list-threads.md) |<span data-ttu-id="9c3f9-127">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="9c3f9-127">[conversationThread](conversationthread.md) collection</span></span>| <span data-ttu-id="9c3f9-128">Obtenga todos los hilos de una conversación de grupo.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-128">Get all the threads in a group conversation.</span></span>|
|[<span data-ttu-id="9c3f9-129">Crear hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="9c3f9-129">Create conversation thread</span></span>](../api/conversation-post-threads.md) |<span data-ttu-id="9c3f9-130">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="9c3f9-130">[conversationThread](conversationthread.md) collection</span></span>| <span data-ttu-id="9c3f9-131">Cree un hilo en la conversación especificada.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-131">Create a thread in the specified conversation.</span></span>|

## <a name="properties"></a><span data-ttu-id="9c3f9-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9c3f9-132">Properties</span></span>
| <span data-ttu-id="9c3f9-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9c3f9-133">Property</span></span>     | <span data-ttu-id="9c3f9-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c3f9-134">Type</span></span>   |<span data-ttu-id="9c3f9-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c3f9-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9c3f9-136">hasAttachments</span><span class="sxs-lookup"><span data-stu-id="9c3f9-136">hasAttachments</span></span>|<span data-ttu-id="9c3f9-137">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c3f9-137">Boolean</span></span>|<span data-ttu-id="9c3f9-138">Indica si alguna de las publicaciones de esta conversación tiene al menos un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-138">Indicates whether any of the posts within this Conversation has at least one attachment.</span></span>|
|<span data-ttu-id="9c3f9-139">id</span><span class="sxs-lookup"><span data-stu-id="9c3f9-139">id</span></span>|<span data-ttu-id="9c3f9-140">String</span><span class="sxs-lookup"><span data-stu-id="9c3f9-140">String</span></span>|<span data-ttu-id="9c3f9-p104">El identificador único de las conversaciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-p104">The conversations's unique identifier. Read-only.</span></span>|
|<span data-ttu-id="9c3f9-143">lastDeliveredDateTime</span><span class="sxs-lookup"><span data-stu-id="9c3f9-143">lastDeliveredDateTime</span></span>|<span data-ttu-id="9c3f9-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9c3f9-144">DateTimeOffset</span></span>|<span data-ttu-id="9c3f9-p105">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="9c3f9-p105">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="9c3f9-147">preview</span><span class="sxs-lookup"><span data-stu-id="9c3f9-147">preview</span></span>|<span data-ttu-id="9c3f9-148">String</span><span class="sxs-lookup"><span data-stu-id="9c3f9-148">String</span></span>|<span data-ttu-id="9c3f9-149">Un breve resumen del cuerpo de la última publicación de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-149">A short summary from the body of the latest post in this converstaion.</span></span>|
|<span data-ttu-id="9c3f9-150">topic</span><span class="sxs-lookup"><span data-stu-id="9c3f9-150">topic</span></span>|<span data-ttu-id="9c3f9-151">String</span><span class="sxs-lookup"><span data-stu-id="9c3f9-151">String</span></span>|<span data-ttu-id="9c3f9-p106">El tema de la conversación. Esta propiedad se puede establecer al crear la conversación, pero no se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-p106">The topic of the conversation. This property can be set when the conversation is created, but it cannot be updated.</span></span>|
|<span data-ttu-id="9c3f9-154">uniqueSenders</span><span class="sxs-lookup"><span data-stu-id="9c3f9-154">uniqueSenders</span></span>|<span data-ttu-id="9c3f9-155">Colección String</span><span class="sxs-lookup"><span data-stu-id="9c3f9-155">String collection</span></span>|<span data-ttu-id="9c3f9-156">Todos los usuarios que envían un mensaje a esta conversación.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-156">All the users that sent a message to this Conversation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9c3f9-157">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9c3f9-157">Relationships</span></span>
| <span data-ttu-id="9c3f9-158">Relación</span><span class="sxs-lookup"><span data-stu-id="9c3f9-158">Relationship</span></span> | <span data-ttu-id="9c3f9-159">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c3f9-159">Type</span></span>   |<span data-ttu-id="9c3f9-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c3f9-160">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9c3f9-161">threads</span><span class="sxs-lookup"><span data-stu-id="9c3f9-161">threads</span></span>|<span data-ttu-id="9c3f9-162">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="9c3f9-162">[conversationThread](conversationthread.md) collection</span></span>|<span data-ttu-id="9c3f9-p107">Una colección de todos los hilos de la conversación. Una propiedad de navegación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9c3f9-p107">A collection of all the conversation threads in the conversation. A navigation property. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9c3f9-167">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9c3f9-167">JSON representation</span></span>

<span data-ttu-id="9c3f9-168">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9c3f9-168">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "threads"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.conversation"
}-->

```json
{
  "hasAttachments": true,
  "id": "string (identifier)",
  "lastDeliveredDateTime": "String (timestamp)",
  "preview": "string",
  "topic": "string",
  "uniqueSenders": ["string"]
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
