---
title: tipo de recurso teamsTab
description: 'Una teamsTab es una ficha que ha anclado (adjunto) a un canal dentro de un equipo. '
localization_priority: Normal
ms.openlocfilehash: a1c3302251ac9b68be1cd8d6a011b7e0a7d216b1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860847"
---
# <a name="teamstab-resource-type"></a><span data-ttu-id="5ffb9-103">tipo de recurso teamsTab</span><span class="sxs-lookup"><span data-stu-id="5ffb9-103">teamsTab resource type</span></span>



<span data-ttu-id="5ffb9-104">Una teamsTab es una [ficha](../resources/teamstab.md) que ha anclado (adjunto) a un [canal](channel.md) dentro de un [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="5ffb9-104">A teamsTab is a [tab](../resources/teamstab.md) that's pinned (attached) to a [channel](channel.md) within a [team](team.md).</span></span> 

## <a name="methods"></a><span data-ttu-id="5ffb9-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="5ffb9-105">Methods</span></span>

| <span data-ttu-id="5ffb9-106">Método</span><span class="sxs-lookup"><span data-stu-id="5ffb9-106">Method</span></span>       | <span data-ttu-id="5ffb9-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ffb9-107">Return Type</span></span>  |<span data-ttu-id="5ffb9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ffb9-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="5ffb9-109">Fichas de lista</span><span class="sxs-lookup"><span data-stu-id="5ffb9-109">List tabs</span></span>](../api/teamstab-list.md) | [<span data-ttu-id="5ffb9-110">teamsTab</span><span class="sxs-lookup"><span data-stu-id="5ffb9-110">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="5ffb9-111">Las fichas de listas anclado a un canal.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-111">Lists tabs pinned to a channel.</span></span>|
|[<span data-ttu-id="5ffb9-112">Obtener la ficha</span><span class="sxs-lookup"><span data-stu-id="5ffb9-112">Get tab</span></span>](../api/teamstab-get.md) | [<span data-ttu-id="5ffb9-113">teamsTab</span><span class="sxs-lookup"><span data-stu-id="5ffb9-113">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="5ffb9-114">Lee una ficha anclada a un canal.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-114">Reads a tab pinned to a channel.</span></span>|
|[<span data-ttu-id="5ffb9-115">Agregar ficha</span><span class="sxs-lookup"><span data-stu-id="5ffb9-115">Add tab</span></span>](../api/teamstab-add.md) | [<span data-ttu-id="5ffb9-116">teamsTab</span><span class="sxs-lookup"><span data-stu-id="5ffb9-116">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="5ffb9-117">(PIN) se agrega una ficha a un canal.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-117">Adds (pins) a tab to a channel.</span></span>|
|[<span data-ttu-id="5ffb9-118">Quitar la ficha</span><span class="sxs-lookup"><span data-stu-id="5ffb9-118">Remove tab</span></span>](../api/teamstab-delete.md) | <span data-ttu-id="5ffb9-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5ffb9-119">None</span></span> | <span data-ttu-id="5ffb9-120">Quita (libera) una ficha de un canal.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-120">Removes (unpins) a tab from a channel.</span></span>|
|[<span data-ttu-id="5ffb9-121">Ficha de actualización</span><span class="sxs-lookup"><span data-stu-id="5ffb9-121">Update tab</span></span>](../api/teamstab-update.md) | [<span data-ttu-id="5ffb9-122">teamsTab</span><span class="sxs-lookup"><span data-stu-id="5ffb9-122">teamsTab</span></span>](teamstab.md) | <span data-ttu-id="5ffb9-123">Actualiza las propiedades de la ficha.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-123">Updates the tab properties.</span></span>|


## <a name="properties"></a><span data-ttu-id="5ffb9-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5ffb9-124">Properties</span></span>

|<span data-ttu-id="5ffb9-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5ffb9-125">Property</span></span>|<span data-ttu-id="5ffb9-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ffb9-126">Type</span></span>|<span data-ttu-id="5ffb9-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ffb9-127">Description</span></span>|
|:---------------|:--------|:----------|
|  <span data-ttu-id="5ffb9-128">id</span><span class="sxs-lookup"><span data-stu-id="5ffb9-128">id</span></span>              |   <span data-ttu-id="5ffb9-129">string</span><span class="sxs-lookup"><span data-stu-id="5ffb9-129">string</span></span>                  |  <span data-ttu-id="5ffb9-130">Identificador que identifica de forma exclusiva una instancia específica de una ficha de canal lectura sólo.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-130">Identifier that uniquely identifies a specific instance of a channel tab. Read only.</span></span>     |
|  <span data-ttu-id="5ffb9-131">displayName</span><span class="sxs-lookup"><span data-stu-id="5ffb9-131">displayName</span></span>            |   <span data-ttu-id="5ffb9-132">string</span><span class="sxs-lookup"><span data-stu-id="5ffb9-132">string</span></span>                  |  <span data-ttu-id="5ffb9-133">Nombre de la ficha.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-133">Name of the tab.</span></span>     |
|  <span data-ttu-id="5ffb9-134">sortOrderIndex</span><span class="sxs-lookup"><span data-stu-id="5ffb9-134">sortOrderIndex</span></span>  |   <span data-ttu-id="5ffb9-135">int</span><span class="sxs-lookup"><span data-stu-id="5ffb9-135">int</span></span>                     |  <span data-ttu-id="5ffb9-136">Índice del orden utilizado para la ordenación de las fichas</span><span class="sxs-lookup"><span data-stu-id="5ffb9-136">Index of the order used for sorting tabs</span></span>     |
|  <span data-ttu-id="5ffb9-137">webUrl</span><span class="sxs-lookup"><span data-stu-id="5ffb9-137">webUrl</span></span>          |   <span data-ttu-id="5ffb9-138">string</span><span class="sxs-lookup"><span data-stu-id="5ffb9-138">string</span></span>                  |  <span data-ttu-id="5ffb9-139">Dirección url del vínculo profundo de la instancia de ficha.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-139">Deep link url of the tab instance.</span></span> <span data-ttu-id="5ffb9-140">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-140">Read only.</span></span>     |
|  <span data-ttu-id="5ffb9-141">configuration</span><span class="sxs-lookup"><span data-stu-id="5ffb9-141">configuration</span></span>        |   [<span data-ttu-id="5ffb9-142">teamsTabConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ffb9-142">teamsTabConfiguration</span></span>](teamstabconfiguration.md) |  <span data-ttu-id="5ffb9-143">Contenedor de configuración personalizada que se aplican a una ficha. La ficha se considera configurado sólo una vez que se establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-143">Container for custom settings applied to a tab. The tab is considered configured only once this property is set.</span></span>     |

## <a name="relationships"></a><span data-ttu-id="5ffb9-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5ffb9-144">Relationships</span></span>

| <span data-ttu-id="5ffb9-145">Relación</span><span class="sxs-lookup"><span data-stu-id="5ffb9-145">Relationship</span></span> | <span data-ttu-id="5ffb9-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ffb9-146">Type</span></span>   | <span data-ttu-id="5ffb9-147">Description</span><span class="sxs-lookup"><span data-stu-id="5ffb9-147">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="5ffb9-148">teamsApp</span><span class="sxs-lookup"><span data-stu-id="5ffb9-148">teamsApp</span></span>|[<span data-ttu-id="5ffb9-149">teamsApp</span><span class="sxs-lookup"><span data-stu-id="5ffb9-149">teamsApp</span></span>](teamsapp.md) | <span data-ttu-id="5ffb9-150">La aplicación que está vinculada a la ficha. Esto no se puede cambiar después de la creación de la ficha.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-150">The application that is linked to the tab. This cannot be changed after tab creation.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="5ffb9-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5ffb9-151">JSON representation</span></span>

<span data-ttu-id="5ffb9-152">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-152">The following is a JSON representation of the resource.</span></span>


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

## <a name="see-also"></a><span data-ttu-id="5ffb9-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ffb9-153">See also</span></span>

[<span data-ttu-id="5ffb9-154">Configuración de los tipos de ficha integrada</span><span class="sxs-lookup"><span data-stu-id="5ffb9-154">Configuring the built-in tab types</span></span>](/graph/teams-configuring-builtin-tabs)
