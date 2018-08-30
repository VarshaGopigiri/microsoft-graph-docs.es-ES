# <a name="icon-resource-type"></a><span data-ttu-id="027d7-101">Tipo de recurso Icon</span><span class="sxs-lookup"><span data-stu-id="027d7-101">Icon resource type</span></span>

<span data-ttu-id="027d7-102">Representa un icono de celda.</span><span class="sxs-lookup"><span data-stu-id="027d7-102">Represents a cell icon.</span></span>


## <a name="methods"></a><span data-ttu-id="027d7-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="027d7-103">Methods</span></span>

| <span data-ttu-id="027d7-104">Método</span><span class="sxs-lookup"><span data-stu-id="027d7-104">Method</span></span>           | <span data-ttu-id="027d7-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="027d7-105">Return Type</span></span>    |<span data-ttu-id="027d7-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="027d7-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="027d7-107">Get Icon</span><span class="sxs-lookup"><span data-stu-id="027d7-107">Get Icon</span></span>](../api/icon_get.md) | [<span data-ttu-id="027d7-108">Icon</span><span class="sxs-lookup"><span data-stu-id="027d7-108">Icon</span></span>](icon.md) |<span data-ttu-id="027d7-109">Lee las propiedades y relaciones del objeto icon.</span><span class="sxs-lookup"><span data-stu-id="027d7-109">Read properties and relationships of icon object.</span></span>|
|[<span data-ttu-id="027d7-110">Update</span><span class="sxs-lookup"><span data-stu-id="027d7-110">Update</span></span>](../api/icon_update.md) | [<span data-ttu-id="027d7-111">Icon</span><span class="sxs-lookup"><span data-stu-id="027d7-111">Icon</span></span>](icon.md)  |<span data-ttu-id="027d7-112">Actualiza el objeto Icon.</span><span class="sxs-lookup"><span data-stu-id="027d7-112">Update Icon object.</span></span> |

## <a name="properties"></a><span data-ttu-id="027d7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="027d7-113">Properties</span></span>
| <span data-ttu-id="027d7-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="027d7-114">Property</span></span>     | <span data-ttu-id="027d7-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="027d7-115">Type</span></span>   |<span data-ttu-id="027d7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="027d7-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="027d7-117">index</span><span class="sxs-lookup"><span data-stu-id="027d7-117">index</span></span>|<span data-ttu-id="027d7-118">int</span><span class="sxs-lookup"><span data-stu-id="027d7-118">int</span></span>|<span data-ttu-id="027d7-119">Representa el índice del icono en el conjunto concreto.</span><span class="sxs-lookup"><span data-stu-id="027d7-119">Represents the index of the icon in the given set.</span></span>|
|<span data-ttu-id="027d7-120">set</span><span class="sxs-lookup"><span data-stu-id="027d7-120">set</span></span>|<span data-ttu-id="027d7-121">cadena</span><span class="sxs-lookup"><span data-stu-id="027d7-121">string</span></span>|<span data-ttu-id="027d7-122">Representa el conjunto del que el icono de forma parte.</span><span class="sxs-lookup"><span data-stu-id="027d7-122">Represents the set that the icon is part of. Possible values are: , , , , , , , , , , , , , , , , , , , , .</span></span> <span data-ttu-id="027d7-123">Los valores posibles son: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles` y `FiveBoxes`.</span><span class="sxs-lookup"><span data-stu-id="027d7-123">The possible values are: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles`, `FiveBoxes`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="027d7-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="027d7-124">Relationships</span></span>
<span data-ttu-id="027d7-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="027d7-125">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="027d7-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="027d7-126">JSON representation</span></span>

<span data-ttu-id="027d7-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="027d7-127">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookIcon"
}-->

```json
{
  "index": 1024,
  "set": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Icon resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->