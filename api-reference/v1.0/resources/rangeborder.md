# <a name="rangeborder-resource-type"></a><span data-ttu-id="da2fa-101">Tipo de recurso RangeBorder</span><span class="sxs-lookup"><span data-stu-id="da2fa-101">RangeBorder resource type</span></span>

<span data-ttu-id="da2fa-102">Representa el borde de un objeto.</span><span class="sxs-lookup"><span data-stu-id="da2fa-102">Represents the border of an object.</span></span>


## <a name="methods"></a><span data-ttu-id="da2fa-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="da2fa-103">Methods</span></span>

| <span data-ttu-id="da2fa-104">Método</span><span class="sxs-lookup"><span data-stu-id="da2fa-104">Method</span></span>           | <span data-ttu-id="da2fa-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da2fa-105">Return Type</span></span>    |<span data-ttu-id="da2fa-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="da2fa-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="da2fa-107">Get RangeBorder</span><span class="sxs-lookup"><span data-stu-id="da2fa-107">Get RangeBorder</span></span>](../api/rangeborder_get.md) | [<span data-ttu-id="da2fa-108">WorkbookRangeBorder</span><span class="sxs-lookup"><span data-stu-id="da2fa-108">WorkbookRangeBorder</span></span>](rangeborder.md) |<span data-ttu-id="da2fa-109">Lee las propiedades y relaciones del objeto rangeBorder.</span><span class="sxs-lookup"><span data-stu-id="da2fa-109">Read properties and relationships of rangeBorder object.</span></span>|
|[<span data-ttu-id="da2fa-110">Update</span><span class="sxs-lookup"><span data-stu-id="da2fa-110">Update</span></span>](../api/rangeborder_update.md) | [<span data-ttu-id="da2fa-111">WorkbookRangeBorder</span><span class="sxs-lookup"><span data-stu-id="da2fa-111">WorkbookRangeBorder</span></span>](rangeborder.md) |<span data-ttu-id="da2fa-112">Actualiza el objeto RangeBorder.</span><span class="sxs-lookup"><span data-stu-id="da2fa-112">Update RangeBorder object.</span></span> |
|[<span data-ttu-id="da2fa-113">List</span><span class="sxs-lookup"><span data-stu-id="da2fa-113">List</span></span>](../api/rangeborder_list.md) | <span data-ttu-id="da2fa-114">Colección [WorkbookRangeBorder](rangeborder.md)</span><span class="sxs-lookup"><span data-stu-id="da2fa-114">[WorkbookRangeBorder](rangeborder.md) collection</span></span> |<span data-ttu-id="da2fa-115">Obtiene la colección de objetos rangeBorder.</span><span class="sxs-lookup"><span data-stu-id="da2fa-115">Get rangeBorder object collection.</span></span> |
|[<span data-ttu-id="da2fa-116">Itemat</span><span class="sxs-lookup"><span data-stu-id="da2fa-116">Itemat</span></span>](../api/rangebordercollection_itemat.md)|[<span data-ttu-id="da2fa-117">WorkbookRangeBorder</span><span class="sxs-lookup"><span data-stu-id="da2fa-117">WorkbookRangeBorder</span></span>](rangeborder.md)|<span data-ttu-id="da2fa-118">Obtiene un objeto de borde mediante su índice</span><span class="sxs-lookup"><span data-stu-id="da2fa-118">Gets a border object using its index</span></span>|

