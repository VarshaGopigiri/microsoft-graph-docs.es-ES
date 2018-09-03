# <a name="chartaxis-resource-type"></a><span data-ttu-id="d791c-101">Tipo de recurso ChartAxis</span><span class="sxs-lookup"><span data-stu-id="d791c-101">ChartAxis resource type</span></span>

<span data-ttu-id="d791c-102">Representa un solo eje de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="d791c-102">Represents a single axis in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="d791c-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="d791c-103">Methods</span></span>

| <span data-ttu-id="d791c-104">Método</span><span class="sxs-lookup"><span data-stu-id="d791c-104">Method</span></span>           | <span data-ttu-id="d791c-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d791c-105">Return Type</span></span>    |<span data-ttu-id="d791c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d791c-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d791c-107">Get ChartAxis</span><span class="sxs-lookup"><span data-stu-id="d791c-107">Get ChartAxis</span></span>](../api/chartaxis_get.md) | [<span data-ttu-id="d791c-108">WorkbookChartAxis</span><span class="sxs-lookup"><span data-stu-id="d791c-108">WorkbookChartAxis</span></span>](chartaxis.md) |<span data-ttu-id="d791c-109">Lee las propiedades y relaciones del objeto chartAxis.</span><span class="sxs-lookup"><span data-stu-id="d791c-109">Read properties and relationships of chartAxis object.</span></span>|
|[<span data-ttu-id="d791c-110">Update</span><span class="sxs-lookup"><span data-stu-id="d791c-110">Update</span></span>](../api/chartaxis_update.md) | [<span data-ttu-id="d791c-111">WorkbookChartAxis</span><span class="sxs-lookup"><span data-stu-id="d791c-111">WorkbookChartAxis</span></span>](chartaxis.md)   |<span data-ttu-id="d791c-112">Actualiza el objeto ChartAxis.</span><span class="sxs-lookup"><span data-stu-id="d791c-112">Update ChartAxis object.</span></span> |

