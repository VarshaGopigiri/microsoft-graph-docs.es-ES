---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Miniatura
ms.openlocfilehash: 8e56612185028891cf380d3240c999af78ff4740
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086648"
---
# <a name="thumbnail-resource-type"></a><span data-ttu-id="879b7-102">Tipo de recurso thumbnail</span><span class="sxs-lookup"><span data-stu-id="879b7-102">Thumbnail resource type</span></span>

> <span data-ttu-id="879b7-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="879b7-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="879b7-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="879b7-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="879b7-105">El tipo de recurso **thumbnail** representa una miniatura de una imagen, un vídeo, un documento o cualquier elemento que tenga una representación en mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="879b7-105">The **thumbnail** resource type represents a thumbnail for an image, video, document, or any item that has a bitmap representation.</span></span>

## <a name="json-representation"></a><span data-ttu-id="879b7-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="879b7-106">JSON representation</span></span>

<span data-ttu-id="879b7-107">A continuación se incluye una representación JSON del recurso **thumbnail**.</span><span class="sxs-lookup"><span data-stu-id="879b7-107">Here is a JSON representation of the **thumbnail** resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="879b7-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="879b7-108">Properties</span></span>

| <span data-ttu-id="879b7-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="879b7-109">Property</span></span>     | <span data-ttu-id="879b7-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="879b7-110">Type</span></span>   | <span data-ttu-id="879b7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="879b7-111">Description</span></span>                                                                                                                 |
| :----------- | :----- | :-------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="879b7-112">height</span><span class="sxs-lookup"><span data-stu-id="879b7-112">height</span></span>       | <span data-ttu-id="879b7-113">Int32</span><span class="sxs-lookup"><span data-stu-id="879b7-113">Int32</span></span>  | <span data-ttu-id="879b7-114">Alto de la miniatura en píxeles.</span><span class="sxs-lookup"><span data-stu-id="879b7-114">The height of the thumbnail, in pixels.</span></span>                                                                                     |
| <span data-ttu-id="879b7-115">sourceItemId</span><span class="sxs-lookup"><span data-stu-id="879b7-115">sourceItemId</span></span> | <span data-ttu-id="879b7-116">String</span><span class="sxs-lookup"><span data-stu-id="879b7-116">String</span></span> | <span data-ttu-id="879b7-p102">Identificador único del elemento que proporciona la vista en miniatura. Solo está disponible cuando se solicita la miniatura de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="879b7-p102">The unique identifier of the item that provided the thumbnail. This is only available when a folder thumbnail is requested.</span></span> |
| <span data-ttu-id="879b7-119">url</span><span class="sxs-lookup"><span data-stu-id="879b7-119">url</span></span>          | <span data-ttu-id="879b7-120">String</span><span class="sxs-lookup"><span data-stu-id="879b7-120">String</span></span> | <span data-ttu-id="879b7-121">Dirección URL usada para recuperar el contenido de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="879b7-121">The URL used to fetch the thumbnail content.</span></span>                                                                                |
| <span data-ttu-id="879b7-122">width</span><span class="sxs-lookup"><span data-stu-id="879b7-122">width</span></span>        | <span data-ttu-id="879b7-123">Int32</span><span class="sxs-lookup"><span data-stu-id="879b7-123">Int32</span></span>  | <span data-ttu-id="879b7-124">Ancho de la miniatura en píxeles.</span><span class="sxs-lookup"><span data-stu-id="879b7-124">The width of the thumbnail, in pixels.</span></span>                                                                                      |

## <a name="relationships"></a><span data-ttu-id="879b7-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="879b7-125">Relationships</span></span>

| <span data-ttu-id="879b7-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="879b7-126">Name</span></span>    | <span data-ttu-id="879b7-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="879b7-127">Type</span></span>   | <span data-ttu-id="879b7-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="879b7-128">Description</span></span>                           |
| :------ | :----- | :------------------------------------ |
| <span data-ttu-id="879b7-129">content</span><span class="sxs-lookup"><span data-stu-id="879b7-129">content</span></span> | <span data-ttu-id="879b7-130">Secuencia</span><span class="sxs-lookup"><span data-stu-id="879b7-130">Stream</span></span> | <span data-ttu-id="879b7-131">La secuencia de contenido de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="879b7-131">The content stream for the thumbnail.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Thumbnail resource represents a single thumbnail for an item.",
  "section": "documentation",
  "tocPath": "Resources/Thumbnail"
} -->