## <a name="properties"></a><span data-ttu-id="da2fa-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="da2fa-119">Properties</span></span>
| <span data-ttu-id="da2fa-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="da2fa-120">Property</span></span>     | <span data-ttu-id="da2fa-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="da2fa-121">Type</span></span>   |<span data-ttu-id="da2fa-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="da2fa-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="da2fa-123">color</span><span class="sxs-lookup"><span data-stu-id="da2fa-123">color</span></span>|<span data-ttu-id="da2fa-124">cadena</span><span class="sxs-lookup"><span data-stu-id="da2fa-124">string</span></span>|<span data-ttu-id="da2fa-125">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="da2fa-125">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|
|<span data-ttu-id="da2fa-126">id</span><span class="sxs-lookup"><span data-stu-id="da2fa-126">id</span></span>|<span data-ttu-id="da2fa-127">cadena</span><span class="sxs-lookup"><span data-stu-id="da2fa-127">string</span></span>|<span data-ttu-id="da2fa-128">Representa el identificador del borde.</span><span class="sxs-lookup"><span data-stu-id="da2fa-128">Represents border identifier. Possible values are: , , , , , , , . Read-only.</span></span> <span data-ttu-id="da2fa-129">Los valores posibles son: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown` y `DiagonalUp`.</span><span class="sxs-lookup"><span data-stu-id="da2fa-129">The possible values are `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`, , , , or .</span></span> <span data-ttu-id="da2fa-130">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="da2fa-130">Read-only.</span></span>|
|<span data-ttu-id="da2fa-131">sideIndex</span><span class="sxs-lookup"><span data-stu-id="da2fa-131">sideIndex</span></span>|<span data-ttu-id="da2fa-132">cadena</span><span class="sxs-lookup"><span data-stu-id="da2fa-132">string</span></span>|<span data-ttu-id="da2fa-133">Valor constante que indica el lado específico del borde.</span><span class="sxs-lookup"><span data-stu-id="da2fa-133">Constant value that indicates the specific side of the border. Possible values are: , , , , , , , . Read-only.</span></span> <span data-ttu-id="da2fa-134">Los valores posibles son: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown` y `DiagonalUp`.</span><span class="sxs-lookup"><span data-stu-id="da2fa-134">The possible values are `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`, , , , or .</span></span> <span data-ttu-id="da2fa-135">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="da2fa-135">Read-only.</span></span>|
|<span data-ttu-id="da2fa-136">style</span><span class="sxs-lookup"><span data-stu-id="da2fa-136">style</span></span>|<span data-ttu-id="da2fa-137">cadena</span><span class="sxs-lookup"><span data-stu-id="da2fa-137">string</span></span>|<span data-ttu-id="da2fa-138">Una de las constantes de estilo de línea que especifica el estilo de línea para el borde.</span><span class="sxs-lookup"><span data-stu-id="da2fa-138">One of the constants of line style specifying the line style for the border. Possible values are: , , , , , , , .</span></span> <span data-ttu-id="da2fa-139">Los valores posibles son: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double` y `SlantDashDot`.</span><span class="sxs-lookup"><span data-stu-id="da2fa-139">The possible values are `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`, , , , or .</span></span>|
|<span data-ttu-id="da2fa-140">weight</span><span class="sxs-lookup"><span data-stu-id="da2fa-140">weight</span></span>|<span data-ttu-id="da2fa-141">cadena</span><span class="sxs-lookup"><span data-stu-id="da2fa-141">string</span></span>|<span data-ttu-id="da2fa-142">Especifica el grosor del borde que rodea un rango.</span><span class="sxs-lookup"><span data-stu-id="da2fa-142">Specifies the weight of the border around a range.</span></span> <span data-ttu-id="da2fa-143">Los valores posibles son: `Hairline`, `Thin`, `Medium` y `Thick`.</span><span class="sxs-lookup"><span data-stu-id="da2fa-143">The possible values are `Hairline`, `Thin`, `Medium`, `Thick`, , , , , , , , or .</span></span>|

## <a name="relationships"></a><span data-ttu-id="da2fa-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="da2fa-144">Relationships</span></span>
<span data-ttu-id="da2fa-145">Ninguno</span><span class="sxs-lookup"><span data-stu-id="da2fa-145">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="da2fa-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="da2fa-146">JSON representation</span></span>

<span data-ttu-id="da2fa-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="da2fa-147">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookRangeBorder"
}-->

```json
{
  "color": "string",
  "id": "string",
  "sideIndex": "string",
  "style": "string",
  "weight": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeBorder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->