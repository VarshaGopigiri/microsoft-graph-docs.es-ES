---
title: Tipo de recurso conversation
description: Una conversación es una colección de hilos y un hilo contiene publicaciones de ese hilo. Todos los hilos y publicaciones de una conversación comparten el mismo asunto.
localization_priority: Normal
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: 0066a636d2b36e74443380598c2ca6e8daf826c1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928160"
---
# <a name="conversation-resource-type"></a><span data-ttu-id="e2d0f-104">Tipo de recurso conversation</span><span class="sxs-lookup"><span data-stu-id="e2d0f-104">conversation resource type</span></span>

<span data-ttu-id="e2d0f-p102">Una conversación es una colección de [hilos](conversationthread.md) y un hilo contiene publicaciones de ese hilo. Todos los hilos y publicaciones de una conversación comparten el mismo asunto.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-p102">A conversation is a collection of [threads](conversationthread.md), and a thread contains posts to that thread. All threads and posts in a conversation share the same subject.</span></span>

<span data-ttu-id="e2d0f-107">Este recurso es compatible con la suscripción a [las notificaciones de cambios](/graph/webhooks).</span><span class="sxs-lookup"><span data-stu-id="e2d0f-107">This resource supports subscribing to [change notifications](/graph/webhooks).</span></span>

## <a name="methods"></a><span data-ttu-id="e2d0f-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2d0f-108">Methods</span></span>

| <span data-ttu-id="e2d0f-109">Método</span><span class="sxs-lookup"><span data-stu-id="e2d0f-109">Method</span></span>       | <span data-ttu-id="e2d0f-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2d0f-110">Return Type</span></span>  |<span data-ttu-id="e2d0f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2d0f-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e2d0f-112">Enumerar conversaciones</span><span class="sxs-lookup"><span data-stu-id="e2d0f-112">List conversations</span></span>](../api/group-list-conversations.md) | <span data-ttu-id="e2d0f-113">Colección [conversation](conversation.md)</span><span class="sxs-lookup"><span data-stu-id="e2d0f-113">[conversation](conversation.md) collection</span></span> |<span data-ttu-id="e2d0f-114">Obtenga la lista de conversaciones en este grupo.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-114">Get the list of conversations in this group.</span></span>|
|[<span data-ttu-id="e2d0f-115">Crear</span><span class="sxs-lookup"><span data-stu-id="e2d0f-115">Create</span></span>](../api/group-post-conversations.md) |[<span data-ttu-id="e2d0f-116">conversation</span><span class="sxs-lookup"><span data-stu-id="e2d0f-116">conversation</span></span>](conversation.md)| <span data-ttu-id="e2d0f-117">Cree una conversación al incluir un hilo y una publicación.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-117">Create a new conversation by including a thread and a post.</span></span>|
|[<span data-ttu-id="e2d0f-118">Obtener conversación</span><span class="sxs-lookup"><span data-stu-id="e2d0f-118">Get conversation</span></span>](../api/conversation-get.md) | [<span data-ttu-id="e2d0f-119">conversation</span><span class="sxs-lookup"><span data-stu-id="e2d0f-119">conversation</span></span>](conversation.md) |<span data-ttu-id="e2d0f-120">Lea las propiedades y las relaciones del objeto de conversación.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-120">Read properties and relationships of conversation object.</span></span>|
|[<span data-ttu-id="e2d0f-121">Eliminar</span><span class="sxs-lookup"><span data-stu-id="e2d0f-121">Delete</span></span>](../api/conversation-delete.md) | <span data-ttu-id="e2d0f-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e2d0f-122">None</span></span> |<span data-ttu-id="e2d0f-123">Elimine el objeto de conversación.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-123">Delete conversation object.</span></span> |
|[<span data-ttu-id="e2d0f-124">Enumerar hilos de conversación</span><span class="sxs-lookup"><span data-stu-id="e2d0f-124">List conversation threads</span></span>](../api/conversation-list-threads.md) |<span data-ttu-id="e2d0f-125">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="e2d0f-125">[conversationThread](conversationthread.md) collection</span></span>| <span data-ttu-id="e2d0f-126">Obtenga todos los hilos de una conversación de grupo.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-126">Get all the threads in a group conversation.</span></span>|
|[<span data-ttu-id="e2d0f-127">Crear hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="e2d0f-127">Create conversation thread</span></span>](../api/conversation-post-threads.md) |<span data-ttu-id="e2d0f-128">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="e2d0f-128">[conversationThread](conversationthread.md) collection</span></span>| <span data-ttu-id="e2d0f-129">Cree un hilo en la conversación especificada.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-129">Create a thread in the specified conversation.</span></span>|

