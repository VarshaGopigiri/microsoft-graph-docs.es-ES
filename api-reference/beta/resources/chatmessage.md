---
title: tipo de recurso chatMessage
description: Representa un mensaje de chat individuales dentro de una entidad de canal o chat. El mensaje puede ser un mensaje de raíz o parte de un subproceso que se define mediante la propiedad **replyToId** en el mensaje.
ms.openlocfilehash: 1fba27567d5a1c80a36a5758925ec427735504cf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083272"
---
# <a name="chatmessage-resource-type"></a><span data-ttu-id="0f638-104">tipo de recurso chatMessage</span><span class="sxs-lookup"><span data-stu-id="0f638-104">chatMessage resource type</span></span>

> <span data-ttu-id="0f638-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0f638-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0f638-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0f638-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0f638-107">Representa un mensaje de chat individuales dentro de una entidad de [canal](channel.md) o chat.</span><span class="sxs-lookup"><span data-stu-id="0f638-107">Represents an individual chat message within a [channel](channel.md) or chat entity.</span></span> <span data-ttu-id="0f638-108">El mensaje puede ser un mensaje de raíz o parte de un subproceso que se define mediante la propiedad **replyToId** en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0f638-108">The message can be an root message or part of a thread that is defined by the **replyToId** property in the message.</span></span>

## <a name="methods"></a><span data-ttu-id="0f638-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0f638-109">Methods</span></span>

| <span data-ttu-id="0f638-110">Método</span><span class="sxs-lookup"><span data-stu-id="0f638-110">Method</span></span>       | <span data-ttu-id="0f638-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f638-111">Return Type</span></span>  |<span data-ttu-id="0f638-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f638-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="0f638-113">Mensajes del canal de lista</span><span class="sxs-lookup"><span data-stu-id="0f638-113">List Channel messages</span></span>](../api/channel-list-messages.md) | <span data-ttu-id="0f638-114">colección de [chatmessage](chatmessage.md)</span><span class="sxs-lookup"><span data-stu-id="0f638-114">[chatmessage](chatmessage.md) collection</span></span> | <span data-ttu-id="0f638-115">Obtener la lista de todos los mensajes de raíz en un canal.</span><span class="sxs-lookup"><span data-stu-id="0f638-115">Get the list of all root messages in a channel.</span></span>|
|[<span data-ttu-id="0f638-116">Mensaje de canal de Get</span><span class="sxs-lookup"><span data-stu-id="0f638-116">Get Channel message</span></span>](../api/channel-get-message.md) | [<span data-ttu-id="0f638-117">chatmessage</span><span class="sxs-lookup"><span data-stu-id="0f638-117">chatmessage</span></span>](chatmessage.md) | <span data-ttu-id="0f638-118">Recibe un mensaje de raíz única de un canal.</span><span class="sxs-lookup"><span data-stu-id="0f638-118">Get a single root message from a channel.</span></span>|
|[<span data-ttu-id="0f638-119">Lista de respuestas a un mensaje</span><span class="sxs-lookup"><span data-stu-id="0f638-119">List replies to a message</span></span>](../api/channel-list-messagereplies.md) | <span data-ttu-id="0f638-120">colección de [chatmessage](chatmessage.md)</span><span class="sxs-lookup"><span data-stu-id="0f638-120">[chatmessage](chatmessage.md) collection</span></span>| <span data-ttu-id="0f638-121">Obtener la lista de todas las respuestas a un mensaje en el canal.</span><span class="sxs-lookup"><span data-stu-id="0f638-121">Get the list of all replies to a message in channel.</span></span>|
|[<span data-ttu-id="0f638-122">Obtener una respuesta a un mensaje</span><span class="sxs-lookup"><span data-stu-id="0f638-122">Get a reply to a message</span></span>](../api/channel-get-messagereply.md) | [<span data-ttu-id="0f638-123">chatmessage</span><span class="sxs-lookup"><span data-stu-id="0f638-123">chatmessage</span></span>](chatmessage.md)| <span data-ttu-id="0f638-124">Obtenga una sola respuesta a un mensaje en un canal.</span><span class="sxs-lookup"><span data-stu-id="0f638-124">Get a single reply to a message in a channel.</span></span>|

