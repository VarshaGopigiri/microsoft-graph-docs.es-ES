# <a name="planner-resource-type"></a><span data-ttu-id="d2f7c-101">Tipo de recurso planner</span><span class="sxs-lookup"><span data-stu-id="d2f7c-101">planner resource type</span></span>

<span data-ttu-id="d2f7c-p101">El recurso **planner** es el punto de entrada para el modelo de objetos de Planner. Devuelve un recurso **planner** singleton.  No contiene ninguna propiedad utilizable.</span><span class="sxs-lookup"><span data-stu-id="d2f7c-p101">The **planner** resource is the entry point for the Planner object model. It returns a singleton **planner** resource.  It doesn't contain any usable properties.</span></span>


## <a name="methods"></a><span data-ttu-id="d2f7c-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="d2f7c-105">Methods</span></span>

| <span data-ttu-id="d2f7c-106">Método</span><span class="sxs-lookup"><span data-stu-id="d2f7c-106">Method</span></span>           | <span data-ttu-id="d2f7c-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2f7c-107">Return Type</span></span>    |<span data-ttu-id="d2f7c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2f7c-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d2f7c-109">Crear plannerBucket</span><span class="sxs-lookup"><span data-stu-id="d2f7c-109">Create plannerBucket</span></span>](../api/planner_post_buckets.md) |[<span data-ttu-id="d2f7c-110">plannerBucket</span><span class="sxs-lookup"><span data-stu-id="d2f7c-110">plannerBucket</span></span>](plannerbucket.md)| <span data-ttu-id="d2f7c-111">Crear un nuevo **plannerBucket** publicándolo en la colección de depósitos.</span><span class="sxs-lookup"><span data-stu-id="d2f7c-111">Create a new **plannerBucket** by posting to the buckets collection.</span></span>|
|[<span data-ttu-id="d2f7c-112">Crear plannerPlan</span><span class="sxs-lookup"><span data-stu-id="d2f7c-112">Create plannerPlan</span></span>](../api/planner_post_plans.md) |[<span data-ttu-id="d2f7c-113">plannerPlan</span><span class="sxs-lookup"><span data-stu-id="d2f7c-113">plannerPlan</span></span>](plannerplan.md)| <span data-ttu-id="d2f7c-114">Crear un nuevo **plannerPlan** publicándolo en la colección de planes.</span><span class="sxs-lookup"><span data-stu-id="d2f7c-114">Create a new **plannerPlan** by posting to the plans collection.</span></span>|
|[<span data-ttu-id="d2f7c-115">Crear plannerTask</span><span class="sxs-lookup"><span data-stu-id="d2f7c-115">Create plannerTask</span></span>](../api/planner_post_tasks.md) |[<span data-ttu-id="d2f7c-116">plannerTask</span><span class="sxs-lookup"><span data-stu-id="d2f7c-116">plannerTask</span></span>](plannertask.md)| <span data-ttu-id="d2f7c-117">Crea una nueva **plannerTask** publicándola en la colección de tareas.</span><span class="sxs-lookup"><span data-stu-id="d2f7c-117">Create a new **plannerTask** by posting to the tasks collection.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d2f7c-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d2f7c-118">Relationships</span></span>
| <span data-ttu-id="d2f7c-119">Relación</span><span class="sxs-lookup"><span data-stu-id="d2f7c-119">Relationship</span></span> | <span data-ttu-id="d2f7c-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2f7c-120">Type</span></span>   |<span data-ttu-id="d2f7c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2f7c-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d2f7c-122">buckets</span><span class="sxs-lookup"><span data-stu-id="d2f7c-122">buckets</span></span>|<span data-ttu-id="d2f7c-123">Colección [plannerBucket](plannerbucket.md)</span><span class="sxs-lookup"><span data-stu-id="d2f7c-123">[plannerBucket](plannerbucket.md) collection</span></span>| <span data-ttu-id="d2f7c-p102">Solo lectura. Admite valores NULL. Devuelve una colección de los depósitos especificados</span><span class="sxs-lookup"><span data-stu-id="d2f7c-p102">Read-only. Nullable. Returns a collection of the specified buckets</span></span>|
|<span data-ttu-id="d2f7c-127">plans</span><span class="sxs-lookup"><span data-stu-id="d2f7c-127">plans</span></span>|<span data-ttu-id="d2f7c-128">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="d2f7c-128">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="d2f7c-p103">Solo lectura. Admite valores NULL. Devuelve una colección de los planes especificados</span><span class="sxs-lookup"><span data-stu-id="d2f7c-p103">Read-only. Nullable. Returns a collection of the specified plans</span></span>|
|<span data-ttu-id="d2f7c-132">tasks</span><span class="sxs-lookup"><span data-stu-id="d2f7c-132">tasks</span></span>|<span data-ttu-id="d2f7c-133">Colección [plannerTask](plannertask.md)</span><span class="sxs-lookup"><span data-stu-id="d2f7c-133">[plannerTask](plannertask.md) collection</span></span>| <span data-ttu-id="d2f7c-p104">Solo lectura. Admite valores NULL. Devuelve una colección de las tareas especificadas</span><span class="sxs-lookup"><span data-stu-id="d2f7c-p104">Read-only. Nullable. Returns a collection of the specified tasks</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d2f7c-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d2f7c-137">JSON representation</span></span>
<span data-ttu-id="d2f7c-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d2f7c-138">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.planner"
}-->

```json
{
}
```

## <a name="example"></a><span data-ttu-id="d2f7c-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2f7c-139">Example</span></span>

<span data-ttu-id="d2f7c-140">El recurso **planner** está disponible en la raíz del gráfico.</span><span class="sxs-lookup"><span data-stu-id="d2f7c-140">The **planner** resource is available at the root of the graph.</span></span>

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