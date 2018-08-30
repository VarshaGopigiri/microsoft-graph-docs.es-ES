# <a name="chartlineformat-resource-type"></a><span data-ttu-id="26838-101">Tipo de recurso ChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="26838-101">ChartLineFormat resource type</span></span>

<span data-ttu-id="26838-102">Encapsula las opciones de formato para los elementos de línea.</span><span class="sxs-lookup"><span data-stu-id="26838-102">Enapsulates the formatting options for line elements.</span></span>


## <a name="methods"></a><span data-ttu-id="26838-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="26838-103">Methods</span></span>

| <span data-ttu-id="26838-104">Método</span><span class="sxs-lookup"><span data-stu-id="26838-104">Method</span></span>           | <span data-ttu-id="26838-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26838-105">Return Type</span></span>    |<span data-ttu-id="26838-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="26838-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="26838-107">Get ChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="26838-107">Get ChartLineFormat</span></span>](../api/chartlineformat_get.md) | [<span data-ttu-id="26838-108">WorkbookChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="26838-108">WorkbookChartLineFormat</span></span>](chartlineformat.md) |<span data-ttu-id="26838-109">Lee las propiedades y relaciones del objeto chartLineFormat.</span><span class="sxs-lookup"><span data-stu-id="26838-109">Read properties and relationships of chartLineFormat object.</span></span>|
|[<span data-ttu-id="26838-110">Update</span><span class="sxs-lookup"><span data-stu-id="26838-110">Update</span></span>](../api/chartlineformat_update.md) | [<span data-ttu-id="26838-111">WorkbookChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="26838-111">WorkbookChartLineFormat</span></span>](chartlineformat.md) |<span data-ttu-id="26838-112">Actualiza el objeto ChartLineFormat.</span><span class="sxs-lookup"><span data-stu-id="26838-112">Update ChartLineFormat object.</span></span> |
|[<span data-ttu-id="26838-113">Clear</span><span class="sxs-lookup"><span data-stu-id="26838-113">Clear</span></span>](../api/chartlineformat_clear.md)|<span data-ttu-id="26838-114">Ninguno</span><span class="sxs-lookup"><span data-stu-id="26838-114">None</span></span>|<span data-ttu-id="26838-115">Borra el formato de línea de un elemento de gráfico.</span><span class="sxs-lookup"><span data-stu-id="26838-115">Clear the line format of a chart element.</span></span>|

## <a name="properties"></a><span data-ttu-id="26838-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26838-116">Properties</span></span>
| <span data-ttu-id="26838-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26838-117">Property</span></span>     | <span data-ttu-id="26838-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="26838-118">Type</span></span>   |<span data-ttu-id="26838-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="26838-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="26838-120">color</span><span class="sxs-lookup"><span data-stu-id="26838-120">color</span></span>|<span data-ttu-id="26838-121">cadena</span><span class="sxs-lookup"><span data-stu-id="26838-121">string</span></span>|<span data-ttu-id="26838-122">Código de color HTML que representa el color de las líneas del gráfico.</span><span class="sxs-lookup"><span data-stu-id="26838-122">HTML color code representing the color of lines in the chart.</span></span>|

## <a name="relationships"></a><span data-ttu-id="26838-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="26838-123">Relationships</span></span>
<span data-ttu-id="26838-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="26838-124">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="26838-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="26838-125">JSON representation</span></span>

<span data-ttu-id="26838-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="26838-126">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartLineFormat"
}-->

```json
{
  "color": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartLineFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->