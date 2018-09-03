# <a name="charttitle-resource-type"></a><span data-ttu-id="04209-101">Tipo de recurso ChartTitle</span><span class="sxs-lookup"><span data-stu-id="04209-101">ChartTitle resource type</span></span>

<span data-ttu-id="04209-102">Representa un objeto de título de gráfico de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="04209-102">Represents a chart title object of a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="04209-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="04209-103">Methods</span></span>

| <span data-ttu-id="04209-104">Método</span><span class="sxs-lookup"><span data-stu-id="04209-104">Method</span></span>           | <span data-ttu-id="04209-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04209-105">Return Type</span></span>    |<span data-ttu-id="04209-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="04209-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="04209-107">Get ChartTitle</span><span class="sxs-lookup"><span data-stu-id="04209-107">Get ChartTitle</span></span>](../api/charttitle_get.md) | [<span data-ttu-id="04209-108">WorkbookChartTitle</span><span class="sxs-lookup"><span data-stu-id="04209-108">WorkbookChartTitle</span></span>](charttitle.md) |<span data-ttu-id="04209-109">Lee las propiedades y relaciones del objeto chartTitle.</span><span class="sxs-lookup"><span data-stu-id="04209-109">Read properties and relationships of chartTitle object.</span></span>|
|[<span data-ttu-id="04209-110">Update</span><span class="sxs-lookup"><span data-stu-id="04209-110">Update</span></span>](../api/charttitle_update.md) | [<span data-ttu-id="04209-111">WorkbookChartTitle</span><span class="sxs-lookup"><span data-stu-id="04209-111">WorkbookChartTitle</span></span>](charttitle.md)    |<span data-ttu-id="04209-112">Actualiza el objeto ChartTitle.</span><span class="sxs-lookup"><span data-stu-id="04209-112">Update ChartTitle object.</span></span> |

## <a name="properties"></a><span data-ttu-id="04209-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="04209-113">Properties</span></span>
| <span data-ttu-id="04209-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04209-114">Property</span></span>     | <span data-ttu-id="04209-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="04209-115">Type</span></span>   |<span data-ttu-id="04209-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="04209-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="04209-117">overlay</span><span class="sxs-lookup"><span data-stu-id="04209-117">overlay</span></span>|<span data-ttu-id="04209-118">booleano</span><span class="sxs-lookup"><span data-stu-id="04209-118">boolean</span></span>|<span data-ttu-id="04209-119">Valor booleano que representa si el título del gráfico se superpondrá al gráfico o no.</span><span class="sxs-lookup"><span data-stu-id="04209-119">Boolean value representing if the chart title will overlay the chart or not.</span></span>|
|<span data-ttu-id="04209-120">text</span><span class="sxs-lookup"><span data-stu-id="04209-120">text</span></span>|<span data-ttu-id="04209-121">cadena</span><span class="sxs-lookup"><span data-stu-id="04209-121">string</span></span>|<span data-ttu-id="04209-122">Representa el texto del título de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="04209-122">Represents the title text of a chart.</span></span>|
|<span data-ttu-id="04209-123">visible</span><span class="sxs-lookup"><span data-stu-id="04209-123">visible</span></span>|<span data-ttu-id="04209-124">booleano</span><span class="sxs-lookup"><span data-stu-id="04209-124">boolean</span></span>|<span data-ttu-id="04209-125">Valor booleano que representa la visibilidad de un objeto de título del gráfico.</span><span class="sxs-lookup"><span data-stu-id="04209-125">A boolean value the represents the visibility of a chart title object.</span></span>|

## <a name="relationships"></a><span data-ttu-id="04209-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="04209-126">Relationships</span></span>
| <span data-ttu-id="04209-127">Relación</span><span class="sxs-lookup"><span data-stu-id="04209-127">Relationship</span></span> | <span data-ttu-id="04209-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="04209-128">Type</span></span>   |<span data-ttu-id="04209-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="04209-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="04209-130">format</span><span class="sxs-lookup"><span data-stu-id="04209-130">format</span></span>|[<span data-ttu-id="04209-131">WorkbookChartTitleFormat</span><span class="sxs-lookup"><span data-stu-id="04209-131">WorkbookChartTitleFormat</span></span>](charttitleformat.md)|<span data-ttu-id="04209-p101">Representa el formato de un título del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="04209-p101">Represents the formatting of a chart title, which includes fill and font formatting. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="04209-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="04209-134">JSON representation</span></span>

<span data-ttu-id="04209-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="04209-135">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartTitle"
}-->

```json
{
  "overlay": true,
  "text": "string",
  "visible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartTitle resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->