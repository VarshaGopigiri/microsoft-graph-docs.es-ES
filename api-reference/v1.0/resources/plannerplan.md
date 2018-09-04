# <a name="plannerplan-resource-type"></a><span data-ttu-id="c8ce5-101">Tipo de recurso plannerPlan</span><span class="sxs-lookup"><span data-stu-id="c8ce5-101">plannerPlan resource type</span></span>

<span data-ttu-id="c8ce5-p101">El recurso **plannerPlan** representa un plan de Office 365. Un plan puede ser propiedad de un [grupo](group.md) y contiene una colección de [plannerTasks](plannerTask.md). También puede tener una colección de [plannerBuckets](plannerBucket.md). Cada objeto plan tiene un objeto [details](plannerPlanDetails.md) que puede contener más información sobre el plan. Para obtener más información sobre la relación entre los grupos, los planes y las categorías, vea [Planner](planner_overview.md).</span><span class="sxs-lookup"><span data-stu-id="c8ce5-p101">The **plannerPlan** resource represents a plan in Office 365. A plan can be owned by a [group](group.md) and contains a collection of [plannerTasks](plannerTask.md). It can also have a collection of [plannerBuckets](plannerBucket.md). Each plan object has a [details](plannerPlanDetails.md) object that can contain more information about the plan. For more information about the relationships between groups, plans, and tasks, see [Planner](planner_overview.md).</span></span>

## <a name="methods"></a><span data-ttu-id="c8ce5-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8ce5-107">Methods</span></span>

