---
title: tipo de recurso de canal
description: 'Un canal es una colección de chatMessages dentro de un equipo. '
ms.openlocfilehash: 90a2c6641a79829e340f2487d7f0381998d2a205
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090292"
---
# <a name="channel-resource-type"></a><span data-ttu-id="5d434-103">tipo de recurso de canal</span><span class="sxs-lookup"><span data-stu-id="5d434-103">channel resource type</span></span>

> <span data-ttu-id="5d434-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5d434-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5d434-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5d434-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5d434-106">Un canal es una colección de [chatMessages](chatmessage.md) dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="5d434-106">A channel is a collection of [chatMessages](chatmessage.md) within a [team](../resources/team.md).</span></span> <span data-ttu-id="5d434-107">Un canal representa un tema y, por lo tanto, un aislamiento lógico de discusión, dentro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="5d434-107">A channel represents a topic, and therefore a logical isolation of discussion, within a team.</span></span> <span data-ttu-id="5d434-108">Ejemplos pueden ser "Viernes equipo comer" canal y canal de "Arquitectura de la discusión".</span><span class="sxs-lookup"><span data-stu-id="5d434-108">Examples can be "Friday Team Lunch" channel, and "Architecture Discussion" channel.</span></span>


## <a name="methods"></a><span data-ttu-id="5d434-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d434-109">Methods</span></span>

| <span data-ttu-id="5d434-110">Método</span><span class="sxs-lookup"><span data-stu-id="5d434-110">Method</span></span>       | <span data-ttu-id="5d434-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d434-111">Return Type</span></span>  |<span data-ttu-id="5d434-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d434-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="5d434-113">Canales de lista</span><span class="sxs-lookup"><span data-stu-id="5d434-113">List channels</span></span>](../api/channel-list.md) | <span data-ttu-id="5d434-114">colección de [canal](channel.md)</span><span class="sxs-lookup"><span data-stu-id="5d434-114">[channel](channel.md) collection</span></span> | <span data-ttu-id="5d434-115">Obtener la lista de canales en este equipo.</span><span class="sxs-lookup"><span data-stu-id="5d434-115">Get the list of channels in this team.</span></span>|
|[<span data-ttu-id="5d434-116">Creación de canal</span><span class="sxs-lookup"><span data-stu-id="5d434-116">Create channel</span></span>](../api/channel-post.md) | [<span data-ttu-id="5d434-117">canal</span><span class="sxs-lookup"><span data-stu-id="5d434-117">channel</span></span>](channel.md) | <span data-ttu-id="5d434-118">Crear un nuevo canal si incluye el nombre para mostrar y la descripción.</span><span class="sxs-lookup"><span data-stu-id="5d434-118">Create a new channel by including the display name and description.</span></span>|
|[<span data-ttu-id="5d434-119">Obtener el canal</span><span class="sxs-lookup"><span data-stu-id="5d434-119">Get channel</span></span>](../api/channel-get.md) | [<span data-ttu-id="5d434-120">canal</span><span class="sxs-lookup"><span data-stu-id="5d434-120">channel</span></span>](channel.md) | <span data-ttu-id="5d434-121">Leer las propiedades y relaciones del canal.</span><span class="sxs-lookup"><span data-stu-id="5d434-121">Read properties and relationships of the channel.</span></span>|
|[<span data-ttu-id="5d434-122">Canal de actualización</span><span class="sxs-lookup"><span data-stu-id="5d434-122">Update channel</span></span>](../api/channel-patch.md) | [<span data-ttu-id="5d434-123">canal</span><span class="sxs-lookup"><span data-stu-id="5d434-123">channel</span></span>](channel.md) | <span data-ttu-id="5d434-124">Actualizar las propiedades del canal.</span><span class="sxs-lookup"><span data-stu-id="5d434-124">Update properties of the channel.</span></span>|
|[<span data-ttu-id="5d434-125">Eliminación de canal</span><span class="sxs-lookup"><span data-stu-id="5d434-125">Delete channel</span></span>](../api/channel-delete.md) | <span data-ttu-id="5d434-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5d434-126">None</span></span> | <span data-ttu-id="5d434-127">Eliminar un canal.</span><span class="sxs-lookup"><span data-stu-id="5d434-127">Delete a channel.</span></span>|
|[<span data-ttu-id="5d434-128">Mensajes del canal de lista</span><span class="sxs-lookup"><span data-stu-id="5d434-128">List channel messages</span></span>](../api/channel-list-messages.md)  | [<span data-ttu-id="5d434-129">chatMessage</span><span class="sxs-lookup"><span data-stu-id="5d434-129">chatMessage</span></span>](../resources/chatmessage.md) | <span data-ttu-id="5d434-130">Obtener los mensajes en un canal</span><span class="sxs-lookup"><span data-stu-id="5d434-130">Get messages in a channel</span></span> |
|[<span data-ttu-id="5d434-131">Crear un subproceso de chat</span><span class="sxs-lookup"><span data-stu-id="5d434-131">Create chat thread</span></span>](../api/channel-post-chatthreads.md) | <span data-ttu-id="5d434-132">colección de [chatThread](chatthread.md)</span><span class="sxs-lookup"><span data-stu-id="5d434-132">[chatThread](chatthread.md) collection</span></span>| <span data-ttu-id="5d434-133">Crear un subproceso de chat en el canal especificado.</span><span class="sxs-lookup"><span data-stu-id="5d434-133">Create a chat thread in the specified channel.</span></span>|

