---
title: tipo de recurso de canal
description: 'Un canal es una colección de chatMessages dentro de un equipo. '
author: nkramer
localization_priority: Priority
ms.openlocfilehash: 058632c9f56462195db0cd268fd0af262d4292f3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842689"
---
# <a name="channel-resource-type"></a><span data-ttu-id="9234c-103">tipo de recurso de canal</span><span class="sxs-lookup"><span data-stu-id="9234c-103">channel resource type</span></span>

> <span data-ttu-id="9234c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9234c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9234c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9234c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9234c-106">Un canal es una colección de [chatMessages](chatmessage.md) dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="9234c-106">A channel is a collection of [chatMessages](chatmessage.md) within a [team](../resources/team.md).</span></span> <span data-ttu-id="9234c-107">Un canal representa un tema y, por lo tanto, un aislamiento lógico de discusión, dentro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="9234c-107">A channel represents a topic, and therefore a logical isolation of discussion, within a team.</span></span> <span data-ttu-id="9234c-108">Ejemplos pueden ser "Viernes equipo comer" canal y canal de "Arquitectura de la discusión".</span><span class="sxs-lookup"><span data-stu-id="9234c-108">Examples can be "Friday Team Lunch" channel, and "Architecture Discussion" channel.</span></span>


## <a name="methods"></a><span data-ttu-id="9234c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9234c-109">Methods</span></span>

| <span data-ttu-id="9234c-110">Método</span><span class="sxs-lookup"><span data-stu-id="9234c-110">Method</span></span>       | <span data-ttu-id="9234c-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9234c-111">Return Type</span></span>  |<span data-ttu-id="9234c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9234c-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9234c-113">Canales de lista</span><span class="sxs-lookup"><span data-stu-id="9234c-113">List channels</span></span>](../api/channel-list.md) | <span data-ttu-id="9234c-114">colección de [canal](channel.md)</span><span class="sxs-lookup"><span data-stu-id="9234c-114">[channel](channel.md) collection</span></span> | <span data-ttu-id="9234c-115">Obtener la lista de canales en este equipo.</span><span class="sxs-lookup"><span data-stu-id="9234c-115">Get the list of channels in this team.</span></span>|
|[<span data-ttu-id="9234c-116">Creación de canal</span><span class="sxs-lookup"><span data-stu-id="9234c-116">Create channel</span></span>](../api/channel-post.md) | [<span data-ttu-id="9234c-117">canal</span><span class="sxs-lookup"><span data-stu-id="9234c-117">channel</span></span>](channel.md) | <span data-ttu-id="9234c-118">Crear un nuevo canal si incluye el nombre para mostrar y la descripción.</span><span class="sxs-lookup"><span data-stu-id="9234c-118">Create a new channel by including the display name and description.</span></span>|
|[<span data-ttu-id="9234c-119">Obtener el canal</span><span class="sxs-lookup"><span data-stu-id="9234c-119">Get channel</span></span>](../api/channel-get.md) | [<span data-ttu-id="9234c-120">canal</span><span class="sxs-lookup"><span data-stu-id="9234c-120">channel</span></span>](channel.md) | <span data-ttu-id="9234c-121">Leer las propiedades y relaciones del canal.</span><span class="sxs-lookup"><span data-stu-id="9234c-121">Read properties and relationships of the channel.</span></span>|
|[<span data-ttu-id="9234c-122">Canal de actualización</span><span class="sxs-lookup"><span data-stu-id="9234c-122">Update channel</span></span>](../api/channel-patch.md) | [<span data-ttu-id="9234c-123">canal</span><span class="sxs-lookup"><span data-stu-id="9234c-123">channel</span></span>](channel.md) | <span data-ttu-id="9234c-124">Actualizar las propiedades del canal.</span><span class="sxs-lookup"><span data-stu-id="9234c-124">Update properties of the channel.</span></span>|
|[<span data-ttu-id="9234c-125">Eliminación de canal</span><span class="sxs-lookup"><span data-stu-id="9234c-125">Delete channel</span></span>](../api/channel-delete.md) | <span data-ttu-id="9234c-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9234c-126">None</span></span> | <span data-ttu-id="9234c-127">Eliminar un canal.</span><span class="sxs-lookup"><span data-stu-id="9234c-127">Delete a channel.</span></span>|
|[<span data-ttu-id="9234c-128">Mensajes del canal de lista</span><span class="sxs-lookup"><span data-stu-id="9234c-128">List channel messages</span></span>](../api/channel-list-messages.md)  | [<span data-ttu-id="9234c-129">chatMessage</span><span class="sxs-lookup"><span data-stu-id="9234c-129">chatMessage</span></span>](../resources/chatmessage.md) | <span data-ttu-id="9234c-130">Obtener los mensajes en un canal</span><span class="sxs-lookup"><span data-stu-id="9234c-130">Get messages in a channel</span></span> |
|[<span data-ttu-id="9234c-131">Crear un subproceso de chat</span><span class="sxs-lookup"><span data-stu-id="9234c-131">Create chat thread</span></span>](../api/channel-post-chatthreads.md) | <span data-ttu-id="9234c-132">colección de [chatThread](chatthread.md)</span><span class="sxs-lookup"><span data-stu-id="9234c-132">[chatThread](chatthread.md) collection</span></span>| <span data-ttu-id="9234c-133">Crear un subproceso de chat en el canal especificado.</span><span class="sxs-lookup"><span data-stu-id="9234c-133">Create a chat thread in the specified channel.</span></span>|

