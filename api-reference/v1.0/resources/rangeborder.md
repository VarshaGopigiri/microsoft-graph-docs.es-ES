---
title: Tipo de recurso RangeBorder
description: Representa el borde de un objeto.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 4b20078b7d4d0cabf4c16e212fd3e9264cad1650
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830803"
---
# <a name="rangeborder-resource-type"></a><span data-ttu-id="09c2e-103">Tipo de recurso RangeBorder</span><span class="sxs-lookup"><span data-stu-id="09c2e-103">RangeBorder resource type</span></span>

<span data-ttu-id="09c2e-104">Representa el borde de un objeto.</span><span class="sxs-lookup"><span data-stu-id="09c2e-104">Represents the border of an object.</span></span>


## <a name="methods"></a><span data-ttu-id="09c2e-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="09c2e-105">Methods</span></span>

| <span data-ttu-id="09c2e-106">Método</span><span class="sxs-lookup"><span data-stu-id="09c2e-106">Method</span></span>           | <span data-ttu-id="09c2e-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09c2e-107">Return Type</span></span>    |<span data-ttu-id="09c2e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="09c2e-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="09c2e-109">Get RangeBorder</span><span class="sxs-lookup"><span data-stu-id="09c2e-109">Get RangeBorder</span></span>](../api/rangeborder-get.md) | [<span data-ttu-id="09c2e-110">WorkbookRangeBorder</span><span class="sxs-lookup"><span data-stu-id="09c2e-110">WorkbookRangeBorder</span></span>](rangeborder.md) |<span data-ttu-id="09c2e-111">Lee las propiedades y relaciones del objeto rangeBorder.</span><span class="sxs-lookup"><span data-stu-id="09c2e-111">Read properties and relationships of rangeBorder object.</span></span>|
|[<span data-ttu-id="09c2e-112">Update</span><span class="sxs-lookup"><span data-stu-id="09c2e-112">Update</span></span>](../api/rangeborder-update.md) | [<span data-ttu-id="09c2e-113">WorkbookRangeBorder</span><span class="sxs-lookup"><span data-stu-id="09c2e-113">WorkbookRangeBorder</span></span>](rangeborder.md) |<span data-ttu-id="09c2e-114">Actualiza el objeto RangeBorder.</span><span class="sxs-lookup"><span data-stu-id="09c2e-114">Update RangeBorder object.</span></span> |
|[<span data-ttu-id="09c2e-115">List</span><span class="sxs-lookup"><span data-stu-id="09c2e-115">List</span></span>](../api/rangeborder-list.md) | <span data-ttu-id="09c2e-116">Colección de [WorkbookRangeBorder](rangeborder.md)</span><span class="sxs-lookup"><span data-stu-id="09c2e-116">[WorkbookRangeBorder](rangeborder.md) collection</span></span> |<span data-ttu-id="09c2e-117">Obtiene la colección de objetos rangeBorder.</span><span class="sxs-lookup"><span data-stu-id="09c2e-117">Get rangeBorder object collection.</span></span> |
|[<span data-ttu-id="09c2e-118">Itemat</span><span class="sxs-lookup"><span data-stu-id="09c2e-118">Itemat</span></span>](../api/rangebordercollection-itemat.md)|[<span data-ttu-id="09c2e-119">WorkbookRangeBorder</span><span class="sxs-lookup"><span data-stu-id="09c2e-119">WorkbookRangeBorder</span></span>](rangeborder.md)|<span data-ttu-id="09c2e-120">Obtiene un objeto de borde mediante su índice.</span><span class="sxs-lookup"><span data-stu-id="09c2e-120">Gets a border object using its index</span></span>|

