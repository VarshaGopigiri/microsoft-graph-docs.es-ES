---
title: Tipo de recurso plannerPlan
description: El recurso **plannerPlan** representa un plan en Office 365. Un plan de puede pertenecer a un grupo y contiene una colección de plannerTasks. También puede tener una colección de plannerBuckets. Cada objeto de plan tiene un objeto de detalles que puede contener más información acerca del plan. Para obtener más información acerca de las relaciones entre los grupos, los planes y tareas, vea organizador.
localization_priority: Priority
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 9e77f2c0163f9093d931c46098498caa8c43f42c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987898"
---
# <a name="plannerplan-resource-type"></a><span data-ttu-id="ac823-107">Tipo de recurso plannerPlan</span><span class="sxs-lookup"><span data-stu-id="ac823-107">plannerPlan resource type</span></span>

<span data-ttu-id="ac823-p102">El recurso **plannerPlan** representa un plan de Office 365. Un plan puede ser propiedad de un [grupo](group.md) y contiene una colección de [plannerTasks](plannertask.md). También puede tener una colección de [plannerBuckets](plannerbucket.md). Cada objeto plan tiene un objeto [details](plannerplandetails.md) que puede contener más información sobre el plan. Para obtener más información sobre la relación entre los grupos, los planes y las categorías, vea [Planner](planner-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ac823-p102">The **plannerPlan** resource represents a plan in Office 365. A plan can be owned by a [group](group.md) and contains a collection of [plannerTasks](plannertask.md). It can also have a collection of [plannerBuckets](plannerbucket.md). Each plan object has a [details](plannerplandetails.md) object that can contain more information about the plan. For more information about the relationships between groups, plans, and tasks, see [Planner](planner-overview.md).</span></span>

## <a name="methods"></a><span data-ttu-id="ac823-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ac823-113">Methods</span></span>

| <span data-ttu-id="ac823-114">Método</span><span class="sxs-lookup"><span data-stu-id="ac823-114">Method</span></span>           | <span data-ttu-id="ac823-115">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac823-115">Return Type</span></span>    |<span data-ttu-id="ac823-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac823-116">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ac823-117">Obtener plannerPlan</span><span class="sxs-lookup"><span data-stu-id="ac823-117">Get plannerPlan</span></span>](../api/plannerplan-get.md) | [<span data-ttu-id="ac823-118">plannerPlan</span><span class="sxs-lookup"><span data-stu-id="ac823-118">plannerPlan</span></span>](plannerplan.md) |<span data-ttu-id="ac823-119">Leer las propiedades y las relaciones del objeto **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="ac823-119">Read properties and relationships of **plannerPlan** object.</span></span>|
|[<span data-ttu-id="ac823-120">Enumerar depósitos</span><span class="sxs-lookup"><span data-stu-id="ac823-120">List buckets</span></span>](../api/plannerplan-list-buckets.md) |<span data-ttu-id="ac823-121">Colección [plannerBucket](plannerbucket.md)</span><span class="sxs-lookup"><span data-stu-id="ac823-121">[plannerBucket](plannerbucket.md) collection</span></span>| <span data-ttu-id="ac823-122">Obtenga una colección de objetos **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="ac823-122">Get a **plannerBucket** object collection.</span></span>|
|[<span data-ttu-id="ac823-123">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="ac823-123">List tasks</span></span>](../api/plannerplan-list-tasks.md) |<span data-ttu-id="ac823-124">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="ac823-124">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="ac823-125">Obtenga una colección de objetos **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="ac823-125">Get a **plannerTask** object collection.</span></span>|
|[<span data-ttu-id="ac823-126">Update</span><span class="sxs-lookup"><span data-stu-id="ac823-126">Update</span></span>](../api/plannerplan-update.md) | [<span data-ttu-id="ac823-127">plannerPlan</span><span class="sxs-lookup"><span data-stu-id="ac823-127">plannerPlan</span></span>](plannerplan.md) |<span data-ttu-id="ac823-128">Actualizar el objeto **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="ac823-128">Update **plannerPlan** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="ac823-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac823-129">Properties</span></span>
| <span data-ttu-id="ac823-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac823-130">Property</span></span>     | <span data-ttu-id="ac823-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac823-131">Type</span></span>   |<span data-ttu-id="ac823-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac823-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ac823-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ac823-133">createdDateTime</span></span>|<span data-ttu-id="ac823-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ac823-134">DateTimeOffset</span></span>|<span data-ttu-id="ac823-p103">Solo lectura. Fecha y hora en que se creó el plan. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="ac823-p103">Read-only. Date and time at which the plan is created. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="ac823-139">id</span><span class="sxs-lookup"><span data-stu-id="ac823-139">id</span></span>|<span data-ttu-id="ac823-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac823-140">String</span></span>| <span data-ttu-id="ac823-141">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ac823-141">Read-only.</span></span> <span data-ttu-id="ac823-142">Identificador del plan.</span><span class="sxs-lookup"><span data-stu-id="ac823-142">ID of the plan.</span></span> <span data-ttu-id="ac823-143">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ac823-143">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="ac823-144">[Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="ac823-144">[Format validation](planner-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="ac823-145">owner</span><span class="sxs-lookup"><span data-stu-id="ac823-145">owner</span></span>|<span data-ttu-id="ac823-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac823-146">String</span></span>|<span data-ttu-id="ac823-147">Identificador del [grupo](group.md) que posee el plan.</span><span class="sxs-lookup"><span data-stu-id="ac823-147">ID of the [Group](group.md) that owns the plan.</span></span> <span data-ttu-id="ac823-148">Un grupo válido debe existir antes de que se puede establecer en este campo.</span><span class="sxs-lookup"><span data-stu-id="ac823-148">A valid group must exist before this field can be set.</span></span> <span data-ttu-id="ac823-149">Una vez establecida, esta propiedad no se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="ac823-149">After it is set, this property can’t be updated.</span></span>|
|<span data-ttu-id="ac823-150">title</span><span class="sxs-lookup"><span data-stu-id="ac823-150">title</span></span>|<span data-ttu-id="ac823-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac823-151">String</span></span>|<span data-ttu-id="ac823-p106">Obligatorio. Título del plan.</span><span class="sxs-lookup"><span data-stu-id="ac823-p106">Required. Title of the plan.</span></span>|
|<span data-ttu-id="ac823-154">createdBy</span><span class="sxs-lookup"><span data-stu-id="ac823-154">createdBy</span></span>|[<span data-ttu-id="ac823-155">identitySet</span><span class="sxs-lookup"><span data-stu-id="ac823-155">identitySet</span></span>](identityset.md)|<span data-ttu-id="ac823-p107">Solo lectura. El usuario que creó el plan.</span><span class="sxs-lookup"><span data-stu-id="ac823-p107">Read-only. The user who created the plan.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ac823-158">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ac823-158">Relationships</span></span>
| <span data-ttu-id="ac823-159">Relación</span><span class="sxs-lookup"><span data-stu-id="ac823-159">Relationship</span></span> | <span data-ttu-id="ac823-160">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac823-160">Type</span></span>   |<span data-ttu-id="ac823-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac823-161">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ac823-162">buckets</span><span class="sxs-lookup"><span data-stu-id="ac823-162">buckets</span></span>|<span data-ttu-id="ac823-163">Colección [plannerBucket](plannerbucket.md)</span><span class="sxs-lookup"><span data-stu-id="ac823-163">[plannerBucket](plannerbucket.md) collection</span></span>| <span data-ttu-id="ac823-p108">Solo lectura. Admite valores NULL. Colección de depósitos del plan.</span><span class="sxs-lookup"><span data-stu-id="ac823-p108">Read-only. Nullable. Collection of buckets in the plan.</span></span>|
|<span data-ttu-id="ac823-167">details</span><span class="sxs-lookup"><span data-stu-id="ac823-167">details</span></span>|[<span data-ttu-id="ac823-168">plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="ac823-168">plannerPlanDetails</span></span>](plannerplandetails.md)| <span data-ttu-id="ac823-p109">Solo lectura. Admite valores NULL. Detalles adicionales sobre el plan.</span><span class="sxs-lookup"><span data-stu-id="ac823-p109">Read-only. Nullable. Additional details about the plan.</span></span>|
|<span data-ttu-id="ac823-172">tasks</span><span class="sxs-lookup"><span data-stu-id="ac823-172">tasks</span></span>|<span data-ttu-id="ac823-173">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="ac823-173">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="ac823-p110">Solo lectura. Admite valores NULL. Colección de tareas en el plan.</span><span class="sxs-lookup"><span data-stu-id="ac823-p110">Read-only. Nullable. Collection of tasks in the plan.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ac823-177">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ac823-177">JSON representation</span></span>

<span data-ttu-id="ac823-178">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ac823-178">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlan"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "owner": "String",
  "title": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlan resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
