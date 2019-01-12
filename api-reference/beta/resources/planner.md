---
title: Tipo de recurso planner
description: El recurso **planner** es el punto de entrada para el modelo de objetos de Planner. Devuelve un recurso **planner** singleton.  No contiene ninguna propiedad utilizable.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: cf2877d5f413f3e54e1e0e750da1f22d6f9ffd95
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27925185"
---
# <a name="planner-resource-type"></a><span data-ttu-id="2ea46-105">Tipo de recurso planner</span><span class="sxs-lookup"><span data-stu-id="2ea46-105">planner resource type</span></span>

> <span data-ttu-id="2ea46-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2ea46-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2ea46-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2ea46-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2ea46-p103">El recurso **planner** es el punto de entrada para el modelo de objetos de Planner. Devuelve un recurso **planner** singleton.  No contiene ninguna propiedad utilizable.</span><span class="sxs-lookup"><span data-stu-id="2ea46-p103">The **planner** resource is the entry point for the Planner object model. It returns a singleton **planner** resource.  It doesn't contain any usable properties.</span></span>


## <a name="methods"></a><span data-ttu-id="2ea46-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2ea46-111">Methods</span></span>

| <span data-ttu-id="2ea46-112">Método</span><span class="sxs-lookup"><span data-stu-id="2ea46-112">Method</span></span>           | <span data-ttu-id="2ea46-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ea46-113">Return Type</span></span>    |<span data-ttu-id="2ea46-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ea46-114">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="2ea46-115">Crear plannerBucket</span><span class="sxs-lookup"><span data-stu-id="2ea46-115">Create plannerBucket</span></span>](../api/planner-post-buckets.md) |[<span data-ttu-id="2ea46-116">plannerBucket</span><span class="sxs-lookup"><span data-stu-id="2ea46-116">plannerBucket</span></span>](plannerbucket.md)| <span data-ttu-id="2ea46-117">Crear un nuevo **plannerBucket** publicándolo en la colección de depósitos.</span><span class="sxs-lookup"><span data-stu-id="2ea46-117">Create a new **plannerBucket** by posting to the buckets collection.</span></span>|
|[<span data-ttu-id="2ea46-118">Crear plannerPlan</span><span class="sxs-lookup"><span data-stu-id="2ea46-118">Create plannerPlan</span></span>](../api/planner-post-plans.md) |[<span data-ttu-id="2ea46-119">plannerPlan</span><span class="sxs-lookup"><span data-stu-id="2ea46-119">plannerPlan</span></span>](plannerplan.md)| <span data-ttu-id="2ea46-120">Crear un nuevo **plannerPlan** publicándolo en la colección de planes.</span><span class="sxs-lookup"><span data-stu-id="2ea46-120">Create a new **plannerPlan** by posting to the plans collection.</span></span>|
|[<span data-ttu-id="2ea46-121">Crear plannerTask</span><span class="sxs-lookup"><span data-stu-id="2ea46-121">Create plannerTask</span></span>](../api/planner-post-tasks.md) |[<span data-ttu-id="2ea46-122">plannerTask</span><span class="sxs-lookup"><span data-stu-id="2ea46-122">plannerTask</span></span>](plannertask.md)| <span data-ttu-id="2ea46-123">Crear una nueva **plannerTask** publicándola en la colección de tareas.</span><span class="sxs-lookup"><span data-stu-id="2ea46-123">Create a new **plannerTask** by posting to the tasks collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="2ea46-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2ea46-124">Properties</span></span>
| <span data-ttu-id="2ea46-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2ea46-125">Property</span></span>     | <span data-ttu-id="2ea46-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ea46-126">Type</span></span>   |<span data-ttu-id="2ea46-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ea46-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2ea46-128">id</span><span class="sxs-lookup"><span data-stu-id="2ea46-128">id</span></span>|<span data-ttu-id="2ea46-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ea46-129">String</span></span>| <span data-ttu-id="2ea46-p104">Solo lectura. Identificador del recurso **planner**.</span><span class="sxs-lookup"><span data-stu-id="2ea46-p104">Read-only. Identifier of the **planner** resource.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2ea46-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2ea46-132">Relationships</span></span>
| <span data-ttu-id="2ea46-133">Relación</span><span class="sxs-lookup"><span data-stu-id="2ea46-133">Relationship</span></span> | <span data-ttu-id="2ea46-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ea46-134">Type</span></span>   |<span data-ttu-id="2ea46-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ea46-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2ea46-136">buckets</span><span class="sxs-lookup"><span data-stu-id="2ea46-136">buckets</span></span>|<span data-ttu-id="2ea46-137">Colección [plannerBucket](plannerbucket.md)</span><span class="sxs-lookup"><span data-stu-id="2ea46-137">[plannerBucket](plannerbucket.md) collection</span></span>| <span data-ttu-id="2ea46-p105">Solo lectura. Admite valores NULL. Devuelve una colección de los depósitos especificados</span><span class="sxs-lookup"><span data-stu-id="2ea46-p105">Read-only. Nullable. Returns a collection of the specified buckets</span></span>|
|<span data-ttu-id="2ea46-141">plans</span><span class="sxs-lookup"><span data-stu-id="2ea46-141">plans</span></span>|<span data-ttu-id="2ea46-142">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="2ea46-142">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="2ea46-p106">Solo lectura. Admite valores NULL. Devuelve una colección de los planes especificados</span><span class="sxs-lookup"><span data-stu-id="2ea46-p106">Read-only. Nullable. Returns a collection of the specified plans</span></span>|
|<span data-ttu-id="2ea46-146">tasks</span><span class="sxs-lookup"><span data-stu-id="2ea46-146">tasks</span></span>|<span data-ttu-id="2ea46-147">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="2ea46-147">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="2ea46-p107">Solo lectura. Admite valores NULL. Devuelve una colección de las tareas especificadas</span><span class="sxs-lookup"><span data-stu-id="2ea46-p107">Read-only. Nullable. Returns a collection of the specified tasks</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2ea46-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2ea46-151">JSON representation</span></span>
<span data-ttu-id="2ea46-152">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2ea46-152">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.planner"
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
  "description": "planner resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
