---
title: Tipo de recurso plannerGroup
description: El recurso **plannerGroup** proporciona acceso a los recursos de organizador para un grupo. No contiene todas las propiedades utilizables.
localization_priority: Normal
ms.openlocfilehash: 1ce71db95924637afe505450c2fd92eaa01f512d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883905"
---
# <a name="plannergroup-resource-type"></a><span data-ttu-id="1da7b-104">Tipo de recurso plannerGroup</span><span class="sxs-lookup"><span data-stu-id="1da7b-104">plannerGroup resource type</span></span>

> <span data-ttu-id="1da7b-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1da7b-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1da7b-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1da7b-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1da7b-p103">El recurso **plannerGroup** proporciona acceso a los recursos Planner de un [grupo](group.md). No contiene ninguna propiedad utilizable.</span><span class="sxs-lookup"><span data-stu-id="1da7b-p103">The **plannerGroup** resource provides access to Planner resources for a [group](group.md). It doesn't contain any usable properties.</span></span>

## <a name="methods"></a><span data-ttu-id="1da7b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1da7b-109">Methods</span></span>

| <span data-ttu-id="1da7b-110">Método</span><span class="sxs-lookup"><span data-stu-id="1da7b-110">Method</span></span>           | <span data-ttu-id="1da7b-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1da7b-111">Return Type</span></span>    |<span data-ttu-id="1da7b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1da7b-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="1da7b-113">Enumerar planes</span><span class="sxs-lookup"><span data-stu-id="1da7b-113">List plans</span></span>](../api/plannergroup-list-plans.md) |<span data-ttu-id="1da7b-114">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="1da7b-114">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="1da7b-115">Obtenga una colección de objetos **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="1da7b-115">Get a **plannerPlan** object collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="1da7b-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1da7b-116">Properties</span></span>
| <span data-ttu-id="1da7b-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1da7b-117">Property</span></span>     | <span data-ttu-id="1da7b-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="1da7b-118">Type</span></span>   |<span data-ttu-id="1da7b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1da7b-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1da7b-120">id</span><span class="sxs-lookup"><span data-stu-id="1da7b-120">id</span></span>|<span data-ttu-id="1da7b-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="1da7b-121">String</span></span>| <span data-ttu-id="1da7b-p104">Solo lectura. Identificador del **plannerGroup**</span><span class="sxs-lookup"><span data-stu-id="1da7b-p104">Read-only. Identifier of the **plannerGroup**</span></span>|

## <a name="relationships"></a><span data-ttu-id="1da7b-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1da7b-124">Relationships</span></span>
| <span data-ttu-id="1da7b-125">Relación</span><span class="sxs-lookup"><span data-stu-id="1da7b-125">Relationship</span></span> | <span data-ttu-id="1da7b-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="1da7b-126">Type</span></span>   |<span data-ttu-id="1da7b-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="1da7b-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1da7b-128">plans</span><span class="sxs-lookup"><span data-stu-id="1da7b-128">plans</span></span>|<span data-ttu-id="1da7b-129">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="1da7b-129">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="1da7b-p105">Solo lectura. Admite valores NULL. Devuelve los [plannerPlans](plannerplan.md) propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="1da7b-p105">Read-only. Nullable. Returns the [plannerPlans](plannerplan.md) owned by the group.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1da7b-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1da7b-133">JSON representation</span></span>
<span data-ttu-id="1da7b-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1da7b-134">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
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
