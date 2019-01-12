---
title: Tipo de recurso plannerGroup
description: El recurso **plannerGroup** proporciona acceso a los recursos de organizador para un grupo. No contiene todas las propiedades utilizables.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 6e60db0a3f33bc47d0ea63b7a773b7bb691cd5be
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981423"
---
# <a name="plannergroup-resource-type"></a><span data-ttu-id="d64ed-104">Tipo de recurso plannerGroup</span><span class="sxs-lookup"><span data-stu-id="d64ed-104">plannerGroup resource type</span></span>

<span data-ttu-id="d64ed-p102">El recurso **plannerGroup** proporciona acceso a los recursos Planner de un [grupo](group.md). No contiene ninguna propiedad utilizable.</span><span class="sxs-lookup"><span data-stu-id="d64ed-p102">The **plannerGroup** resource provides access to Planner resources for a [group](group.md). It doesn't contain any usable properties.</span></span>

## <a name="methods"></a><span data-ttu-id="d64ed-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="d64ed-107">Methods</span></span>

| <span data-ttu-id="d64ed-108">Método</span><span class="sxs-lookup"><span data-stu-id="d64ed-108">Method</span></span>           | <span data-ttu-id="d64ed-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d64ed-109">Return Type</span></span>    |<span data-ttu-id="d64ed-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d64ed-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d64ed-111">Enumerar planes</span><span class="sxs-lookup"><span data-stu-id="d64ed-111">List plans</span></span>](../api/plannergroup-list-plans.md) |<span data-ttu-id="d64ed-112">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="d64ed-112">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="d64ed-113">Obtenga una colección de objetos **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="d64ed-113">Get a **plannerPlan** object collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="d64ed-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d64ed-114">Properties</span></span>
| <span data-ttu-id="d64ed-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d64ed-115">Property</span></span>     | <span data-ttu-id="d64ed-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="d64ed-116">Type</span></span>   |<span data-ttu-id="d64ed-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d64ed-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d64ed-118">id</span><span class="sxs-lookup"><span data-stu-id="d64ed-118">id</span></span>|<span data-ttu-id="d64ed-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="d64ed-119">String</span></span>| <span data-ttu-id="d64ed-p103">Solo lectura. Identificador del **plannerGroup**</span><span class="sxs-lookup"><span data-stu-id="d64ed-p103">Read-only. Identifier of the **plannerGroup**</span></span>|

## <a name="relationships"></a><span data-ttu-id="d64ed-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d64ed-122">Relationships</span></span>
| <span data-ttu-id="d64ed-123">Relación</span><span class="sxs-lookup"><span data-stu-id="d64ed-123">Relationship</span></span> | <span data-ttu-id="d64ed-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="d64ed-124">Type</span></span>   |<span data-ttu-id="d64ed-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="d64ed-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d64ed-126">plans</span><span class="sxs-lookup"><span data-stu-id="d64ed-126">plans</span></span>|<span data-ttu-id="d64ed-127">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="d64ed-127">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="d64ed-p104">Solo lectura. Admite valores NULL. Devuelve los [plannerPlans](plannerplan.md) propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="d64ed-p104">Read-only. Nullable. Returns the [plannerPlans](plannerplan.md) owned by the group.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d64ed-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d64ed-131">JSON representation</span></span>
<span data-ttu-id="d64ed-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d64ed-132">Here is a JSON representation of the resource.</span></span>

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