## <a name="properties"></a><span data-ttu-id="09c2e-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09c2e-121">Properties</span></span>
| <span data-ttu-id="09c2e-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="09c2e-122">Property</span></span>     | <span data-ttu-id="09c2e-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="09c2e-123">Type</span></span>   |<span data-ttu-id="09c2e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="09c2e-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="09c2e-125">color</span><span class="sxs-lookup"><span data-stu-id="09c2e-125">color</span></span>|<span data-ttu-id="09c2e-126">string</span><span class="sxs-lookup"><span data-stu-id="09c2e-126">string</span></span>|<span data-ttu-id="09c2e-127">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="09c2e-127">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|
|<span data-ttu-id="09c2e-128">id</span><span class="sxs-lookup"><span data-stu-id="09c2e-128">id</span></span>|<span data-ttu-id="09c2e-129">string</span><span class="sxs-lookup"><span data-stu-id="09c2e-129">string</span></span>|<span data-ttu-id="09c2e-130">Representa el identificador del borde.</span><span class="sxs-lookup"><span data-stu-id="09c2e-130">Represents border identifier.</span></span> <span data-ttu-id="09c2e-131">Los valores posibles son: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`.</span><span class="sxs-lookup"><span data-stu-id="09c2e-131">The possible values are: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`.</span></span> <span data-ttu-id="09c2e-132">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09c2e-132">Read-only.</span></span>|
|<span data-ttu-id="09c2e-133">sideIndex</span><span class="sxs-lookup"><span data-stu-id="09c2e-133">sideIndex</span></span>|<span data-ttu-id="09c2e-134">string</span><span class="sxs-lookup"><span data-stu-id="09c2e-134">string</span></span>|<span data-ttu-id="09c2e-135">Valor constante que indica el lado específico del borde.</span><span class="sxs-lookup"><span data-stu-id="09c2e-135">Constant value that indicates the specific side of the border.</span></span> <span data-ttu-id="09c2e-136">Los valores posibles son: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`.</span><span class="sxs-lookup"><span data-stu-id="09c2e-136">The possible values are: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`.</span></span> <span data-ttu-id="09c2e-137">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09c2e-137">Read-only.</span></span>|
|<span data-ttu-id="09c2e-138">style</span><span class="sxs-lookup"><span data-stu-id="09c2e-138">style</span></span>|<span data-ttu-id="09c2e-139">string</span><span class="sxs-lookup"><span data-stu-id="09c2e-139">string</span></span>|<span data-ttu-id="09c2e-140">Una de las constantes de estilo de línea que especifica el estilo de línea para el borde.</span><span class="sxs-lookup"><span data-stu-id="09c2e-140">One of the constants of line style specifying the line style for the border.</span></span> <span data-ttu-id="09c2e-141">Los valores posibles son: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.</span><span class="sxs-lookup"><span data-stu-id="09c2e-141">The possible values are: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.</span></span>|
|<span data-ttu-id="09c2e-142">weight</span><span class="sxs-lookup"><span data-stu-id="09c2e-142">weight</span></span>|<span data-ttu-id="09c2e-143">string</span><span class="sxs-lookup"><span data-stu-id="09c2e-143">string</span></span>|<span data-ttu-id="09c2e-144">Especifica el grosor del borde que rodea un rango.</span><span class="sxs-lookup"><span data-stu-id="09c2e-144">Specifies the weight of the border around a range.</span></span> <span data-ttu-id="09c2e-145">Los valores posibles son: `Hairline`, `Thin`, `Medium`, `Thick`.</span><span class="sxs-lookup"><span data-stu-id="09c2e-145">The possible values are: `Hairline`, `Thin`, `Medium`, `Thick`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="09c2e-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="09c2e-146">Relationships</span></span>
<span data-ttu-id="09c2e-147">Ninguno</span><span class="sxs-lookup"><span data-stu-id="09c2e-147">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="09c2e-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="09c2e-148">JSON representation</span></span>

<span data-ttu-id="09c2e-149">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="09c2e-149">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookRangeBorder"
}-->

```json
{
  "color": "string",
  "id": "string",
  "sideIndex": "string",
  "style": "string",
  "weight": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeBorder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
