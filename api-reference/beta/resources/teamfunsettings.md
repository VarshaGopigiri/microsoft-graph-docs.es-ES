---
title: tipo de recurso teamFunSettings
description: Opciones para configurar el uso de Giphy, memes y pegatinas en el equipo.
localization_priority: Normal
ms.openlocfilehash: c53d3215e5f515361c66fe2d3d0ad10a5338e0c4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852069"
---
# <a name="teamfunsettings-resource-type"></a><span data-ttu-id="ff54e-103">tipo de recurso teamFunSettings</span><span class="sxs-lookup"><span data-stu-id="ff54e-103">teamFunSettings resource type</span></span>

> <span data-ttu-id="ff54e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ff54e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ff54e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ff54e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ff54e-106">Opciones para configurar el uso de Giphy, memes y pegatinas en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="ff54e-106">Settings to configure use of Giphy, memes, and stickers in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ff54e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff54e-107">Properties</span></span>
| <span data-ttu-id="ff54e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ff54e-108">Property</span></span>     | <span data-ttu-id="ff54e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff54e-109">Type</span></span>   |<span data-ttu-id="ff54e-110">Description</span><span class="sxs-lookup"><span data-stu-id="ff54e-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ff54e-111">allowGiphy</span><span class="sxs-lookup"><span data-stu-id="ff54e-111">allowGiphy</span></span>|<span data-ttu-id="ff54e-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="ff54e-112">Boolean</span></span>|<span data-ttu-id="ff54e-113">Si establece en verdadero, permite el uso de Giphy.</span><span class="sxs-lookup"><span data-stu-id="ff54e-113">If set to true, enables Giphy use.</span></span>|
|<span data-ttu-id="ff54e-114">giphyContentRating</span><span class="sxs-lookup"><span data-stu-id="ff54e-114">giphyContentRating</span></span>|<span data-ttu-id="ff54e-115">Cadena (enumeración)</span><span class="sxs-lookup"><span data-stu-id="ff54e-115">String (enum)</span></span>|<span data-ttu-id="ff54e-116">Clasificación de contenido de Giphy.</span><span class="sxs-lookup"><span data-stu-id="ff54e-116">Giphy content rating.</span></span> <span data-ttu-id="ff54e-117">Los valores posibles son: `moderate` y `strict`.</span><span class="sxs-lookup"><span data-stu-id="ff54e-117">Possible values are: `moderate`, `strict`.</span></span>|
|<span data-ttu-id="ff54e-118">allowStickersAndMemes</span><span class="sxs-lookup"><span data-stu-id="ff54e-118">allowStickersAndMemes</span></span>|<span data-ttu-id="ff54e-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="ff54e-119">Boolean</span></span>|<span data-ttu-id="ff54e-120">Si establece en true, permite a los usuarios para que incluya pegatinas y memes.</span><span class="sxs-lookup"><span data-stu-id="ff54e-120">If set to true, enables users to include stickers and memes.</span></span>|
|<span data-ttu-id="ff54e-121">allowCustomMemes</span><span class="sxs-lookup"><span data-stu-id="ff54e-121">allowCustomMemes</span></span>|<span data-ttu-id="ff54e-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="ff54e-122">Boolean</span></span>|<span data-ttu-id="ff54e-123">Si establece en true, permite a los usuarios para incluir memes personalizado.</span><span class="sxs-lookup"><span data-stu-id="ff54e-123">If set to true, enables users to include custom memes.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ff54e-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ff54e-124">JSON representation</span></span>

<span data-ttu-id="ff54e-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ff54e-125">The following is a JSON representation of the resource.</span></span>

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
