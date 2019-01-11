---
title: Tipo de recurso plannerGroup
description: El recurso **plannerGroup** proporciona acceso a los recursos de organizador para un grupo. No contiene todas las propiedades utilizables.
localization_priority: Normal
ms.openlocfilehash: ac55c0acd3561205654383cbb1b3d264c219d1a3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871970"
---
# <a name="plannergroup-resource-type"></a><span data-ttu-id="e20fd-104">Tipo de recurso plannerGroup</span><span class="sxs-lookup"><span data-stu-id="e20fd-104">plannerGroup resource type</span></span>

<span data-ttu-id="e20fd-p102">El recurso **plannerGroup** proporciona acceso a los recursos Planner de un [grupo](group.md). No contiene ninguna propiedad utilizable.</span><span class="sxs-lookup"><span data-stu-id="e20fd-p102">The **plannerGroup** resource provides access to Planner resources for a [group](group.md). It doesn't contain any usable properties.</span></span>

## <a name="methods"></a><span data-ttu-id="e20fd-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="e20fd-107">Methods</span></span>

| <span data-ttu-id="e20fd-108">Método</span><span class="sxs-lookup"><span data-stu-id="e20fd-108">Method</span></span>           | <span data-ttu-id="e20fd-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e20fd-109">Return Type</span></span>    |<span data-ttu-id="e20fd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e20fd-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e20fd-111">Enumerar planes</span><span class="sxs-lookup"><span data-stu-id="e20fd-111">List plans</span></span>](../api/plannergroup-list-plans.md) |<span data-ttu-id="e20fd-112">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="e20fd-112">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="e20fd-113">Obtenga una colección de objetos **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="e20fd-113">Get a **plannerPlan** object collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="e20fd-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e20fd-114">Properties</span></span>
| <span data-ttu-id="e20fd-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e20fd-115">Property</span></span>     | <span data-ttu-id="e20fd-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="e20fd-116">Type</span></span>   |<span data-ttu-id="e20fd-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e20fd-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e20fd-118">id</span><span class="sxs-lookup"><span data-stu-id="e20fd-118">id</span></span>|<span data-ttu-id="e20fd-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="e20fd-119">String</span></span>| <span data-ttu-id="e20fd-p103">Solo lectura. Identificador del **plannerGroup**</span><span class="sxs-lookup"><span data-stu-id="e20fd-p103">Read-only. Identifier of the **plannerGroup**</span></span>|

## <a name="relationships"></a><span data-ttu-id="e20fd-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e20fd-122">Relationships</span></span>
| <span data-ttu-id="e20fd-123">Relación</span><span class="sxs-lookup"><span data-stu-id="e20fd-123">Relationship</span></span> | <span data-ttu-id="e20fd-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="e20fd-124">Type</span></span>   |<span data-ttu-id="e20fd-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="e20fd-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e20fd-126">plans</span><span class="sxs-lookup"><span data-stu-id="e20fd-126">plans</span></span>|<span data-ttu-id="e20fd-127">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="e20fd-127">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="e20fd-p104">Solo lectura. Admite valores NULL. Devuelve los [plannerPlans](plannerplan.md) propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="e20fd-p104">Read-only. Nullable. Returns the [plannerPlans](plannerplan.md) owned by the group.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e20fd-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e20fd-131">JSON representation</span></span>
<span data-ttu-id="e20fd-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e20fd-132">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerGroup"
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
  "description": "plannerGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
