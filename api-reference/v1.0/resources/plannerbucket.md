# <a name="plannerbucket-resource-type"></a><span data-ttu-id="9324e-101">Tipo de recurso plannerBucket</span><span class="sxs-lookup"><span data-stu-id="9324e-101">plannerBucket resource type</span></span>

<span data-ttu-id="9324e-p101">El recurso **plannerBucket** representa un depósito (o "columna personalizada") para las tareas de un plan de Office 365. Se encuentra en un [plannerPlan](plannerPlan.md) y puede tener una colección de [plannerTasks](plannerTask.md).</span><span class="sxs-lookup"><span data-stu-id="9324e-p101">The **plannerBucket** resource represents a bucket (or "custom column") for tasks in a plan in Office 365. It is contained in a [plannerPlan](plannerPlan.md) and can have a collection of [plannerTasks](plannerTask.md).</span></span>



## <a name="methods"></a><span data-ttu-id="9324e-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="9324e-104">Methods</span></span>

| <span data-ttu-id="9324e-105">Método</span><span class="sxs-lookup"><span data-stu-id="9324e-105">Method</span></span>           | <span data-ttu-id="9324e-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9324e-106">Return Type</span></span>    |<span data-ttu-id="9324e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9324e-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9324e-108">Obtener plannerBucket</span><span class="sxs-lookup"><span data-stu-id="9324e-108">Get plannerBucket</span></span>](../api/plannerbucket_get.md) | [<span data-ttu-id="9324e-109">plannerBucket</span><span class="sxs-lookup"><span data-stu-id="9324e-109">plannerBucket</span></span>](plannerbucket.md) |<span data-ttu-id="9324e-110">Leer las propiedades y las relaciones del objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="9324e-110">Read properties and relationships of **plannerBucket** object.</span></span>|
|[<span data-ttu-id="9324e-111">Enumerar plannerTasks</span><span class="sxs-lookup"><span data-stu-id="9324e-111">List plannerTasks</span></span>](../api/plannerbucket_list_tasks.md) |<span data-ttu-id="9324e-112">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="9324e-112">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="9324e-113">Obtenga una colección de objetos **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="9324e-113">Get a **plannerTask** object collection.</span></span>|
|[<span data-ttu-id="9324e-114">Create</span><span class="sxs-lookup"><span data-stu-id="9324e-114">Create</span></span>](../api/planner_post_buckets.md) | [<span data-ttu-id="9324e-115">plannerBucket</span><span class="sxs-lookup"><span data-stu-id="9324e-115">plannerBucket</span></span>](plannerbucket.md)   | <span data-ttu-id="9324e-116">Crear un nuevo objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="9324e-116">Create a new **plannerBucket** object.</span></span> |
|[<span data-ttu-id="9324e-117">Update</span><span class="sxs-lookup"><span data-stu-id="9324e-117">Update</span></span>](../api/plannerbucket_update.md) | [<span data-ttu-id="9324e-118">plannerBucket</span><span class="sxs-lookup"><span data-stu-id="9324e-118">plannerBucket</span></span>](plannerbucket.md)   |<span data-ttu-id="9324e-119">Actualizar el objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="9324e-119">Update **plannerBucket** object.</span></span> |
|[<span data-ttu-id="9324e-120">Delete</span><span class="sxs-lookup"><span data-stu-id="9324e-120">Delete</span></span>](../api/plannerbucket_delete.md) | <span data-ttu-id="9324e-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9324e-121">None</span></span> |<span data-ttu-id="9324e-122">Eliminar el objeto **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="9324e-122">Delete **plannerBucket** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="9324e-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9324e-123">Properties</span></span>
| <span data-ttu-id="9324e-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9324e-124">Property</span></span>     | <span data-ttu-id="9324e-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="9324e-125">Type</span></span>   |<span data-ttu-id="9324e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="9324e-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9324e-127">id</span><span class="sxs-lookup"><span data-stu-id="9324e-127">id</span></span>|<span data-ttu-id="9324e-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="9324e-128">String</span></span>| <span data-ttu-id="9324e-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9324e-129">Read-only.</span></span> <span data-ttu-id="9324e-130">Identificador del depósito.</span><span class="sxs-lookup"><span data-stu-id="9324e-130">Name of the bucket.</span></span> <span data-ttu-id="9324e-131">Tiene 28 caracteres y distingue mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9324e-131">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="9324e-132">[La validación de formato](planner_identifiers_disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="9324e-132">[Format validation](planner_identifiers_disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="9324e-133">name</span><span class="sxs-lookup"><span data-stu-id="9324e-133">name</span></span>|<span data-ttu-id="9324e-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="9324e-134">String</span></span>|<span data-ttu-id="9324e-135">Nombre del depósito.</span><span class="sxs-lookup"><span data-stu-id="9324e-135">Name of the bucket.</span></span>|
|<span data-ttu-id="9324e-136">orderHint</span><span class="sxs-lookup"><span data-stu-id="9324e-136">orderHint</span></span>|<span data-ttu-id="9324e-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="9324e-137">String</span></span>|<span data-ttu-id="9324e-p103">Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](planner_order_hint_format.md).</span><span class="sxs-lookup"><span data-stu-id="9324e-p103">Hint used to order items of this type in a list view. The format is defined as outlined [here](planner_order_hint_format.md).</span></span>|
|<span data-ttu-id="9324e-140">planId</span><span class="sxs-lookup"><span data-stu-id="9324e-140">planId</span></span>|<span data-ttu-id="9324e-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="9324e-141">String</span></span>|<span data-ttu-id="9324e-142">Id. de plan al que pertenece el depósito.</span><span class="sxs-lookup"><span data-stu-id="9324e-142">Plan ID to which the bucket belongs.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9324e-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9324e-143">Relationships</span></span>
| <span data-ttu-id="9324e-144">Relación</span><span class="sxs-lookup"><span data-stu-id="9324e-144">Relationship</span></span> | <span data-ttu-id="9324e-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="9324e-145">Type</span></span>   |<span data-ttu-id="9324e-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="9324e-146">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9324e-147">tasks</span><span class="sxs-lookup"><span data-stu-id="9324e-147">tasks</span></span>|<span data-ttu-id="9324e-148">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="9324e-148">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="9324e-p104">Solo lectura. Admite valores NULL. Colección de tareas del depósito.</span><span class="sxs-lookup"><span data-stu-id="9324e-p104">Read-only. Nullable. The collection of tasks in the bucket.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9324e-152">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9324e-152">JSON representation</span></span>
<span data-ttu-id="9324e-153">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9324e-153">Here is a JSON representation of the resource.</span></span>

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