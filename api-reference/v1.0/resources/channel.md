---
title: tipo de recurso de canal
description: 'Un canal es una colección de los mensajes dentro de un equipo. '
ms.openlocfilehash: 17a2e2edb86bfe7e107e69414a70dbe92fe4d3bc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030002"
---
# <a name="channel-resource-type"></a><span data-ttu-id="bb84c-103">tipo de recurso de canal</span><span class="sxs-lookup"><span data-stu-id="bb84c-103">channel resource type</span></span>



<span data-ttu-id="bb84c-104">Un canal es una colección de los mensajes dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="bb84c-104">A channel is a collection of messages within a [team](../resources/team.md).</span></span> <span data-ttu-id="bb84c-105">Un canal representa un tema y, por lo tanto, un aislamiento lógico de discusión, dentro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="bb84c-105">A channel represents a topic, and therefore a logical isolation of discussion, within a team.</span></span> <span data-ttu-id="bb84c-106">Ejemplos pueden ser "Viernes equipo comer" canal y canal de "Arquitectura de la discusión".</span><span class="sxs-lookup"><span data-stu-id="bb84c-106">Examples can be "Friday Team Lunch" channel, and "Architecture Discussion" channel.</span></span>


## <a name="methods"></a><span data-ttu-id="bb84c-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="bb84c-107">Methods</span></span>

| <span data-ttu-id="bb84c-108">Método</span><span class="sxs-lookup"><span data-stu-id="bb84c-108">Method</span></span>       | <span data-ttu-id="bb84c-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb84c-109">Return Type</span></span>  |<span data-ttu-id="bb84c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb84c-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="bb84c-111">Canales de lista</span><span class="sxs-lookup"><span data-stu-id="bb84c-111">List channels</span></span>](../api/channel-list.md) | <span data-ttu-id="bb84c-112">colección de [canal](channel.md)</span><span class="sxs-lookup"><span data-stu-id="bb84c-112">[channel](channel.md) collection</span></span> | <span data-ttu-id="bb84c-113">Obtener la lista de canales en este equipo.</span><span class="sxs-lookup"><span data-stu-id="bb84c-113">Get the list of channels in this team.</span></span>|
|[<span data-ttu-id="bb84c-114">Creación de canal</span><span class="sxs-lookup"><span data-stu-id="bb84c-114">Create channel</span></span>](../api/channel-post.md) | [<span data-ttu-id="bb84c-115">canal</span><span class="sxs-lookup"><span data-stu-id="bb84c-115">channel</span></span>](channel.md) | <span data-ttu-id="bb84c-116">Crear un nuevo canal si incluye el nombre para mostrar y la descripción.</span><span class="sxs-lookup"><span data-stu-id="bb84c-116">Create a new channel by including the display name and description.</span></span>|
|[<span data-ttu-id="bb84c-117">Obtener el canal</span><span class="sxs-lookup"><span data-stu-id="bb84c-117">Get channel</span></span>](../api/channel-get.md) | [<span data-ttu-id="bb84c-118">canal</span><span class="sxs-lookup"><span data-stu-id="bb84c-118">channel</span></span>](channel.md) | <span data-ttu-id="bb84c-119">Leer las propiedades y relaciones del canal.</span><span class="sxs-lookup"><span data-stu-id="bb84c-119">Read properties and relationships of the channel.</span></span>|
|[<span data-ttu-id="bb84c-120">Canal de actualización</span><span class="sxs-lookup"><span data-stu-id="bb84c-120">Update channel</span></span>](../api/channel-patch.md) | [<span data-ttu-id="bb84c-121">canal</span><span class="sxs-lookup"><span data-stu-id="bb84c-121">channel</span></span>](channel.md) | <span data-ttu-id="bb84c-122">Actualizar las propiedades del canal.</span><span class="sxs-lookup"><span data-stu-id="bb84c-122">Update properties of the channel.</span></span>|
|[<span data-ttu-id="bb84c-123">Eliminación de canal</span><span class="sxs-lookup"><span data-stu-id="bb84c-123">Delete channel</span></span>](../api/channel-delete.md) | <span data-ttu-id="bb84c-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bb84c-124">None</span></span> | <span data-ttu-id="bb84c-125">Eliminar un canal.</span><span class="sxs-lookup"><span data-stu-id="bb84c-125">Delete a channel.</span></span>|

## <a name="properties"></a><span data-ttu-id="bb84c-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb84c-126">Properties</span></span>
| <span data-ttu-id="bb84c-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb84c-127">Property</span></span>     | <span data-ttu-id="bb84c-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb84c-128">Type</span></span>   |<span data-ttu-id="bb84c-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb84c-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bb84c-130">description</span><span class="sxs-lookup"><span data-stu-id="bb84c-130">description</span></span>|<span data-ttu-id="bb84c-131">String</span><span class="sxs-lookup"><span data-stu-id="bb84c-131">String</span></span>|<span data-ttu-id="bb84c-132">Descripción textual opcional para el canal.</span><span class="sxs-lookup"><span data-stu-id="bb84c-132">Optional textual description for the channel.</span></span>|
|<span data-ttu-id="bb84c-133">displayName</span><span class="sxs-lookup"><span data-stu-id="bb84c-133">displayName</span></span>|<span data-ttu-id="bb84c-134">String</span><span class="sxs-lookup"><span data-stu-id="bb84c-134">String</span></span>|<span data-ttu-id="bb84c-135">Nombre de canal tal y como aparecerá para el usuario en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bb84c-135">Channel name as it will appear to the user in Microsoft Teams.</span></span>|
|<span data-ttu-id="bb84c-136">id</span><span class="sxs-lookup"><span data-stu-id="bb84c-136">id</span></span>|<span data-ttu-id="bb84c-137">String</span><span class="sxs-lookup"><span data-stu-id="bb84c-137">String</span></span>|<span data-ttu-id="bb84c-138">Identificador único de la de los canales.</span><span class="sxs-lookup"><span data-stu-id="bb84c-138">The channels's unique identifier.</span></span> <span data-ttu-id="bb84c-139">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb84c-139">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bb84c-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bb84c-140">Relationships</span></span>
| <span data-ttu-id="bb84c-141">Relación</span><span class="sxs-lookup"><span data-stu-id="bb84c-141">Relationship</span></span> | <span data-ttu-id="bb84c-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb84c-142">Type</span></span>   |<span data-ttu-id="bb84c-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb84c-143">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bb84c-144">fichas</span><span class="sxs-lookup"><span data-stu-id="bb84c-144">tabs</span></span>|<span data-ttu-id="bb84c-145">colección de [teamsTab](../resources/teamstab.md)</span><span class="sxs-lookup"><span data-stu-id="bb84c-145">[teamsTab](../resources/teamstab.md) collection</span></span>|<span data-ttu-id="bb84c-146">Una colección de todas las fichas en el canal.</span><span class="sxs-lookup"><span data-stu-id="bb84c-146">A collection of all the tabs in the channel.</span></span> <span data-ttu-id="bb84c-147">Una propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="bb84c-147">A navigation property.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="bb84c-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bb84c-148">JSON representation</span></span>

<span data-ttu-id="bb84c-149">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="bb84c-149">Here is a JSON representation of the resource</span></span>

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
