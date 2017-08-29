# <a name="geocoordinates-resource-type"></a><span data-ttu-id="cfc8c-101">Tipo de recurso GeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="cfc8c-101">GeoCoordinates resource type</span></span>

<span data-ttu-id="cfc8c-p101">El recurso **GeoCoordinates** proporciona las coordenadas geográficas y la elevación de una ubicación en función de metadatos contenidos en el archivo. Si un [**DriveItem**](driveitem.md) tiene una faceta **location** no null, el elemento representa un archivo que tiene asociada una ubicación conocida.</span><span class="sxs-lookup"><span data-stu-id="cfc8c-p101">The **GeoCoordinates** resource provides geographic coordinates and elevation of a location based on metadata contained within the file. If a [**DriveItem**](driveitem.md) has a non-null **location** facet, the item represents a file with a known location assocaited with it.</span></span>

## <a name="json-representation"></a><span data-ttu-id="cfc8c-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cfc8c-104">JSON representation</span></span>

<span data-ttu-id="cfc8c-105">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="cfc8c-105">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.geoCoordinates"
}-->

```json
{
  "altitude": 1024.13,
  "latitude": 26.13246,
  "longitude": 24.34616
}
```

## <a name="properties"></a><span data-ttu-id="cfc8c-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cfc8c-106">Properties</span></span>

| <span data-ttu-id="cfc8c-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cfc8c-107">Property</span></span>  | <span data-ttu-id="cfc8c-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="cfc8c-108">Type</span></span>   | <span data-ttu-id="cfc8c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cfc8c-109">Description</span></span>                                                    |
|:----------|:-------|:---------------------------------------------------------------|
| <span data-ttu-id="cfc8c-110">altitude</span><span class="sxs-lookup"><span data-stu-id="cfc8c-110">altitude</span></span>  | <span data-ttu-id="cfc8c-111">Doble</span><span class="sxs-lookup"><span data-stu-id="cfc8c-111">Double</span></span> | <span data-ttu-id="cfc8c-p102">Opcional. Altitud (alto) en pies sobre el nivel del mar del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cfc8c-p102">Optional. The altitude (height), in feet,  above sea level for the item. Read-only.</span></span> |
| <span data-ttu-id="cfc8c-115">latitude</span><span class="sxs-lookup"><span data-stu-id="cfc8c-115">latitude</span></span>  | <span data-ttu-id="cfc8c-116">Doble</span><span class="sxs-lookup"><span data-stu-id="cfc8c-116">Double</span></span> | <span data-ttu-id="cfc8c-p103">Opcional. Latitud en formato decimal del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cfc8c-p103">Optional. The latitude, in decimal, for the item. Read-only.</span></span>   |
| <span data-ttu-id="cfc8c-120">longitude</span><span class="sxs-lookup"><span data-stu-id="cfc8c-120">longitude</span></span> | <span data-ttu-id="cfc8c-121">Doble</span><span class="sxs-lookup"><span data-stu-id="cfc8c-121">Double</span></span> | <span data-ttu-id="cfc8c-p104">Opcional. Longitud en formato decimal del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cfc8c-p104">Optional. The longitude, in decimal, for the item. Read-only.</span></span>  |

## <a name="remarks"></a><span data-ttu-id="cfc8c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfc8c-125">Remarks</span></span>

<span data-ttu-id="cfc8c-126">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="cfc8c-126">For more information about the facets on a [driveItem](driveitem.md), see driveItem.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "geoCoordinates resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
