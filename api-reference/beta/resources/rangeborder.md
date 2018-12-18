---
title: Tipo de recurso RangeBorder
description: Representa el borde de un objeto.
author: lumine2008
ms.openlocfilehash: 2aa8807949724766930c5938d1ee6e06db98212a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301221"
---
# <a name="rangeborder-resource-type"></a><span data-ttu-id="48b19-103">Tipo de recurso RangeBorder</span><span class="sxs-lookup"><span data-stu-id="48b19-103">RangeBorder resource type</span></span>

> <span data-ttu-id="48b19-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="48b19-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="48b19-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="48b19-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="48b19-106">Representa el borde de un objeto.</span><span class="sxs-lookup"><span data-stu-id="48b19-106">Represents the border of an object.</span></span>


## <a name="methods"></a><span data-ttu-id="48b19-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="48b19-107">Methods</span></span>

| <span data-ttu-id="48b19-108">Método</span><span class="sxs-lookup"><span data-stu-id="48b19-108">Method</span></span>           | <span data-ttu-id="48b19-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48b19-109">Return Type</span></span>    |<span data-ttu-id="48b19-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="48b19-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="48b19-111">Get RangeBorder</span><span class="sxs-lookup"><span data-stu-id="48b19-111">Get RangeBorder</span></span>](../api/rangeborder-get.md) | [<span data-ttu-id="48b19-112">RangeBorder</span><span class="sxs-lookup"><span data-stu-id="48b19-112">RangeBorder</span></span>](rangeborder.md) |<span data-ttu-id="48b19-113">Lee las propiedades y relaciones del objeto rangeBorder.</span><span class="sxs-lookup"><span data-stu-id="48b19-113">Read properties and relationships of rangeBorder object.</span></span>|
|[<span data-ttu-id="48b19-114">Actualizar</span><span class="sxs-lookup"><span data-stu-id="48b19-114">Update</span></span>](../api/rangeborder-update.md) | [<span data-ttu-id="48b19-115">RangeBorder</span><span class="sxs-lookup"><span data-stu-id="48b19-115">RangeBorder</span></span>](rangeborder.md) |<span data-ttu-id="48b19-116">Actualiza el objeto RangeBorder.</span><span class="sxs-lookup"><span data-stu-id="48b19-116">Update RangeBorder object.</span></span> |
|[<span data-ttu-id="48b19-117">List</span><span class="sxs-lookup"><span data-stu-id="48b19-117">List</span></span>](../api/rangeborder-list.md) | <span data-ttu-id="48b19-118">Colección [RangeBorder](rangeborder.md)</span><span class="sxs-lookup"><span data-stu-id="48b19-118">[RangeBorder](rangeborder.md) collection</span></span> |<span data-ttu-id="48b19-119">Obtiene la colección de objetos rangeBorder.</span><span class="sxs-lookup"><span data-stu-id="48b19-119">Get rangeBorder object collection.</span></span> |
|[<span data-ttu-id="48b19-120">Itemat</span><span class="sxs-lookup"><span data-stu-id="48b19-120">Itemat</span></span>](../api/rangebordercollection-itemat.md)|[<span data-ttu-id="48b19-121">RangeBorder</span><span class="sxs-lookup"><span data-stu-id="48b19-121">RangeBorder</span></span>](rangeborder.md)|<span data-ttu-id="48b19-122">Obtiene un objeto de borde mediante su índice.</span><span class="sxs-lookup"><span data-stu-id="48b19-122">Gets a border object using its index</span></span>|

## <a name="properties"></a><span data-ttu-id="48b19-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48b19-123">Properties</span></span>
| <span data-ttu-id="48b19-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="48b19-124">Property</span></span>     | <span data-ttu-id="48b19-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="48b19-125">Type</span></span>   |<span data-ttu-id="48b19-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="48b19-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="48b19-127">color</span><span class="sxs-lookup"><span data-stu-id="48b19-127">color</span></span>|<span data-ttu-id="48b19-128">string</span><span class="sxs-lookup"><span data-stu-id="48b19-128">string</span></span>|<span data-ttu-id="48b19-129">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="48b19-129">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|
|<span data-ttu-id="48b19-130">id</span><span class="sxs-lookup"><span data-stu-id="48b19-130">id</span></span>|<span data-ttu-id="48b19-131">string</span><span class="sxs-lookup"><span data-stu-id="48b19-131">string</span></span>|<span data-ttu-id="48b19-p102">Representa el identificador de borde. Valores posibles: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="48b19-p102">Represents border identifier. Possible values are: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`. Read-only.</span></span>|
|<span data-ttu-id="48b19-135">sideIndex</span><span class="sxs-lookup"><span data-stu-id="48b19-135">sideIndex</span></span>|<span data-ttu-id="48b19-136">string</span><span class="sxs-lookup"><span data-stu-id="48b19-136">string</span></span>|<span data-ttu-id="48b19-p103">Valor constante que indica el lado específico del borde. Valores posibles: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="48b19-p103">Constant value that indicates the specific side of the border. Possible values are: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`. Read-only.</span></span>|
|<span data-ttu-id="48b19-140">style</span><span class="sxs-lookup"><span data-stu-id="48b19-140">style</span></span>|<span data-ttu-id="48b19-141">string</span><span class="sxs-lookup"><span data-stu-id="48b19-141">string</span></span>|<span data-ttu-id="48b19-p104">Una de las constantes de estilo de línea que especifica el estilo de línea del borde. Valores posibles: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.</span><span class="sxs-lookup"><span data-stu-id="48b19-p104">One of the constants of line style specifying the line style for the border. Possible values are: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.</span></span>|
|<span data-ttu-id="48b19-144">weight</span><span class="sxs-lookup"><span data-stu-id="48b19-144">weight</span></span>|<span data-ttu-id="48b19-145">string</span><span class="sxs-lookup"><span data-stu-id="48b19-145">string</span></span>|<span data-ttu-id="48b19-p105">Especifica el grosor del borde alrededor de un rango. Valores posibles: `Hairline`, `Thin`, `Medium`, `Thick`.</span><span class="sxs-lookup"><span data-stu-id="48b19-p105">Specifies the weight of the border around a range. Possible values are: `Hairline`, `Thin`, `Medium`, `Thick`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="48b19-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="48b19-148">Relationships</span></span>
<span data-ttu-id="48b19-149">Ninguno</span><span class="sxs-lookup"><span data-stu-id="48b19-149">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="48b19-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="48b19-150">JSON representation</span></span>

<span data-ttu-id="48b19-151">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="48b19-151">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rangeBorder"
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