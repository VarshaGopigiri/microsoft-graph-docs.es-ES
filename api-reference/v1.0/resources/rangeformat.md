# <a name="rangeformat-resource-type"></a><span data-ttu-id="87673-101">Tipo de recurso RangeFormat</span><span class="sxs-lookup"><span data-stu-id="87673-101">RangeFormat resource type</span></span>

<span data-ttu-id="87673-102">Objeto de formato que encapsula la fuente, el relleno, los bordes, la alineación y otras propiedades del rango.</span><span class="sxs-lookup"><span data-stu-id="87673-102">A format object encapsulating the range's font, fill, borders, alignment, and other properties.</span></span>


## <a name="methods"></a><span data-ttu-id="87673-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="87673-103">Methods</span></span>

| <span data-ttu-id="87673-104">Método</span><span class="sxs-lookup"><span data-stu-id="87673-104">Method</span></span>           | <span data-ttu-id="87673-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87673-105">Return Type</span></span>    |<span data-ttu-id="87673-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="87673-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="87673-107">Get RangeFormat</span><span class="sxs-lookup"><span data-stu-id="87673-107">Get RangeFormat</span></span>](../api/rangeformat_get.md) | [<span data-ttu-id="87673-108">WorkbookRangeFormat</span><span class="sxs-lookup"><span data-stu-id="87673-108">WorkbookRangeFormat</span></span>](rangeformat.md) |<span data-ttu-id="87673-109">Lee las propiedades y relaciones del objeto rangeFormat.</span><span class="sxs-lookup"><span data-stu-id="87673-109">Read properties and relationships of rangeFormat object.</span></span>|
|[<span data-ttu-id="87673-110">Create RangeBorder</span><span class="sxs-lookup"><span data-stu-id="87673-110">Create RangeBorder</span></span>](../api/rangeformat_post_borders.md) |[<span data-ttu-id="87673-111">WorkbookRangeBorder</span><span class="sxs-lookup"><span data-stu-id="87673-111">WorkbookRangeBorder</span></span>](rangeborder.md)| <span data-ttu-id="87673-112">Crea un RangeBorder publicándolo en la colección borders.</span><span class="sxs-lookup"><span data-stu-id="87673-112">Create a new RangeBorder by posting to the borders collection.</span></span>|
|[<span data-ttu-id="87673-113">List borders</span><span class="sxs-lookup"><span data-stu-id="87673-113">List borders</span></span>](../api/rangeformat_list_borders.md) |<span data-ttu-id="87673-114">Colección [WorkbookRangeBorder](rangeborder.md)</span><span class="sxs-lookup"><span data-stu-id="87673-114">[WorkbookRangeBorder](rangeborder.md) collection</span></span>| <span data-ttu-id="87673-115">Obtiene una colección de objetos RangeBorder.</span><span class="sxs-lookup"><span data-stu-id="87673-115">Get a RangeBorder object collection.</span></span>|
|[<span data-ttu-id="87673-116">Update</span><span class="sxs-lookup"><span data-stu-id="87673-116">Update</span></span>](../api/rangeformat_update.md) | [<span data-ttu-id="87673-117">WorkbookRangeFormat</span><span class="sxs-lookup"><span data-stu-id="87673-117">WorkbookRangeFormat</span></span>](rangeformat.md) |<span data-ttu-id="87673-118">Actualiza el objeto RangeFormat.</span><span class="sxs-lookup"><span data-stu-id="87673-118">Update RangeFormat object.</span></span> |
|[<span data-ttu-id="87673-119">Autofitcolumns</span><span class="sxs-lookup"><span data-stu-id="87673-119">Autofitcolumns</span></span>](../api/rangeformat_autofitcolumns.md)|<span data-ttu-id="87673-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="87673-120">None</span></span>|<span data-ttu-id="87673-121">Cambia el ancho de las columnas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).</span><span class="sxs-lookup"><span data-stu-id="87673-121">Changes the width of the columns of the current range to achieve the best fit, based on the current data in the columns.</span></span>|
|[<span data-ttu-id="87673-122">Autofitrows</span><span class="sxs-lookup"><span data-stu-id="87673-122">Autofitrows</span></span>](../api/rangeformat_autofitrows.md)|<span data-ttu-id="87673-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="87673-123">None</span></span>|<span data-ttu-id="87673-124">Cambia el alto de las filas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).</span><span class="sxs-lookup"><span data-stu-id="87673-124">Changes the height of the rows of the current range to achieve the best fit, based on the current data in the columns.</span></span>|