## <a name="properties"></a><span data-ttu-id="d791c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d791c-113">Properties</span></span>
| <span data-ttu-id="d791c-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d791c-114">Property</span></span>     | <span data-ttu-id="d791c-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="d791c-115">Type</span></span>   |<span data-ttu-id="d791c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d791c-116">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="d791c-117">id</span><span class="sxs-lookup"><span data-stu-id="d791c-117">id</span></span>       |<span data-ttu-id="d791c-118">cadena</span><span class="sxs-lookup"><span data-stu-id="d791c-118">string</span></span>   | <span data-ttu-id="d791c-119">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="d791c-119">Unique Identifier</span></span> <span data-ttu-id="d791c-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d791c-120">Read-only.</span></span>|
|<span data-ttu-id="d791c-121">majorUnit</span><span class="sxs-lookup"><span data-stu-id="d791c-121">majorUnit</span></span>|<span data-ttu-id="d791c-122">Json</span><span class="sxs-lookup"><span data-stu-id="d791c-122">Json</span></span>|<span data-ttu-id="d791c-p102">Representa el intervalo entre dos marcas de graduación principales. Puede establecerse en un valor numérico o en una cadena vacía.  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="d791c-p102">Represents the interval between two major tick marks. Can be set to a numeric value or an empty string.  The returned value is always a number.</span></span>|
|<span data-ttu-id="d791c-126">maximum</span><span class="sxs-lookup"><span data-stu-id="d791c-126">maximum</span></span>|<span data-ttu-id="d791c-127">Json</span><span class="sxs-lookup"><span data-stu-id="d791c-127">Json</span></span>|<span data-ttu-id="d791c-p103">Representa el valor máximo del eje de valores.  Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos).  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="d791c-p103">Represents the maximum value on the value axis.  Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="d791c-131">minimum</span><span class="sxs-lookup"><span data-stu-id="d791c-131">minimum</span></span>|<span data-ttu-id="d791c-132">Json</span><span class="sxs-lookup"><span data-stu-id="d791c-132">Json</span></span>|<span data-ttu-id="d791c-p104">Representa el valor mínimo del eje de valores. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="d791c-p104">Represents the minimum value on the value axis. Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="d791c-136">minorUnit</span><span class="sxs-lookup"><span data-stu-id="d791c-136">minorUnit</span></span>|<span data-ttu-id="d791c-137">Json</span><span class="sxs-lookup"><span data-stu-id="d791c-137">Json</span></span>|<span data-ttu-id="d791c-p105">Representa el rango entre dos marcas de graduación secundarias. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="d791c-p105">Represents the interval between two minor tick marks. "Can be set to a numeric value or an empty string (for automatic axis values). The returned value is always a number.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d791c-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d791c-141">Relationships</span></span>
| <span data-ttu-id="d791c-142">Relación</span><span class="sxs-lookup"><span data-stu-id="d791c-142">Relationship</span></span> | <span data-ttu-id="d791c-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="d791c-143">Type</span></span>   |<span data-ttu-id="d791c-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="d791c-144">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d791c-145">format</span><span class="sxs-lookup"><span data-stu-id="d791c-145">format</span></span>|[<span data-ttu-id="d791c-146">WorkbookChartAxisFormat</span><span class="sxs-lookup"><span data-stu-id="d791c-146">WorkbookChartAxisFormat</span></span>](chartaxisformat.md)|<span data-ttu-id="d791c-p106">Representa el formato de un objeto de gráfico, que incluye el formato de línea y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d791c-p106">Represents the formatting of a chart object, which includes line and font formatting. Read-only.</span></span>|
|<span data-ttu-id="d791c-149">majorGridlines</span><span class="sxs-lookup"><span data-stu-id="d791c-149">majorGridlines</span></span>|[<span data-ttu-id="d791c-150">WorkbookChartGridlines</span><span class="sxs-lookup"><span data-stu-id="d791c-150">WorkbookChartGridlines</span></span>](chartgridlines.md)|<span data-ttu-id="d791c-p107">Devuelve un objeto de línea de cuadrícula que representa las líneas de cuadrícula principales del eje especificado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d791c-p107">Returns a gridlines object that represents the major gridlines for the specified axis. Read-only.</span></span>|
|<span data-ttu-id="d791c-153">minorGridlines</span><span class="sxs-lookup"><span data-stu-id="d791c-153">minorGridlines</span></span>|[<span data-ttu-id="d791c-154">WorkbookChartGridlines</span><span class="sxs-lookup"><span data-stu-id="d791c-154">WorkbookChartGridlines</span></span>](chartgridlines.md)|<span data-ttu-id="d791c-p108">Devuelve un objeto de línea de cuadrícula que representa las líneas de cuadrícula secundarias del eje especificado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d791c-p108">Returns a Gridlines object that represents the minor gridlines for the specified axis. Read-only.</span></span>|
|<span data-ttu-id="d791c-157">title</span><span class="sxs-lookup"><span data-stu-id="d791c-157">title</span></span>|[<span data-ttu-id="d791c-158">WorkbookChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="d791c-158">WorkbookChartAxisTitle</span></span>](chartaxistitle.md)|<span data-ttu-id="d791c-p109">Representa el título del eje. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d791c-p109">Represents the axis title. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d791c-161">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d791c-161">JSON representation</span></span>

<span data-ttu-id="d791c-162">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d791c-162">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartAxis"
}-->

```json
{
  "id": "string",
  "majorUnit": "string",
  "maximum": "string",
  "minimum": "string",
  "minorUnit": "string",
   "format": {"@odata.type": "microsoft.graph.workbookChartAxisFormat"},
  "majorGridlines": {"@odata.type": "microsoft.graph.workbookChartGridlines"},
  "minorGridlines": {"@odata.type": "microsoft.graph.workbookChartGridlines"},
  "title": {"@odata.type": "microsoft.graph.workbookChartAxisTitle"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxis resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->