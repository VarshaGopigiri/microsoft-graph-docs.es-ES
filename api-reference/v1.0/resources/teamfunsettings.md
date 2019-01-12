---
title: tipo de recurso teamFunSettings
description: Opciones para configurar el uso de Giphy, memes y pegatinas en el equipo.
localization_priority: Normal
author: nkramer
ms.prod: microsoft-teams
ms.openlocfilehash: c701ffe76c82a6cb4b3586272926290f634a02d9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987674"
---
# <a name="teamfunsettings-resource-type"></a><span data-ttu-id="d190c-103">tipo de recurso teamFunSettings</span><span class="sxs-lookup"><span data-stu-id="d190c-103">teamFunSettings resource type</span></span>



<span data-ttu-id="d190c-104">Opciones para configurar el uso de Giphy, memes y pegatinas en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="d190c-104">Settings to configure use of Giphy, memes, and stickers in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d190c-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d190c-105">Properties</span></span>
| <span data-ttu-id="d190c-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d190c-106">Property</span></span>     | <span data-ttu-id="d190c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d190c-107">Type</span></span>   |<span data-ttu-id="d190c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d190c-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d190c-109">allowGiphy</span><span class="sxs-lookup"><span data-stu-id="d190c-109">allowGiphy</span></span>|<span data-ttu-id="d190c-110">Booleano</span><span class="sxs-lookup"><span data-stu-id="d190c-110">Boolean</span></span>|<span data-ttu-id="d190c-111">Si establece en verdadero, permite el uso de Giphy.</span><span class="sxs-lookup"><span data-stu-id="d190c-111">If set to true, enables Giphy use.</span></span>|
|<span data-ttu-id="d190c-112">giphyContentRating</span><span class="sxs-lookup"><span data-stu-id="d190c-112">giphyContentRating</span></span>|<span data-ttu-id="d190c-113">Cadena (enumeración)</span><span class="sxs-lookup"><span data-stu-id="d190c-113">String (enum)</span></span>|<span data-ttu-id="d190c-114">Clasificación de contenido de Giphy.</span><span class="sxs-lookup"><span data-stu-id="d190c-114">Giphy content rating.</span></span> <span data-ttu-id="d190c-115">Los valores posibles son: `moderate` y `strict`.</span><span class="sxs-lookup"><span data-stu-id="d190c-115">Possible values are: `moderate`, `strict`.</span></span>|
|<span data-ttu-id="d190c-116">allowStickersAndMemes</span><span class="sxs-lookup"><span data-stu-id="d190c-116">allowStickersAndMemes</span></span>|<span data-ttu-id="d190c-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="d190c-117">Boolean</span></span>|<span data-ttu-id="d190c-118">Si establece en true, permite a los usuarios para que incluya pegatinas y memes.</span><span class="sxs-lookup"><span data-stu-id="d190c-118">If set to true, enables users to include stickers and memes.</span></span>|
|<span data-ttu-id="d190c-119">allowCustomMemes</span><span class="sxs-lookup"><span data-stu-id="d190c-119">allowCustomMemes</span></span>|<span data-ttu-id="d190c-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="d190c-120">Boolean</span></span>|<span data-ttu-id="d190c-121">Si establece en true, permite a los usuarios para incluir memes personalizado.</span><span class="sxs-lookup"><span data-stu-id="d190c-121">If set to true, enables users to include custom memes.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d190c-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d190c-122">JSON representation</span></span>

<span data-ttu-id="d190c-123">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d190c-123">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamFunSettings"
}-->

```json
{
  "allowGiphy": true,
  "giphyContentRating": "strict",
  "allowStickersAndMemes": true,
  "allowCustomMemes": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's funSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
