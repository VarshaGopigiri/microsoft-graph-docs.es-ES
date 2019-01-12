---
title: tipo de recurso teamsTab
description: 'Una teamsTab es una ficha que ha anclado (adjunto) a un canal dentro de un equipo. '
localization_priority: Normal
author: nkramer
ms.prod: microsoft-teams
ms.openlocfilehash: 305b8d530eb0b10a658a1b5e5051f7854e3919ee
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917780"
---
# <a name="teamstab-resource-type"></a><span data-ttu-id="61a6e-103">tipo de recurso teamsTab</span><span class="sxs-lookup"><span data-stu-id="61a6e-103">teamsTab resource type</span></span>



<span data-ttu-id="61a6e-104">Una teamsTab es una [ficha](../resources/teamstab.md) que ha anclado (adjunto) a un [canal](channel.md) dentro de un [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="61a6e-104">A teamsTab is a [tab](../resources/teamstab.md) that's pinned (attached) to a [channel](channel.md) within a [team](team.md).</span></span> 

## <a name="methods"></a><span data-ttu-id="61a6e-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="61a6e-105">Methods</span></span>

| <span data-ttu-id="61a6e-106">Método</span><span class="sxs-lookup"><span data-stu-id="61a6e-106">Method</span></span>       | <span data-ttu-id="61a6e-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61a6e-107">Return Type</span></span>  |<span data-ttu-id="61a6e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="61a6e-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="61a6e-109">Fichas de lista</span><span class="sxs-lookup"><span data-stu-id="61a6e-109">List tabs</span></span>](../api/teamstab-list.md) | [<span data-ttu-id="61a6e-110">teamsTab</span><span class="sxs-lookup"><span data-stu-id="61a6e-110">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="61a6e-111">Las fichas de listas anclado a un canal.</span><span class="sxs-lookup"><span data-stu-id="61a6e-111">Lists tabs pinned to a channel.</span></span>|
|[<span data-ttu-id="61a6e-112">Obtener la ficha</span><span class="sxs-lookup"><span data-stu-id="61a6e-112">Get tab</span></span>](../api/teamstab-get.md) | [<span data-ttu-id="61a6e-113">teamsTab</span><span class="sxs-lookup"><span data-stu-id="61a6e-113">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="61a6e-114">Lee una ficha anclada a un canal.</span><span class="sxs-lookup"><span data-stu-id="61a6e-114">Reads a tab pinned to a channel.</span></span>|
|[<span data-ttu-id="61a6e-115">Agregar ficha</span><span class="sxs-lookup"><span data-stu-id="61a6e-115">Add tab</span></span>](../api/teamstab-add.md) | [<span data-ttu-id="61a6e-116">teamsTab</span><span class="sxs-lookup"><span data-stu-id="61a6e-116">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="61a6e-117">(PIN) se agrega una ficha a un canal.</span><span class="sxs-lookup"><span data-stu-id="61a6e-117">Adds (pins) a tab to a channel.</span></span>|
|[<span data-ttu-id="61a6e-118">Quitar la ficha</span><span class="sxs-lookup"><span data-stu-id="61a6e-118">Remove tab</span></span>](../api/teamstab-delete.md) | <span data-ttu-id="61a6e-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="61a6e-119">None</span></span> | <span data-ttu-id="61a6e-120">Quita (libera) una ficha de un canal.</span><span class="sxs-lookup"><span data-stu-id="61a6e-120">Removes (unpins) a tab from a channel.</span></span>|
|[<span data-ttu-id="61a6e-121">Ficha de actualización</span><span class="sxs-lookup"><span data-stu-id="61a6e-121">Update tab</span></span>](../api/teamstab-update.md) | [<span data-ttu-id="61a6e-122">teamsTab</span><span class="sxs-lookup"><span data-stu-id="61a6e-122">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="61a6e-123">Actualiza las propiedades de la ficha.</span><span class="sxs-lookup"><span data-stu-id="61a6e-123">Updates the tab properties.</span></span>|


## <a name="properties"></a><span data-ttu-id="61a6e-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61a6e-124">Properties</span></span>

|<span data-ttu-id="61a6e-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="61a6e-125">Property</span></span>|<span data-ttu-id="61a6e-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="61a6e-126">Type</span></span>|<span data-ttu-id="61a6e-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="61a6e-127">Description</span></span>|
|:---------------|:--------|:----------|
|  <span data-ttu-id="61a6e-128">id</span><span class="sxs-lookup"><span data-stu-id="61a6e-128">id</span></span>              |   <span data-ttu-id="61a6e-129">string</span><span class="sxs-lookup"><span data-stu-id="61a6e-129">string</span></span>                  |  <span data-ttu-id="61a6e-130">Identificador que identifica de forma exclusiva una instancia específica de una ficha de canal lectura sólo.</span><span class="sxs-lookup"><span data-stu-id="61a6e-130">Identifier that uniquely identifies a specific instance of a channel tab. Read only.</span></span>     |
|  <span data-ttu-id="61a6e-131">displayName</span><span class="sxs-lookup"><span data-stu-id="61a6e-131">displayName</span></span>            |   <span data-ttu-id="61a6e-132">string</span><span class="sxs-lookup"><span data-stu-id="61a6e-132">string</span></span>                  |  <span data-ttu-id="61a6e-133">Nombre de la ficha.</span><span class="sxs-lookup"><span data-stu-id="61a6e-133">Name of the tab.</span></span>     |
|  <span data-ttu-id="61a6e-134">sortOrderIndex</span><span class="sxs-lookup"><span data-stu-id="61a6e-134">sortOrderIndex</span></span>  |   <span data-ttu-id="61a6e-135">int</span><span class="sxs-lookup"><span data-stu-id="61a6e-135">int</span></span>                     |  <span data-ttu-id="61a6e-136">Índice del orden utilizado para la ordenación de las fichas</span><span class="sxs-lookup"><span data-stu-id="61a6e-136">Index of the order used for sorting tabs</span></span>     |
|  <span data-ttu-id="61a6e-137">webUrl</span><span class="sxs-lookup"><span data-stu-id="61a6e-137">webUrl</span></span>          |   <span data-ttu-id="61a6e-138">string</span><span class="sxs-lookup"><span data-stu-id="61a6e-138">string</span></span>                  |  <span data-ttu-id="61a6e-139">Dirección url del vínculo profundo de la instancia de ficha.</span><span class="sxs-lookup"><span data-stu-id="61a6e-139">Deep link url of the tab instance.</span></span> <span data-ttu-id="61a6e-140">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="61a6e-140">Read only.</span></span>     |
|  <span data-ttu-id="61a6e-141">configuration</span><span class="sxs-lookup"><span data-stu-id="61a6e-141">configuration</span></span>        |   [<span data-ttu-id="61a6e-142">teamsTabConfiguration</span><span class="sxs-lookup"><span data-stu-id="61a6e-142">teamsTabConfiguration</span></span>](teamstabconfiguration.md) |  <span data-ttu-id="61a6e-143">Contenedor de configuración personalizada que se aplican a una ficha. La ficha se considera configurado sólo una vez que se establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="61a6e-143">Container for custom settings applied to a tab. The tab is considered configured only once this property is set.</span></span>     |

## <a name="relationships"></a><span data-ttu-id="61a6e-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="61a6e-144">Relationships</span></span>

| <span data-ttu-id="61a6e-145">Relación</span><span class="sxs-lookup"><span data-stu-id="61a6e-145">Relationship</span></span> | <span data-ttu-id="61a6e-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="61a6e-146">Type</span></span>   | <span data-ttu-id="61a6e-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="61a6e-147">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="61a6e-148">teamsApp</span><span class="sxs-lookup"><span data-stu-id="61a6e-148">teamsApp</span></span>|[<span data-ttu-id="61a6e-149">teamsApp</span><span class="sxs-lookup"><span data-stu-id="61a6e-149">teamsApp</span></span>](teamsapp.md) | <span data-ttu-id="61a6e-150">La aplicación que está vinculada a la ficha. Esto no se puede cambiar después de la creación de la ficha.</span><span class="sxs-lookup"><span data-stu-id="61a6e-150">The application that is linked to the tab. This cannot be changed after tab creation.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="61a6e-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="61a6e-151">JSON representation</span></span>

<span data-ttu-id="61a6e-152">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="61a6e-152">The following is a JSON representation of the resource.</span></span>


<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.teamsTab"
}-->

```json
{  
  "id": "string",
  "displayName": "string",
  "sortOrderIndex": "string",
  "webUrl": "string",
  "configuration" : "teamsTabConfiguration"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsTab resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

## <a name="see-also"></a><span data-ttu-id="61a6e-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="61a6e-153">See also</span></span>

[<span data-ttu-id="61a6e-154">Configuración de los tipos de ficha integrada</span><span class="sxs-lookup"><span data-stu-id="61a6e-154">Configuring the built-in tab types</span></span>](/graph/teams-configuring-builtin-tabs)
