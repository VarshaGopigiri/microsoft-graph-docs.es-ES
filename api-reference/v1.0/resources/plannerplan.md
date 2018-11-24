# <a name="plannerplan-resource-type"></a><span data-ttu-id="c6e82-101">Tipo de recurso plannerPlan</span><span class="sxs-lookup"><span data-stu-id="c6e82-101">plannerPlan resource type</span></span>

<span data-ttu-id="c6e82-p101">El recurso **plannerPlan** representa un plan de Office 365. Un plan puede ser propiedad de un [grupo](group.md) y contiene una colección de [plannerTasks](plannerTask.md). También puede tener una colección de [plannerBuckets](plannerBucket.md). Cada objeto plan tiene un objeto [details](plannerPlanDetails.md) que puede contener más información sobre el plan. Para obtener más información sobre la relación entre los grupos, los planes y las categorías, vea [Planner](planner_overview.md).</span><span class="sxs-lookup"><span data-stu-id="c6e82-p101">The **plannerPlan** resource represents a plan in Office 365. A plan can be owned by a [group](group.md) and contains a collection of [plannerTasks](plannerTask.md). It can also have a collection of [plannerBuckets](plannerBucket.md). Each plan object has a [details](plannerPlanDetails.md) object that can contain more information about the plan. For more information about the relationships between groups, plans, and tasks, see [Planner](planner_overview.md).</span></span>

## <a name="methods"></a><span data-ttu-id="c6e82-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="c6e82-107">Methods</span></span>

