---
title: Tipo de recurso plannerUser
description: El recurso **plannerUser** proporcionan acceso a los recursos de organizador para un usuario. No contiene todas las propiedades utilizables.
localization_priority: Normal
ms.openlocfilehash: 733c20d45e1c0b1e0e454b2c5ae03105a9ab5d24
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805946"
---
# <a name="planneruser-resource-type"></a><span data-ttu-id="114f1-104">Tipo de recurso plannerUser</span><span class="sxs-lookup"><span data-stu-id="114f1-104">plannerUser resource type</span></span>

<span data-ttu-id="114f1-p102">El recurso **plannerUser** proporciona acceso a los recursos Planner de un [usuario](user.md). No contiene ninguna propiedad utilizable.</span><span class="sxs-lookup"><span data-stu-id="114f1-p102">The **plannerUser** resource provide access to Planner resources for a [user](user.md). It doesn't contain any usable properties.</span></span>


## <a name="methods"></a><span data-ttu-id="114f1-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="114f1-107">Methods</span></span>

| <span data-ttu-id="114f1-108">Método</span><span class="sxs-lookup"><span data-stu-id="114f1-108">Method</span></span>           | <span data-ttu-id="114f1-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="114f1-109">Return Type</span></span>    |<span data-ttu-id="114f1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="114f1-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="114f1-111">Enumerar planes</span><span class="sxs-lookup"><span data-stu-id="114f1-111">List plans</span></span>](../api/planneruser-list-plans.md) |<span data-ttu-id="114f1-112">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="114f1-112">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="114f1-113">Obtenga una colección de objetos **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="114f1-113">Get a **plannerPlan** object collection.</span></span>|
|[<span data-ttu-id="114f1-114">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="114f1-114">List tasks</span></span>](../api/planneruser-list-tasks.md) |<span data-ttu-id="114f1-115">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="114f1-115">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="114f1-116">Obtenga una colección de objetos **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="114f1-116">Get a **plannerTask** object collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="114f1-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="114f1-117">Properties</span></span>
| <span data-ttu-id="114f1-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="114f1-118">Property</span></span>     | <span data-ttu-id="114f1-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="114f1-119">Type</span></span>   |<span data-ttu-id="114f1-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="114f1-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="114f1-121">id</span><span class="sxs-lookup"><span data-stu-id="114f1-121">id</span></span>|<span data-ttu-id="114f1-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="114f1-122">String</span></span>| <span data-ttu-id="114f1-p103">Solo lectura. Identificador del planenrUser</span><span class="sxs-lookup"><span data-stu-id="114f1-p103">Read-only. Identifier of the planenrUser</span></span>|

## <a name="relationships"></a><span data-ttu-id="114f1-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="114f1-125">Relationships</span></span>
| <span data-ttu-id="114f1-126">Relación</span><span class="sxs-lookup"><span data-stu-id="114f1-126">Relationship</span></span> | <span data-ttu-id="114f1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="114f1-127">Type</span></span>   |<span data-ttu-id="114f1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="114f1-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="114f1-129">plans</span><span class="sxs-lookup"><span data-stu-id="114f1-129">plans</span></span>|<span data-ttu-id="114f1-130">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="114f1-130">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="114f1-p104">Solo lectura. Admite valores NULL. Devuelve las [plannerTasks](plannertask.md) asignadas al usuario.</span><span class="sxs-lookup"><span data-stu-id="114f1-p104">Read-only. Nullable. Returns the [plannerTasks](plannertask.md) assigned to the user.</span></span>|
|<span data-ttu-id="114f1-134">tasks</span><span class="sxs-lookup"><span data-stu-id="114f1-134">tasks</span></span>|<span data-ttu-id="114f1-135">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="114f1-135">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="114f1-p105">Solo lectura. Admite valores NULL. Devuelve los [plannerPlans](plannerplan.md) compartidos con el usuario.</span><span class="sxs-lookup"><span data-stu-id="114f1-p105">Read-only. Nullable. Returns the [plannerPlans](plannerplan.md) shared with the user.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="114f1-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="114f1-139">JSON representation</span></span>
<span data-ttu-id="114f1-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="114f1-140">Here is a JSON representation of the resource.</span></span>

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
