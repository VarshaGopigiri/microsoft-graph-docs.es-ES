---
title: Tipo de recurso plannerUser
description: 'El recurso **plannerUser** proporciona acceso a los recursos del organizador para un usuario. '
localization_priority: Normal
ms.openlocfilehash: 709b259c88d8fe0f02defaa57e77727a7b967cfd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820807"
---
# <a name="planneruser-resource-type"></a><span data-ttu-id="0cbbc-103">Tipo de recurso plannerUser</span><span class="sxs-lookup"><span data-stu-id="0cbbc-103">plannerUser resource type</span></span>

> <span data-ttu-id="0cbbc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0cbbc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0cbbc-106">El recurso **plannerUser** proporciona acceso a los recursos de organizador para un [usuario](user.md).</span><span class="sxs-lookup"><span data-stu-id="0cbbc-106">The **plannerUser** resource provides access to Planner resources for a [user](user.md).</span></span> 


## <a name="methods"></a><span data-ttu-id="0cbbc-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="0cbbc-107">Methods</span></span>

| <span data-ttu-id="0cbbc-108">Método</span><span class="sxs-lookup"><span data-stu-id="0cbbc-108">Method</span></span>           | <span data-ttu-id="0cbbc-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cbbc-109">Return Type</span></span>    |<span data-ttu-id="0cbbc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cbbc-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="0cbbc-111">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="0cbbc-111">List tasks</span></span>](../api/planneruser-list-tasks.md) |<span data-ttu-id="0cbbc-112">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="0cbbc-112">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="0cbbc-113">Obtenga el [plannerTasks](plannertask.md) asignados al usuario.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-113">Get the [plannerTasks](plannertask.md) assigned to the user.</span></span>|
|[<span data-ttu-id="0cbbc-114">Lista favoritePlans</span><span class="sxs-lookup"><span data-stu-id="0cbbc-114">List favoritePlans</span></span>](../api/planneruser-list-favoriteplans.md) |<span data-ttu-id="0cbbc-115">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="0cbbc-115">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="0cbbc-116">Obtenga el [plannerPlans](plannerplan.md) marcados como favoritas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-116">Get the [plannerPlans](plannerplan.md) marked as favorite by the user.</span></span>|
|[<span data-ttu-id="0cbbc-117">Lista recentPlans</span><span class="sxs-lookup"><span data-stu-id="0cbbc-117">List recentPlans</span></span>](../api/planneruser-list-recentplans.md) |<span data-ttu-id="0cbbc-118">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="0cbbc-118">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="0cbbc-119">Obtenga el [plannerPlans](plannerplan.md) visto recientemente por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-119">Get the [plannerPlans](plannerplan.md) recently viewed by the user.</span></span>|
|[<span data-ttu-id="0cbbc-120">Update</span><span class="sxs-lookup"><span data-stu-id="0cbbc-120">Update</span></span>](../api/planneruser-update.md) | [<span data-ttu-id="0cbbc-121">plannerUser</span><span class="sxs-lookup"><span data-stu-id="0cbbc-121">plannerUser</span></span>](planneruser.md)| <span data-ttu-id="0cbbc-122">Actualizar un objeto **plannerUser** .</span><span class="sxs-lookup"><span data-stu-id="0cbbc-122">Update a **plannerUser** object.</span></span> |


