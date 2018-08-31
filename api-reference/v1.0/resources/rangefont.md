# <a name="rangefont-resource-type"></a><span data-ttu-id="9d624-101">Tipo de recurso RangeFont</span><span class="sxs-lookup"><span data-stu-id="9d624-101">RangeFont resource type</span></span>

<span data-ttu-id="9d624-102">Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto.</span><span class="sxs-lookup"><span data-stu-id="9d624-102">This object represents the font attributes (font name, font size, color, etc.) for an object.</span></span>


## <a name="methods"></a><span data-ttu-id="9d624-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d624-103">Methods</span></span>

| <span data-ttu-id="9d624-104">Método</span><span class="sxs-lookup"><span data-stu-id="9d624-104">Method</span></span>           | <span data-ttu-id="9d624-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d624-105">Return Type</span></span>    |<span data-ttu-id="9d624-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d624-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9d624-107">Get RangeFont</span><span class="sxs-lookup"><span data-stu-id="9d624-107">Get RangeFont</span></span>](../api/rangefont_get.md) | [<span data-ttu-id="9d624-108">WorkbookRangeFont</span><span class="sxs-lookup"><span data-stu-id="9d624-108">WorkbookRangeFont</span></span>](rangefont.md) |<span data-ttu-id="9d624-109">Lee las propiedades y relaciones del objeto rangeFont.</span><span class="sxs-lookup"><span data-stu-id="9d624-109">Read properties and relationships of rangeFont object.</span></span>|
|[<span data-ttu-id="9d624-110">Update</span><span class="sxs-lookup"><span data-stu-id="9d624-110">Update</span></span>](../api/rangefont_update.md) | [<span data-ttu-id="9d624-111">WorkbookRangeFont</span><span class="sxs-lookup"><span data-stu-id="9d624-111">WorkbookRangeFont</span></span>](rangefont.md)   |<span data-ttu-id="9d624-112">Actualiza el objeto RangeFont.</span><span class="sxs-lookup"><span data-stu-id="9d624-112">Update RangeFont object.</span></span> |

## <a name="properties"></a><span data-ttu-id="9d624-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9d624-113">Properties</span></span>
| <span data-ttu-id="9d624-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9d624-114">Property</span></span>     | <span data-ttu-id="9d624-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d624-115">Type</span></span>   |<span data-ttu-id="9d624-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d624-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9d624-117">bold</span><span class="sxs-lookup"><span data-stu-id="9d624-117">bold</span></span>|<span data-ttu-id="9d624-118">booleano</span><span class="sxs-lookup"><span data-stu-id="9d624-118">boolean</span></span>|<span data-ttu-id="9d624-119">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="9d624-119">Represents the bold status of font.</span></span>|
|<span data-ttu-id="9d624-120">color</span><span class="sxs-lookup"><span data-stu-id="9d624-120">color</span></span>|<span data-ttu-id="9d624-121">cadena</span><span class="sxs-lookup"><span data-stu-id="9d624-121">string</span></span>|<span data-ttu-id="9d624-p101">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="9d624-p101">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="9d624-125">italic</span><span class="sxs-lookup"><span data-stu-id="9d624-125">italic</span></span>|<span data-ttu-id="9d624-126">booleano</span><span class="sxs-lookup"><span data-stu-id="9d624-126">boolean</span></span>|<span data-ttu-id="9d624-127">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="9d624-127">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="9d624-128">name</span><span class="sxs-lookup"><span data-stu-id="9d624-128">name</span></span>|<span data-ttu-id="9d624-129">cadena</span><span class="sxs-lookup"><span data-stu-id="9d624-129">string</span></span>|<span data-ttu-id="9d624-130">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="9d624-130">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="9d624-131">size</span><span class="sxs-lookup"><span data-stu-id="9d624-131">size</span></span>|<span data-ttu-id="9d624-132">doble</span><span class="sxs-lookup"><span data-stu-id="9d624-132">double</span></span>|<span data-ttu-id="9d624-133">Tamaño de fuente</span><span class="sxs-lookup"><span data-stu-id="9d624-133">Font size.</span></span>|
|<span data-ttu-id="9d624-134">underline</span><span class="sxs-lookup"><span data-stu-id="9d624-134">underline</span></span>|<span data-ttu-id="9d624-135">cadena</span><span class="sxs-lookup"><span data-stu-id="9d624-135">string</span></span>|<span data-ttu-id="9d624-136">Tipo de subrayado aplicado a la fuente.</span><span class="sxs-lookup"><span data-stu-id="9d624-136">Returns or sets the type of underline applied to the font.</span></span> <span data-ttu-id="9d624-137">Los valores posibles son: `None`, `Single`, `Double`, `SingleAccountant` y `DoubleAccountant`.</span><span class="sxs-lookup"><span data-stu-id="9d624-137">The possible values are `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`, , , , , , , or .</span></span>|

## <a name="relationships"></a><span data-ttu-id="9d624-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9d624-138">Relationships</span></span>
<span data-ttu-id="9d624-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9d624-139">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="9d624-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9d624-140">JSON representation</span></span>

<span data-ttu-id="9d624-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9d624-141">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookRangeFont"
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
  "description": "RangeFont resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->