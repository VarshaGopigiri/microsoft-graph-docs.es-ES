---
title: Tipo de recurso plannerPlan
description: El recurso **plannerPlan** representa un plan en Office 365. Un plan de puede pertenecer a un grupo y contiene una colección de plannerTasks. También puede tener una colección de plannerBuckets. Cada objeto de plan tiene un objeto de detalles que puede contener más información acerca del plan. Para obtener más información acerca de las relaciones entre los grupos, los planes y tareas, vea organizador.
ms.openlocfilehash: 236b6cb5d35e11a30bcb4371e0563b56ac93de8f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085348"
---
# <a name="plannerplan-resource-type"></a><span data-ttu-id="c6c7b-107">Tipo de recurso plannerPlan</span><span class="sxs-lookup"><span data-stu-id="c6c7b-107">plannerPlan resource type</span></span>

> <span data-ttu-id="c6c7b-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c6c7b-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c6c7b-110">El recurso **plannerPlan** representa un plan en Office 365.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-110">The **plannerPlan** resource represents a plan in Office 365.</span></span> <span data-ttu-id="c6c7b-111">Un plan de puede pertenecer a un [grupo](group.md) y contiene una colección de [plannerTasks](plannertask.md).</span><span class="sxs-lookup"><span data-stu-id="c6c7b-111">A plan can be owned by a [group](group.md) and contains a collection of [plannerTasks](plannertask.md).</span></span> <span data-ttu-id="c6c7b-112">También puede tener una colección de [plannerBuckets](plannerbucket.md).</span><span class="sxs-lookup"><span data-stu-id="c6c7b-112">It can also have a collection of [plannerBuckets](plannerbucket.md).</span></span> <span data-ttu-id="c6c7b-113">Cada objeto de plan tiene un objeto de [Detalles](plannerplandetails.md) que puede contener más información acerca del plan.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-113">Each plan object has a [details](plannerplandetails.md) object which can contain more information about the plan.</span></span> <span data-ttu-id="c6c7b-114">Para obtener más información acerca de las relaciones entre los grupos, los planes y tareas, vea [Organizador](planner-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c6c7b-114">For more information about the relationships between groups, plans, and tasks, see [Planner](planner-overview.md).</span></span>



## <a name="methods"></a><span data-ttu-id="c6c7b-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="c6c7b-115">Methods</span></span>

| <span data-ttu-id="c6c7b-116">Método</span><span class="sxs-lookup"><span data-stu-id="c6c7b-116">Method</span></span>           | <span data-ttu-id="c6c7b-117">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6c7b-117">Return Type</span></span>    |<span data-ttu-id="c6c7b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6c7b-118">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c6c7b-119">Obtener plannerPlan</span><span class="sxs-lookup"><span data-stu-id="c6c7b-119">Get plannerPlan</span></span>](../api/plannerplan-get.md) | [<span data-ttu-id="c6c7b-120">plannerPlan</span><span class="sxs-lookup"><span data-stu-id="c6c7b-120">plannerPlan</span></span>](plannerplan.md) |<span data-ttu-id="c6c7b-121">Leer las propiedades y las relaciones del objeto **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-121">Read properties and relationships of **plannerPlan** object.</span></span>|
|[<span data-ttu-id="c6c7b-122">Enumerar depósitos</span><span class="sxs-lookup"><span data-stu-id="c6c7b-122">List buckets</span></span>](../api/plannerplan-list-buckets.md) |<span data-ttu-id="c6c7b-123">Colección [plannerBucket](plannerbucket.md)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-123">[plannerBucket](plannerbucket.md) collection</span></span>| <span data-ttu-id="c6c7b-124">Obtenga una colección de objetos **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-124">Get a **plannerBucket** object collection.</span></span>|
|[<span data-ttu-id="c6c7b-125">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="c6c7b-125">List tasks</span></span>](../api/plannerplan-list-tasks.md) |<span data-ttu-id="c6c7b-126">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-126">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="c6c7b-127">Obtenga una colección de objetos **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-127">Get a **plannerTask** object collection.</span></span>|
|[<span data-ttu-id="c6c7b-128">Update</span><span class="sxs-lookup"><span data-stu-id="c6c7b-128">Update</span></span>](../api/plannerplan-update.md) | [<span data-ttu-id="c6c7b-129">plannerPlan</span><span class="sxs-lookup"><span data-stu-id="c6c7b-129">plannerPlan</span></span>](plannerplan.md) |<span data-ttu-id="c6c7b-130">Actualizar el objeto **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-130">Update **plannerPlan** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="c6c7b-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c6c7b-131">Properties</span></span>
| <span data-ttu-id="c6c7b-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c6c7b-132">Property</span></span>     | <span data-ttu-id="c6c7b-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6c7b-133">Type</span></span>   |<span data-ttu-id="c6c7b-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6c7b-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c6c7b-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c6c7b-135">createdDateTime</span></span>|<span data-ttu-id="c6c7b-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c6c7b-136">DateTimeOffset</span></span>|<span data-ttu-id="c6c7b-p104">Solo lectura. Fecha y hora en que se creó el plan. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="c6c7b-p104">Read-only. Date and time at which the plan is created. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="c6c7b-141">id</span><span class="sxs-lookup"><span data-stu-id="c6c7b-141">id</span></span>|<span data-ttu-id="c6c7b-142">String</span><span class="sxs-lookup"><span data-stu-id="c6c7b-142">String</span></span>| <span data-ttu-id="c6c7b-143">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-143">Read-only.</span></span> <span data-ttu-id="c6c7b-144">Identificador del plan.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-144">ID of the plan.</span></span> <span data-ttu-id="c6c7b-145">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-145">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="c6c7b-146">[Validación de formato](tasks-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-146">[Format validation](tasks-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="c6c7b-147">owner</span><span class="sxs-lookup"><span data-stu-id="c6c7b-147">owner</span></span>|<span data-ttu-id="c6c7b-148">String</span><span class="sxs-lookup"><span data-stu-id="c6c7b-148">String</span></span>|<span data-ttu-id="c6c7b-149">Identificador del [grupo](group.md) que posee el plan.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-149">ID of the [Group](group.md) that owns the plan.</span></span> <span data-ttu-id="c6c7b-150">Un grupo válido debe existir antes de que se puede establecer en este campo.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-150">A valid group must exist before this field can be set.</span></span> <span data-ttu-id="c6c7b-151">Una vez establecida, esta propiedad no se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-151">After it is set, this property can’t be updated.</span></span>|
|<span data-ttu-id="c6c7b-152">title</span><span class="sxs-lookup"><span data-stu-id="c6c7b-152">title</span></span>|<span data-ttu-id="c6c7b-153">String</span><span class="sxs-lookup"><span data-stu-id="c6c7b-153">String</span></span>|<span data-ttu-id="c6c7b-p107">Obligatorio. Título del plan.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-p107">Required. Title of the plan.</span></span>|
|<span data-ttu-id="c6c7b-156">createdBy</span><span class="sxs-lookup"><span data-stu-id="c6c7b-156">createdBy</span></span>|[<span data-ttu-id="c6c7b-157">identitySet</span><span class="sxs-lookup"><span data-stu-id="c6c7b-157">identitySet</span></span>](identityset.md)|<span data-ttu-id="c6c7b-p108">Solo lectura. El usuario que creó el plan.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-p108">Read-only. The user who created the plan.</span></span>|
|<span data-ttu-id="c6c7b-160">contextos</span><span class="sxs-lookup"><span data-stu-id="c6c7b-160">contexts</span></span>|[<span data-ttu-id="c6c7b-161">plannerPlanContextCollection</span><span class="sxs-lookup"><span data-stu-id="c6c7b-161">plannerPlanContextCollection</span></span>](plannerplancontextcollection.md)| <span data-ttu-id="c6c7b-162">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-162">Read-only.</span></span> <span data-ttu-id="c6c7b-163">Experiencias de usuario adicionales en el que se usa este plan, representado como entradas de [plannerPlanContext](plannerplancontext.md) .</span><span class="sxs-lookup"><span data-stu-id="c6c7b-163">Additional user experiences in which this plan is used, represented as [plannerPlanContext](plannerplancontext.md) entries.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c6c7b-164">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c6c7b-164">Relationships</span></span>
| <span data-ttu-id="c6c7b-165">Relación</span><span class="sxs-lookup"><span data-stu-id="c6c7b-165">Relationship</span></span> | <span data-ttu-id="c6c7b-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6c7b-166">Type</span></span>   |<span data-ttu-id="c6c7b-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6c7b-167">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c6c7b-168">buckets</span><span class="sxs-lookup"><span data-stu-id="c6c7b-168">buckets</span></span>|<span data-ttu-id="c6c7b-169">Colección [plannerBucket](plannerbucket.md)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-169">[plannerBucket](plannerbucket.md) collection</span></span>| <span data-ttu-id="c6c7b-p110">Solo lectura. Admite valores NULL. Colección de depósitos del plan.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-p110">Read-only. Nullable. Collection of buckets in the plan.</span></span>|
|<span data-ttu-id="c6c7b-173">details</span><span class="sxs-lookup"><span data-stu-id="c6c7b-173">details</span></span>|[<span data-ttu-id="c6c7b-174">plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="c6c7b-174">plannerPlanDetails</span></span>](plannerplandetails.md)| <span data-ttu-id="c6c7b-p111">Solo lectura. Admite valores NULL. Detalles adicionales sobre el plan.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-p111">Read-only. Nullable. Additional details about the plan.</span></span>|
|<span data-ttu-id="c6c7b-178">tasks</span><span class="sxs-lookup"><span data-stu-id="c6c7b-178">tasks</span></span>|<span data-ttu-id="c6c7b-179">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="c6c7b-179">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="c6c7b-p112">Solo lectura. Admite valores NULL. Colección de tareas en el plan.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-p112">Read-only. Nullable. Collection of tasks in the plan.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c6c7b-183">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c6c7b-183">JSON representation</span></span>

<span data-ttu-id="c6c7b-184">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-184">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlan"
}-->

```json
{
  "contexts": {
    "48#19%3Ad128c63941b24733951ea7defd81e550%40thread%2Eskype19%3Ad128c63941b24733951ea7defd81e550%40thread%2Eskype": {
        "@odata.type": "#microsoft.graph.plannerPlanContext",
        "associationType": "Board",
        "createdDateTime": "2015-10-14T00:57:28.4698344Z",
        "displayNameSegments": [
            "Finance Team",
            "Budget Plans"
        ],
        "ownerAppId": "5e3ce6c0-2b1f-4285-8d4b-75ee78787346"
    }
  },
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