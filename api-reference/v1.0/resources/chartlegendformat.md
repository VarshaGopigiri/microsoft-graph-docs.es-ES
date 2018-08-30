# <a name="chartlegendformat-resource-type"></a><span data-ttu-id="11cf4-101">Tipo de recurso ChartLegendFormat</span><span class="sxs-lookup"><span data-stu-id="11cf4-101">ChartLegendFormat resource type</span></span>

<span data-ttu-id="11cf4-102">Encapsula las propiedades de formato de una leyenda del gráfico.</span><span class="sxs-lookup"><span data-stu-id="11cf4-102">Encapsulates the format properties of a chart legend.</span></span>


## <a name="methods"></a><span data-ttu-id="11cf4-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="11cf4-103">Methods</span></span>
<span data-ttu-id="11cf4-104">Ninguno</span><span class="sxs-lookup"><span data-stu-id="11cf4-104">None</span></span>

## <a name="properties"></a><span data-ttu-id="11cf4-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11cf4-105">Properties</span></span>
<span data-ttu-id="11cf4-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="11cf4-106">None</span></span>

## <a name="relationships"></a><span data-ttu-id="11cf4-107">Relaciones</span><span class="sxs-lookup"><span data-stu-id="11cf4-107">Relationships</span></span>
| <span data-ttu-id="11cf4-108">Relación</span><span class="sxs-lookup"><span data-stu-id="11cf4-108">Relationship</span></span> | <span data-ttu-id="11cf4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="11cf4-109">Type</span></span>   |<span data-ttu-id="11cf4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="11cf4-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="11cf4-111">fill</span><span class="sxs-lookup"><span data-stu-id="11cf4-111">fill</span></span>|[<span data-ttu-id="11cf4-112">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="11cf4-112">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="11cf4-p101">Representa el formato de relleno de un objeto, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="11cf4-p101">Represents the fill format of an object, which includes background formating information. Read-only.</span></span>|
|<span data-ttu-id="11cf4-115">font</span><span class="sxs-lookup"><span data-stu-id="11cf4-115">font</span></span>|[<span data-ttu-id="11cf4-116">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="11cf4-116">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="11cf4-p102">Representa los atributos de fuente (por ejemplo, nombre de fuente, tamaño de fuente, color, etc.) de una leyenda del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="11cf4-p102">Represents the font attributes such as font name, font size, color, etc. of a chart legend. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="11cf4-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="11cf4-119">JSON representation</span></span>

<span data-ttu-id="11cf4-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="11cf4-120">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartLegendFormat"
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
  "description": "ChartLegendFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->