# <a name="plannergroup-resource-type"></a><span data-ttu-id="f8545-101">Tipo de recurso plannerGroup</span><span class="sxs-lookup"><span data-stu-id="f8545-101">plannerGroup resource type</span></span>

<span data-ttu-id="f8545-p101">El recurso **plannerGroup** proporciona acceso a los recursos Planner de un [grupo](group.md). No contiene ninguna propiedad utilizable.</span><span class="sxs-lookup"><span data-stu-id="f8545-p101">The **plannerGroup** resource provides access to Planner resources for a [group](group.md). It doesn't contain any usable properties.</span></span>

## <a name="methods"></a><span data-ttu-id="f8545-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="f8545-104">Methods</span></span>

| <span data-ttu-id="f8545-105">Método</span><span class="sxs-lookup"><span data-stu-id="f8545-105">Method</span></span>           | <span data-ttu-id="f8545-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8545-106">Return Type</span></span>    |<span data-ttu-id="f8545-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8545-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="f8545-108">Enumerar planes</span><span class="sxs-lookup"><span data-stu-id="f8545-108">List plans</span></span>](../api/plannergroup_list_plans.md) |<span data-ttu-id="f8545-109">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="f8545-109">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="f8545-110">Obtenga una colección de objetos **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="f8545-110">Get a **plannerPlan** object collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="f8545-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f8545-111">Properties</span></span>
| <span data-ttu-id="f8545-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f8545-112">Property</span></span>     | <span data-ttu-id="f8545-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8545-113">Type</span></span>   |<span data-ttu-id="f8545-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8545-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f8545-115">id</span><span class="sxs-lookup"><span data-stu-id="f8545-115">id</span></span>|<span data-ttu-id="f8545-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8545-116">String</span></span>| <span data-ttu-id="f8545-p102">Solo lectura. Identificador del **plannerGroup**</span><span class="sxs-lookup"><span data-stu-id="f8545-p102">Read-only. Identifier of the **plannerGroup**</span></span>|

## <a name="relationships"></a><span data-ttu-id="f8545-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f8545-119">Relationships</span></span>
| <span data-ttu-id="f8545-120">Relación</span><span class="sxs-lookup"><span data-stu-id="f8545-120">Relationship</span></span> | <span data-ttu-id="f8545-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8545-121">Type</span></span>   |<span data-ttu-id="f8545-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8545-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f8545-123">plans</span><span class="sxs-lookup"><span data-stu-id="f8545-123">plans</span></span>|<span data-ttu-id="f8545-124">Colección [plannerPlan](plannerplan.md)</span><span class="sxs-lookup"><span data-stu-id="f8545-124">[plannerPlan](plannerplan.md) collection</span></span>| <span data-ttu-id="f8545-p103">Solo lectura. Admite valores NULL. Devuelve los [plannerPlans](plannerplan.md) propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="f8545-p103">Read-only. Nullable. Returns the [plannerPlans](plannerplan.md) owned by the group.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f8545-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f8545-128">JSON representation</span></span>
<span data-ttu-id="f8545-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f8545-129">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerGroup"
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
  "description": "plannerGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->