## <a name="properties"></a><span data-ttu-id="e2d0f-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2d0f-130">Properties</span></span>
| <span data-ttu-id="e2d0f-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e2d0f-131">Property</span></span>     | <span data-ttu-id="e2d0f-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2d0f-132">Type</span></span>   |<span data-ttu-id="e2d0f-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2d0f-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e2d0f-134">hasAttachments</span><span class="sxs-lookup"><span data-stu-id="e2d0f-134">hasAttachments</span></span>|<span data-ttu-id="e2d0f-135">Boolean</span><span class="sxs-lookup"><span data-stu-id="e2d0f-135">Boolean</span></span>|<span data-ttu-id="e2d0f-136">Indica si alguna de las publicaciones de esta conversación tiene al menos un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-136">Indicates whether any of the posts within this Conversation has at least one attachment.</span></span>|
|<span data-ttu-id="e2d0f-137">id</span><span class="sxs-lookup"><span data-stu-id="e2d0f-137">id</span></span>|<span data-ttu-id="e2d0f-138">String</span><span class="sxs-lookup"><span data-stu-id="e2d0f-138">String</span></span>|<span data-ttu-id="e2d0f-p103">El identificador único de las conversaciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-p103">The conversations's unique identifier. Read-only.</span></span>|
|<span data-ttu-id="e2d0f-141">lastDeliveredDateTime</span><span class="sxs-lookup"><span data-stu-id="e2d0f-141">lastDeliveredDateTime</span></span>|<span data-ttu-id="e2d0f-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e2d0f-142">DateTimeOffset</span></span>|<span data-ttu-id="e2d0f-p104">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="e2d0f-p104">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="e2d0f-145">preview</span><span class="sxs-lookup"><span data-stu-id="e2d0f-145">preview</span></span>|<span data-ttu-id="e2d0f-146">String</span><span class="sxs-lookup"><span data-stu-id="e2d0f-146">String</span></span>|<span data-ttu-id="e2d0f-147">Un breve resumen del cuerpo de la última publicación de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-147">A short summary from the body of the latest post in this converstaion.</span></span>|
|<span data-ttu-id="e2d0f-148">topic</span><span class="sxs-lookup"><span data-stu-id="e2d0f-148">topic</span></span>|<span data-ttu-id="e2d0f-149">String</span><span class="sxs-lookup"><span data-stu-id="e2d0f-149">String</span></span>|<span data-ttu-id="e2d0f-p105">El tema de la conversación. Esta propiedad se puede establecer al crear la conversación, pero no se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-p105">The topic of the conversation. This property can be set when the conversation is created, but it cannot be updated.</span></span>|
|<span data-ttu-id="e2d0f-152">uniqueSenders</span><span class="sxs-lookup"><span data-stu-id="e2d0f-152">uniqueSenders</span></span>|<span data-ttu-id="e2d0f-153">Colección String</span><span class="sxs-lookup"><span data-stu-id="e2d0f-153">String collection</span></span>|<span data-ttu-id="e2d0f-154">Todos los usuarios que envían un mensaje a esta conversación.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-154">All the users that sent a message to this Conversation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e2d0f-155">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e2d0f-155">Relationships</span></span>
| <span data-ttu-id="e2d0f-156">Relación</span><span class="sxs-lookup"><span data-stu-id="e2d0f-156">Relationship</span></span> | <span data-ttu-id="e2d0f-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2d0f-157">Type</span></span>   |<span data-ttu-id="e2d0f-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2d0f-158">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e2d0f-159">threads</span><span class="sxs-lookup"><span data-stu-id="e2d0f-159">threads</span></span>|<span data-ttu-id="e2d0f-160">Colección [conversationThread](conversationthread.md)</span><span class="sxs-lookup"><span data-stu-id="e2d0f-160">[conversationThread](conversationthread.md) collection</span></span>|<span data-ttu-id="e2d0f-p106">Una colección de todos los hilos de la conversación. Una propiedad de navegación. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-p106">A collection of all the conversation threads in the conversation. A navigation property. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e2d0f-165">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e2d0f-165">JSON representation</span></span>

<span data-ttu-id="e2d0f-166">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e2d0f-166">Here is a JSON representation of the resource</span></span>

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
