# <a name="chartaxes-resource-type"></a><span data-ttu-id="bed5d-101">Tipo de recurso ChartAxes</span><span class="sxs-lookup"><span data-stu-id="bed5d-101">ChartAxes resource type</span></span>

<span data-ttu-id="bed5d-102">Representa los ejes del gráfico.</span><span class="sxs-lookup"><span data-stu-id="bed5d-102">Represents the chart axes.</span></span>


## <a name="methods"></a><span data-ttu-id="bed5d-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="bed5d-103">Methods</span></span>
<span data-ttu-id="bed5d-104">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bed5d-104">None</span></span>

## <a name="properties"></a><span data-ttu-id="bed5d-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bed5d-105">Properties</span></span>
<span data-ttu-id="bed5d-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bed5d-106">None</span></span>

## <a name="relationships"></a><span data-ttu-id="bed5d-107">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bed5d-107">Relationships</span></span>
| <span data-ttu-id="bed5d-108">Relación</span><span class="sxs-lookup"><span data-stu-id="bed5d-108">Relationship</span></span> | <span data-ttu-id="bed5d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="bed5d-109">Type</span></span>   |<span data-ttu-id="bed5d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bed5d-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bed5d-111">categoryAxis</span><span class="sxs-lookup"><span data-stu-id="bed5d-111">categoryAxis</span></span>|[<span data-ttu-id="bed5d-112">WorkbookChartAxis</span><span class="sxs-lookup"><span data-stu-id="bed5d-112">WorkbookChartAxis</span></span>](chartaxis.md)|<span data-ttu-id="bed5d-p101">Representa el eje de categorías de un gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bed5d-p101">Represents the category axis in a chart. Read-only.</span></span>|
|<span data-ttu-id="bed5d-115">seriesAxis</span><span class="sxs-lookup"><span data-stu-id="bed5d-115">seriesAxis</span></span>|[<span data-ttu-id="bed5d-116">WorkbookChartAxis</span><span class="sxs-lookup"><span data-stu-id="bed5d-116">WorkbookChartAxis</span></span>](chartaxis.md)|<span data-ttu-id="bed5d-p102">Representa el eje de series de un gráfico tridimensional. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bed5d-p102">Represents the series axis of a 3-dimensional chart. Read-only.</span></span>|
|<span data-ttu-id="bed5d-119">valueAxis</span><span class="sxs-lookup"><span data-stu-id="bed5d-119">valueAxis</span></span>|[<span data-ttu-id="bed5d-120">WorkbookChartAxis</span><span class="sxs-lookup"><span data-stu-id="bed5d-120">WorkbookChartAxis</span></span>](chartaxis.md)|<span data-ttu-id="bed5d-p103">Representa el eje de valores de un eje. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bed5d-p103">Represents the value axis in an axis. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="bed5d-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bed5d-123">JSON representation</span></span>

<span data-ttu-id="bed5d-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bed5d-124">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartAxes"
}-->

```json
{
  "categoryAxis": {"@odata.type": "microsoft.graph.workbookChartAxis"},
  "seriesAxis": {"@odata.type": "microsoft.graph.workbookChartAxis"},
  "valueAxis": {"@odata.type": "microsoft.graph.workbookChartAxis"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxes resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->