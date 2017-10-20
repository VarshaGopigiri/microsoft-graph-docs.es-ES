---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Image
ms.openlocfilehash: 4488aedaf5c71f6484a0ccf33949fac2569d7af1
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="image-resource-type"></a><span data-ttu-id="4a519-102">Tipo de recurso Image</span><span class="sxs-lookup"><span data-stu-id="4a519-102">Image resource type</span></span>

<span data-ttu-id="4a519-p101">El recurso **Image** agrupa en una sola estructura las propiedades relacionadas con la imagen. Si un [**DriveItem**](driveitem.md) tiene una faceta de **image** no null, el elemento representa una imagen de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="4a519-p101">The **Image** resource groups image-related properties into a single structure. If a [**DriveItem**](driveitem.md) has a non-null **image** facet, the item represents a bitmap image.</span></span>

<span data-ttu-id="4a519-105">**Nota:** Si el servicio no puede determinar el ancho y el alto de la imagen, puede que el recurso **image** esté vacío.</span><span class="sxs-lookup"><span data-stu-id="4a519-105">**Note:** If the service is unable to determine the width and height of the image, the **Image** resource may be empty.</span></span>

## <a name="json-representation"></a><span data-ttu-id="4a519-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4a519-106">JSON representation</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.image" } -->
```json
{
  "width": 100,
  "height": 200
}
```

## <a name="properties"></a><span data-ttu-id="4a519-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a519-107">Properties</span></span>

| <span data-ttu-id="4a519-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a519-108">Property</span></span>   | <span data-ttu-id="4a519-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a519-109">Type</span></span>  | <span data-ttu-id="4a519-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a519-110">Description</span></span>                                |
|:-----------|:------|:-------------------------------------------|
| <span data-ttu-id="4a519-111">**height**</span><span class="sxs-lookup"><span data-stu-id="4a519-111">**height**</span></span> | <span data-ttu-id="4a519-112">Int32</span><span class="sxs-lookup"><span data-stu-id="4a519-112">Int32</span></span> | <span data-ttu-id="4a519-p102">Opcional. Ancho o alto de la imagen en píxeles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4a519-p102">Optional. Height of the image, in pixels. Read-only.</span></span> |
| <span data-ttu-id="4a519-116">**width**</span><span class="sxs-lookup"><span data-stu-id="4a519-116">**width**</span></span>  | <span data-ttu-id="4a519-117">Int32</span><span class="sxs-lookup"><span data-stu-id="4a519-117">Int32</span></span> | <span data-ttu-id="4a519-p103">Opcional. Ancho de la imagen en píxeles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4a519-p103">Optional. Width of the image, in pixels. Read-only.</span></span>  |

## <a name="remarks"></a><span data-ttu-id="4a519-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a519-121">Remarks</span></span>

<span data-ttu-id="4a519-122">En OneDrive para la Empresa, este recurso se devuelve en los elementos que se esperan que sean imágenes en función de la extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="4a519-122">In OneDrive for Business, this resource is returned on items that are expected to be images based on file extension. This resource returns no properties in OneDrive for Business.</span></span>

<span data-ttu-id="4a519-123">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="4a519-123">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "The image facet describes properties of an image like width and height",
  "keywords": "image,width,height,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Image"
} -->
