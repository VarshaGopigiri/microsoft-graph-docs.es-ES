---
title: Tipo de recurso plannerUser
description: El recurso **plannerUser** proporcionan acceso a los recursos de organizador para un usuario. No contiene todas las propiedades utilizables.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: b73e422e232a96068f4545def0f0fdbd9f74ff07
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953571"
---
# <a name="planneruser-resource-type"></a><span data-ttu-id="e4edd-104">Tipo de recurso plannerUser</span><span class="sxs-lookup"><span data-stu-id="e4edd-104">plannerUser resource type</span></span>

<span data-ttu-id="e4edd-p102">El recurso **plannerUser** proporciona acceso a los recursos Planner de un [usuario](user.md). No contiene ninguna propiedad utilizable.</span><span class="sxs-lookup"><span data-stu-id="e4edd-p102">The **plannerUser** resource provide access to Planner resources for a [user](user.md). It doesn't contain any usable properties.</span></span>


## <a name="methods"></a><span data-ttu-id="e4edd-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4edd-107">Methods</span></span>

| <span data-ttu-id="e4edd-108">Método</span><span class="sxs-lookup"><span data-stu-id="e4edd-108">Method</span></span>           | <span data-ttu-id="e4edd-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4edd-109">Return Type</span></span>    |<span data-ttu-id="e4edd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4edd-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e4edd-111">Enumerar planes</span><span class="sxs-lookup"><span data-stu-id="e4edd-111">List plans</span></span>](../api/planneruser-list-plans.md) |<span data-ttu-id="e4edd-112">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="e4edd-112">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="e4edd-113">Obtenga una colección de objetos **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="e4edd-113">Get a **plannerPlan** object collection.</span></span>|
|[<span data-ttu-id="e4edd-114">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="e4edd-114">List tasks</span></span>](../api/planneruser-list-tasks.md) |<span data-ttu-id="e4edd-115">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="e4edd-115">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="e4edd-116">Obtenga una colección de objetos **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="e4edd-116">Get a **plannerTask** object collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="e4edd-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4edd-117">Properties</span></span>
| <span data-ttu-id="e4edd-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e4edd-118">Property</span></span>     | <span data-ttu-id="e4edd-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4edd-119">Type</span></span>   |<span data-ttu-id="e4edd-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4edd-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e4edd-121">id</span><span class="sxs-lookup"><span data-stu-id="e4edd-121">id</span></span>|<span data-ttu-id="e4edd-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="e4edd-122">String</span></span>| <span data-ttu-id="e4edd-p103">Solo lectura. Identificador del planenrUser</span><span class="sxs-lookup"><span data-stu-id="e4edd-p103">Read-only. Identifier of the planenrUser</span></span>|

## <a name="relationships"></a><span data-ttu-id="e4edd-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e4edd-125">Relationships</span></span>
| <span data-ttu-id="e4edd-126">Relación</span><span class="sxs-lookup"><span data-stu-id="e4edd-126">Relationship</span></span> | <span data-ttu-id="e4edd-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4edd-127">Type</span></span>   |<span data-ttu-id="e4edd-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4edd-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e4edd-129">plans</span><span class="sxs-lookup"><span data-stu-id="e4edd-129">plans</span></span>|<span data-ttu-id="e4edd-130">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="e4edd-130">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="e4edd-p104">Solo lectura. Admite valores NULL. Devuelve las [plannerTasks](plannertask.md) asignadas al usuario.</span><span class="sxs-lookup"><span data-stu-id="e4edd-p104">Read-only. Nullable. Returns the [plannerTasks](plannertask.md) assigned to the user.</span></span>|
|<span data-ttu-id="e4edd-134">tasks</span><span class="sxs-lookup"><span data-stu-id="e4edd-134">tasks</span></span>|<span data-ttu-id="e4edd-135">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="e4edd-135">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="e4edd-p105">Solo lectura. Admite valores NULL. Devuelve los [plannerPlans](plannerplan.md) compartidos con el usuario.</span><span class="sxs-lookup"><span data-stu-id="e4edd-p105">Read-only. Nullable. Returns the [plannerPlans](plannerplan.md) shared with the user.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e4edd-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e4edd-139">JSON representation</span></span>
<span data-ttu-id="e4edd-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e4edd-140">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerUser"
}-->

```json
{
  "id": "String (identifier)"
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
