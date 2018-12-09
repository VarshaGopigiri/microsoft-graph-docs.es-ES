---
title: tipo de recurso de canal
description: 'Un canal es una colección de chatMessages dentro de un equipo. '
ms.openlocfilehash: e69c0e7cdef347c59006b1dcce192e7949c2f07e
ms.sourcegitcommit: 12c6e82f1417022540e534ebadbd0e8d7fb5abde
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/08/2018
ms.locfileid: "27209715"
---
# <a name="channel-resource-type"></a><span data-ttu-id="5177d-103">tipo de recurso de canal</span><span class="sxs-lookup"><span data-stu-id="5177d-103">channel resource type</span></span>

> <span data-ttu-id="5177d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5177d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5177d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5177d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5177d-106">Un canal es una colección de [chatMessages](chatmessage.md) dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="5177d-106">A channel is a collection of [chatMessages](chatmessage.md) within a [team](../resources/team.md).</span></span> <span data-ttu-id="5177d-107">Un canal representa un tema y, por lo tanto, un aislamiento lógico de discusión, dentro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="5177d-107">A channel represents a topic, and therefore a logical isolation of discussion, within a team.</span></span> <span data-ttu-id="5177d-108">Ejemplos pueden ser "Viernes equipo comer" canal y canal de "Arquitectura de la discusión".</span><span class="sxs-lookup"><span data-stu-id="5177d-108">Examples can be "Friday Team Lunch" channel, and "Architecture Discussion" channel.</span></span>


## <a name="methods"></a><span data-ttu-id="5177d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5177d-109">Methods</span></span>

| <span data-ttu-id="5177d-110">Método</span><span class="sxs-lookup"><span data-stu-id="5177d-110">Method</span></span>       | <span data-ttu-id="5177d-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5177d-111">Return Type</span></span>  |<span data-ttu-id="5177d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5177d-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="5177d-113">Canales de lista</span><span class="sxs-lookup"><span data-stu-id="5177d-113">List channels</span></span>](../api/channel-list.md) | <span data-ttu-id="5177d-114">colección de [canal](channel.md)</span><span class="sxs-lookup"><span data-stu-id="5177d-114">[channel](channel.md) collection</span></span> | <span data-ttu-id="5177d-115">Obtener la lista de canales en este equipo.</span><span class="sxs-lookup"><span data-stu-id="5177d-115">Get the list of channels in this team.</span></span>|
|[<span data-ttu-id="5177d-116">Creación de canal</span><span class="sxs-lookup"><span data-stu-id="5177d-116">Create channel</span></span>](../api/channel-post.md) | [<span data-ttu-id="5177d-117">canal</span><span class="sxs-lookup"><span data-stu-id="5177d-117">channel</span></span>](channel.md) | <span data-ttu-id="5177d-118">Crear un nuevo canal si incluye el nombre para mostrar y la descripción.</span><span class="sxs-lookup"><span data-stu-id="5177d-118">Create a new channel by including the display name and description.</span></span>|
|[<span data-ttu-id="5177d-119">Obtener el canal</span><span class="sxs-lookup"><span data-stu-id="5177d-119">Get channel</span></span>](../api/channel-get.md) | [<span data-ttu-id="5177d-120">canal</span><span class="sxs-lookup"><span data-stu-id="5177d-120">channel</span></span>](channel.md) | <span data-ttu-id="5177d-121">Leer las propiedades y relaciones del canal.</span><span class="sxs-lookup"><span data-stu-id="5177d-121">Read properties and relationships of the channel.</span></span>|
|[<span data-ttu-id="5177d-122">Canal de actualización</span><span class="sxs-lookup"><span data-stu-id="5177d-122">Update channel</span></span>](../api/channel-patch.md) | [<span data-ttu-id="5177d-123">canal</span><span class="sxs-lookup"><span data-stu-id="5177d-123">channel</span></span>](channel.md) | <span data-ttu-id="5177d-124">Actualizar las propiedades del canal.</span><span class="sxs-lookup"><span data-stu-id="5177d-124">Update properties of the channel.</span></span>|
|[<span data-ttu-id="5177d-125">Eliminación de canal</span><span class="sxs-lookup"><span data-stu-id="5177d-125">Delete channel</span></span>](../api/channel-delete.md) | <span data-ttu-id="5177d-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5177d-126">None</span></span> | <span data-ttu-id="5177d-127">Eliminar un canal.</span><span class="sxs-lookup"><span data-stu-id="5177d-127">Delete a channel.</span></span>|
|[<span data-ttu-id="5177d-128">Mensajes del canal de lista</span><span class="sxs-lookup"><span data-stu-id="5177d-128">List channel messages</span></span>](../api/channel-list-messages.md)  | [<span data-ttu-id="5177d-129">chatMessage</span><span class="sxs-lookup"><span data-stu-id="5177d-129">chatMessage</span></span>](../resources/chatmessage.md) | <span data-ttu-id="5177d-130">Obtener los mensajes en un canal</span><span class="sxs-lookup"><span data-stu-id="5177d-130">Get messages in a channel</span></span> |
|[<span data-ttu-id="5177d-131">Crear un subproceso de chat</span><span class="sxs-lookup"><span data-stu-id="5177d-131">Create chat thread</span></span>](../api/channel-post-chatthreads.md) | <span data-ttu-id="5177d-132">colección de [chatThread](chatthread.md)</span><span class="sxs-lookup"><span data-stu-id="5177d-132">[chatThread](chatthread.md) collection</span></span>| <span data-ttu-id="5177d-133">Crear un subproceso de chat en el canal especificado.</span><span class="sxs-lookup"><span data-stu-id="5177d-133">Create a chat thread in the specified channel.</span></span>|

