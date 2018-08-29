# <a name="chartseries-resource-type"></a><span data-ttu-id="a2cd3-101">Tipo de recurso ChartSeries</span><span class="sxs-lookup"><span data-stu-id="a2cd3-101">ChartSeries resource type</span></span>

<span data-ttu-id="a2cd3-102">Representa una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="a2cd3-102">Represents a series in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="a2cd3-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="a2cd3-103">Methods</span></span>

| <span data-ttu-id="a2cd3-104">Método</span><span class="sxs-lookup"><span data-stu-id="a2cd3-104">Method</span></span>           | <span data-ttu-id="a2cd3-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2cd3-105">Return Type</span></span>    |<span data-ttu-id="a2cd3-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2cd3-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a2cd3-107">Get ChartSeries</span><span class="sxs-lookup"><span data-stu-id="a2cd3-107">Get ChartSeries</span></span>](../api/chartseries_get.md) | [<span data-ttu-id="a2cd3-108">WorkbookChartSeries</span><span class="sxs-lookup"><span data-stu-id="a2cd3-108">WorkbookChartSeries</span></span>](chartseries.md) |<span data-ttu-id="a2cd3-109">Lee las propiedades y relaciones del objeto chartSeries.</span><span class="sxs-lookup"><span data-stu-id="a2cd3-109">Read properties and relationships of chartSeries object.</span></span>|
|[<span data-ttu-id="a2cd3-110">Create ChartPoints</span><span class="sxs-lookup"><span data-stu-id="a2cd3-110">Create ChartPoints</span></span>](../api/chartseries_post_points.md) |[<span data-ttu-id="a2cd3-111">ChartPoints</span><span class="sxs-lookup"><span data-stu-id="a2cd3-111">ChartPoints</span></span>](chartpoint.md)| <span data-ttu-id="a2cd3-112">Crea un nuevo ChartPoints publicándolo en la colección points.</span><span class="sxs-lookup"><span data-stu-id="a2cd3-112">Create a new ChartPoints by posting to the points collection.</span></span>|
|[<span data-ttu-id="a2cd3-113">List points</span><span class="sxs-lookup"><span data-stu-id="a2cd3-113">List points</span></span>](../api/chartseries_list_points.md) |<span data-ttu-id="a2cd3-114">Colección [ChartPoints](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="a2cd3-114">[ChartPoints](chartpoint.md) collection</span></span>| <span data-ttu-id="a2cd3-115">Obtiene la colección de objetos ChartPoints.</span><span class="sxs-lookup"><span data-stu-id="a2cd3-115">Get a ChartPoints object collection.</span></span>|
|[<span data-ttu-id="a2cd3-116">Update</span><span class="sxs-lookup"><span data-stu-id="a2cd3-116">Update</span></span>](../api/chartseries_update.md) | [<span data-ttu-id="a2cd3-117">WorkbookChartSeries</span><span class="sxs-lookup"><span data-stu-id="a2cd3-117">WorkbookChartSeries</span></span>](chartseries.md) |<span data-ttu-id="a2cd3-118">Actualiza el objeto ChartSeries.</span><span class="sxs-lookup"><span data-stu-id="a2cd3-118">Update ChartSeries object.</span></span> |
|[<span data-ttu-id="a2cd3-119">List</span><span class="sxs-lookup"><span data-stu-id="a2cd3-119">List</span></span>](../api/chartseries_list.md) | <span data-ttu-id="a2cd3-120">Colección de [WorkbookChartSeries](chartseries.md)</span><span class="sxs-lookup"><span data-stu-id="a2cd3-120">[WorkbookChartSeries](chartseries.md) collection</span></span> |<span data-ttu-id="a2cd3-121">Obtiene la colección de objetos chartSeries.</span><span class="sxs-lookup"><span data-stu-id="a2cd3-121">Get chartSeries object collection.</span></span> |
|[<span data-ttu-id="a2cd3-122">Itemat</span><span class="sxs-lookup"><span data-stu-id="a2cd3-122">Itemat</span></span>](../api/chartseriescollection_itemat.md)|[<span data-ttu-id="a2cd3-123">WorkbookChartSeries</span><span class="sxs-lookup"><span data-stu-id="a2cd3-123">WorkbookChartSeries</span></span>](chartseries.md)|<span data-ttu-id="a2cd3-124">Recupera una serie en función de su posición en la colección</span><span class="sxs-lookup"><span data-stu-id="a2cd3-124">Retrieves a series based on its position in the collection</span></span>|

## <a name="properties"></a><span data-ttu-id="a2cd3-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a2cd3-125">Properties</span></span>
| <span data-ttu-id="a2cd3-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2cd3-126">Property</span></span>     | <span data-ttu-id="a2cd3-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2cd3-127">Type</span></span>   |<span data-ttu-id="a2cd3-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2cd3-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a2cd3-129">name</span><span class="sxs-lookup"><span data-stu-id="a2cd3-129">name</span></span>|<span data-ttu-id="a2cd3-130">cadena</span><span class="sxs-lookup"><span data-stu-id="a2cd3-130">string</span></span>|<span data-ttu-id="a2cd3-131">Representa el nombre de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="a2cd3-131">Represents the name of a series in a chart.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a2cd3-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a2cd3-132">Relationships</span></span>
| <span data-ttu-id="a2cd3-133">Relación</span><span class="sxs-lookup"><span data-stu-id="a2cd3-133">Relationship</span></span> | <span data-ttu-id="a2cd3-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2cd3-134">Type</span></span>   |<span data-ttu-id="a2cd3-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2cd3-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a2cd3-136">format</span><span class="sxs-lookup"><span data-stu-id="a2cd3-136">format</span></span>|[<span data-ttu-id="a2cd3-137">WorkbookChartSeriesFormat</span><span class="sxs-lookup"><span data-stu-id="a2cd3-137">WorkbookChartSeriesFormat</span></span>](chartseriesformat.md)|<span data-ttu-id="a2cd3-p101">Representa el formato de una serie del gráfico, que incluye el formato de relleno y de línea. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a2cd3-p101">Represents the formatting of a chart series, which includes fill and line formatting. Read-only.</span></span>|
|<span data-ttu-id="a2cd3-140">points</span><span class="sxs-lookup"><span data-stu-id="a2cd3-140">points</span></span>|<span data-ttu-id="a2cd3-141">Colección de [WorkbookChartPoint](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="a2cd3-141">[WorkbookChartPoint](chartpoint.md) collection</span></span>|<span data-ttu-id="a2cd3-p102">Representa una colección de todos los puntos de la serie. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a2cd3-p102">Represents a collection of all points in the series. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a2cd3-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a2cd3-144">JSON representation</span></span>

<span data-ttu-id="a2cd3-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a2cd3-145">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartSeries"
}-->

```json
{
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartSeries resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->