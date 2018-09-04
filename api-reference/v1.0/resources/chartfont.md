# <a name="chartfont-resource-type"></a><span data-ttu-id="18447-101">Tipo de recurso ChartFont</span><span class="sxs-lookup"><span data-stu-id="18447-101">ChartFont resource type</span></span>

<span data-ttu-id="18447-102">Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="18447-102">This object represents the font attributes (font name, font size, color, etc.) for a chart object.</span></span>


## <a name="methods"></a><span data-ttu-id="18447-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="18447-103">Methods</span></span>

| <span data-ttu-id="18447-104">Método</span><span class="sxs-lookup"><span data-stu-id="18447-104">Method</span></span>           | <span data-ttu-id="18447-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18447-105">Return Type</span></span>    |<span data-ttu-id="18447-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="18447-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="18447-107">Get ChartFont</span><span class="sxs-lookup"><span data-stu-id="18447-107">Get ChartFont</span></span>](../api/chartfont_get.md) | [<span data-ttu-id="18447-108">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="18447-108">WorkbookChartFont</span></span>](chartfont.md) |<span data-ttu-id="18447-109">Lee las propiedades y relaciones del objeto chartFont.</span><span class="sxs-lookup"><span data-stu-id="18447-109">Read properties and relationships of chartFont object.</span></span>|
|[<span data-ttu-id="18447-110">Update</span><span class="sxs-lookup"><span data-stu-id="18447-110">Update</span></span>](../api/chartfont_update.md) | [<span data-ttu-id="18447-111">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="18447-111">WorkbookChartFont</span></span>](chartfont.md)   |<span data-ttu-id="18447-112">Actualiza el objeto ChartFont.</span><span class="sxs-lookup"><span data-stu-id="18447-112">Update ChartFont object.</span></span> |

## <a name="properties"></a><span data-ttu-id="18447-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="18447-113">Properties</span></span>
| <span data-ttu-id="18447-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="18447-114">Property</span></span>     | <span data-ttu-id="18447-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="18447-115">Type</span></span>   |<span data-ttu-id="18447-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="18447-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="18447-117">bold</span><span class="sxs-lookup"><span data-stu-id="18447-117">bold</span></span>|<span data-ttu-id="18447-118">booleano</span><span class="sxs-lookup"><span data-stu-id="18447-118">boolean</span></span>|<span data-ttu-id="18447-119">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="18447-119">Represents the bold status of font.</span></span>|
|<span data-ttu-id="18447-120">color</span><span class="sxs-lookup"><span data-stu-id="18447-120">color</span></span>|<span data-ttu-id="18447-121">cadena</span><span class="sxs-lookup"><span data-stu-id="18447-121">string</span></span>|<span data-ttu-id="18447-p101">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="18447-p101">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="18447-125">italic</span><span class="sxs-lookup"><span data-stu-id="18447-125">italic</span></span>|<span data-ttu-id="18447-126">booleano</span><span class="sxs-lookup"><span data-stu-id="18447-126">boolean</span></span>|<span data-ttu-id="18447-127">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="18447-127">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="18447-128">name</span><span class="sxs-lookup"><span data-stu-id="18447-128">name</span></span>|<span data-ttu-id="18447-129">cadena</span><span class="sxs-lookup"><span data-stu-id="18447-129">string</span></span>|<span data-ttu-id="18447-130">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="18447-130">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="18447-131">Tamaño</span><span class="sxs-lookup"><span data-stu-id="18447-131">size</span></span>|<span data-ttu-id="18447-132">doble</span><span class="sxs-lookup"><span data-stu-id="18447-132">double</span></span>|<span data-ttu-id="18447-133">Tamaño de la fuente (por ejemplo, 11).</span><span class="sxs-lookup"><span data-stu-id="18447-133">Size of the font (e.g. 11)</span></span>|
|<span data-ttu-id="18447-134">underline</span><span class="sxs-lookup"><span data-stu-id="18447-134">underline</span></span>|<span data-ttu-id="18447-135">cadena</span><span class="sxs-lookup"><span data-stu-id="18447-135">string</span></span>|<span data-ttu-id="18447-136">Tipo de subrayado aplicado a la fuente.</span><span class="sxs-lookup"><span data-stu-id="18447-136">Returns or sets the type of underline applied to the font.</span></span> <span data-ttu-id="18447-137">Los valores posibles son: `None` y `Single`.</span><span class="sxs-lookup"><span data-stu-id="18447-137">The possible values are:</span></span>|

## <a name="relationships"></a><span data-ttu-id="18447-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="18447-138">Relationships</span></span>
<span data-ttu-id="18447-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="18447-139">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="18447-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="18447-140">JSON representation</span></span>

<span data-ttu-id="18447-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="18447-141">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartFont"
}-->

```json
{
  "bold": true,
  "color": "string",
  "italic": true,
  "name": "string",
  "size": 1024,
  "underline": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartFont resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->