---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: ThumbnailSet
localization_priority: Normal
ms.openlocfilehash: 779cc9129bbbe660286d2350a76451c9666752d5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888875"
---
# <a name="thumbnailset-resource-type"></a><span data-ttu-id="33850-102">Tipo de recurso ThumbnailSet</span><span class="sxs-lookup"><span data-stu-id="33850-102">ThumbnailSet resource type</span></span>

<span data-ttu-id="33850-p101">El recurso **ThumbnailSet** es una colección de claves de recursos [thumbnail](thumbnail.md). Se usa para representar un conjunto de miniaturas asociadas a un DriveItem.</span><span class="sxs-lookup"><span data-stu-id="33850-p101">The **ThumbnailSet** resource is a keyed collection of [thumbnail](thumbnail.md) resources. It is used to represent a set of thumbnails associated with a DriveItem.</span></span>

## <a name="json-representation"></a><span data-ttu-id="33850-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="33850-105">JSON representation</span></span>

<span data-ttu-id="33850-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="33850-106">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "source",
    "small",
    "medium",
    "large"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.thumbnailSet",
  "openType": true
}-->

```json
{
  "id": "string (identifier)",
  "large": { "@odata.type": "microsoft.graph.thumbnail" },
  "medium": { "@odata.type": "microsoft.graph.thumbnail" },
  "small": { "@odata.type": "microsoft.graph.thumbnail" },
  "source": { "@odata.type": "microsoft.graph.thumbnail" }
}
```

## <a name="properties"></a><span data-ttu-id="33850-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33850-107">Properties</span></span>

| <span data-ttu-id="33850-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="33850-108">Property</span></span> | <span data-ttu-id="33850-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="33850-109">Type</span></span>                      | <span data-ttu-id="33850-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="33850-110">Description</span></span>                                                                       |
|:---------|:--------------------------|:----------------------------------------------------------------------------------|
| <span data-ttu-id="33850-111">id</span><span class="sxs-lookup"><span data-stu-id="33850-111">id</span></span>       | <span data-ttu-id="33850-112">String</span><span class="sxs-lookup"><span data-stu-id="33850-112">String</span></span>                    | <span data-ttu-id="33850-p102">Identificador del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="33850-p102">The id within the item. Read-only.</span></span>                                                |
| <span data-ttu-id="33850-115">large</span><span class="sxs-lookup"><span data-stu-id="33850-115">large</span></span>    | [<span data-ttu-id="33850-116">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="33850-116">Thumbnail</span></span>](thumbnail.md) | <span data-ttu-id="33850-117">Miniatura escalada de 1920 x 1920.</span><span class="sxs-lookup"><span data-stu-id="33850-117">A 1920x1920 scaled thumbnail.</span></span>                                                     |
| <span data-ttu-id="33850-118">medium</span><span class="sxs-lookup"><span data-stu-id="33850-118">medium</span></span>   | [<span data-ttu-id="33850-119">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="33850-119">Thumbnail</span></span>](thumbnail.md) | <span data-ttu-id="33850-120">Miniatura escalada de 176 x 176.</span><span class="sxs-lookup"><span data-stu-id="33850-120">A 176x176 scaled thumbnail.</span></span>                                                       |
| <span data-ttu-id="33850-121">small</span><span class="sxs-lookup"><span data-stu-id="33850-121">small</span></span>    | [<span data-ttu-id="33850-122">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="33850-122">Thumbnail</span></span>](thumbnail.md) | <span data-ttu-id="33850-123">Miniatura recortada de 48 x 48.</span><span class="sxs-lookup"><span data-stu-id="33850-123">A 48x48 cropped thumbnail.</span></span>                                                        |
| <span data-ttu-id="33850-124">source</span><span class="sxs-lookup"><span data-stu-id="33850-124">source</span></span>   | [<span data-ttu-id="33850-125">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="33850-125">Thumbnail</span></span>](thumbnail.md) | <span data-ttu-id="33850-126">Imagen en miniatura personalizada o imagen original usada para generar otras miniaturas.</span><span class="sxs-lookup"><span data-stu-id="33850-126">A custom thumbnail image or the original image used to generate other thumbnails.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ThumbnailSet enables access to thumbnails of different sizes",
  "section": "documentation",
  "tocPath": "Resources/ThumbnailSet"
} -->
