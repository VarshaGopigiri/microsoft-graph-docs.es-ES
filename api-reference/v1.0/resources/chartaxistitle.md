# <a name="chartaxistitle-resource-type"></a><span data-ttu-id="2f275-101">Tipo de recurso ChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="2f275-101">ChartAxisTitle resource type</span></span>

<span data-ttu-id="2f275-102">Representa el título del eje de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="2f275-102">Represents the title of a chart axis.</span></span>


## <a name="methods"></a><span data-ttu-id="2f275-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="2f275-103">Methods</span></span>

| <span data-ttu-id="2f275-104">Método</span><span class="sxs-lookup"><span data-stu-id="2f275-104">Method</span></span>           | <span data-ttu-id="2f275-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f275-105">Return Type</span></span>    |<span data-ttu-id="2f275-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f275-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="2f275-107">Obtener ChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="2f275-107">Get ChartAxisTitle</span></span>](../api/chartaxistitle_get.md) | [<span data-ttu-id="2f275-108">WorkbookChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="2f275-108">WorkbookChartAxisTitle</span></span>](chartaxistitle.md) |<span data-ttu-id="2f275-109">Lee las propiedades y relaciones del objeto chartAxisTitle.</span><span class="sxs-lookup"><span data-stu-id="2f275-109">Read properties and relationships of chartAxisTitle object.</span></span>|
|[<span data-ttu-id="2f275-110">Actualizar</span><span class="sxs-lookup"><span data-stu-id="2f275-110">Update</span></span>](../api/chartaxistitle_update.md) | [<span data-ttu-id="2f275-111">WorkbookChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="2f275-111">WorkbookChartAxisTitle</span></span>](chartaxistitle.md)    |<span data-ttu-id="2f275-112">Actualiza el objeto ChartAxisTitle.</span><span class="sxs-lookup"><span data-stu-id="2f275-112">Update ChartAxisTitle object.</span></span> |

## <a name="properties"></a><span data-ttu-id="2f275-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2f275-113">Properties</span></span>
| <span data-ttu-id="2f275-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2f275-114">Property</span></span>     | <span data-ttu-id="2f275-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f275-115">Type</span></span>   |<span data-ttu-id="2f275-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f275-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2f275-117">texto.</span><span class="sxs-lookup"><span data-stu-id="2f275-117">text</span></span>|<span data-ttu-id="2f275-118">cadena</span><span class="sxs-lookup"><span data-stu-id="2f275-118">string</span></span>|<span data-ttu-id="2f275-119">Representa el título del eje.</span><span class="sxs-lookup"><span data-stu-id="2f275-119">Represents the axis title.</span></span>|
|<span data-ttu-id="2f275-120">visible</span><span class="sxs-lookup"><span data-stu-id="2f275-120">visible</span></span>|<span data-ttu-id="2f275-121">booleano</span><span class="sxs-lookup"><span data-stu-id="2f275-121">boolean</span></span>|<span data-ttu-id="2f275-122">Valor booleano que especifica la visibilidad del título de un eje.</span><span class="sxs-lookup"><span data-stu-id="2f275-122">A boolean that specifies the visibility of an axis title.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2f275-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2f275-123">Relationships</span></span>
| <span data-ttu-id="2f275-124">Relación</span><span class="sxs-lookup"><span data-stu-id="2f275-124">Relationship</span></span> | <span data-ttu-id="2f275-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f275-125">Type</span></span>   |<span data-ttu-id="2f275-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f275-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2f275-127">format</span><span class="sxs-lookup"><span data-stu-id="2f275-127">format</span></span>|[<span data-ttu-id="2f275-128">WorkbookChartAxisTitleFormat</span><span class="sxs-lookup"><span data-stu-id="2f275-128">WorkbookChartAxisTitleFormat</span></span>](chartaxistitleformat.md)|<span data-ttu-id="2f275-p101">Representa el formato del título del eje del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2f275-p101">Represents the formatting of chart axis title. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2f275-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2f275-131">JSON representation</span></span>

<span data-ttu-id="2f275-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2f275-132">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartAxisTitle"
}-->

```json
{
  "text": "string",
  "visible": true,
  "format": {"@odata.type":"microsoft.graph.workbookChartAxisTitleFormat"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxisTitle resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->