## <a name="properties"></a><span data-ttu-id="5d434-134">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5d434-134">Properties</span></span>
| <span data-ttu-id="5d434-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5d434-135">Property</span></span>     | <span data-ttu-id="5d434-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="5d434-136">Type</span></span>   |<span data-ttu-id="5d434-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d434-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5d434-138">description</span><span class="sxs-lookup"><span data-stu-id="5d434-138">description</span></span>|<span data-ttu-id="5d434-139">String</span><span class="sxs-lookup"><span data-stu-id="5d434-139">String</span></span>|<span data-ttu-id="5d434-140">Descripción textual opcional para el canal.</span><span class="sxs-lookup"><span data-stu-id="5d434-140">Optional textual description for the channel.</span></span>|
|<span data-ttu-id="5d434-141">displayName</span><span class="sxs-lookup"><span data-stu-id="5d434-141">displayName</span></span>|<span data-ttu-id="5d434-142">String</span><span class="sxs-lookup"><span data-stu-id="5d434-142">String</span></span>|<span data-ttu-id="5d434-143">Nombre de canal tal y como aparecerá para el usuario en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5d434-143">Channel name as it will appear to the user in Microsoft Teams.</span></span>|
|<span data-ttu-id="5d434-144">id</span><span class="sxs-lookup"><span data-stu-id="5d434-144">id</span></span>|<span data-ttu-id="5d434-145">String</span><span class="sxs-lookup"><span data-stu-id="5d434-145">String</span></span>|<span data-ttu-id="5d434-146">Identificador único de la de los canales.</span><span class="sxs-lookup"><span data-stu-id="5d434-146">The channels's unique identifier.</span></span> <span data-ttu-id="5d434-147">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5d434-147">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5d434-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5d434-148">Relationships</span></span>
| <span data-ttu-id="5d434-149">Relación</span><span class="sxs-lookup"><span data-stu-id="5d434-149">Relationship</span></span> | <span data-ttu-id="5d434-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="5d434-150">Type</span></span>   |<span data-ttu-id="5d434-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d434-151">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5d434-152">messages</span><span class="sxs-lookup"><span data-stu-id="5d434-152">messages</span></span>|<span data-ttu-id="5d434-153">colección de [chatMessage](chatmessage.md)</span><span class="sxs-lookup"><span data-stu-id="5d434-153">[chatMessage](chatmessage.md) collection</span></span>|<span data-ttu-id="5d434-154">Una colección de todos los mensajes en el canal.</span><span class="sxs-lookup"><span data-stu-id="5d434-154">A collection of all the messages in the channel.</span></span> <span data-ttu-id="5d434-155">Una propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="5d434-155">A navigation property.</span></span> <span data-ttu-id="5d434-156">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="5d434-156">Nullable.</span></span> <span data-ttu-id="5d434-157">Actualmente esta API sólo admite operaciones de lectura, pero finalmente será compatible con los mensajes de escritura demasiado.</span><span class="sxs-lookup"><span data-stu-id="5d434-157">Currently this API only supports reading but will eventually support writing messages too.</span></span>|
|<span data-ttu-id="5d434-158">chatThreads</span><span class="sxs-lookup"><span data-stu-id="5d434-158">chatThreads</span></span>|<span data-ttu-id="5d434-159">colección de [chatThread](chatthread.md)</span><span class="sxs-lookup"><span data-stu-id="5d434-159">[chatThread](chatthread.md) collection</span></span>|<span data-ttu-id="5d434-160">(Esto se están quedando obsoletas en favor de la propiedad de los mensajes) chatThreads admite la creación de nuevos mensajes, pero no leer mensajes.</span><span class="sxs-lookup"><span data-stu-id="5d434-160">(This is being phased out in favor of the messages property) chatThreads supports creating new messages but not reading messages.</span></span> <span data-ttu-id="5d434-161">ChatThreads es una propiedad de navegación y es Nullable.</span><span class="sxs-lookup"><span data-stu-id="5d434-161">ChatThreads is a navigation property, and is Nullable.</span></span>|
|<span data-ttu-id="5d434-162">fichas</span><span class="sxs-lookup"><span data-stu-id="5d434-162">tabs</span></span>|<span data-ttu-id="5d434-163">colección de [teamsTab](../resources/teamstab.md)</span><span class="sxs-lookup"><span data-stu-id="5d434-163">[teamsTab](../resources/teamstab.md) collection</span></span>|<span data-ttu-id="5d434-164">Una colección de todas las fichas en el canal.</span><span class="sxs-lookup"><span data-stu-id="5d434-164">A collection of all the tabs in the channel.</span></span> <span data-ttu-id="5d434-165">Una propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="5d434-165">A navigation property.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="5d434-166">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5d434-166">JSON representation</span></span>

<span data-ttu-id="5d434-167">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5d434-167">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "chatthreads"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.channel"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "channel resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
