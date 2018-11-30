---
title: Tipo de recurso Icon
description: Representa un icono de celda.
ms.openlocfilehash: fd3e0682a7eb73dd4e3286e11d9f9680755db265
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085172"
---
# <a name="icon-resource-type"></a><span data-ttu-id="3a650-103">Tipo de recurso Icon</span><span class="sxs-lookup"><span data-stu-id="3a650-103">Icon resource type</span></span>

> <span data-ttu-id="3a650-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3a650-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3a650-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3a650-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3a650-106">Representa un icono de celda.</span><span class="sxs-lookup"><span data-stu-id="3a650-106">Represents a cell icon.</span></span>


## <a name="methods"></a><span data-ttu-id="3a650-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a650-107">Methods</span></span>

| <span data-ttu-id="3a650-108">Método</span><span class="sxs-lookup"><span data-stu-id="3a650-108">Method</span></span>           | <span data-ttu-id="3a650-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a650-109">Return Type</span></span>    |<span data-ttu-id="3a650-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a650-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="3a650-111">Get Icon</span><span class="sxs-lookup"><span data-stu-id="3a650-111">Get Icon</span></span>](../api/icon-get.md) | [<span data-ttu-id="3a650-112">Icon</span><span class="sxs-lookup"><span data-stu-id="3a650-112">Icon</span></span>](icon.md) |<span data-ttu-id="3a650-113">Lee las propiedades y relaciones del objeto icon.</span><span class="sxs-lookup"><span data-stu-id="3a650-113">Read properties and relationships of icon object.</span></span>|
|[<span data-ttu-id="3a650-114">Update</span><span class="sxs-lookup"><span data-stu-id="3a650-114">Update</span></span>](../api/icon-update.md) | [<span data-ttu-id="3a650-115">Icon</span><span class="sxs-lookup"><span data-stu-id="3a650-115">Icon</span></span>](icon.md)  |<span data-ttu-id="3a650-116">Actualiza el objeto Icon.</span><span class="sxs-lookup"><span data-stu-id="3a650-116">Update Icon object.</span></span> |

## <a name="properties"></a><span data-ttu-id="3a650-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a650-117">Properties</span></span>
| <span data-ttu-id="3a650-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3a650-118">Property</span></span>     | <span data-ttu-id="3a650-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a650-119">Type</span></span>   |<span data-ttu-id="3a650-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a650-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3a650-121">index</span><span class="sxs-lookup"><span data-stu-id="3a650-121">index</span></span>|<span data-ttu-id="3a650-122">int</span><span class="sxs-lookup"><span data-stu-id="3a650-122">int</span></span>|<span data-ttu-id="3a650-123">Representa el índice del icono en el conjunto concreto.</span><span class="sxs-lookup"><span data-stu-id="3a650-123">Represents the index of the icon in the given set.</span></span>|
|<span data-ttu-id="3a650-124">set</span><span class="sxs-lookup"><span data-stu-id="3a650-124">set</span></span>|<span data-ttu-id="3a650-125">string</span><span class="sxs-lookup"><span data-stu-id="3a650-125">string</span></span>|<span data-ttu-id="3a650-p102">Representa el conjunto al que pertenece el icono. Valores posibles: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles`, `FiveBoxes`.</span><span class="sxs-lookup"><span data-stu-id="3a650-p102">Represents the set that the icon is part of. Possible values are: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles`, `FiveBoxes`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3a650-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3a650-128">Relationships</span></span>
<span data-ttu-id="3a650-129">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3a650-129">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="3a650-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3a650-130">JSON representation</span></span>

<span data-ttu-id="3a650-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3a650-131">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.icon"
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