## <a name="properties"></a><span data-ttu-id="9234c-134">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9234c-134">Properties</span></span>
| <span data-ttu-id="9234c-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9234c-135">Property</span></span>     | <span data-ttu-id="9234c-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="9234c-136">Type</span></span>   |<span data-ttu-id="9234c-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="9234c-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9234c-138">description</span><span class="sxs-lookup"><span data-stu-id="9234c-138">description</span></span>|<span data-ttu-id="9234c-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="9234c-139">String</span></span>|<span data-ttu-id="9234c-140">Descripción textual opcional para el canal.</span><span class="sxs-lookup"><span data-stu-id="9234c-140">Optional textual description for the channel.</span></span>|
|<span data-ttu-id="9234c-141">displayName</span><span class="sxs-lookup"><span data-stu-id="9234c-141">displayName</span></span>|<span data-ttu-id="9234c-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="9234c-142">String</span></span>|<span data-ttu-id="9234c-143">Nombre de canal tal y como aparecerá para el usuario en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="9234c-143">Channel name as it will appear to the user in Microsoft Teams.</span></span>|
|<span data-ttu-id="9234c-144">id</span><span class="sxs-lookup"><span data-stu-id="9234c-144">id</span></span>|<span data-ttu-id="9234c-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="9234c-145">String</span></span>|<span data-ttu-id="9234c-146">Identificador único de la de los canales.</span><span class="sxs-lookup"><span data-stu-id="9234c-146">The channels's unique identifier.</span></span> <span data-ttu-id="9234c-147">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9234c-147">Read-only.</span></span>|
|<span data-ttu-id="9234c-148">isFavoriteByDefault</span><span class="sxs-lookup"><span data-stu-id="9234c-148">isFavoriteByDefault</span></span>|<span data-ttu-id="9234c-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="9234c-149">Boolean</span></span>|<span data-ttu-id="9234c-150">Si el canal automáticamente se debe marcar 'favorito' para todos los miembros del equipo.</span><span class="sxs-lookup"><span data-stu-id="9234c-150">Whether the channel should automatically be marked 'favorite' for all members of the team.</span></span> <span data-ttu-id="9234c-151">Valor predeterminado: `false`.</span><span class="sxs-lookup"><span data-stu-id="9234c-151">Default: `false`.</span></span>|
|<span data-ttu-id="9234c-152">email</span><span class="sxs-lookup"><span data-stu-id="9234c-152">email</span></span>|<span data-ttu-id="9234c-153">Booleano</span><span class="sxs-lookup"><span data-stu-id="9234c-153">Boolean</span></span>| <span data-ttu-id="9234c-154">La dirección de correo electrónico para el envío de mensajes para el canal.</span><span class="sxs-lookup"><span data-stu-id="9234c-154">The email address for sending messages to the channel.</span></span> <span data-ttu-id="9234c-155">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9234c-155">Read-only.</span></span>|
|<span data-ttu-id="9234c-156">webUrl</span><span class="sxs-lookup"><span data-stu-id="9234c-156">webUrl</span></span>|<span data-ttu-id="9234c-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="9234c-157">String</span></span>|<span data-ttu-id="9234c-158">Un hipervínculo que se desplazará el canal en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="9234c-158">A hyperlink that will navigate to the channel in Microsoft Teams.</span></span> <span data-ttu-id="9234c-159">Esta es la URL que se obtiene cuando haga clic en un canal en Microsoft Teams y seleccione vínculo Get a canal.</span><span class="sxs-lookup"><span data-stu-id="9234c-159">This is the URL that you get when you right-click a channel in Microsoft Teams and select Get link to channel.</span></span> <span data-ttu-id="9234c-160">Esta dirección URL debe se trata como un objeto binario opaco y no puede analizar.</span><span class="sxs-lookup"><span data-stu-id="9234c-160">This URL should be treated as an opaque blob, and not parsed.</span></span> <span data-ttu-id="9234c-161">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9234c-161">Read-only.</span></span>|


