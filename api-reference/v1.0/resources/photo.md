# <a name="photo-resource-type"></a><span data-ttu-id="71d86-101">Tipo de recurso Photo</span><span class="sxs-lookup"><span data-stu-id="71d86-101">Photo resource type</span></span>

<span data-ttu-id="71d86-102">El recurso **photo** proporciona propiedades de foto y cámara, por ejemplo, los metadatos EXIF, en un [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="71d86-102">The **photo** resource provides photo and camera properties, for example, EXIF metadata, on a [driveItem](driveitem.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="71d86-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="71d86-103">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.photo"
}-->
```json
{
  "cameraMake": "string",
  "cameraModel": "string",
  "exposureDenominator": 1024,
  "exposureNumerator": 1024,
  "fNumber": 1024,
  "focalLength": 1024,
  "iso": 1024,
  "takenDateTime": "String (timestamp)"
}
```

## <a name="properties"></a><span data-ttu-id="71d86-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71d86-104">Properties</span></span>
| <span data-ttu-id="71d86-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="71d86-105">Property</span></span>                | <span data-ttu-id="71d86-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="71d86-106">Type</span></span>                      | <span data-ttu-id="71d86-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="71d86-107">Description</span></span>                                                     |
|:------------------------|:--------------------------|:----------------------------------------------------------------|
| <span data-ttu-id="71d86-108">**takenDateTime**</span><span class="sxs-lookup"><span data-stu-id="71d86-108">**takenDateTime**</span></span>       | <span data-ttu-id="71d86-109">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="71d86-109">DateTimeOffset</span></span>            | <span data-ttu-id="71d86-p101">Representa la fecha y hora en que se tomó la foto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71d86-p101">Represents the date and time the photo was taken. Read-only.</span></span>               |
| <span data-ttu-id="71d86-112">**cameraMake**</span><span class="sxs-lookup"><span data-stu-id="71d86-112">**cameraMake**</span></span>          | <span data-ttu-id="71d86-113">String</span><span class="sxs-lookup"><span data-stu-id="71d86-113">String</span></span>                    | <span data-ttu-id="71d86-p102">Fabricante de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71d86-p102">Camera manufacturer. Read-only.</span></span>                                            |
| <span data-ttu-id="71d86-116">**cameraModel**</span><span class="sxs-lookup"><span data-stu-id="71d86-116">**cameraModel**</span></span>         | <span data-ttu-id="71d86-117">String</span><span class="sxs-lookup"><span data-stu-id="71d86-117">String</span></span>                    | <span data-ttu-id="71d86-p103">Modelo de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71d86-p103">Camera model. Read-only.</span></span>                                                   |
| <span data-ttu-id="71d86-120">**fNumber**</span><span class="sxs-lookup"><span data-stu-id="71d86-120">**fNumber**</span></span>             | <span data-ttu-id="71d86-121">Double</span><span class="sxs-lookup"><span data-stu-id="71d86-121">Double</span></span>                    | <span data-ttu-id="71d86-p104">Valor punto F de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71d86-p104">The F-stop value from the camera. Read-only.</span></span>                               |
| <span data-ttu-id="71d86-124">**exposureDenominator**</span><span class="sxs-lookup"><span data-stu-id="71d86-124">**exposureDenominator**</span></span> | <span data-ttu-id="71d86-125">Int32</span><span class="sxs-lookup"><span data-stu-id="71d86-125">Int32</span></span>                     | <span data-ttu-id="71d86-p105">Denominador de la fracción de tiempo de exposición de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71d86-p105">The denominator for the exposure time fraction from the camera. Read-only.</span></span> |
| <span data-ttu-id="71d86-128">**exposureNumerator**</span><span class="sxs-lookup"><span data-stu-id="71d86-128">**exposureNumerator**</span></span>   | <span data-ttu-id="71d86-129">Int32</span><span class="sxs-lookup"><span data-stu-id="71d86-129">Int32</span></span>                     | <span data-ttu-id="71d86-p106">Numerador de la fracción de tiempo de exposición de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71d86-p106">The numerator for the exposure time fraction from the camera. Read-only.</span></span>   |
| <span data-ttu-id="71d86-132">**focalLength**</span><span class="sxs-lookup"><span data-stu-id="71d86-132">**focalLength**</span></span>         | <span data-ttu-id="71d86-133">Double</span><span class="sxs-lookup"><span data-stu-id="71d86-133">Double</span></span>                    | <span data-ttu-id="71d86-p107">Distancia focal de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71d86-p107">The focal length from the camera. Read-only.</span></span>                               |
| <span data-ttu-id="71d86-136">**iso**</span><span class="sxs-lookup"><span data-stu-id="71d86-136">**iso**</span></span>                 | <span data-ttu-id="71d86-137">Int32</span><span class="sxs-lookup"><span data-stu-id="71d86-137">Int32</span></span>                     | <span data-ttu-id="71d86-p108">Valor ISO de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71d86-p108">The ISO value from the camera. Read-only.</span></span>                                  |

## <a name="remarks"></a><span data-ttu-id="71d86-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71d86-140">Remarks</span></span>
<span data-ttu-id="71d86-141">OneDrive para la Empresa y SharePoint solo devuelven la propiedad **takenDateTime**.</span><span class="sxs-lookup"><span data-stu-id="71d86-141">OneDrive for Business and SharePoint only return the **takenDateTime** property.</span></span>

<span data-ttu-id="71d86-142">Para obtener más información sobre las facetas de un DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="71d86-142">For more information about the facets on a [driveItem](driveitem.md), see driveItem.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "photo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
