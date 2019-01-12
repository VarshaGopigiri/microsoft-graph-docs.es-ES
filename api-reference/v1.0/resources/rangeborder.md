---
title: Tipo de recurso RangeBorder
description: Representa el borde de un objeto.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 9c32264311400951152f892e6f88d70645f47064
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947613"
---
# <a name="rangeborder-resource-type"></a><span data-ttu-id="c0e94-103">Tipo de recurso RangeBorder</span><span class="sxs-lookup"><span data-stu-id="c0e94-103">RangeBorder resource type</span></span>

<span data-ttu-id="c0e94-104">Representa el borde de un objeto.</span><span class="sxs-lookup"><span data-stu-id="c0e94-104">Represents the border of an object.</span></span>


## <a name="methods"></a><span data-ttu-id="c0e94-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="c0e94-105">Methods</span></span>

| <span data-ttu-id="c0e94-106">Método</span><span class="sxs-lookup"><span data-stu-id="c0e94-106">Method</span></span>           | <span data-ttu-id="c0e94-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0e94-107">Return Type</span></span>    |<span data-ttu-id="c0e94-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0e94-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c0e94-109">Get RangeBorder</span><span class="sxs-lookup"><span data-stu-id="c0e94-109">Get RangeBorder</span></span>](../api/rangeborder-get.md) | [<span data-ttu-id="c0e94-110">WorkbookRangeBorder</span><span class="sxs-lookup"><span data-stu-id="c0e94-110">WorkbookRangeBorder</span></span>](rangeborder.md) |<span data-ttu-id="c0e94-111">Lee las propiedades y relaciones del objeto rangeBorder.</span><span class="sxs-lookup"><span data-stu-id="c0e94-111">Read properties and relationships of rangeBorder object.</span></span>|
|[<span data-ttu-id="c0e94-112">Update</span><span class="sxs-lookup"><span data-stu-id="c0e94-112">Update</span></span>](../api/rangeborder-update.md) | [<span data-ttu-id="c0e94-113">WorkbookRangeBorder</span><span class="sxs-lookup"><span data-stu-id="c0e94-113">WorkbookRangeBorder</span></span>](rangeborder.md) |<span data-ttu-id="c0e94-114">Actualiza el objeto RangeBorder.</span><span class="sxs-lookup"><span data-stu-id="c0e94-114">Update RangeBorder object.</span></span> |
|[<span data-ttu-id="c0e94-115">List</span><span class="sxs-lookup"><span data-stu-id="c0e94-115">List</span></span>](../api/rangeborder-list.md) | <span data-ttu-id="c0e94-116">Colección de [WorkbookRangeBorder](rangeborder.md)</span><span class="sxs-lookup"><span data-stu-id="c0e94-116">[WorkbookRangeBorder](rangeborder.md) collection</span></span> |<span data-ttu-id="c0e94-117">Obtiene la colección de objetos rangeBorder.</span><span class="sxs-lookup"><span data-stu-id="c0e94-117">Get rangeBorder object collection.</span></span> |
|[<span data-ttu-id="c0e94-118">Itemat</span><span class="sxs-lookup"><span data-stu-id="c0e94-118">Itemat</span></span>](../api/rangebordercollection-itemat.md)|[<span data-ttu-id="c0e94-119">WorkbookRangeBorder</span><span class="sxs-lookup"><span data-stu-id="c0e94-119">WorkbookRangeBorder</span></span>](rangeborder.md)|<span data-ttu-id="c0e94-120">Obtiene un objeto de borde mediante su índice.</span><span class="sxs-lookup"><span data-stu-id="c0e94-120">Gets a border object using its index</span></span>|

## <a name="properties"></a><span data-ttu-id="c0e94-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c0e94-121">Properties</span></span>
| <span data-ttu-id="c0e94-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c0e94-122">Property</span></span>     | <span data-ttu-id="c0e94-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0e94-123">Type</span></span>   |<span data-ttu-id="c0e94-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0e94-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c0e94-125">color</span><span class="sxs-lookup"><span data-stu-id="c0e94-125">color</span></span>|<span data-ttu-id="c0e94-126">string</span><span class="sxs-lookup"><span data-stu-id="c0e94-126">string</span></span>|<span data-ttu-id="c0e94-127">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="c0e94-127">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|
|<span data-ttu-id="c0e94-128">id</span><span class="sxs-lookup"><span data-stu-id="c0e94-128">id</span></span>|<span data-ttu-id="c0e94-129">string</span><span class="sxs-lookup"><span data-stu-id="c0e94-129">string</span></span>|<span data-ttu-id="c0e94-130">Representa el identificador del borde.</span><span class="sxs-lookup"><span data-stu-id="c0e94-130">Represents border identifier.</span></span> <span data-ttu-id="c0e94-131">Los valores posibles son: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`.</span><span class="sxs-lookup"><span data-stu-id="c0e94-131">The possible values are: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`.</span></span> <span data-ttu-id="c0e94-132">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c0e94-132">Read-only.</span></span>|
|<span data-ttu-id="c0e94-133">sideIndex</span><span class="sxs-lookup"><span data-stu-id="c0e94-133">sideIndex</span></span>|<span data-ttu-id="c0e94-134">string</span><span class="sxs-lookup"><span data-stu-id="c0e94-134">string</span></span>|<span data-ttu-id="c0e94-135">Valor constante que indica el lado específico del borde.</span><span class="sxs-lookup"><span data-stu-id="c0e94-135">Constant value that indicates the specific side of the border.</span></span> <span data-ttu-id="c0e94-136">Los valores posibles son: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`.</span><span class="sxs-lookup"><span data-stu-id="c0e94-136">The possible values are: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`.</span></span> <span data-ttu-id="c0e94-137">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c0e94-137">Read-only.</span></span>|
|<span data-ttu-id="c0e94-138">style</span><span class="sxs-lookup"><span data-stu-id="c0e94-138">style</span></span>|<span data-ttu-id="c0e94-139">string</span><span class="sxs-lookup"><span data-stu-id="c0e94-139">string</span></span>|<span data-ttu-id="c0e94-140">Una de las constantes de estilo de línea que especifica el estilo de línea para el borde.</span><span class="sxs-lookup"><span data-stu-id="c0e94-140">One of the constants of line style specifying the line style for the border.</span></span> <span data-ttu-id="c0e94-141">Los valores posibles son: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.</span><span class="sxs-lookup"><span data-stu-id="c0e94-141">The possible values are: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.</span></span>|
|<span data-ttu-id="c0e94-142">weight</span><span class="sxs-lookup"><span data-stu-id="c0e94-142">weight</span></span>|<span data-ttu-id="c0e94-143">string</span><span class="sxs-lookup"><span data-stu-id="c0e94-143">string</span></span>|<span data-ttu-id="c0e94-144">Especifica el grosor del borde que rodea un rango.</span><span class="sxs-lookup"><span data-stu-id="c0e94-144">Specifies the weight of the border around a range.</span></span> <span data-ttu-id="c0e94-145">Los valores posibles son: `Hairline`, `Thin`, `Medium`, `Thick`.</span><span class="sxs-lookup"><span data-stu-id="c0e94-145">The possible values are: `Hairline`, `Thin`, `Medium`, `Thick`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c0e94-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c0e94-146">Relationships</span></span>
<span data-ttu-id="c0e94-147">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c0e94-147">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="c0e94-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c0e94-148">JSON representation</span></span>

<span data-ttu-id="c0e94-149">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c0e94-149">Here is a JSON representation of the resource.</span></span>

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