## <a name="properties"></a><span data-ttu-id="0f638-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0f638-125">Properties</span></span>
| <span data-ttu-id="0f638-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0f638-126">Property</span></span>     | <span data-ttu-id="0f638-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0f638-127">Type</span></span>   |<span data-ttu-id="0f638-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f638-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0f638-129">id</span><span class="sxs-lookup"><span data-stu-id="0f638-129">id</span></span>|<span data-ttu-id="0f638-130">String</span><span class="sxs-lookup"><span data-stu-id="0f638-130">String</span></span>| <span data-ttu-id="0f638-131">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0f638-131">Read-only.</span></span> <span data-ttu-id="0f638-132">Identificador único del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0f638-132">Unique ID of the message.</span></span>|
|<span data-ttu-id="0f638-133">replyToId</span><span class="sxs-lookup"><span data-stu-id="0f638-133">replyToId</span></span>| <span data-ttu-id="0f638-134">string</span><span class="sxs-lookup"><span data-stu-id="0f638-134">string</span></span> | <span data-ttu-id="0f638-135">Identificador del mensaje de mensaje/raíz primario del subproceso</span><span class="sxs-lookup"><span data-stu-id="0f638-135">Id of the parent message/root message of the thread</span></span> |
|<span data-ttu-id="0f638-136">from</span><span class="sxs-lookup"><span data-stu-id="0f638-136">from</span></span>|[<span data-ttu-id="0f638-137">identitySet</span><span class="sxs-lookup"><span data-stu-id="0f638-137">identitySet</span></span>](identityset.md)| <span data-ttu-id="0f638-138">Detalles del remitente del mensaje</span><span class="sxs-lookup"><span data-stu-id="0f638-138">Details of the sender of the message</span></span>|
|<span data-ttu-id="0f638-139">etag</span><span class="sxs-lookup"><span data-stu-id="0f638-139">etag</span></span>| <span data-ttu-id="0f638-140">string</span><span class="sxs-lookup"><span data-stu-id="0f638-140">string</span></span> | <span data-ttu-id="0f638-141">Número de versión del mensaje</span><span class="sxs-lookup"><span data-stu-id="0f638-141">Version number of the message</span></span> |
|<span data-ttu-id="0f638-142">messageType</span><span class="sxs-lookup"><span data-stu-id="0f638-142">messageType</span></span>|<span data-ttu-id="0f638-143">String</span><span class="sxs-lookup"><span data-stu-id="0f638-143">String</span></span>|<span data-ttu-id="0f638-144">Los valores de tipo de mensaje, actual admitido son: mensajes, chatEvent, escribir</span><span class="sxs-lookup"><span data-stu-id="0f638-144">The type of message, current supported values are: message, chatEvent, Typing</span></span>|
|<span data-ttu-id="0f638-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0f638-145">createdDateTime</span></span>|<span data-ttu-id="0f638-146">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0f638-146">dateTimeOffset</span></span>|<span data-ttu-id="0f638-147">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0f638-147">Read only.</span></span> <span data-ttu-id="0f638-148">Marca de hora de cuándo se creó el mensaje</span><span class="sxs-lookup"><span data-stu-id="0f638-148">Timestamp of when the message was created</span></span>|
|<span data-ttu-id="0f638-149">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0f638-149">lastModifiedDateTime</span></span>|<span data-ttu-id="0f638-150">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0f638-150">dateTimeOffset</span></span>|<span data-ttu-id="0f638-151">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0f638-151">Read only.</span></span> <span data-ttu-id="0f638-152">Marca de hora de cuando el mensaje fue editado o actualizado</span><span class="sxs-lookup"><span data-stu-id="0f638-152">Timestamp of when the message was edited/updated</span></span>|
|<span data-ttu-id="0f638-153">isDeleted</span><span class="sxs-lookup"><span data-stu-id="0f638-153">isDeleted</span></span>|<span data-ttu-id="0f638-154">boolean</span><span class="sxs-lookup"><span data-stu-id="0f638-154">boolean</span></span>|<span data-ttu-id="0f638-155">Representa si un mensaje se ha eliminado suave</span><span class="sxs-lookup"><span data-stu-id="0f638-155">Represents if a message has been soft deleted</span></span>|
|<span data-ttu-id="0f638-156">deletedDateTime</span><span class="sxs-lookup"><span data-stu-id="0f638-156">deletedDateTime</span></span>|<span data-ttu-id="0f638-157">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0f638-157">dateTimeOffset</span></span>|<span data-ttu-id="0f638-158">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0f638-158">Read only.</span></span> <span data-ttu-id="0f638-159">Marca de tiempo en el que se ha eliminado el mensaje</span><span class="sxs-lookup"><span data-stu-id="0f638-159">Timestamp at which the message was deleted</span></span> |
|<span data-ttu-id="0f638-160">subject</span><span class="sxs-lookup"><span data-stu-id="0f638-160">subject</span></span>|<span data-ttu-id="0f638-161">string</span><span class="sxs-lookup"><span data-stu-id="0f638-161">string</span></span>|<span data-ttu-id="0f638-162">Línea de asunto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0f638-162">Message subject line.</span></span> <span data-ttu-id="0f638-163">Opcional</span><span class="sxs-lookup"><span data-stu-id="0f638-163">Optional</span></span>|
|<span data-ttu-id="0f638-164">body</span><span class="sxs-lookup"><span data-stu-id="0f638-164">body</span></span>|[<span data-ttu-id="0f638-165">itemBody</span><span class="sxs-lookup"><span data-stu-id="0f638-165">itemBody</span></span>](itembody.md)|<span data-ttu-id="0f638-166">Representación de texto sin formato o HTML del contenido del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0f638-166">Plaintext/HTML representation of the content of the message.</span></span> <span data-ttu-id="0f638-167">Devuelve el texto sin formato de forma predeterminada, la aplicación elegir HTML como parte de un parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="0f638-167">Returns plain text by default, application can choose HTML as part of a query param</span></span>|
|<span data-ttu-id="0f638-168">Resumen</span><span class="sxs-lookup"><span data-stu-id="0f638-168">summary</span></span>|<span data-ttu-id="0f638-169">string</span><span class="sxs-lookup"><span data-stu-id="0f638-169">string</span></span>|<span data-ttu-id="0f638-170">Texto del resumen del mensaje que se puedan usar para las notificaciones de inserción y vistas de resumen o vistas de atrás retroceso</span><span class="sxs-lookup"><span data-stu-id="0f638-170">Summary text of the message that could be used for push notifications and summary views or fall back views</span></span>|
|<span data-ttu-id="0f638-171">menciones</span><span class="sxs-lookup"><span data-stu-id="0f638-171">mentions</span></span>|<span data-ttu-id="0f638-172">colección de [chatMessageMention](chatmention.md)</span><span class="sxs-lookup"><span data-stu-id="0f638-172">[chatMessageMention](chatmention.md) collection</span></span>| <span data-ttu-id="0f638-173">Lista de entidades que se mencionan en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0f638-173">List of entities mentioned in the message.</span></span> <span data-ttu-id="0f638-174">Admite actualmente el usuario, bot, equipo, canal</span><span class="sxs-lookup"><span data-stu-id="0f638-174">Currently supports user, bot, team, channel</span></span>|
|<span data-ttu-id="0f638-175">importance</span><span class="sxs-lookup"><span data-stu-id="0f638-175">importance</span></span>| <span data-ttu-id="0f638-176">string</span><span class="sxs-lookup"><span data-stu-id="0f638-176">string</span></span> | <span data-ttu-id="0f638-177">La importancia del mensaje: Normal, alta</span><span class="sxs-lookup"><span data-stu-id="0f638-177">The importance of the message: Normal, High</span></span>|
|<span data-ttu-id="0f638-178">reacciones</span><span class="sxs-lookup"><span data-stu-id="0f638-178">reactions</span></span>| <span data-ttu-id="0f638-179">colección de [chatMessageReaction](chatreaction.md)</span><span class="sxs-lookup"><span data-stu-id="0f638-179">[chatMessageReaction](chatreaction.md) collection</span></span> | <span data-ttu-id="0f638-180">Las reacciones de este mensaje (como por ejemplo,)</span><span class="sxs-lookup"><span data-stu-id="0f638-180">Reactions for this message (for example, Like)</span></span>|
|<span data-ttu-id="0f638-181">configuración regional</span><span class="sxs-lookup"><span data-stu-id="0f638-181">locale</span></span>|<span data-ttu-id="0f638-182">string</span><span class="sxs-lookup"><span data-stu-id="0f638-182">string</span></span>|<span data-ttu-id="0f638-183">Configuración regional del mensaje establecido por el cliente</span><span class="sxs-lookup"><span data-stu-id="0f638-183">Locale of the message set by the client</span></span>|
|<span data-ttu-id="0f638-184">attachments</span><span class="sxs-lookup"><span data-stu-id="0f638-184">attachments</span></span>|<span data-ttu-id="0f638-185">colección de [chatMessageAttachment](chatattachment.md)</span><span class="sxs-lookup"><span data-stu-id="0f638-185">[chatMessageAttachment](chatattachment.md) collection</span></span> |<span data-ttu-id="0f638-186">Archivos adjuntos</span><span class="sxs-lookup"><span data-stu-id="0f638-186">Attached files</span></span>|


## <a name="json-representation"></a><span data-ttu-id="0f638-187">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0f638-187">JSON representation</span></span>

<span data-ttu-id="0f638-188">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0f638-188">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "isDeleted",
    "deletedDateTime",
    "attachments",
    "importance",
    "reactions",
    "mentions",
    "subject",
    "summary"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.chatMessage"
}-->

```json
{
  "id": "string (identifier)",
  "replyToId": "string (identifier)",
  "from": {"@odata.type": "microsoft.graph.identitySet"},
  "etag": "string",
  "messageType": "string",
  "createdDateTime": "string (timestamp)",
  "lastModifiedDateTime": "string (timestamp)",
  "isDeleted": "boolean",
  "deletedDateTime": "string (timestamp)",
  "subject": "string",
  "body": {"@odata.type": "microsoft.graph.itemBody"},
  "summary": "string",
  "attachments": [{"@odata.type": "microsoft.graph.chatMessageAttachment"}],
  "mentions": [{"@odata.type": "microsoft.graph.chatMessageMention"}],
  "importance": "string",
  "reactions": [{"@odata.type": "microsoft.graph.chatMessageReaction"}],
  "locale": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chat message resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
