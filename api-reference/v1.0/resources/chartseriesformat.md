# <a name="chartseriesformat-resource-type"></a><span data-ttu-id="e4760-101">Tipo de recurso ChartSeriesFormat</span><span class="sxs-lookup"><span data-stu-id="e4760-101">ChartSeriesFormat resource type</span></span>

<span data-ttu-id="e4760-102">Encapsula las propiedades de formato de la serie del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e4760-102">encapsulates the format properties for the chart series</span></span>


## <a name="methods"></a><span data-ttu-id="e4760-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4760-103">Methods</span></span>
<span data-ttu-id="e4760-104">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e4760-104">None</span></span>

## <a name="properties"></a><span data-ttu-id="e4760-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4760-105">Properties</span></span>
<span data-ttu-id="e4760-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e4760-106">None</span></span>

## <a name="relationships"></a><span data-ttu-id="e4760-107">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e4760-107">Relationships</span></span>
| <span data-ttu-id="e4760-108">Relación</span><span class="sxs-lookup"><span data-stu-id="e4760-108">Relationship</span></span> | <span data-ttu-id="e4760-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4760-109">Type</span></span>   |<span data-ttu-id="e4760-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4760-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e4760-111">fill</span><span class="sxs-lookup"><span data-stu-id="e4760-111">fill</span></span>|[<span data-ttu-id="e4760-112">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="e4760-112">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="e4760-p101">Representa el formato de relleno de una serie del gráfico, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e4760-p101">Represents the fill format of a chart series, which includes background formating information. Read-only.</span></span>|
|<span data-ttu-id="e4760-115">line</span><span class="sxs-lookup"><span data-stu-id="e4760-115">line</span></span>|[<span data-ttu-id="e4760-116">WorkbookChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="e4760-116">WorkbookChartLineFormat</span></span>](chartlineformat.md)|<span data-ttu-id="e4760-p102">Representa el formato de línea. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e4760-p102">Represents line formatting. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="e4760-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e4760-119">JSON representation</span></span>

<span data-ttu-id="e4760-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e4760-120">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartSeriesFormat"
}-->

```json
{
  "fill": {"@odata.type": "microsoft.graph.workbookChartFill"},
  "line": {"@odata.type": "microsoft.graph.workbookChartLineFormat"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartSeriesFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->