## <a name="properties"></a><span data-ttu-id="0cbbc-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0cbbc-123">Properties</span></span>
| <span data-ttu-id="0cbbc-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0cbbc-124">Property</span></span>     | <span data-ttu-id="0cbbc-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="0cbbc-125">Type</span></span>   |<span data-ttu-id="0cbbc-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cbbc-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0cbbc-127">id</span><span class="sxs-lookup"><span data-stu-id="0cbbc-127">id</span></span>|<span data-ttu-id="0cbbc-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="0cbbc-128">String</span></span>| <span data-ttu-id="0cbbc-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-129">Read-only.</span></span> <span data-ttu-id="0cbbc-130">Identificador de la plannerUser</span><span class="sxs-lookup"><span data-stu-id="0cbbc-130">Identifier of the plannerUser</span></span>|
|<span data-ttu-id="0cbbc-131">favoritePlanReferences</span><span class="sxs-lookup"><span data-stu-id="0cbbc-131">favoritePlanReferences</span></span>|[<span data-ttu-id="0cbbc-132">plannerFavoritePlanReferenceCollection</span><span class="sxs-lookup"><span data-stu-id="0cbbc-132">plannerFavoritePlanReferenceCollection</span></span>](plannerfavoriteplanreferencecollection.md)| <span data-ttu-id="0cbbc-133">Una colección que contiene las referencias a los planes de que el usuario ha marcado como favoritos.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-133">A collection containing the references to the plans that the user has marked as favorites.</span></span>|
|<span data-ttu-id="0cbbc-134">recentPlanReferences</span><span class="sxs-lookup"><span data-stu-id="0cbbc-134">recentPlanReferences</span></span>|[<span data-ttu-id="0cbbc-135">plannerRecentPlanReferenceCollection</span><span class="sxs-lookup"><span data-stu-id="0cbbc-135">plannerRecentPlanReferenceCollection</span></span>](plannerrecentplanreferencecollection.md)| <span data-ttu-id="0cbbc-136">Una colección que contiene referencias a los planes que se han visto recientemente por el usuario en las aplicaciones que admiten los planes de recientes.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-136">A collection containing references to the plans that were viewed recently by the user in apps that support recent plans.</span></span>|

## <a name="relationships"></a><span data-ttu-id="0cbbc-137">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0cbbc-137">Relationships</span></span>
| <span data-ttu-id="0cbbc-138">Relación</span><span class="sxs-lookup"><span data-stu-id="0cbbc-138">Relationship</span></span> | <span data-ttu-id="0cbbc-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="0cbbc-139">Type</span></span>   |<span data-ttu-id="0cbbc-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cbbc-140">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0cbbc-141">tasks</span><span class="sxs-lookup"><span data-stu-id="0cbbc-141">tasks</span></span>|<span data-ttu-id="0cbbc-142">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="0cbbc-142">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="0cbbc-p103">Solo lectura. Admite valores NULL. Devuelve las [plannerTasks](plannertask.md) asignadas al usuario.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-p103">Read-only. Nullable. Returns the [plannerTasks](plannertask.md) assigned to the user.</span></span>|
|<span data-ttu-id="0cbbc-146">favoritePlans</span><span class="sxs-lookup"><span data-stu-id="0cbbc-146">favoritePlans</span></span>|<span data-ttu-id="0cbbc-147">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="0cbbc-147">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="0cbbc-148">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-148">Read-only.</span></span> <span data-ttu-id="0cbbc-149">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-149">Nullable.</span></span> <span data-ttu-id="0cbbc-150">Devuelve el [plannerPlans](plannerplan.md) que el usuario marcado como favoritos.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-150">Returns the [plannerPlans](plannerplan.md) that the user marked as favorites.</span></span>|
|<span data-ttu-id="0cbbc-151">recentPlans</span><span class="sxs-lookup"><span data-stu-id="0cbbc-151">recentPlans</span></span>|<span data-ttu-id="0cbbc-152">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="0cbbc-152">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="0cbbc-153">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-153">Read-only.</span></span> <span data-ttu-id="0cbbc-154">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-154">Nullable.</span></span> <span data-ttu-id="0cbbc-155">Devuelve el [plannerPlans](plannerplan.md) que se han visto recientemente por el usuario en las aplicaciones que admiten los planes de recientes.</span><span class="sxs-lookup"><span data-stu-id="0cbbc-155">Returns the [plannerPlans](plannerplan.md) that have been recently viewed by the user in apps that support recent plans.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="0cbbc-156">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0cbbc-156">JSON representation</span></span>
<span data-ttu-id="0cbbc-157">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0cbbc-157">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerUser"
}-->

```json
{
  "favoritePlanReferences": {"@odata.type": "microsoft.graph.plannerFavoritePlanReferenceCollection"},
  "id": "String (identifier)",
  "recentPlanReferences": {"@odata.type": "microsoft.graph.plannerRecentPlanReferenceCollection"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