| <span data-ttu-id="c6e82-108">Método</span><span class="sxs-lookup"><span data-stu-id="c6e82-108">Method</span></span>           | <span data-ttu-id="c6e82-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6e82-109">Return Type</span></span>    |<span data-ttu-id="c6e82-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6e82-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c6e82-111">Obtener plannerPlan</span><span class="sxs-lookup"><span data-stu-id="c6e82-111">Get plannerPlan</span></span>](../api/plannerplan_get.md) | [<span data-ttu-id="c6e82-112">plannerPlan</span><span class="sxs-lookup"><span data-stu-id="c6e82-112">plannerPlan</span></span>](plannerplan.md) |<span data-ttu-id="c6e82-113">Leer las propiedades y las relaciones del objeto **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="c6e82-113">Read properties and relationships of **plannerPlan** object.</span></span>|
|[<span data-ttu-id="c6e82-114">Enumerar depósitos</span><span class="sxs-lookup"><span data-stu-id="c6e82-114">List buckets</span></span>](../api/plannerplan_list_buckets.md) |<span data-ttu-id="c6e82-115">Colección [plannerBucket](plannerbucket.md)</span><span class="sxs-lookup"><span data-stu-id="c6e82-115">[plannerBucket](plannerbucket.md) collection</span></span>| <span data-ttu-id="c6e82-116">Obtenga una colección de objetos **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="c6e82-116">Get a **plannerBucket** object collection.</span></span>|
|[<span data-ttu-id="c6e82-117">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="c6e82-117">List tasks</span></span>](../api/plannerplan_list_tasks.md) |<span data-ttu-id="c6e82-118">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="c6e82-118">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="c6e82-119">Obtenga una colección de objetos **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="c6e82-119">Get a **plannerTask** object collection.</span></span>|
|[<span data-ttu-id="c6e82-120">Update</span><span class="sxs-lookup"><span data-stu-id="c6e82-120">Update</span></span>](../api/plannerplan_update.md) | [<span data-ttu-id="c6e82-121">plannerPlan</span><span class="sxs-lookup"><span data-stu-id="c6e82-121">plannerPlan</span></span>](plannerplan.md) |<span data-ttu-id="c6e82-122">Actualizar el objeto **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="c6e82-122">Update **plannerPlan** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="c6e82-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c6e82-123">Properties</span></span>
| <span data-ttu-id="c6e82-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c6e82-124">Property</span></span>     | <span data-ttu-id="c6e82-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6e82-125">Type</span></span>   |<span data-ttu-id="c6e82-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6e82-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c6e82-127">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c6e82-127">createdDateTime</span></span>|<span data-ttu-id="c6e82-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c6e82-128">DateTimeOffset</span></span>|<span data-ttu-id="c6e82-p102">Solo lectura. Fecha y hora en que se creó el plan. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="c6e82-p102">Read-only. Date and time at which the plan is created. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="c6e82-133">id</span><span class="sxs-lookup"><span data-stu-id="c6e82-133">id</span></span>|<span data-ttu-id="c6e82-134">String</span><span class="sxs-lookup"><span data-stu-id="c6e82-134">String</span></span>| <span data-ttu-id="c6e82-135">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c6e82-135">Read-only.</span></span> <span data-ttu-id="c6e82-136">Identificador del plan.</span><span class="sxs-lookup"><span data-stu-id="c6e82-136">ID of the plan.</span></span> <span data-ttu-id="c6e82-137">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c6e82-137">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="c6e82-138">[Validación de formato](planner_identifiers_disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="c6e82-138">[Format validation](planner_identifiers_disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="c6e82-139">owner</span><span class="sxs-lookup"><span data-stu-id="c6e82-139">owner</span></span>|<span data-ttu-id="c6e82-140">String</span><span class="sxs-lookup"><span data-stu-id="c6e82-140">String</span></span>|<span data-ttu-id="c6e82-141">Identificador del [grupo](group.md) que posee el plan.</span><span class="sxs-lookup"><span data-stu-id="c6e82-141">ID of the [Group](group.md) that owns the plan.</span></span> <span data-ttu-id="c6e82-142">Un grupo válido debe existir antes de que se puede establecer en este campo.</span><span class="sxs-lookup"><span data-stu-id="c6e82-142">A valid group must exist before this field can be set.</span></span> <span data-ttu-id="c6e82-143">Una vez establecida, esta propiedad no se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="c6e82-143">After it is set, this property can’t be updated.</span></span>|
|<span data-ttu-id="c6e82-144">title</span><span class="sxs-lookup"><span data-stu-id="c6e82-144">title</span></span>|<span data-ttu-id="c6e82-145">String</span><span class="sxs-lookup"><span data-stu-id="c6e82-145">String</span></span>|<span data-ttu-id="c6e82-p105">Obligatorio. Título del plan.</span><span class="sxs-lookup"><span data-stu-id="c6e82-p105">Required. Title of the plan.</span></span>|
|<span data-ttu-id="c6e82-148">createdBy</span><span class="sxs-lookup"><span data-stu-id="c6e82-148">createdBy</span></span>|[<span data-ttu-id="c6e82-149">identitySet</span><span class="sxs-lookup"><span data-stu-id="c6e82-149">identitySet</span></span>](identityset.md)|<span data-ttu-id="c6e82-p106">Solo lectura. El usuario que creó el plan.</span><span class="sxs-lookup"><span data-stu-id="c6e82-p106">Read-only. The user who created the plan.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c6e82-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c6e82-152">Relationships</span></span>
| <span data-ttu-id="c6e82-153">Relación</span><span class="sxs-lookup"><span data-stu-id="c6e82-153">Relationship</span></span> | <span data-ttu-id="c6e82-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6e82-154">Type</span></span>   |<span data-ttu-id="c6e82-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6e82-155">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c6e82-156">buckets</span><span class="sxs-lookup"><span data-stu-id="c6e82-156">buckets</span></span>|<span data-ttu-id="c6e82-157">Colección [plannerBucket](plannerbucket.md)</span><span class="sxs-lookup"><span data-stu-id="c6e82-157">[plannerBucket](plannerbucket.md) collection</span></span>| <span data-ttu-id="c6e82-p107">Solo lectura. Admite valores NULL. Colección de depósitos del plan.</span><span class="sxs-lookup"><span data-stu-id="c6e82-p107">Read-only. Nullable. Collection of buckets in the plan.</span></span>|
|<span data-ttu-id="c6e82-161">details</span><span class="sxs-lookup"><span data-stu-id="c6e82-161">details</span></span>|[<span data-ttu-id="c6e82-162">plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="c6e82-162">plannerPlanDetails</span></span>](plannerplandetails.md)| <span data-ttu-id="c6e82-p108">Solo lectura. Admite valores NULL. Detalles adicionales sobre el plan.</span><span class="sxs-lookup"><span data-stu-id="c6e82-p108">Read-only. Nullable. Additional details about the plan.</span></span>|
|<span data-ttu-id="c6e82-166">tasks</span><span class="sxs-lookup"><span data-stu-id="c6e82-166">tasks</span></span>|<span data-ttu-id="c6e82-167">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="c6e82-167">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="c6e82-p109">Solo lectura. Admite valores NULL. Colección de tareas en el plan.</span><span class="sxs-lookup"><span data-stu-id="c6e82-p109">Read-only. Nullable. Collection of tasks in the plan.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c6e82-171">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c6e82-171">JSON representation</span></span>

<span data-ttu-id="c6e82-172">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c6e82-172">Here is a JSON representation of the resource.</span></span>

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