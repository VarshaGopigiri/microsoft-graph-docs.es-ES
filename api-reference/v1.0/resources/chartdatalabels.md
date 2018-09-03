# <a name="chartdatalabels-resource-type"></a><span data-ttu-id="9b0b2-101">Tipo de recurso ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="9b0b2-101">ChartDataLabels resource type</span></span>

<span data-ttu-id="9b0b2-102">Representa una colección de todas las etiquetas de datos en un punto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-102">Represents a collection of all the data labels on a chart point.</span></span>


## <a name="methods"></a><span data-ttu-id="9b0b2-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b0b2-103">Methods</span></span>

| <span data-ttu-id="9b0b2-104">Método</span><span class="sxs-lookup"><span data-stu-id="9b0b2-104">Method</span></span>           | <span data-ttu-id="9b0b2-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b0b2-105">Return Type</span></span>    |<span data-ttu-id="9b0b2-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b0b2-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9b0b2-107">Obtener ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="9b0b2-107">Get ChartDataLabels</span></span>](../api/chartdatalabels_get.md) | [<span data-ttu-id="9b0b2-108">WorkbookChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="9b0b2-108">WorkbookChartDataLabels</span></span>](chartdatalabels.md) |<span data-ttu-id="9b0b2-109">Lee las propiedades y relaciones del objeto chartDataLabels.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-109">Read properties and relationships of chartDataLabels object.</span></span>|
|[<span data-ttu-id="9b0b2-110">Update</span><span class="sxs-lookup"><span data-stu-id="9b0b2-110">Update</span></span>](../api/chartdatalabels_update.md) | [<span data-ttu-id="9b0b2-111">WorkbookChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="9b0b2-111">WorkbookChartDataLabels</span></span>](chartdatalabels.md) |<span data-ttu-id="9b0b2-112">Actualiza el objeto ChartDataLabels.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-112">Update ChartDataLabels object.</span></span> |

## <a name="properties"></a><span data-ttu-id="9b0b2-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b0b2-113">Properties</span></span>
| <span data-ttu-id="9b0b2-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9b0b2-114">Property</span></span>     | <span data-ttu-id="9b0b2-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b0b2-115">Type</span></span>   |<span data-ttu-id="9b0b2-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b0b2-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9b0b2-117">position</span><span class="sxs-lookup"><span data-stu-id="9b0b2-117">position</span></span>|<span data-ttu-id="9b0b2-118">cadena</span><span class="sxs-lookup"><span data-stu-id="9b0b2-118">string</span></span>|<span data-ttu-id="9b0b2-119">Valor de DataLabelPosition que representa la posición de la etiqueta de datos.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-119">DataLabelPosition value that represents the position of the data label. Possible values are: , , , , , , , , , , .</span></span> <span data-ttu-id="9b0b2-120">Los valores posibles son: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit` y `Callout`.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-120">The possible values are `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`, or .</span></span>|
|<span data-ttu-id="9b0b2-121">separator</span><span class="sxs-lookup"><span data-stu-id="9b0b2-121">separator</span></span>|<span data-ttu-id="9b0b2-122">cadena</span><span class="sxs-lookup"><span data-stu-id="9b0b2-122">string</span></span>|<span data-ttu-id="9b0b2-123">Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-123">String representing the separator used for the data labels on a chart.</span></span>|
|<span data-ttu-id="9b0b2-124">showBubbleSize</span><span class="sxs-lookup"><span data-stu-id="9b0b2-124">showBubbleSize</span></span>|<span data-ttu-id="9b0b2-125">booleano</span><span class="sxs-lookup"><span data-stu-id="9b0b2-125">boolean</span></span>|<span data-ttu-id="9b0b2-126">Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-126">Boolean value representing if the data label bubble size is visible or not.</span></span>|
|<span data-ttu-id="9b0b2-127">showCategoryName</span><span class="sxs-lookup"><span data-stu-id="9b0b2-127">showCategoryName</span></span>|<span data-ttu-id="9b0b2-128">booleano</span><span class="sxs-lookup"><span data-stu-id="9b0b2-128">boolean</span></span>|<span data-ttu-id="9b0b2-129">Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-129">Boolean value representing if the data label category name is visible or not.</span></span>|
|<span data-ttu-id="9b0b2-130">showLegendKey</span><span class="sxs-lookup"><span data-stu-id="9b0b2-130">showLegendKey</span></span>|<span data-ttu-id="9b0b2-131">booleano</span><span class="sxs-lookup"><span data-stu-id="9b0b2-131">boolean</span></span>|<span data-ttu-id="9b0b2-132">Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-132">Boolean value representing if the data label legend key is visible or not.</span></span>|
|<span data-ttu-id="9b0b2-133">showPercentage</span><span class="sxs-lookup"><span data-stu-id="9b0b2-133">showPercentage</span></span>|<span data-ttu-id="9b0b2-134">booleano</span><span class="sxs-lookup"><span data-stu-id="9b0b2-134">boolean</span></span>|<span data-ttu-id="9b0b2-135">Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-135">Boolean value representing if the data label percentage is visible or not.</span></span>|
|<span data-ttu-id="9b0b2-136">showSeriesName</span><span class="sxs-lookup"><span data-stu-id="9b0b2-136">showSeriesName</span></span>|<span data-ttu-id="9b0b2-137">booleano</span><span class="sxs-lookup"><span data-stu-id="9b0b2-137">boolean</span></span>|<span data-ttu-id="9b0b2-138">Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-138">Boolean value representing if the data label series name is visible or not.</span></span>|
|<span data-ttu-id="9b0b2-139">showValue</span><span class="sxs-lookup"><span data-stu-id="9b0b2-139">showValue</span></span>|<span data-ttu-id="9b0b2-140">booleano</span><span class="sxs-lookup"><span data-stu-id="9b0b2-140">boolean</span></span>|<span data-ttu-id="9b0b2-141">Valor booleano que representa si el valor de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-141">Boolean value representing if the data label value is visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9b0b2-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9b0b2-142">Relationships</span></span>
| <span data-ttu-id="9b0b2-143">Relación</span><span class="sxs-lookup"><span data-stu-id="9b0b2-143">Relationship</span></span> | <span data-ttu-id="9b0b2-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b0b2-144">Type</span></span>   |<span data-ttu-id="9b0b2-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b0b2-145">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9b0b2-146">format</span><span class="sxs-lookup"><span data-stu-id="9b0b2-146">format</span></span>|[<span data-ttu-id="9b0b2-147">WorkbookChartDataLabelFormat</span><span class="sxs-lookup"><span data-stu-id="9b0b2-147">WorkbookChartDataLabelFormat</span></span>](chartdatalabelformat.md)|<span data-ttu-id="9b0b2-p102">Representa el formato de las etiquetas de datos del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-p102">Represents the format of chart data labels, which includes fill and font formatting. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9b0b2-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9b0b2-150">JSON representation</span></span>

<span data-ttu-id="9b0b2-151">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9b0b2-151">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartDataLabels"
}-->

```json
{
  "position": "string",
  "separator": "string",
  "showBubbleSize": true,
  "showCategoryName": true,
  "showLegendKey": true,
  "showPercentage": true,
  "showSeriesName": true,
  "showValue": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartDataLabels resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->