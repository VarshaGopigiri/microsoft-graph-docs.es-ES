# <a name="outlookgeocoordinates-resource-type"></a><span data-ttu-id="0049d-101">Tipo de recurso outlookGeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="0049d-101">outlookGeoCoordinates resource type</span></span>

<span data-ttu-id="0049d-102">Coordenadas geográficas, elevación y su grado de precisión para una ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="0049d-102">The geographic coordinates, elevation, and their degree of accuracy for a physical location.</span></span>

## <a name="json-representation"></a><span data-ttu-id="0049d-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0049d-103">JSON representation</span></span>

<span data-ttu-id="0049d-104">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0049d-104">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.outlookGeoCoordinates"
}-->

```json
{
  "accuracy": 1024.13,
  "altitude": 1024.13,
  "altitudeAccuracy": 1024.13,
  "latitude": 1024.13,
  "longitude": 1024.13
}

```
## <a name="properties"></a><span data-ttu-id="0049d-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0049d-105">Properties</span></span>
| <span data-ttu-id="0049d-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0049d-106">Property</span></span>     | <span data-ttu-id="0049d-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="0049d-107">Type</span></span>   |<span data-ttu-id="0049d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0049d-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0049d-109">accuracy</span><span class="sxs-lookup"><span data-stu-id="0049d-109">accuracy</span></span>|<span data-ttu-id="0049d-110">double</span><span class="sxs-lookup"><span data-stu-id="0049d-110">double</span></span>|<span data-ttu-id="0049d-111">Exactitud de la latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="0049d-111">The accuracy of the latitude and longitude.</span></span> <span data-ttu-id="0049d-112">Por ejemplo, la precisión puede medirse en metros, como que la latitud y longitud tienen una precisión de 50 metros.</span><span class="sxs-lookup"><span data-stu-id="0049d-112">As an example, the accuracy can be measured in meters, such as the latitude and longitude are accurate to within 50 meters.</span></span>|
|<span data-ttu-id="0049d-113">altitude</span><span class="sxs-lookup"><span data-stu-id="0049d-113">altitude</span></span>|<span data-ttu-id="0049d-114">double</span><span class="sxs-lookup"><span data-stu-id="0049d-114">double</span></span>|<span data-ttu-id="0049d-115">Altitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="0049d-115">The altitude of the location.</span></span>|
|<span data-ttu-id="0049d-116">altitudeAccuracy</span><span class="sxs-lookup"><span data-stu-id="0049d-116">altitudeAccuracy</span></span>|<span data-ttu-id="0049d-117">double</span><span class="sxs-lookup"><span data-stu-id="0049d-117">double</span></span>|<span data-ttu-id="0049d-118">Exactitud de la altitud.</span><span class="sxs-lookup"><span data-stu-id="0049d-118">The accuracy of the altitude.</span></span>|
|<span data-ttu-id="0049d-119">latitude</span><span class="sxs-lookup"><span data-stu-id="0049d-119">latitude</span></span>|<span data-ttu-id="0049d-120">double</span><span class="sxs-lookup"><span data-stu-id="0049d-120">double</span></span>|<span data-ttu-id="0049d-121">Latitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="0049d-121">The latitude of the location.</span></span>|
|<span data-ttu-id="0049d-122">longitude</span><span class="sxs-lookup"><span data-stu-id="0049d-122">longitude</span></span>|<span data-ttu-id="0049d-123">double</span><span class="sxs-lookup"><span data-stu-id="0049d-123">double</span></span>|<span data-ttu-id="0049d-124">Longitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="0049d-124">The longitude of the location.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookGeoCoordinates resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->