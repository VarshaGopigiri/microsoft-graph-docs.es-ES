# <a name="chartpointformat-resource-type"></a><span data-ttu-id="3f30b-101">Tipo de recurso ChartPointFormat</span><span class="sxs-lookup"><span data-stu-id="3f30b-101">ChartPointFormat resource type</span></span>

<span data-ttu-id="3f30b-102">Representa el objeto de formato para los puntos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="3f30b-102">Represents formatting object for chart points.</span></span>


## <a name="methods"></a><span data-ttu-id="3f30b-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f30b-103">Methods</span></span>
<span data-ttu-id="3f30b-104">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3f30b-104">None</span></span>

## <a name="properties"></a><span data-ttu-id="3f30b-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3f30b-105">Properties</span></span>
<span data-ttu-id="3f30b-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3f30b-106">None</span></span>

## <a name="relationships"></a><span data-ttu-id="3f30b-107">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3f30b-107">Relationships</span></span>
| <span data-ttu-id="3f30b-108">Relación</span><span class="sxs-lookup"><span data-stu-id="3f30b-108">Relationship</span></span> | <span data-ttu-id="3f30b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f30b-109">Type</span></span>   |<span data-ttu-id="3f30b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f30b-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3f30b-111">fill</span><span class="sxs-lookup"><span data-stu-id="3f30b-111">fill</span></span>|[<span data-ttu-id="3f30b-112">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="3f30b-112">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="3f30b-p101">Representa el formato de relleno de un gráfico, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3f30b-p101">Represents the fill format of a chart, which includes background formating information. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="3f30b-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3f30b-115">JSON representation</span></span>

<span data-ttu-id="3f30b-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3f30b-116">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartPointFormat"
}-->

```json
{
  "fill": {"@odata.type": "microsoft.graph.workbookChartFill"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartPointFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->