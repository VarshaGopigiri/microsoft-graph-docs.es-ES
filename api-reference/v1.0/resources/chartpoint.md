# <a name="chartpoint-resource-type"></a><span data-ttu-id="985e1-101">Tipo de recurso ChartPoint</span><span class="sxs-lookup"><span data-stu-id="985e1-101">ChartPoint resource type</span></span>

<span data-ttu-id="985e1-102">Representa un punto de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="985e1-102">Represents a point of a series in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="985e1-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="985e1-103">Methods</span></span>

| <span data-ttu-id="985e1-104">Método</span><span class="sxs-lookup"><span data-stu-id="985e1-104">Method</span></span>           | <span data-ttu-id="985e1-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="985e1-105">Return Type</span></span>    |<span data-ttu-id="985e1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="985e1-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="985e1-107">Get ChartPoint</span><span class="sxs-lookup"><span data-stu-id="985e1-107">Get ChartPoint</span></span>](../api/chartpoint_get.md) | [<span data-ttu-id="985e1-108">WorkbookChartPoint</span><span class="sxs-lookup"><span data-stu-id="985e1-108">WorkbookChartPoint</span></span>](chartpoint.md) |<span data-ttu-id="985e1-109">Lee las propiedades y relaciones del objeto chartPoint.</span><span class="sxs-lookup"><span data-stu-id="985e1-109">Read properties and relationships of chartPoint object.</span></span>|
|[<span data-ttu-id="985e1-110">Lista</span><span class="sxs-lookup"><span data-stu-id="985e1-110">List</span></span>](../api/chartpoint_list.md) | <span data-ttu-id="985e1-111">Colección de [WorkbookChartPoint](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="985e1-111">[WorkbookChartPoint](chartpoint.md) collection</span></span> |<span data-ttu-id="985e1-112">Obtiene la colección de objetos chartPoint.</span><span class="sxs-lookup"><span data-stu-id="985e1-112">Get chartPoint object collection.</span></span> |
|[<span data-ttu-id="985e1-113">Itemat</span><span class="sxs-lookup"><span data-stu-id="985e1-113">Itemat</span></span>](../api/chartpointscollection_itemat.md)|[<span data-ttu-id="985e1-114">WorkbookChartPoint</span><span class="sxs-lookup"><span data-stu-id="985e1-114">WorkbookChartPoint</span></span>](chartpoint.md)|<span data-ttu-id="985e1-115">Recupera un punto en función de su posición dentro de la serie.</span><span class="sxs-lookup"><span data-stu-id="985e1-115">Retrieve a point based on its position within the series.</span></span>|

## <a name="properties"></a><span data-ttu-id="985e1-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="985e1-116">Properties</span></span>
| <span data-ttu-id="985e1-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="985e1-117">Property</span></span>     | <span data-ttu-id="985e1-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="985e1-118">Type</span></span>   |<span data-ttu-id="985e1-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="985e1-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="985e1-120">value</span><span class="sxs-lookup"><span data-stu-id="985e1-120">value</span></span>|<span data-ttu-id="985e1-121">Json</span><span class="sxs-lookup"><span data-stu-id="985e1-121">Json</span></span>|<span data-ttu-id="985e1-p101">Devuelve el valor de un punto del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="985e1-p101">Returns the value of a chart point. Read-only.</span></span>|
|<span data-ttu-id="985e1-124">id</span><span class="sxs-lookup"><span data-stu-id="985e1-124">id</span></span>|<span data-ttu-id="985e1-125">cadena</span><span class="sxs-lookup"><span data-stu-id="985e1-125">string</span></span>|<span data-ttu-id="985e1-126">identificador único</span><span class="sxs-lookup"><span data-stu-id="985e1-126">unique identifier</span></span>|

## <a name="relationships"></a><span data-ttu-id="985e1-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="985e1-127">Relationships</span></span>
| <span data-ttu-id="985e1-128">Relación</span><span class="sxs-lookup"><span data-stu-id="985e1-128">Relationship</span></span> | <span data-ttu-id="985e1-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="985e1-129">Type</span></span>   |<span data-ttu-id="985e1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="985e1-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="985e1-131">format</span><span class="sxs-lookup"><span data-stu-id="985e1-131">format</span></span>|[<span data-ttu-id="985e1-132">WorkbookChartPointFormat</span><span class="sxs-lookup"><span data-stu-id="985e1-132">WorkbookChartPointFormat</span></span>](chartpointformat.md)|<span data-ttu-id="985e1-p102">Encapsula las propiedades de formato del punto del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="985e1-p102">Encapsulates the format properties chart point. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="985e1-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="985e1-135">JSON representation</span></span>

<span data-ttu-id="985e1-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="985e1-136">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartPoint"
}-->

```json
{
  "value": "string",
  "id": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartPoint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->