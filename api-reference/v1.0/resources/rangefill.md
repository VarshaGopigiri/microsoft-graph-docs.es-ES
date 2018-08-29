# <a name="rangefill-resource-type"></a><span data-ttu-id="6a9c5-101">Tipo de recurso RangeFill</span><span class="sxs-lookup"><span data-stu-id="6a9c5-101">RangeFill resource type</span></span>

<span data-ttu-id="6a9c5-102">Representa el fondo de un objeto de rango.</span><span class="sxs-lookup"><span data-stu-id="6a9c5-102">Represents the background of a range object.</span></span>


## <a name="methods"></a><span data-ttu-id="6a9c5-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="6a9c5-103">Methods</span></span>

| <span data-ttu-id="6a9c5-104">Método</span><span class="sxs-lookup"><span data-stu-id="6a9c5-104">Method</span></span>           | <span data-ttu-id="6a9c5-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a9c5-105">Return Type</span></span>    |<span data-ttu-id="6a9c5-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a9c5-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="6a9c5-107">Obtener RangeFill</span><span class="sxs-lookup"><span data-stu-id="6a9c5-107">Get RangeFill</span></span>](../api/rangefill_get.md) | [<span data-ttu-id="6a9c5-108">WorkbookRangeFill</span><span class="sxs-lookup"><span data-stu-id="6a9c5-108">WorkbookRangeFill</span></span>](rangefill.md) |<span data-ttu-id="6a9c5-109">Lee las propiedades y relaciones del objeto rangeFill.</span><span class="sxs-lookup"><span data-stu-id="6a9c5-109">Read properties and relationships of rangeFill object.</span></span>|
|[<span data-ttu-id="6a9c5-110">Actualizar</span><span class="sxs-lookup"><span data-stu-id="6a9c5-110">Update</span></span>](../api/rangefill_update.md) | [<span data-ttu-id="6a9c5-111">WorkbookRangeFill</span><span class="sxs-lookup"><span data-stu-id="6a9c5-111">WorkbookRangeFill</span></span>](rangefill.md)   |<span data-ttu-id="6a9c5-112">Actualiza el objeto RangeFill.</span><span class="sxs-lookup"><span data-stu-id="6a9c5-112">Update RangeFill object.</span></span> |
|[<span data-ttu-id="6a9c5-113">Borrar</span><span class="sxs-lookup"><span data-stu-id="6a9c5-113">Clear</span></span>](../api/rangefill_clear.md)|<span data-ttu-id="6a9c5-114">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6a9c5-114">None</span></span>|<span data-ttu-id="6a9c5-115">Restablece el fondo del rango.</span><span class="sxs-lookup"><span data-stu-id="6a9c5-115">Resets the range background.</span></span>|

## <a name="properties"></a><span data-ttu-id="6a9c5-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a9c5-116">Properties</span></span>
| <span data-ttu-id="6a9c5-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6a9c5-117">Property</span></span>     | <span data-ttu-id="6a9c5-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a9c5-118">Type</span></span>   |<span data-ttu-id="6a9c5-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a9c5-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6a9c5-120">color</span><span class="sxs-lookup"><span data-stu-id="6a9c5-120">color</span></span>|<span data-ttu-id="6a9c5-121">cadena</span><span class="sxs-lookup"><span data-stu-id="6a9c5-121">string</span></span>|<span data-ttu-id="6a9c5-122">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="6a9c5-122">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange")</span></span>|

## <a name="relationships"></a><span data-ttu-id="6a9c5-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6a9c5-123">Relationships</span></span>
<span data-ttu-id="6a9c5-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6a9c5-124">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="6a9c5-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6a9c5-125">JSON representation</span></span>

<span data-ttu-id="6a9c5-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6a9c5-126">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookRangeFill"
}-->

```json
{
  "color": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFill resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->