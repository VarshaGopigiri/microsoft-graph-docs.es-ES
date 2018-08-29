# <a name="chartlegend-resource-type"></a><span data-ttu-id="aa974-101">Tipo de recurso ChartLegend</span><span class="sxs-lookup"><span data-stu-id="aa974-101">ChartLegend resource type</span></span>

<span data-ttu-id="aa974-102">Representa la leyenda de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="aa974-102">Represents the legend in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="aa974-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="aa974-103">Methods</span></span>

| <span data-ttu-id="aa974-104">Método</span><span class="sxs-lookup"><span data-stu-id="aa974-104">Method</span></span>           | <span data-ttu-id="aa974-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa974-105">Return Type</span></span>    |<span data-ttu-id="aa974-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa974-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="aa974-107">Obtener ChartLegend</span><span class="sxs-lookup"><span data-stu-id="aa974-107">Get ChartLegend</span></span>](../api/chartlegend_get.md) | [<span data-ttu-id="aa974-108">WorkbookChartLegend</span><span class="sxs-lookup"><span data-stu-id="aa974-108">WorkbookChartLegend</span></span>](chartlegend.md) |<span data-ttu-id="aa974-109">Lee las propiedades y relaciones del objeto chartLegend.</span><span class="sxs-lookup"><span data-stu-id="aa974-109">Read properties and relationships of chartLegend object.</span></span>|
|[<span data-ttu-id="aa974-110">Update</span><span class="sxs-lookup"><span data-stu-id="aa974-110">Update</span></span>](../api/chartlegend_update.md) | [<span data-ttu-id="aa974-111">WorkbookChartLegend</span><span class="sxs-lookup"><span data-stu-id="aa974-111">WorkbookChartLegend</span></span>](chartlegend.md) |<span data-ttu-id="aa974-112">Actualiza el objeto ChartLegend.</span><span class="sxs-lookup"><span data-stu-id="aa974-112">Update ChartLegend object.</span></span> |

## <a name="properties"></a><span data-ttu-id="aa974-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa974-113">Properties</span></span>
| <span data-ttu-id="aa974-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aa974-114">Property</span></span>     | <span data-ttu-id="aa974-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa974-115">Type</span></span>   |<span data-ttu-id="aa974-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa974-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="aa974-117">overlay</span><span class="sxs-lookup"><span data-stu-id="aa974-117">overlay</span></span>|<span data-ttu-id="aa974-118">booleano</span><span class="sxs-lookup"><span data-stu-id="aa974-118">boolean</span></span>|<span data-ttu-id="aa974-119">Valor booleano que indica si la leyenda del gráfico debe superponerse al cuerpo principal del gráfico.</span><span class="sxs-lookup"><span data-stu-id="aa974-119">Boolean value for whether the chart legend should overlap with the main body of the chart.</span></span>|
|<span data-ttu-id="aa974-120">position</span><span class="sxs-lookup"><span data-stu-id="aa974-120">position</span></span>|<span data-ttu-id="aa974-121">cadena</span><span class="sxs-lookup"><span data-stu-id="aa974-121">string</span></span>|<span data-ttu-id="aa974-122">Representa la posición de la leyenda del gráfico.</span><span class="sxs-lookup"><span data-stu-id="aa974-122">Represents the position of the legend on the chart. Possible values are: , , , , , .</span></span> <span data-ttu-id="aa974-123">Los valores posibles son `Top`, `Bottom`, `Left`, `Right`, `Corner` y `Custom`.</span><span class="sxs-lookup"><span data-stu-id="aa974-123">The possible values are `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`, , , , , , or .</span></span>|
|<span data-ttu-id="aa974-124">visible</span><span class="sxs-lookup"><span data-stu-id="aa974-124">visible</span></span>|<span data-ttu-id="aa974-125">booleano</span><span class="sxs-lookup"><span data-stu-id="aa974-125">boolean</span></span>|<span data-ttu-id="aa974-126">Valor booleano que representa la visibilidad de un objeto ChartLegend.</span><span class="sxs-lookup"><span data-stu-id="aa974-126">A boolean value the represents the visibility of a ChartLegend object.</span></span>|

## <a name="relationships"></a><span data-ttu-id="aa974-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="aa974-127">Relationships</span></span>
| <span data-ttu-id="aa974-128">Relación</span><span class="sxs-lookup"><span data-stu-id="aa974-128">Relationship</span></span> | <span data-ttu-id="aa974-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa974-129">Type</span></span>   |<span data-ttu-id="aa974-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa974-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="aa974-131">format</span><span class="sxs-lookup"><span data-stu-id="aa974-131">format</span></span>|[<span data-ttu-id="aa974-132">WorkbookChartLegendFormat</span><span class="sxs-lookup"><span data-stu-id="aa974-132">WorkbookChartLegendFormat</span></span>](chartlegendformat.md)|<span data-ttu-id="aa974-p102">Representa el formato de una leyenda del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="aa974-p102">Represents the formatting of a chart legend, which includes fill and font formatting. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="aa974-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="aa974-135">JSON representation</span></span>

<span data-ttu-id="aa974-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="aa974-136">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartLegend"
}-->

```json
{
  "overlay": true,
  "position": "string",
  "visible": true,
  "format": {"@odata.type":"microsoft.graph.workbookChartLegendFormat"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartLegend resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->