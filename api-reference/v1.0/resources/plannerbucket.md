---
title: Tipo de recurso plannerBucket
description: ) para las tareas de un plan de Office 365. Está contenida en un plannerPlan y puede tener una colección de plannerTasks.
author: TarkanSevilmis
localization_priority: Normal
ms.prod: planner
ms.openlocfilehash: 8cfc25e5554b20d4f808c8929b53549f4c44d7a2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982837"
---
# <a name="plannerbucket-resource-type"></a><span data-ttu-id="ecb76-104">Tipo de recurso plannerBucket</span><span class="sxs-lookup"><span data-stu-id="ecb76-104">plannerBucket resource type</span></span>

<span data-ttu-id="ecb76-p102">El recurso **plannerBucket** representa un depósito (o "columna personalizada") para las tareas de un plan de Office 365. Se encuentra en un [plannerPlan](plannerplan.md) y puede tener una colección de [plannerTasks](plannertask.md).</span><span class="sxs-lookup"><span data-stu-id="ecb76-p102">The **plannerBucket** resource represents a bucket (or "custom column") for tasks in a plan in Office 365. It is contained in a [plannerPlan](plannerplan.md) and can have a collection of [plannerTasks](plannertask.md).</span></span>



## <a name="methods"></a><span data-ttu-id="ecb76-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="ecb76-107">Methods</span></span>

| <span data-ttu-id="ecb76-108">Método</span><span class="sxs-lookup"><span data-stu-id="ecb76-108">Method</span></span>           | <span data-ttu-id="ecb76-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ecb76-109">Return Type</span></span>    |<span data-ttu-id="ecb76-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecb76-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ecb76-111">Obtener plannerBucket</span><span class="sxs-lookup"><span data-stu-id="ecb76-111">Get plannerBucket</span></span>](../api/plannerbucket-get.md) | [<span data-ttu-id="ecb76-112">plannerBucket</span><span class="sxs-lookup"><span data-stu-id="ecb76-112">plannerBucket</span></span>](plannerbucket.md) |<span data-ttu-id="ecb76-113">Leer las propiedades y las relaciones del objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="ecb76-113">Read properties and relationships of **plannerBucket** object.</span></span>|
|[<span data-ttu-id="ecb76-114">Enumerar plannerTasks</span><span class="sxs-lookup"><span data-stu-id="ecb76-114">List plannerTasks</span></span>](../api/plannerbucket-list-tasks.md) |<span data-ttu-id="ecb76-115">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="ecb76-115">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="ecb76-116">Obtenga una colección de objetos **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="ecb76-116">Get a **plannerTask** object collection.</span></span>|
|[<span data-ttu-id="ecb76-117">Create</span><span class="sxs-lookup"><span data-stu-id="ecb76-117">Create</span></span>](../api/planner-post-buckets.md) | [<span data-ttu-id="ecb76-118">plannerBucket</span><span class="sxs-lookup"><span data-stu-id="ecb76-118">plannerBucket</span></span>](plannerbucket.md)   | <span data-ttu-id="ecb76-119">Crear un nuevo objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="ecb76-119">Create a new **plannerBucket** object.</span></span> |
|[<span data-ttu-id="ecb76-120">Update</span><span class="sxs-lookup"><span data-stu-id="ecb76-120">Update</span></span>](../api/plannerbucket-update.md) | [<span data-ttu-id="ecb76-121">plannerBucket</span><span class="sxs-lookup"><span data-stu-id="ecb76-121">plannerBucket</span></span>](plannerbucket.md)   |<span data-ttu-id="ecb76-122">Actualizar el objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="ecb76-122">Update **plannerBucket** object.</span></span> |
|[<span data-ttu-id="ecb76-123">Delete</span><span class="sxs-lookup"><span data-stu-id="ecb76-123">Delete</span></span>](../api/plannerbucket-delete.md) | <span data-ttu-id="ecb76-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ecb76-124">None</span></span> |<span data-ttu-id="ecb76-125">Eliminar el objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="ecb76-125">Delete **plannerBucket** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="ecb76-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ecb76-126">Properties</span></span>
| <span data-ttu-id="ecb76-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ecb76-127">Property</span></span>     | <span data-ttu-id="ecb76-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="ecb76-128">Type</span></span>   |<span data-ttu-id="ecb76-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecb76-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ecb76-130">id</span><span class="sxs-lookup"><span data-stu-id="ecb76-130">id</span></span>|<span data-ttu-id="ecb76-131">String</span><span class="sxs-lookup"><span data-stu-id="ecb76-131">String</span></span>| <span data-ttu-id="ecb76-132">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ecb76-132">Read-only.</span></span> <span data-ttu-id="ecb76-133">Identificador del depósito de.</span><span class="sxs-lookup"><span data-stu-id="ecb76-133">ID of the bucket.</span></span> <span data-ttu-id="ecb76-134">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ecb76-134">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="ecb76-135">[Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="ecb76-135">[Format validation](planner-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="ecb76-136">name</span><span class="sxs-lookup"><span data-stu-id="ecb76-136">name</span></span>|<span data-ttu-id="ecb76-137">String</span><span class="sxs-lookup"><span data-stu-id="ecb76-137">String</span></span>|<span data-ttu-id="ecb76-138">Nombre del depósito.</span><span class="sxs-lookup"><span data-stu-id="ecb76-138">Name of the bucket.</span></span>|
|<span data-ttu-id="ecb76-139">orderHint</span><span class="sxs-lookup"><span data-stu-id="ecb76-139">orderHint</span></span>|<span data-ttu-id="ecb76-140">String</span><span class="sxs-lookup"><span data-stu-id="ecb76-140">String</span></span>|<span data-ttu-id="ecb76-p104">Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="ecb76-p104">Hint used to order items of this type in a list view. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|
|<span data-ttu-id="ecb76-143">planId</span><span class="sxs-lookup"><span data-stu-id="ecb76-143">planId</span></span>|<span data-ttu-id="ecb76-144">String</span><span class="sxs-lookup"><span data-stu-id="ecb76-144">String</span></span>|<span data-ttu-id="ecb76-145">Id. de plan al que pertenece el depósito.</span><span class="sxs-lookup"><span data-stu-id="ecb76-145">Plan ID to which the bucket belongs.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ecb76-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ecb76-146">Relationships</span></span>
| <span data-ttu-id="ecb76-147">Relación</span><span class="sxs-lookup"><span data-stu-id="ecb76-147">Relationship</span></span> | <span data-ttu-id="ecb76-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="ecb76-148">Type</span></span>   |<span data-ttu-id="ecb76-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecb76-149">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ecb76-150">tasks</span><span class="sxs-lookup"><span data-stu-id="ecb76-150">tasks</span></span>|<span data-ttu-id="ecb76-151">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="ecb76-151">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="ecb76-p105">Solo lectura. Admite valores NULL. Colección de tareas del depósito.</span><span class="sxs-lookup"><span data-stu-id="ecb76-p105">Read-only. Nullable. The collection of tasks in the bucket.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ecb76-155">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ecb76-155">JSON representation</span></span>
<span data-ttu-id="ecb76-156">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ecb76-156">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
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
