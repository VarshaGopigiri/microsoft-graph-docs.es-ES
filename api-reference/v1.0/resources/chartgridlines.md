# <a name="chartgridlines-resource-type"></a><span data-ttu-id="77933-101">Tipo de recurso ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="77933-101">ChartGridlines resource type</span></span>

<span data-ttu-id="77933-102">Representa las líneas de cuadrícula principales o secundarias del eje de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="77933-102">Represents major or minor gridlines on a chart axis.</span></span>


## <a name="methods"></a><span data-ttu-id="77933-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="77933-103">Methods</span></span>

| <span data-ttu-id="77933-104">Método</span><span class="sxs-lookup"><span data-stu-id="77933-104">Method</span></span>           | <span data-ttu-id="77933-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77933-105">Return Type</span></span>    |<span data-ttu-id="77933-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="77933-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="77933-107">Get ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="77933-107">Get ChartGridlines</span></span>](../api/chartgridlines_get.md) | [<span data-ttu-id="77933-108">WorkbookChartGridlines</span><span class="sxs-lookup"><span data-stu-id="77933-108">WorkbookChartGridlines</span></span>](chartgridlines.md) |<span data-ttu-id="77933-109">Lee las propiedades y relaciones del objeto chartGridlines.</span><span class="sxs-lookup"><span data-stu-id="77933-109">Read properties and relationships of chartGridlines object.</span></span>|
|[<span data-ttu-id="77933-110">Actualizar</span><span class="sxs-lookup"><span data-stu-id="77933-110">Update</span></span>](../api/chartgridlines_update.md) | [<span data-ttu-id="77933-111">WorkbookChartGridlines</span><span class="sxs-lookup"><span data-stu-id="77933-111">WorkbookChartGridlines</span></span>](chartgridlines.md)    |<span data-ttu-id="77933-112">Actualiza el objeto ChartGridlines.</span><span class="sxs-lookup"><span data-stu-id="77933-112">Update ChartGridlines object.</span></span> |

## <a name="properties"></a><span data-ttu-id="77933-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="77933-113">Properties</span></span>
| <span data-ttu-id="77933-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="77933-114">Property</span></span>     | <span data-ttu-id="77933-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="77933-115">Type</span></span>   |<span data-ttu-id="77933-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="77933-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="77933-117">visible</span><span class="sxs-lookup"><span data-stu-id="77933-117">visible</span></span>|<span data-ttu-id="77933-118">booleano</span><span class="sxs-lookup"><span data-stu-id="77933-118">boolean</span></span>|<span data-ttu-id="77933-119">Valor booleano que representa si las líneas de cuadrícula del eje están visibles o no.</span><span class="sxs-lookup"><span data-stu-id="77933-119">Boolean value representing if the axis gridlines are visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="77933-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="77933-120">Relationships</span></span>
| <span data-ttu-id="77933-121">Relación</span><span class="sxs-lookup"><span data-stu-id="77933-121">Relationship</span></span> | <span data-ttu-id="77933-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="77933-122">Type</span></span>   |<span data-ttu-id="77933-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="77933-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="77933-124">format</span><span class="sxs-lookup"><span data-stu-id="77933-124">format</span></span>|[<span data-ttu-id="77933-125">WorkbookChartGridlinesFormat</span><span class="sxs-lookup"><span data-stu-id="77933-125">WorkbookChartGridlinesFormat</span></span>](chartgridlinesformat.md)|<span data-ttu-id="77933-p101">Representa el formato de las líneas de cuadrícula del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="77933-p101">Represents the formatting of chart gridlines. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="77933-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="77933-128">JSON representation</span></span>

<span data-ttu-id="77933-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="77933-129">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartGridlines"
}-->

```json
{
  "visible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartGridlines resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->