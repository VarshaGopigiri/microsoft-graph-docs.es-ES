---
title: Tipo de recurso plannerCategoryDescriptions
description: 'El recurso **plannerCategoryDescriptions** representa las etiquetas descriptivas de las categorías que se han definido para un plan. Pertenece al objeto plan details. Puede haber hasta 6 categorías definidas. '
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 4175692182d115e884642ef8f9956cc4db5dae2e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27930946"
---
# <a name="plannercategorydescriptions-resource-type"></a><span data-ttu-id="31977-105">Tipo de recurso plannerCategoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="31977-105">plannerCategoryDescriptions resource type</span></span>

> <span data-ttu-id="31977-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="31977-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="31977-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="31977-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="31977-p103">El recurso **plannerCategoryDescriptions** representa las etiquetas descriptivas de las categorías que se han definido para un plan. Pertenece al objeto [plan details](plannerplandetails.md). Puede haber hasta 6 categorías definidas.</span><span class="sxs-lookup"><span data-stu-id="31977-p103">The **plannerCategoryDescriptions** resource represents the descriptive labels for the categories that have been defined for a plan. It belongs to the [plan details](plannerplandetails.md) object. There can be up to 6 categories defined.</span></span> 


## <a name="properties"></a><span data-ttu-id="31977-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31977-111">Properties</span></span>
| <span data-ttu-id="31977-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31977-112">Property</span></span>     | <span data-ttu-id="31977-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="31977-113">Type</span></span>   |<span data-ttu-id="31977-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="31977-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="31977-115">category1</span><span class="sxs-lookup"><span data-stu-id="31977-115">category1</span></span>|<span data-ttu-id="31977-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="31977-116">String</span></span>|<span data-ttu-id="31977-117">Etiqueta asociada a la categoría 1</span><span class="sxs-lookup"><span data-stu-id="31977-117">The label associated with Category 1</span></span>|
|<span data-ttu-id="31977-118">category2</span><span class="sxs-lookup"><span data-stu-id="31977-118">category2</span></span>|<span data-ttu-id="31977-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="31977-119">String</span></span>|<span data-ttu-id="31977-120">Etiqueta asociada a la categoría 2</span><span class="sxs-lookup"><span data-stu-id="31977-120">The label associated with Category 2</span></span>|
|<span data-ttu-id="31977-121">category3</span><span class="sxs-lookup"><span data-stu-id="31977-121">category3</span></span>|<span data-ttu-id="31977-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="31977-122">String</span></span>|<span data-ttu-id="31977-123">Etiqueta asociada a la categoría 3</span><span class="sxs-lookup"><span data-stu-id="31977-123">The label associated with Category 3</span></span>|
|<span data-ttu-id="31977-124">category4</span><span class="sxs-lookup"><span data-stu-id="31977-124">category4</span></span>|<span data-ttu-id="31977-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="31977-125">String</span></span>|<span data-ttu-id="31977-126">Etiqueta asociada a la categoría 4</span><span class="sxs-lookup"><span data-stu-id="31977-126">The label associated with Category 4</span></span>|
|<span data-ttu-id="31977-127">category5</span><span class="sxs-lookup"><span data-stu-id="31977-127">category5</span></span>|<span data-ttu-id="31977-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="31977-128">String</span></span>|<span data-ttu-id="31977-129">Etiqueta asociada a la categoría 5</span><span class="sxs-lookup"><span data-stu-id="31977-129">The label associated with Category 5</span></span>|
|<span data-ttu-id="31977-130">category6</span><span class="sxs-lookup"><span data-stu-id="31977-130">category6</span></span>|<span data-ttu-id="31977-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="31977-131">String</span></span>|<span data-ttu-id="31977-132">Etiqueta asociada a la categoría 6</span><span class="sxs-lookup"><span data-stu-id="31977-132">The label associated with Category 6</span></span>|

## <a name="json-representation"></a><span data-ttu-id="31977-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="31977-133">JSON representation</span></span>
<span data-ttu-id="31977-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="31977-134">Here is a JSON representation of the resource.</span></span>

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
