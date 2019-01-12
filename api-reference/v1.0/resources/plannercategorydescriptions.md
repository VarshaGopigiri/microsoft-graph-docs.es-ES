---
title: Tipo de recurso plannerCategoryDescriptions
description: 'El recurso **plannerCategoryDescriptions** representa las etiquetas descriptivas de las categorías que se han definido para un plan. Pertenece al objeto plan details. Puede haber hasta 6 categorías definidas. '
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 1cf1ee1c6e8ccc4e90f78985b352062fce37df88
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984349"
---
# <a name="plannercategorydescriptions-resource-type"></a><span data-ttu-id="6b85c-105">Tipo de recurso plannerCategoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="6b85c-105">plannerCategoryDescriptions resource type</span></span>

<span data-ttu-id="6b85c-p102">El recurso **plannerCategoryDescriptions** representa las etiquetas descriptivas de las categorías que se han definido para un plan. Pertenece al objeto [plan details](plannerplandetails.md). Puede haber hasta 6 categorías definidas.</span><span class="sxs-lookup"><span data-stu-id="6b85c-p102">The **plannerCategoryDescriptions** resource represents the descriptive labels for the categories that have been defined for a plan. It belongs to the [plan details](plannerplandetails.md) object. There can be up to 6 categories defined.</span></span> 


## <a name="properties"></a><span data-ttu-id="6b85c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b85c-109">Properties</span></span>
| <span data-ttu-id="6b85c-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6b85c-110">Property</span></span>     | <span data-ttu-id="6b85c-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="6b85c-111">Type</span></span>   |<span data-ttu-id="6b85c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b85c-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6b85c-113">category1</span><span class="sxs-lookup"><span data-stu-id="6b85c-113">category1</span></span>|<span data-ttu-id="6b85c-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="6b85c-114">String</span></span>|<span data-ttu-id="6b85c-115">Etiqueta asociada a la categoría 1</span><span class="sxs-lookup"><span data-stu-id="6b85c-115">The label associated with Category 1</span></span>|
|<span data-ttu-id="6b85c-116">category2</span><span class="sxs-lookup"><span data-stu-id="6b85c-116">category2</span></span>|<span data-ttu-id="6b85c-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="6b85c-117">String</span></span>|<span data-ttu-id="6b85c-118">Etiqueta asociada a la categoría 2</span><span class="sxs-lookup"><span data-stu-id="6b85c-118">The label associated with Category 2</span></span>|
|<span data-ttu-id="6b85c-119">category3</span><span class="sxs-lookup"><span data-stu-id="6b85c-119">category3</span></span>|<span data-ttu-id="6b85c-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="6b85c-120">String</span></span>|<span data-ttu-id="6b85c-121">Etiqueta asociada a la categoría 3</span><span class="sxs-lookup"><span data-stu-id="6b85c-121">The label associated with Category 3</span></span>|
|<span data-ttu-id="6b85c-122">category4</span><span class="sxs-lookup"><span data-stu-id="6b85c-122">category4</span></span>|<span data-ttu-id="6b85c-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="6b85c-123">String</span></span>|<span data-ttu-id="6b85c-124">Etiqueta asociada a la categoría 4</span><span class="sxs-lookup"><span data-stu-id="6b85c-124">The label associated with Category 4</span></span>|
|<span data-ttu-id="6b85c-125">category5</span><span class="sxs-lookup"><span data-stu-id="6b85c-125">category5</span></span>|<span data-ttu-id="6b85c-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="6b85c-126">String</span></span>|<span data-ttu-id="6b85c-127">Etiqueta asociada a la categoría 5</span><span class="sxs-lookup"><span data-stu-id="6b85c-127">The label associated with Category 5</span></span>|
|<span data-ttu-id="6b85c-128">category6</span><span class="sxs-lookup"><span data-stu-id="6b85c-128">category6</span></span>|<span data-ttu-id="6b85c-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="6b85c-129">String</span></span>|<span data-ttu-id="6b85c-130">Etiqueta asociada a la categoría 6</span><span class="sxs-lookup"><span data-stu-id="6b85c-130">The label associated with Category 6</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6b85c-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6b85c-131">JSON representation</span></span>
<span data-ttu-id="6b85c-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6b85c-132">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerCategoryDescriptions"
}-->

```json
{
  "category1": "String",
  "category2": "String",
  "category3": "String",
  "category4": "String",
  "category5": "String",
  "category6": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerCategoryDescriptions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
