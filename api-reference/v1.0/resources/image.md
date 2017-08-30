# <a name="image-resource-type"></a><span data-ttu-id="7ba32-101">Tipo de recurso Image</span><span class="sxs-lookup"><span data-stu-id="7ba32-101">Image resource type</span></span>

<span data-ttu-id="7ba32-p101">El recurso **Image** agrupa en una sola estructura las propiedades relacionadas con la imagen. Si un [**DriveItem**](driveitem.md) tiene una faceta de **image** no null, el elemento representa una imagen de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="7ba32-p101">The **Image** resource groups image-related properties into a single structure. If a [**DriveItem**](driveitem.md) has a non-null **image** facet, the item represents a bitmap image.</span></span>

<span data-ttu-id="7ba32-104">**Nota**: Si el servicio no puede determinar el ancho y el alto de la imagen, puede que el recurso **image** esté vacío.</span><span class="sxs-lookup"><span data-stu-id="7ba32-104">**Note:** If the service is unable to determine the width and height of the image, the **Image** resource may be empty.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7ba32-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7ba32-105">JSON representation</span></span>

<span data-ttu-id="7ba32-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7ba32-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@odata.type": "microsoft.graph.image"
}-->

```json
{
  "height": 1024,
  "width": 1024
}
```

## <a name="properties"></a><span data-ttu-id="7ba32-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ba32-107">Properties</span></span>

| <span data-ttu-id="7ba32-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7ba32-108">Property</span></span>   | <span data-ttu-id="7ba32-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ba32-109">Type</span></span>  | <span data-ttu-id="7ba32-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ba32-110">Description</span></span>                                |
|:-----------|:------|:-------------------------------------------|
| <span data-ttu-id="7ba32-111">**height**</span><span class="sxs-lookup"><span data-stu-id="7ba32-111">**height**</span></span> | <span data-ttu-id="7ba32-112">Int32</span><span class="sxs-lookup"><span data-stu-id="7ba32-112">Int32</span></span> | <span data-ttu-id="7ba32-p102">Opcional. Ancho o alto de la imagen en píxeles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7ba32-p102">Optional. Height of the image, in pixels. Read-only.</span></span> |
| <span data-ttu-id="7ba32-116">**width**</span><span class="sxs-lookup"><span data-stu-id="7ba32-116">**width**</span></span>  | <span data-ttu-id="7ba32-117">Int32</span><span class="sxs-lookup"><span data-stu-id="7ba32-117">Int32</span></span> | <span data-ttu-id="7ba32-p103">Opcional. Ancho de la imagen en píxeles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7ba32-p103">Optional. Width of the image, in pixels. Read-only.</span></span>  |

## <a name="remarks"></a><span data-ttu-id="7ba32-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ba32-121">Remarks</span></span>

<span data-ttu-id="7ba32-p104">En OneDrive para la Empresa, este recurso se devuelve en los elementos que se esperan que sean imágenes en función de la extensión de archivo. Este recurso no devuelve propiedades en OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="7ba32-p104">In OneDrive for Business, this resource is returned on items that are expected to be images based on file extension. This resource returns no properties in OneDrive for Business.</span></span>

<span data-ttu-id="7ba32-124">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="7ba32-124">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "image resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
