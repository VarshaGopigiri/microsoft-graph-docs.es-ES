---
title: Tipo de recurso plannerBucket
description: ) para las tareas de un plan de Office 365. Está contenida en un plannerPlan y puede tener una colección de plannerTasks.
ms.openlocfilehash: 4ccf4d683fd11caeb4a0f9800afd9811a137eefb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087303"
---
# <a name="plannerbucket-resource-type"></a><span data-ttu-id="ffff1-104">Tipo de recurso plannerBucket</span><span class="sxs-lookup"><span data-stu-id="ffff1-104">plannerBucket resource type</span></span>

> <span data-ttu-id="ffff1-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ffff1-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ffff1-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ffff1-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ffff1-p103">El recurso **plannerBucket** representa un depósito (o "columna personalizada") para las tareas de un plan de Office 365. Se encuentra en un [plannerPlan](plannerplan.md) y puede tener una colección de [plannerTasks](plannertask.md).</span><span class="sxs-lookup"><span data-stu-id="ffff1-p103">The **plannerBucket** resource represents a bucket (or "custom column") for tasks in a plan in Office 365. It is contained in a [plannerPlan](plannerplan.md) and can have a collection of [plannerTasks](plannertask.md).</span></span>



## <a name="methods"></a><span data-ttu-id="ffff1-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ffff1-109">Methods</span></span>

| <span data-ttu-id="ffff1-110">Método</span><span class="sxs-lookup"><span data-stu-id="ffff1-110">Method</span></span>           | <span data-ttu-id="ffff1-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffff1-111">Return Type</span></span>    |<span data-ttu-id="ffff1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffff1-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ffff1-113">Obtener plannerBucket</span><span class="sxs-lookup"><span data-stu-id="ffff1-113">Get plannerBucket</span></span>](../api/plannerbucket-get.md) | [<span data-ttu-id="ffff1-114">plannerBucket</span><span class="sxs-lookup"><span data-stu-id="ffff1-114">plannerBucket</span></span>](plannerbucket.md) |<span data-ttu-id="ffff1-115">Leer las propiedades y las relaciones del objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="ffff1-115">Read properties and relationships of **plannerBucket** object.</span></span>|
|[<span data-ttu-id="ffff1-116">Enumerar plannerTasks</span><span class="sxs-lookup"><span data-stu-id="ffff1-116">List plannerTasks</span></span>](../api/plannerbucket-list-tasks.md) |<span data-ttu-id="ffff1-117">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="ffff1-117">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="ffff1-118">Obtenga una colección de objetos **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="ffff1-118">Get a **plannerTask** object collection.</span></span>|
|[<span data-ttu-id="ffff1-119">Create</span><span class="sxs-lookup"><span data-stu-id="ffff1-119">Create</span></span>](../api/planner-post-buckets.md) | [<span data-ttu-id="ffff1-120">plannerBucket</span><span class="sxs-lookup"><span data-stu-id="ffff1-120">plannerBucket</span></span>](plannerbucket.md)   | <span data-ttu-id="ffff1-121">Crear un nuevo objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="ffff1-121">Create a new **plannerBucket** object.</span></span> |
|[<span data-ttu-id="ffff1-122">Update</span><span class="sxs-lookup"><span data-stu-id="ffff1-122">Update</span></span>](../api/plannerbucket-update.md) | [<span data-ttu-id="ffff1-123">plannerBucket</span><span class="sxs-lookup"><span data-stu-id="ffff1-123">plannerBucket</span></span>](plannerbucket.md)   |<span data-ttu-id="ffff1-124">Actualizar el objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="ffff1-124">Update **plannerBucket** object.</span></span> |
|[<span data-ttu-id="ffff1-125">Delete</span><span class="sxs-lookup"><span data-stu-id="ffff1-125">Delete</span></span>](../api/plannerbucket-delete.md) | <span data-ttu-id="ffff1-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ffff1-126">None</span></span> |<span data-ttu-id="ffff1-127">Eliminar el objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="ffff1-127">Delete **plannerBucket** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="ffff1-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ffff1-128">Properties</span></span>
| <span data-ttu-id="ffff1-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ffff1-129">Property</span></span>     | <span data-ttu-id="ffff1-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffff1-130">Type</span></span>   |<span data-ttu-id="ffff1-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffff1-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ffff1-132">id</span><span class="sxs-lookup"><span data-stu-id="ffff1-132">id</span></span>|<span data-ttu-id="ffff1-133">String</span><span class="sxs-lookup"><span data-stu-id="ffff1-133">String</span></span>| <span data-ttu-id="ffff1-134">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ffff1-134">Read-only.</span></span> <span data-ttu-id="ffff1-135">Identificador del depósito de.</span><span class="sxs-lookup"><span data-stu-id="ffff1-135">ID of the bucket.</span></span> <span data-ttu-id="ffff1-136">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ffff1-136">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="ffff1-137">[Validación de formato](tasks-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="ffff1-137">[Format validation](tasks-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="ffff1-138">name</span><span class="sxs-lookup"><span data-stu-id="ffff1-138">name</span></span>|<span data-ttu-id="ffff1-139">String</span><span class="sxs-lookup"><span data-stu-id="ffff1-139">String</span></span>|<span data-ttu-id="ffff1-140">Nombre del depósito.</span><span class="sxs-lookup"><span data-stu-id="ffff1-140">Name of the bucket.</span></span>|
|<span data-ttu-id="ffff1-141">orderHint</span><span class="sxs-lookup"><span data-stu-id="ffff1-141">orderHint</span></span>|<span data-ttu-id="ffff1-142">String</span><span class="sxs-lookup"><span data-stu-id="ffff1-142">String</span></span>|<span data-ttu-id="ffff1-p105">Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="ffff1-p105">Hint used to order items of this type in a list view. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|
|<span data-ttu-id="ffff1-145">planId</span><span class="sxs-lookup"><span data-stu-id="ffff1-145">planId</span></span>|<span data-ttu-id="ffff1-146">String</span><span class="sxs-lookup"><span data-stu-id="ffff1-146">String</span></span>|<span data-ttu-id="ffff1-147">Id. de plan al que pertenece el depósito.</span><span class="sxs-lookup"><span data-stu-id="ffff1-147">Plan ID to which the bucket belongs.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ffff1-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ffff1-148">Relationships</span></span>
| <span data-ttu-id="ffff1-149">Relación</span><span class="sxs-lookup"><span data-stu-id="ffff1-149">Relationship</span></span> | <span data-ttu-id="ffff1-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffff1-150">Type</span></span>   |<span data-ttu-id="ffff1-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffff1-151">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ffff1-152">tasks</span><span class="sxs-lookup"><span data-stu-id="ffff1-152">tasks</span></span>|<span data-ttu-id="ffff1-153">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="ffff1-153">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="ffff1-p106">Solo lectura. Admite valores NULL. Colección de tareas del depósito.</span><span class="sxs-lookup"><span data-stu-id="ffff1-p106">Read-only. Nullable. The collection of tasks in the bucket.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ffff1-157">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ffff1-157">JSON representation</span></span>
<span data-ttu-id="ffff1-158">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ffff1-158">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerBucket"
}-->

```json
{
  "id": "String (identifier)",
  "name": "String",
  "orderHint": "String",
  "planId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerBucket resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->