## <a name="properties"></a><span data-ttu-id="5177d-134">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5177d-134">Properties</span></span>
| <span data-ttu-id="5177d-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5177d-135">Property</span></span>     | <span data-ttu-id="5177d-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="5177d-136">Type</span></span>   |<span data-ttu-id="5177d-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="5177d-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5177d-138">description</span><span class="sxs-lookup"><span data-stu-id="5177d-138">description</span></span>|<span data-ttu-id="5177d-139">String</span><span class="sxs-lookup"><span data-stu-id="5177d-139">String</span></span>|<span data-ttu-id="5177d-140">Descripción textual opcional para el canal.</span><span class="sxs-lookup"><span data-stu-id="5177d-140">Optional textual description for the channel.</span></span>|
|<span data-ttu-id="5177d-141">displayName</span><span class="sxs-lookup"><span data-stu-id="5177d-141">displayName</span></span>|<span data-ttu-id="5177d-142">String</span><span class="sxs-lookup"><span data-stu-id="5177d-142">String</span></span>|<span data-ttu-id="5177d-143">Nombre de canal tal y como aparecerá para el usuario en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5177d-143">Channel name as it will appear to the user in Microsoft Teams.</span></span>|
|<span data-ttu-id="5177d-144">id</span><span class="sxs-lookup"><span data-stu-id="5177d-144">id</span></span>|<span data-ttu-id="5177d-145">String</span><span class="sxs-lookup"><span data-stu-id="5177d-145">String</span></span>|<span data-ttu-id="5177d-146">Identificador único de la de los canales.</span><span class="sxs-lookup"><span data-stu-id="5177d-146">The channels's unique identifier.</span></span> <span data-ttu-id="5177d-147">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5177d-147">Read-only.</span></span>|
|<span data-ttu-id="5177d-148">isFavoriteByDefault</span><span class="sxs-lookup"><span data-stu-id="5177d-148">isFavoriteByDefault</span></span>|<span data-ttu-id="5177d-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="5177d-149">Boolean</span></span>|<span data-ttu-id="5177d-150">Si el canal automáticamente se debe marcar 'favorito' para todos los miembros del equipo.</span><span class="sxs-lookup"><span data-stu-id="5177d-150">Whether the channel should automatically be marked 'favorite' for all members of the team.</span></span> <span data-ttu-id="5177d-151">Valor predeterminado: `false`.</span><span class="sxs-lookup"><span data-stu-id="5177d-151">Default: `false`.</span></span>|
|<span data-ttu-id="5177d-152">email</span><span class="sxs-lookup"><span data-stu-id="5177d-152">email</span></span>|<span data-ttu-id="5177d-153">Booleano</span><span class="sxs-lookup"><span data-stu-id="5177d-153">Boolean</span></span>| <span data-ttu-id="5177d-154">La dirección de correo electrónico para el envío de mensajes para el canal.</span><span class="sxs-lookup"><span data-stu-id="5177d-154">The email address for sending messages to the channel.</span></span> <span data-ttu-id="5177d-155">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5177d-155">Read-only.</span></span>|
|<span data-ttu-id="5177d-156">webUrl</span><span class="sxs-lookup"><span data-stu-id="5177d-156">webUrl</span></span>|<span data-ttu-id="5177d-157">String</span><span class="sxs-lookup"><span data-stu-id="5177d-157">String</span></span>|<span data-ttu-id="5177d-158">Un hipervínculo que se desplazará el canal en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5177d-158">A hyperlink that will navigate to the channel in Microsoft Teams.</span></span> <span data-ttu-id="5177d-159">Esta es la URL que se obtiene cuando haga clic en un canal en Microsoft Teams y seleccione vínculo Get a canal.</span><span class="sxs-lookup"><span data-stu-id="5177d-159">This is the URL that you get when you right-click a channel in Microsoft Teams and select Get link to channel.</span></span> <span data-ttu-id="5177d-160">Esta dirección URL debe se trata como un objeto binario opaco y no puede analizar.</span><span class="sxs-lookup"><span data-stu-id="5177d-160">This URL should be treated as an opaque blob, and not parsed.</span></span> <span data-ttu-id="5177d-161">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5177d-161">Read-only.</span></span>|


