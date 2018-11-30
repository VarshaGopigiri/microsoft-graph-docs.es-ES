---
title: Tipo de recurso planner
description: El recurso **planner** es el punto de entrada para el modelo de objetos de Planner. Devuelve un recurso **planner** singleton.  No contiene ninguna propiedad utilizable.
ms.openlocfilehash: e5980f6f4037b57e977b12ef223e8a5a2cf7c77c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031911"
---
# <a name="planner-resource-type"></a><span data-ttu-id="ce8b6-105">Tipo de recurso planner</span><span class="sxs-lookup"><span data-stu-id="ce8b6-105">planner resource type</span></span>

<span data-ttu-id="ce8b6-p102">El recurso **planner** es el punto de entrada para el modelo de objetos de Planner. Devuelve un recurso **planner** singleton.  No contiene ninguna propiedad utilizable.</span><span class="sxs-lookup"><span data-stu-id="ce8b6-p102">The **planner** resource is the entry point for the Planner object model. It returns a singleton **planner** resource.  It doesn't contain any usable properties.</span></span>


## <a name="methods"></a><span data-ttu-id="ce8b6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce8b6-109">Methods</span></span>

| <span data-ttu-id="ce8b6-110">Método</span><span class="sxs-lookup"><span data-stu-id="ce8b6-110">Method</span></span>           | <span data-ttu-id="ce8b6-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce8b6-111">Return Type</span></span>    |<span data-ttu-id="ce8b6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce8b6-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ce8b6-113">Crear plannerBucket</span><span class="sxs-lookup"><span data-stu-id="ce8b6-113">Create plannerBucket</span></span>](../api/planner-post-buckets.md) |[<span data-ttu-id="ce8b6-114">plannerBucket</span><span class="sxs-lookup"><span data-stu-id="ce8b6-114">plannerBucket</span></span>](plannerbucket.md)| <span data-ttu-id="ce8b6-115">Crear un nuevo **plannerBucket** publicándolo en la colección de depósitos.</span><span class="sxs-lookup"><span data-stu-id="ce8b6-115">Create a new **plannerBucket** by posting to the buckets collection.</span></span>|
|[<span data-ttu-id="ce8b6-116">Crear plannerPlan</span><span class="sxs-lookup"><span data-stu-id="ce8b6-116">Create plannerPlan</span></span>](../api/planner-post-plans.md) |[<span data-ttu-id="ce8b6-117">plannerPlan</span><span class="sxs-lookup"><span data-stu-id="ce8b6-117">plannerPlan</span></span>](plannerplan.md)| <span data-ttu-id="ce8b6-118">Crear un nuevo **plannerPlan** publicándolo en la colección de planes.</span><span class="sxs-lookup"><span data-stu-id="ce8b6-118">Create a new **plannerPlan** by posting to the plans collection.</span></span>|
|[<span data-ttu-id="ce8b6-119">Crear plannerTask</span><span class="sxs-lookup"><span data-stu-id="ce8b6-119">Create plannerTask</span></span>](../api/planner-post-tasks.md) |[<span data-ttu-id="ce8b6-120">plannerTask</span><span class="sxs-lookup"><span data-stu-id="ce8b6-120">plannerTask</span></span>](plannertask.md)| <span data-ttu-id="ce8b6-121">Crear una nueva **plannerTask** publicándola en la colección de tareas.</span><span class="sxs-lookup"><span data-stu-id="ce8b6-121">Create a new **plannerTask** by posting to the tasks collection.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ce8b6-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ce8b6-122">Relationships</span></span>
| <span data-ttu-id="ce8b6-123">Relación</span><span class="sxs-lookup"><span data-stu-id="ce8b6-123">Relationship</span></span> | <span data-ttu-id="ce8b6-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce8b6-124">Type</span></span>   |<span data-ttu-id="ce8b6-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce8b6-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ce8b6-126">buckets</span><span class="sxs-lookup"><span data-stu-id="ce8b6-126">buckets</span></span>|<span data-ttu-id="ce8b6-127">Colección [plannerBucket](plannerbucket.md)</span><span class="sxs-lookup"><span data-stu-id="ce8b6-127">[plannerBucket](plannerbucket.md) collection</span></span>| <span data-ttu-id="ce8b6-p103">Solo lectura. Admite valores NULL. Devuelve una colección de los depósitos especificados</span><span class="sxs-lookup"><span data-stu-id="ce8b6-p103">Read-only. Nullable. Returns a collection of the specified buckets</span></span>|
|<span data-ttu-id="ce8b6-131">plans</span><span class="sxs-lookup"><span data-stu-id="ce8b6-131">plans</span></span>|<span data-ttu-id="ce8b6-132">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="ce8b6-132">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="ce8b6-p104">Solo lectura. Admite valores NULL. Devuelve una colección de los planes especificados</span><span class="sxs-lookup"><span data-stu-id="ce8b6-p104">Read-only. Nullable. Returns a collection of the specified plans</span></span>|
|<span data-ttu-id="ce8b6-136">tasks</span><span class="sxs-lookup"><span data-stu-id="ce8b6-136">tasks</span></span>|<span data-ttu-id="ce8b6-137">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="ce8b6-137">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="ce8b6-p105">Solo lectura. Admite valores NULL. Devuelve una colección de las tareas especificadas</span><span class="sxs-lookup"><span data-stu-id="ce8b6-p105">Read-only. Nullable. Returns a collection of the specified tasks</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ce8b6-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ce8b6-141">JSON representation</span></span>
<span data-ttu-id="ce8b6-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ce8b6-142">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.planner"
}-->

```json
{
}
```

## <a name="example"></a><span data-ttu-id="ce8b6-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce8b6-143">Example</span></span>

<span data-ttu-id="ce8b6-144">El recurso de **Organizador** está disponible en la raíz del gráfico.</span><span class="sxs-lookup"><span data-stu-id="ce8b6-144">The **planner** resource is available at the root of the graph.</span></span>

<!--{
  "blockType": "request"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner
```

<!--{
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.planner"
}-->
```json
HTTP/1.1 200 OK
Content-type: application/json

{
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