## <a name="relationships"></a><span data-ttu-id="9234c-162">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9234c-162">Relationships</span></span>
| <span data-ttu-id="9234c-163">Relación</span><span class="sxs-lookup"><span data-stu-id="9234c-163">Relationship</span></span> | <span data-ttu-id="9234c-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="9234c-164">Type</span></span>   |<span data-ttu-id="9234c-165">Description</span><span class="sxs-lookup"><span data-stu-id="9234c-165">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9234c-166">messages</span><span class="sxs-lookup"><span data-stu-id="9234c-166">messages</span></span>|<span data-ttu-id="9234c-167">colección de [chatMessage](chatmessage.md)</span><span class="sxs-lookup"><span data-stu-id="9234c-167">[chatMessage](chatmessage.md) collection</span></span>|<span data-ttu-id="9234c-168">Una colección de todos los mensajes en el canal.</span><span class="sxs-lookup"><span data-stu-id="9234c-168">A collection of all the messages in the channel.</span></span> <span data-ttu-id="9234c-169">Una propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="9234c-169">A navigation property.</span></span> <span data-ttu-id="9234c-170">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9234c-170">Nullable.</span></span> <span data-ttu-id="9234c-171">Actualmente esta API sólo admite operaciones de lectura, pero finalmente será compatible con los mensajes de escritura demasiado.</span><span class="sxs-lookup"><span data-stu-id="9234c-171">Currently this API only supports reading but will eventually support writing messages too.</span></span>|
|<span data-ttu-id="9234c-172">chatThreads</span><span class="sxs-lookup"><span data-stu-id="9234c-172">chatThreads</span></span>|<span data-ttu-id="9234c-173">colección de [chatThread](chatthread.md)</span><span class="sxs-lookup"><span data-stu-id="9234c-173">[chatThread](chatthread.md) collection</span></span>|<span data-ttu-id="9234c-174">(Esto se están quedando obsoletas en favor de la propiedad de los mensajes) chatThreads admite la creación de nuevos mensajes, pero no leer mensajes.</span><span class="sxs-lookup"><span data-stu-id="9234c-174">(This is being phased out in favor of the messages property) chatThreads supports creating new messages but not reading messages.</span></span> <span data-ttu-id="9234c-175">ChatThreads es una propiedad de navegación y es Nullable.</span><span class="sxs-lookup"><span data-stu-id="9234c-175">ChatThreads is a navigation property, and is Nullable.</span></span>|
|<span data-ttu-id="9234c-176">fichas</span><span class="sxs-lookup"><span data-stu-id="9234c-176">tabs</span></span>|<span data-ttu-id="9234c-177">colección de [teamsTab](../resources/teamstab.md)</span><span class="sxs-lookup"><span data-stu-id="9234c-177">[teamsTab](../resources/teamstab.md) collection</span></span>|<span data-ttu-id="9234c-178">Una colección de todas las fichas en el canal.</span><span class="sxs-lookup"><span data-stu-id="9234c-178">A collection of all the tabs in the channel.</span></span> <span data-ttu-id="9234c-179">Una propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="9234c-179">A navigation property.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="9234c-180">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9234c-180">JSON representation</span></span>

<span data-ttu-id="9234c-181">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9234c-181">Here is a JSON representation of the resource</span></span>

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
