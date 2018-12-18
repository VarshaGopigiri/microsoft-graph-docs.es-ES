---
title: tipo de recurso de canal
description: 'Un canal es una colección de los mensajes dentro de un equipo. '
author: nkramer
ms.openlocfilehash: f9ab71213180732a0c8c626d5b32b9074bd135d9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337089"
---
# <a name="channel-resource-type"></a><span data-ttu-id="fb8b2-103">tipo de recurso de canal</span><span class="sxs-lookup"><span data-stu-id="fb8b2-103">channel resource type</span></span>



<span data-ttu-id="fb8b2-104">Un canal es una colección de los mensajes dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="fb8b2-104">A channel is a collection of messages within a [team](../resources/team.md).</span></span> <span data-ttu-id="fb8b2-105">Un canal representa un tema y, por lo tanto, un aislamiento lógico de discusión, dentro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="fb8b2-105">A channel represents a topic, and therefore a logical isolation of discussion, within a team.</span></span> <span data-ttu-id="fb8b2-106">Ejemplos pueden ser "Viernes equipo comer" canal y canal de "Arquitectura de la discusión".</span><span class="sxs-lookup"><span data-stu-id="fb8b2-106">Examples can be "Friday Team Lunch" channel, and "Architecture Discussion" channel.</span></span>


## <a name="methods"></a><span data-ttu-id="fb8b2-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb8b2-107">Methods</span></span>

| <span data-ttu-id="fb8b2-108">Método</span><span class="sxs-lookup"><span data-stu-id="fb8b2-108">Method</span></span>       | <span data-ttu-id="fb8b2-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb8b2-109">Return Type</span></span>  |<span data-ttu-id="fb8b2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb8b2-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="fb8b2-111">Canales de lista</span><span class="sxs-lookup"><span data-stu-id="fb8b2-111">List channels</span></span>](../api/channel-list.md) | <span data-ttu-id="fb8b2-112">colección de [canal](channel.md)</span><span class="sxs-lookup"><span data-stu-id="fb8b2-112">[channel](channel.md) collection</span></span> | <span data-ttu-id="fb8b2-113">Obtener la lista de canales en este equipo.</span><span class="sxs-lookup"><span data-stu-id="fb8b2-113">Get the list of channels in this team.</span></span>|
|[<span data-ttu-id="fb8b2-114">Creación de canal</span><span class="sxs-lookup"><span data-stu-id="fb8b2-114">Create channel</span></span>](../api/channel-post.md) | [<span data-ttu-id="fb8b2-115">canal</span><span class="sxs-lookup"><span data-stu-id="fb8b2-115">channel</span></span>](channel.md) | <span data-ttu-id="fb8b2-116">Crear un nuevo canal si incluye el nombre para mostrar y la descripción.</span><span class="sxs-lookup"><span data-stu-id="fb8b2-116">Create a new channel by including the display name and description.</span></span>|
|[<span data-ttu-id="fb8b2-117">Obtener el canal</span><span class="sxs-lookup"><span data-stu-id="fb8b2-117">Get channel</span></span>](../api/channel-get.md) | [<span data-ttu-id="fb8b2-118">canal</span><span class="sxs-lookup"><span data-stu-id="fb8b2-118">channel</span></span>](channel.md) | <span data-ttu-id="fb8b2-119">Leer las propiedades y relaciones del canal.</span><span class="sxs-lookup"><span data-stu-id="fb8b2-119">Read properties and relationships of the channel.</span></span>|
|[<span data-ttu-id="fb8b2-120">Canal de actualización</span><span class="sxs-lookup"><span data-stu-id="fb8b2-120">Update channel</span></span>](../api/channel-patch.md) | [<span data-ttu-id="fb8b2-121">canal</span><span class="sxs-lookup"><span data-stu-id="fb8b2-121">channel</span></span>](channel.md) | <span data-ttu-id="fb8b2-122">Actualizar las propiedades del canal.</span><span class="sxs-lookup"><span data-stu-id="fb8b2-122">Update properties of the channel.</span></span>|
|[<span data-ttu-id="fb8b2-123">Eliminación de canal</span><span class="sxs-lookup"><span data-stu-id="fb8b2-123">Delete channel</span></span>](../api/channel-delete.md) | <span data-ttu-id="fb8b2-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fb8b2-124">None</span></span> | <span data-ttu-id="fb8b2-125">Eliminar un canal.</span><span class="sxs-lookup"><span data-stu-id="fb8b2-125">Delete a channel.</span></span>|

## <a name="properties"></a><span data-ttu-id="fb8b2-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb8b2-126">Properties</span></span>
| <span data-ttu-id="fb8b2-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb8b2-127">Property</span></span>     | <span data-ttu-id="fb8b2-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb8b2-128">Type</span></span>   |<span data-ttu-id="fb8b2-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb8b2-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fb8b2-130">description</span><span class="sxs-lookup"><span data-stu-id="fb8b2-130">description</span></span>|<span data-ttu-id="fb8b2-131">String</span><span class="sxs-lookup"><span data-stu-id="fb8b2-131">String</span></span>|<span data-ttu-id="fb8b2-132">Descripción textual opcional para el canal.</span><span class="sxs-lookup"><span data-stu-id="fb8b2-132">Optional textual description for the channel.</span></span>|
|<span data-ttu-id="fb8b2-133">displayName</span><span class="sxs-lookup"><span data-stu-id="fb8b2-133">displayName</span></span>|<span data-ttu-id="fb8b2-134">String</span><span class="sxs-lookup"><span data-stu-id="fb8b2-134">String</span></span>|<span data-ttu-id="fb8b2-135">Nombre de canal tal y como aparecerá para el usuario en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="fb8b2-135">Channel name as it will appear to the user in Microsoft Teams.</span></span>|
|<span data-ttu-id="fb8b2-136">id</span><span class="sxs-lookup"><span data-stu-id="fb8b2-136">id</span></span>|<span data-ttu-id="fb8b2-137">String</span><span class="sxs-lookup"><span data-stu-id="fb8b2-137">String</span></span>|<span data-ttu-id="fb8b2-138">Identificador único de la de los canales.</span><span class="sxs-lookup"><span data-stu-id="fb8b2-138">The channels's unique identifier.</span></span> <span data-ttu-id="fb8b2-139">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fb8b2-139">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fb8b2-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fb8b2-140">Relationships</span></span>
| <span data-ttu-id="fb8b2-141">Relación</span><span class="sxs-lookup"><span data-stu-id="fb8b2-141">Relationship</span></span> | <span data-ttu-id="fb8b2-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb8b2-142">Type</span></span>   |<span data-ttu-id="fb8b2-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb8b2-143">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fb8b2-144">fichas</span><span class="sxs-lookup"><span data-stu-id="fb8b2-144">tabs</span></span>|<span data-ttu-id="fb8b2-145">colección de [teamsTab](../resources/teamstab.md)</span><span class="sxs-lookup"><span data-stu-id="fb8b2-145">[teamsTab](../resources/teamstab.md) collection</span></span>|<span data-ttu-id="fb8b2-146">Una colección de todas las fichas en el canal.</span><span class="sxs-lookup"><span data-stu-id="fb8b2-146">A collection of all the tabs in the channel.</span></span> <span data-ttu-id="fb8b2-147">Una propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="fb8b2-147">A navigation property.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="fb8b2-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fb8b2-148">JSON representation</span></span>

<span data-ttu-id="fb8b2-149">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fb8b2-149">Here is a JSON representation of the resource</span></span>

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