## <a name="properties"></a><span data-ttu-id="87673-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="87673-125">Properties</span></span>
| <span data-ttu-id="87673-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="87673-126">Property</span></span>     | <span data-ttu-id="87673-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="87673-127">Type</span></span>   |<span data-ttu-id="87673-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="87673-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="87673-129">columnWidth</span><span class="sxs-lookup"><span data-stu-id="87673-129">columnWidth</span></span>|<span data-ttu-id="87673-130">doble</span><span class="sxs-lookup"><span data-stu-id="87673-130">double</span></span>|<span data-ttu-id="87673-p101">Obtiene o establece el ancho de todas las columnas del rango. Si los anchos de columna no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="87673-p101">Gets or sets the width of all colums within the range. If the column widths are not uniform, null will be returned.</span></span>|
|<span data-ttu-id="87673-133">horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="87673-133">horizontalAlignment</span></span>|<span data-ttu-id="87673-134">cadena</span><span class="sxs-lookup"><span data-stu-id="87673-134">string</span></span>|<span data-ttu-id="87673-135">Representa la alineación horizontal del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="87673-135">Returns or sets the horizontal alignment for the specified object.</span></span> <span data-ttu-id="87673-136">Los valores posibles son: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection` y `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="87673-136">The possible values are `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`, , , , or .</span></span>|
|<span data-ttu-id="87673-137">rowHeight</span><span class="sxs-lookup"><span data-stu-id="87673-137">rowHeight</span></span>|<span data-ttu-id="87673-138">doble</span><span class="sxs-lookup"><span data-stu-id="87673-138">double</span></span>|<span data-ttu-id="87673-p103">Obtiene o establece el alto de todas las filas del rango. Si los altos de fila no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="87673-p103">Gets or sets the height of all rows in the range. If the row heights are not uniform null will be returned.</span></span>|
|<span data-ttu-id="87673-141">verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="87673-141">verticalAlignment</span></span>|<span data-ttu-id="87673-142">cadena</span><span class="sxs-lookup"><span data-stu-id="87673-142">string</span></span>|<span data-ttu-id="87673-143">Representa la alineación vertical del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="87673-143">Represents the vertical alignment for the specified object. Possible values are: , , , , .</span></span> <span data-ttu-id="87673-144">Los valores posibles son: `Top`, `Center`, `Bottom`, `Justify` y `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="87673-144">The possible values are `Top`, `Center`, `Bottom`, `Justify`, `Distributed`, , , , , , , or .</span></span>|
|<span data-ttu-id="87673-145">wrapText</span><span class="sxs-lookup"><span data-stu-id="87673-145">wrapText</span></span>|<span data-ttu-id="87673-146">booleano</span><span class="sxs-lookup"><span data-stu-id="87673-146">boolean</span></span>|<span data-ttu-id="87673-p105">Indica si Excel ajusta el texto del objeto. Un valor null indica que el intervalo no tiene una configuración de ajuste uniforme.</span><span class="sxs-lookup"><span data-stu-id="87673-p105">Indicates if Excel wraps the text in the object. A null value indicates that the entire range doesn't have uniform wrap setting</span></span>|

## <a name="relationships"></a><span data-ttu-id="87673-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="87673-149">Relationships</span></span>
| <span data-ttu-id="87673-150">Relación</span><span class="sxs-lookup"><span data-stu-id="87673-150">Relationship</span></span> | <span data-ttu-id="87673-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="87673-151">Type</span></span>   |<span data-ttu-id="87673-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="87673-152">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="87673-153">borders</span><span class="sxs-lookup"><span data-stu-id="87673-153">borders</span></span>|<span data-ttu-id="87673-154">Colección [WorkbookRangeBorder](rangeborder.md)</span><span class="sxs-lookup"><span data-stu-id="87673-154">[WorkbookRangeBorder](rangeborder.md) collection</span></span>|<span data-ttu-id="87673-155">Colección de objetos border que se aplican al rango global seleccionado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87673-155">Collection of border objects that apply to the overall range selected Read-only.</span></span>|
|<span data-ttu-id="87673-156">fill</span><span class="sxs-lookup"><span data-stu-id="87673-156">fill</span></span>|[<span data-ttu-id="87673-157">WorkbookRangeFill</span><span class="sxs-lookup"><span data-stu-id="87673-157">WorkbookRangeFill</span></span>](rangefill.md)|<span data-ttu-id="87673-p106">Devuelve el objeto de relleno definido en el rango global. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87673-p106">Returns the fill object defined on the overall range. Read-only.</span></span>|
|<span data-ttu-id="87673-160">font</span><span class="sxs-lookup"><span data-stu-id="87673-160">font</span></span>|[<span data-ttu-id="87673-161">WorkbookRangeFont</span><span class="sxs-lookup"><span data-stu-id="87673-161">WorkbookRangeFont</span></span>](rangefont.md)|<span data-ttu-id="87673-162">Devuelve el objeto de fuente definido en el intervalo global seleccionado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87673-162">Returns the font object defined on the overall range selected Read-only.</span></span>|
|<span data-ttu-id="87673-163">protection</span><span class="sxs-lookup"><span data-stu-id="87673-163">protection</span></span>|[<span data-ttu-id="87673-164">WorkbookFormatProtection</span><span class="sxs-lookup"><span data-stu-id="87673-164">WorkbookFormatProtection</span></span>](formatprotection.md)|<span data-ttu-id="87673-p107">Devuelve el objeto de protección de formato de un rango. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87673-p107">Returns the format protection object for a range. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="87673-167">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="87673-167">JSON representation</span></span>

<span data-ttu-id="87673-168">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="87673-168">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookRangeFormat"
}-->

```json
{
  "columnWidth": 1024,
  "horizontalAlignment": "string",
  "rowHeight": 1024,
  "verticalAlignment": "string",
  "wrapText": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->