# <a name="charttitleformat-resource-type"></a><span data-ttu-id="e9cc3-101">Tipo de recurso ChartTitleFormat</span><span class="sxs-lookup"><span data-stu-id="e9cc3-101">ChartTitleFormat resource type</span></span>

<span data-ttu-id="e9cc3-102">Encapsula las propiedades de formato del título del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e9cc3-102">Encapsulates the format properties for the chart title.</span></span>


## <a name="methods"></a><span data-ttu-id="e9cc3-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="e9cc3-103">Methods</span></span>
<span data-ttu-id="e9cc3-104">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e9cc3-104">None</span></span>

## <a name="properties"></a><span data-ttu-id="e9cc3-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9cc3-105">Properties</span></span>
<span data-ttu-id="e9cc3-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e9cc3-106">None</span></span>

## <a name="relationships"></a><span data-ttu-id="e9cc3-107">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e9cc3-107">Relationships</span></span>
| <span data-ttu-id="e9cc3-108">Relación</span><span class="sxs-lookup"><span data-stu-id="e9cc3-108">Relationship</span></span> | <span data-ttu-id="e9cc3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9cc3-109">Type</span></span>   |<span data-ttu-id="e9cc3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9cc3-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e9cc3-111">fill</span><span class="sxs-lookup"><span data-stu-id="e9cc3-111">fill</span></span>|[<span data-ttu-id="e9cc3-112">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="e9cc3-112">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="e9cc3-p101">Representa el formato de relleno de un objeto, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e9cc3-p101">Represents the fill format of an object, which includes background formatting information. Read-only.</span></span>|
|<span data-ttu-id="e9cc3-115">font</span><span class="sxs-lookup"><span data-stu-id="e9cc3-115">font</span></span>|[<span data-ttu-id="e9cc3-116">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="e9cc3-116">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="e9cc3-p102">Representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) del objeto actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e9cc3-p102">Represents the font attributes (font name, font size, color, etc.) for the current object. Read-only.</span></span>|



## <a name="json-representation"></a><span data-ttu-id="e9cc3-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e9cc3-119">JSON representation</span></span>

<span data-ttu-id="e9cc3-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e9cc3-120">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartTitleFormat"
}-->

```json
{
  "fill": {"@odata.type": "microsoft.graph.workbookChartFill"},
  "font": {"@odata.type": "microsoft.graph.workbookChartFont"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAreaFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