| <span data-ttu-id="c8ce5-108">Método</span><span class="sxs-lookup"><span data-stu-id="c8ce5-108">Method</span></span>           | <span data-ttu-id="c8ce5-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8ce5-109">Return Type</span></span>    |<span data-ttu-id="c8ce5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8ce5-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c8ce5-111">Get plannerPlan</span><span class="sxs-lookup"><span data-stu-id="c8ce5-111">Get plannerPlan</span></span>](../api/plannerplan_get.md) | [<span data-ttu-id="c8ce5-112">plannerPlan</span><span class="sxs-lookup"><span data-stu-id="c8ce5-112">plannerPlan</span></span>](plannerplan.md) |<span data-ttu-id="c8ce5-113">Leer las propiedades y las relaciones del objeto **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-113">Read properties and relationships of **plannerPlan** object.</span></span>|
|[<span data-ttu-id="c8ce5-114">List buckets</span><span class="sxs-lookup"><span data-stu-id="c8ce5-114">List buckets</span></span>](../api/plannerplan_list_buckets.md) |<span data-ttu-id="c8ce5-115">Colección [plannerBucket](plannerbucket.md)</span><span class="sxs-lookup"><span data-stu-id="c8ce5-115">[plannerBucket](plannerbucket.md) collection</span></span>| <span data-ttu-id="c8ce5-116">Obtenga una colección de objetos **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-116">Get a **plannerBucket** object collection.</span></span>|
|[<span data-ttu-id="c8ce5-117">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="c8ce5-117">List tasks</span></span>](../api/plannerplan_list_tasks.md) |<span data-ttu-id="c8ce5-118">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="c8ce5-118">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="c8ce5-119">Obtenga una colección de objetos **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-119">Get a **plannerTask** object collection.</span></span>|
|[<span data-ttu-id="c8ce5-120">Actualizar</span><span class="sxs-lookup"><span data-stu-id="c8ce5-120">Update</span></span>](../api/plannerplan_update.md) | [<span data-ttu-id="c8ce5-121">plannerPlan</span><span class="sxs-lookup"><span data-stu-id="c8ce5-121">plannerPlan</span></span>](plannerplan.md) |<span data-ttu-id="c8ce5-122">Actualizar el objeto **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-122">Update **plannerPlan** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="c8ce5-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8ce5-123">Properties</span></span>
| <span data-ttu-id="c8ce5-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c8ce5-124">Property</span></span>     | <span data-ttu-id="c8ce5-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8ce5-125">Type</span></span>   |<span data-ttu-id="c8ce5-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8ce5-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c8ce5-127">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c8ce5-127">createdDateTime</span></span>|<span data-ttu-id="c8ce5-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c8ce5-128">DateTimeOffset</span></span>|<span data-ttu-id="c8ce5-p102">Solo lectura. Fecha y hora en que se creó el plan. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="c8ce5-p102">Read-only. Date and time at which the plan is created. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="c8ce5-133">id</span><span class="sxs-lookup"><span data-stu-id="c8ce5-133">id</span></span>|<span data-ttu-id="c8ce5-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8ce5-134">String</span></span>| <span data-ttu-id="c8ce5-135">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-135">Read-only.</span></span> <span data-ttu-id="c8ce5-136">Identificador del plan.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-136">Title of the plan.</span></span> <span data-ttu-id="c8ce5-137">Tiene 28 caracteres y distingue mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-137">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="c8ce5-138">[La validación de formato](planner_identifiers_disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-138">[Format validation](planner_identifiers_disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="c8ce5-139">owner</span><span class="sxs-lookup"><span data-stu-id="c8ce5-139">owner</span></span>|<span data-ttu-id="c8ce5-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8ce5-140">String</span></span>|<span data-ttu-id="c8ce5-p104">Id. del [grupo](group.md) que tiene el plan. Para poder establecer este campo, debe existir un grupo válido. Una vez establecido, solo lo puede actualizar el propietario.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-p104">ID of the [Group](group.md) that owns the plan. A valid group must exist before this field can be set. Once set, this can only be updated by the owner.</span></span>|
|<span data-ttu-id="c8ce5-144">title</span><span class="sxs-lookup"><span data-stu-id="c8ce5-144">title</span></span>|<span data-ttu-id="c8ce5-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8ce5-145">String</span></span>|<span data-ttu-id="c8ce5-p105">Obligatorio. Título del plan.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-p105">Required. Title of the plan.</span></span>|
|<span data-ttu-id="c8ce5-148">createdBy</span><span class="sxs-lookup"><span data-stu-id="c8ce5-148">createdBy</span></span>|[<span data-ttu-id="c8ce5-149">identitySet</span><span class="sxs-lookup"><span data-stu-id="c8ce5-149">identitySet</span></span>](identityset.md)|<span data-ttu-id="c8ce5-p106">Solo lectura. El usuario que creó el plan.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-p106">Read-only. The user who created the plan.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c8ce5-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c8ce5-152">Relationships</span></span>
| <span data-ttu-id="c8ce5-153">Relación</span><span class="sxs-lookup"><span data-stu-id="c8ce5-153">Relationship</span></span> | <span data-ttu-id="c8ce5-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8ce5-154">Type</span></span>   |<span data-ttu-id="c8ce5-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8ce5-155">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c8ce5-156">buckets</span><span class="sxs-lookup"><span data-stu-id="c8ce5-156">buckets</span></span>|<span data-ttu-id="c8ce5-157">Colección [plannerBucket](plannerbucket.md)</span><span class="sxs-lookup"><span data-stu-id="c8ce5-157">[plannerBucket](plannerbucket.md) collection</span></span>| <span data-ttu-id="c8ce5-p107">Solo lectura. Admite valores NULL. Colección de depósitos del plan.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-p107">Read-only. Nullable. Collection of buckets in the plan.</span></span>|
|<span data-ttu-id="c8ce5-161">details</span><span class="sxs-lookup"><span data-stu-id="c8ce5-161">details</span></span>|[<span data-ttu-id="c8ce5-162">plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="c8ce5-162">plannerPlanDetails</span></span>](plannerplandetails.md)| <span data-ttu-id="c8ce5-p108">Solo lectura. Admite valores NULL. Detalles adicionales sobre el plan.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-p108">Read-only. Nullable. Additional details about the plan.</span></span>|
|<span data-ttu-id="c8ce5-166">tasks</span><span class="sxs-lookup"><span data-stu-id="c8ce5-166">tasks</span></span>|<span data-ttu-id="c8ce5-167">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="c8ce5-167">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="c8ce5-p109">Solo lectura. Admite valores NULL. Colección de tareas en el plan.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-p109">Read-only. Nullable. Collection of tasks in the plan.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c8ce5-171">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c8ce5-171">JSON representation</span></span>

<span data-ttu-id="c8ce5-172">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c8ce5-172">Here is a JSON representation of the resource.</span></span>

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