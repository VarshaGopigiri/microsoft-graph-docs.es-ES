---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: ThumbnailSet
localization_priority: Normal
ms.openlocfilehash: 145134d6a3ad85134ea2d6c4d72e050bc17b31d1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830194"
---
# <a name="thumbnailset-resource-type"></a><span data-ttu-id="8daad-102">Tipo de recurso ThumbnailSet</span><span class="sxs-lookup"><span data-stu-id="8daad-102">ThumbnailSet resource type</span></span>

> <span data-ttu-id="8daad-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8daad-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8daad-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8daad-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8daad-p102">El recurso **ThumbnailSet** es una colección de claves de recursos [thumbnail](thumbnail.md). Se usa para representar un conjunto de miniaturas asociadas a un DriveItem.</span><span class="sxs-lookup"><span data-stu-id="8daad-p102">The **ThumbnailSet** resource is a keyed collection of [thumbnail](thumbnail.md) resources. It is used to represent a set of thumbnails associated with a DriveItem.</span></span>

## <a name="json-representation"></a><span data-ttu-id="8daad-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8daad-107">JSON representation</span></span>

<span data-ttu-id="8daad-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8daad-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": ["source", "small", "medium", "large"],
  "openType": true,
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.thumbnailSet"
} -->

```json
{
  "id": "string (identifier)",
  "large": { "@odata.type": "microsoft.graph.thumbnail" },
  "medium": { "@odata.type": "microsoft.graph.thumbnail" },
  "small": { "@odata.type": "microsoft.graph.thumbnail" },
  "source": { "@odata.type": "microsoft.graph.thumbnail" }
}
```

## <a name="properties"></a><span data-ttu-id="8daad-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8daad-109">Properties</span></span>

| <span data-ttu-id="8daad-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8daad-110">Property</span></span> | <span data-ttu-id="8daad-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="8daad-111">Type</span></span>                      | <span data-ttu-id="8daad-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8daad-112">Description</span></span>                                                                       |
|:---------|:--------------------------|:----------------------------------------------------------------------------------|
| <span data-ttu-id="8daad-113">id</span><span class="sxs-lookup"><span data-stu-id="8daad-113">id</span></span>       | <span data-ttu-id="8daad-114">String</span><span class="sxs-lookup"><span data-stu-id="8daad-114">String</span></span>                    | <span data-ttu-id="8daad-p103">Identificador del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8daad-p103">The id within the item. Read-only.</span></span>                                                |
| <span data-ttu-id="8daad-117">large</span><span class="sxs-lookup"><span data-stu-id="8daad-117">large</span></span>    | [<span data-ttu-id="8daad-118">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="8daad-118">Thumbnail</span></span>](thumbnail.md) | <span data-ttu-id="8daad-119">Miniatura escalada de 1920 x 1920.</span><span class="sxs-lookup"><span data-stu-id="8daad-119">A 1920x1920 scaled thumbnail.</span></span>                                                     |
| <span data-ttu-id="8daad-120">medium</span><span class="sxs-lookup"><span data-stu-id="8daad-120">medium</span></span>   | [<span data-ttu-id="8daad-121">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="8daad-121">Thumbnail</span></span>](thumbnail.md) | <span data-ttu-id="8daad-122">Miniatura escalada de 176 x 176.</span><span class="sxs-lookup"><span data-stu-id="8daad-122">A 176x176 scaled thumbnail.</span></span>                                                       |
| <span data-ttu-id="8daad-123">small</span><span class="sxs-lookup"><span data-stu-id="8daad-123">small</span></span>    | [<span data-ttu-id="8daad-124">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="8daad-124">Thumbnail</span></span>](thumbnail.md) | <span data-ttu-id="8daad-125">Miniatura recortada de 48 x 48.</span><span class="sxs-lookup"><span data-stu-id="8daad-125">A 48x48 cropped thumbnail.</span></span>                                                        |
| <span data-ttu-id="8daad-126">source</span><span class="sxs-lookup"><span data-stu-id="8daad-126">source</span></span>   | [<span data-ttu-id="8daad-127">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="8daad-127">Thumbnail</span></span>](thumbnail.md) | <span data-ttu-id="8daad-128">Imagen en miniatura personalizada o imagen original usada para generar otras miniaturas.</span><span class="sxs-lookup"><span data-stu-id="8daad-128">A custom thumbnail image or the original image used to generate other thumbnails.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ThumbnailSet enables access to thumbnails of different sizes",
  "section": "documentation",
  "tocPath": "Resources/ThumbnailSet"
} -->