## <a name="relationships"></a><span data-ttu-id="5177d-162">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5177d-162">Relationships</span></span>
| <span data-ttu-id="5177d-163">Relación</span><span class="sxs-lookup"><span data-stu-id="5177d-163">Relationship</span></span> | <span data-ttu-id="5177d-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="5177d-164">Type</span></span>   |<span data-ttu-id="5177d-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="5177d-165">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5177d-166">messages</span><span class="sxs-lookup"><span data-stu-id="5177d-166">messages</span></span>|<span data-ttu-id="5177d-167">colección de [chatMessage](chatmessage.md)</span><span class="sxs-lookup"><span data-stu-id="5177d-167">[chatMessage](chatmessage.md) collection</span></span>|<span data-ttu-id="5177d-168">Una colección de todos los mensajes en el canal.</span><span class="sxs-lookup"><span data-stu-id="5177d-168">A collection of all the messages in the channel.</span></span> <span data-ttu-id="5177d-169">Una propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="5177d-169">A navigation property.</span></span> <span data-ttu-id="5177d-170">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="5177d-170">Nullable.</span></span> <span data-ttu-id="5177d-171">Actualmente esta API sólo admite operaciones de lectura, pero finalmente será compatible con los mensajes de escritura demasiado.</span><span class="sxs-lookup"><span data-stu-id="5177d-171">Currently this API only supports reading but will eventually support writing messages too.</span></span>|
|<span data-ttu-id="5177d-172">chatThreads</span><span class="sxs-lookup"><span data-stu-id="5177d-172">chatThreads</span></span>|<span data-ttu-id="5177d-173">colección de [chatThread](chatthread.md)</span><span class="sxs-lookup"><span data-stu-id="5177d-173">[chatThread](chatthread.md) collection</span></span>|<span data-ttu-id="5177d-174">(Esto se están quedando obsoletas en favor de la propiedad de los mensajes) chatThreads admite la creación de nuevos mensajes, pero no leer mensajes.</span><span class="sxs-lookup"><span data-stu-id="5177d-174">(This is being phased out in favor of the messages property) chatThreads supports creating new messages but not reading messages.</span></span> <span data-ttu-id="5177d-175">ChatThreads es una propiedad de navegación y es Nullable.</span><span class="sxs-lookup"><span data-stu-id="5177d-175">ChatThreads is a navigation property, and is Nullable.</span></span>|
|<span data-ttu-id="5177d-176">fichas</span><span class="sxs-lookup"><span data-stu-id="5177d-176">tabs</span></span>|<span data-ttu-id="5177d-177">colección de [teamsTab](../resources/teamstab.md)</span><span class="sxs-lookup"><span data-stu-id="5177d-177">[teamsTab](../resources/teamstab.md) collection</span></span>|<span data-ttu-id="5177d-178">Una colección de todas las fichas en el canal.</span><span class="sxs-lookup"><span data-stu-id="5177d-178">A collection of all the tabs in the channel.</span></span> <span data-ttu-id="5177d-179">Una propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="5177d-179">A navigation property.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="5177d-180">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5177d-180">JSON representation</span></span>

<span data-ttu-id="5177d-181">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5177d-181">Here is a JSON representation of the resource</span></span>

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
