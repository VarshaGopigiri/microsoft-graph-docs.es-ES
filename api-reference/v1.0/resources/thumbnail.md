---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Miniatura
ms.openlocfilehash: 065c6ae7bbd4f6aca3172afd4399f0a1b5ff3d25
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="thumbnail-resource-type"></a><span data-ttu-id="f9a74-102">Tipo de recurso thumbnail</span><span class="sxs-lookup"><span data-stu-id="f9a74-102">Thumbnail resource type</span></span>

<span data-ttu-id="f9a74-103">El tipo de recurso **thumbnail** representa una miniatura de una imagen, un vídeo, un documento o cualquier elemento que tenga una representación en mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="f9a74-103">The **thumbnail** resource type represents a thumbnail for an image, video, document, or any item that has a bitmap representation.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f9a74-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f9a74-104">JSON representation</span></span>

<span data-ttu-id="f9a74-105">A continuación se incluye una representación JSON del recurso **thumbnail**.</span><span class="sxs-lookup"><span data-stu-id="f9a74-105">Here is a JSON representation of the **thumbnail** resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": ["content", "height", "width", "sourceItemId"],
  "@odata.type": "microsoft.graph.thumbnail"
}-->

```json
{
  "height": 1024,
  "sourceItemId": "string",
  "url": "string",
  "width": 1024,

  /* relationships */
  "content": "stream"
}
```

## <a name="properties"></a><span data-ttu-id="f9a74-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9a74-106">Properties</span></span>

| <span data-ttu-id="f9a74-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f9a74-107">Property</span></span>     | <span data-ttu-id="f9a74-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9a74-108">Type</span></span>   | <span data-ttu-id="f9a74-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9a74-109">Description</span></span>                                                                                                                 |
| :----------- | :----- | :-------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="f9a74-110">height</span><span class="sxs-lookup"><span data-stu-id="f9a74-110">height</span></span>       | <span data-ttu-id="f9a74-111">Int32</span><span class="sxs-lookup"><span data-stu-id="f9a74-111">Int32</span></span>  | <span data-ttu-id="f9a74-112">Alto de la miniatura en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f9a74-112">The height of the thumbnail, in pixels.</span></span>                                                                                     |
| <span data-ttu-id="f9a74-113">sourceItemId</span><span class="sxs-lookup"><span data-stu-id="f9a74-113">sourceItemId</span></span> | <span data-ttu-id="f9a74-114">String</span><span class="sxs-lookup"><span data-stu-id="f9a74-114">String</span></span> | <span data-ttu-id="f9a74-p101">Identificador único del elemento que proporciona la vista en miniatura. Solo está disponible cuando se solicita la miniatura de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f9a74-p101">The unique identifier of the item that provided the thumbnail. This is only available when a folder thumbnail is requested.</span></span> |
| <span data-ttu-id="f9a74-117">url</span><span class="sxs-lookup"><span data-stu-id="f9a74-117">url</span></span>          | <span data-ttu-id="f9a74-118">String</span><span class="sxs-lookup"><span data-stu-id="f9a74-118">String</span></span> | <span data-ttu-id="f9a74-119">Dirección URL usada para recuperar el contenido de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="f9a74-119">The URL used to fetch the thumbnail content.</span></span>                                                                                |
| <span data-ttu-id="f9a74-120">width</span><span class="sxs-lookup"><span data-stu-id="f9a74-120">width</span></span>        | <span data-ttu-id="f9a74-121">Int32</span><span class="sxs-lookup"><span data-stu-id="f9a74-121">Int32</span></span>  | <span data-ttu-id="f9a74-122">Ancho de la miniatura en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f9a74-122">The width of the thumbnail, in pixels.</span></span>                                                                                      |

## <a name="relationships"></a><span data-ttu-id="f9a74-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f9a74-123">Relationships</span></span>

| <span data-ttu-id="f9a74-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="f9a74-124">Name</span></span>    | <span data-ttu-id="f9a74-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9a74-125">Type</span></span>   | <span data-ttu-id="f9a74-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9a74-126">Description</span></span>                           |
| :------ | :----- | :------------------------------------ |
| <span data-ttu-id="f9a74-127">content</span><span class="sxs-lookup"><span data-stu-id="f9a74-127">content</span></span> | <span data-ttu-id="f9a74-128">Secuencia</span><span class="sxs-lookup"><span data-stu-id="f9a74-128">Stream</span></span> | <span data-ttu-id="f9a74-129">La secuencia de contenido de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="f9a74-129">The content stream for the thumbnail.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Thumbnail resource represents a single thumbnail for an item.",
  "section": "documentation",
  "tocPath": "Resources/Thumbnail"
} -->
