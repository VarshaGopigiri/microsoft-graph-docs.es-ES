# <a name="chartaxistitleformat-resource-type"></a><span data-ttu-id="313fd-101">Tipo de recurso ChartAxisTitleFormat</span><span class="sxs-lookup"><span data-stu-id="313fd-101">ChartAxisTitleFormat resource type</span></span>

<span data-ttu-id="313fd-102">Representa el formato de título del eje del gráfico.</span><span class="sxs-lookup"><span data-stu-id="313fd-102">Represents the chart axis title formatting.</span></span>


## <a name="methods"></a><span data-ttu-id="313fd-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="313fd-103">Methods</span></span>
<span data-ttu-id="313fd-104">Ninguno</span><span class="sxs-lookup"><span data-stu-id="313fd-104">None</span></span>

## <a name="properties"></a><span data-ttu-id="313fd-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="313fd-105">Properties</span></span>
<span data-ttu-id="313fd-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="313fd-106">None</span></span>

## <a name="relationships"></a><span data-ttu-id="313fd-107">Relaciones</span><span class="sxs-lookup"><span data-stu-id="313fd-107">Relationships</span></span>
| <span data-ttu-id="313fd-108">Relación</span><span class="sxs-lookup"><span data-stu-id="313fd-108">Relationship</span></span> | <span data-ttu-id="313fd-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="313fd-109">Type</span></span>   |<span data-ttu-id="313fd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="313fd-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="313fd-111">font</span><span class="sxs-lookup"><span data-stu-id="313fd-111">font</span></span>|[<span data-ttu-id="313fd-112">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="313fd-112">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="313fd-p101">Representa los atributos de fuente (por ejemplo, nombre de fuente, tamaño de fuente, color, etc.) de un objeto de título del eje del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="313fd-p101">Represents the font attributes, such as font name, font size, color, etc. of chart axis title object. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="313fd-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="313fd-115">JSON representation</span></span>

<span data-ttu-id="313fd-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="313fd-116">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartAxisTitleFormat"
}-->

```json
{
  "font": {"@odata.type": "microsoft.graph.workbookChartFont"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxisTitleFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->