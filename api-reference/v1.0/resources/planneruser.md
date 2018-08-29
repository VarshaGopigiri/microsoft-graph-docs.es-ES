# <a name="planneruser-resource-type"></a><span data-ttu-id="10a1d-101">Tipo de recurso plannerUser</span><span class="sxs-lookup"><span data-stu-id="10a1d-101">plannerUser resource type</span></span>

<span data-ttu-id="10a1d-p101">El recurso **plannerUser** proporciona acceso a los recursos Planner de un [usuario](user.md). No contiene ninguna propiedad utilizable.</span><span class="sxs-lookup"><span data-stu-id="10a1d-p101">The **plannerUser** resource provide access to Planner resources for a [user](user.md). It doesn't contain any usable properties.</span></span>


## <a name="methods"></a><span data-ttu-id="10a1d-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="10a1d-104">Methods</span></span>

| <span data-ttu-id="10a1d-105">Método</span><span class="sxs-lookup"><span data-stu-id="10a1d-105">Method</span></span>           | <span data-ttu-id="10a1d-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10a1d-106">Return Type</span></span>    |<span data-ttu-id="10a1d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="10a1d-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="10a1d-108">Enumerar planes</span><span class="sxs-lookup"><span data-stu-id="10a1d-108">List plans</span></span>](../api/planneruser_list_plans.md) |<span data-ttu-id="10a1d-109">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="10a1d-109">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="10a1d-110">Obtenga una colección de objetos **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="10a1d-110">Get a **plannerPlan** object collection.</span></span>|
|[<span data-ttu-id="10a1d-111">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="10a1d-111">List tasks</span></span>](../api/planneruser_list_tasks.md) |<span data-ttu-id="10a1d-112">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="10a1d-112">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="10a1d-113">Obtenga una colección de objetos **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="10a1d-113">Get a **plannerTask** object collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="10a1d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10a1d-114">Properties</span></span>
| <span data-ttu-id="10a1d-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="10a1d-115">Property</span></span>     | <span data-ttu-id="10a1d-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="10a1d-116">Type</span></span>   |<span data-ttu-id="10a1d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="10a1d-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="10a1d-118">id</span><span class="sxs-lookup"><span data-stu-id="10a1d-118">id</span></span>|<span data-ttu-id="10a1d-119">String</span><span class="sxs-lookup"><span data-stu-id="10a1d-119">String</span></span>| <span data-ttu-id="10a1d-p102">Solo lectura. Identificador del planenrUser</span><span class="sxs-lookup"><span data-stu-id="10a1d-p102">Read-only. Identifier of the planenrUser</span></span>|

## <a name="relationships"></a><span data-ttu-id="10a1d-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="10a1d-122">Relationships</span></span>
| <span data-ttu-id="10a1d-123">Relación</span><span class="sxs-lookup"><span data-stu-id="10a1d-123">Relationship</span></span> | <span data-ttu-id="10a1d-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="10a1d-124">Type</span></span>   |<span data-ttu-id="10a1d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="10a1d-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="10a1d-126">plans</span><span class="sxs-lookup"><span data-stu-id="10a1d-126">plans</span></span>|<span data-ttu-id="10a1d-127">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="10a1d-127">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="10a1d-p103">Solo lectura. Admite valores NULL. Devuelve las [plannerTasks](plannertask.md) asignadas al usuario.</span><span class="sxs-lookup"><span data-stu-id="10a1d-p103">Read-only. Nullable. Returns the [plannerTasks](plannertask.md) assigned to the user.</span></span>|
|<span data-ttu-id="10a1d-131">tasks</span><span class="sxs-lookup"><span data-stu-id="10a1d-131">tasks</span></span>|<span data-ttu-id="10a1d-132">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="10a1d-132">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="10a1d-p104">Solo lectura. Admite valores NULL. Devuelve los [plannerPlans](plannerplan.md) compartidos con el usuario.</span><span class="sxs-lookup"><span data-stu-id="10a1d-p104">Read-only. Nullable. Returns the [plannerPlans](plannerplan.md) shared with the user.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="10a1d-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="10a1d-136">JSON representation</span></span>
<span data-ttu-id="10a1d-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="10a1d-137">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerUser"
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
  "description": "plannerUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->