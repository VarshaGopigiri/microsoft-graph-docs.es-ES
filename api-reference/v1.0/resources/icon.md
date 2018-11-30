---
title: Tipo de recurso Icon
description: Representa un icono de celda.
ms.openlocfilehash: 9485a831241ce92be3f8e7c4df5173285f926bbf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031392"
---
# <a name="icon-resource-type"></a><span data-ttu-id="19f74-103">Tipo de recurso Icon</span><span class="sxs-lookup"><span data-stu-id="19f74-103">Icon resource type</span></span>

<span data-ttu-id="19f74-104">Representa un icono de celda.</span><span class="sxs-lookup"><span data-stu-id="19f74-104">Represents a cell icon.</span></span>


## <a name="methods"></a><span data-ttu-id="19f74-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="19f74-105">Methods</span></span>

| <span data-ttu-id="19f74-106">Método</span><span class="sxs-lookup"><span data-stu-id="19f74-106">Method</span></span>           | <span data-ttu-id="19f74-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19f74-107">Return Type</span></span>    |<span data-ttu-id="19f74-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="19f74-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="19f74-109">Get Icon</span><span class="sxs-lookup"><span data-stu-id="19f74-109">Get Icon</span></span>](../api/icon-get.md) | [<span data-ttu-id="19f74-110">Icon</span><span class="sxs-lookup"><span data-stu-id="19f74-110">Icon</span></span>](icon.md) |<span data-ttu-id="19f74-111">Lee las propiedades y relaciones del objeto icon.</span><span class="sxs-lookup"><span data-stu-id="19f74-111">Read properties and relationships of icon object.</span></span>|
|[<span data-ttu-id="19f74-112">Update</span><span class="sxs-lookup"><span data-stu-id="19f74-112">Update</span></span>](../api/icon-update.md) | [<span data-ttu-id="19f74-113">Icon</span><span class="sxs-lookup"><span data-stu-id="19f74-113">Icon</span></span>](icon.md)  |<span data-ttu-id="19f74-114">Actualiza el objeto Icon.</span><span class="sxs-lookup"><span data-stu-id="19f74-114">Update Icon object.</span></span> |

## <a name="properties"></a><span data-ttu-id="19f74-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19f74-115">Properties</span></span>
| <span data-ttu-id="19f74-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="19f74-116">Property</span></span>     | <span data-ttu-id="19f74-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="19f74-117">Type</span></span>   |<span data-ttu-id="19f74-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="19f74-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="19f74-119">index</span><span class="sxs-lookup"><span data-stu-id="19f74-119">index</span></span>|<span data-ttu-id="19f74-120">int</span><span class="sxs-lookup"><span data-stu-id="19f74-120">int</span></span>|<span data-ttu-id="19f74-121">Representa el índice del icono en el conjunto concreto.</span><span class="sxs-lookup"><span data-stu-id="19f74-121">Represents the index of the icon in the given set.</span></span>|
|<span data-ttu-id="19f74-122">set</span><span class="sxs-lookup"><span data-stu-id="19f74-122">set</span></span>|<span data-ttu-id="19f74-123">string</span><span class="sxs-lookup"><span data-stu-id="19f74-123">string</span></span>|<span data-ttu-id="19f74-124">Representa el conjunto de que el icono de forma parte de.</span><span class="sxs-lookup"><span data-stu-id="19f74-124">Represents the set that the icon is part of.</span></span> <span data-ttu-id="19f74-125">Los valores posibles son: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars` , `ThreeTriangles`, `FiveBoxes`.</span><span class="sxs-lookup"><span data-stu-id="19f74-125">The possible values are: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles`, `FiveBoxes`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="19f74-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="19f74-126">Relationships</span></span>
<span data-ttu-id="19f74-127">Ninguno</span><span class="sxs-lookup"><span data-stu-id="19f74-127">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="19f74-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="19f74-128">JSON representation</span></span>

<span data-ttu-id="19f74-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="19f74-129">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookIcon"
}-->

```json
{
  "index": 1024,
  "set": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Icon resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->