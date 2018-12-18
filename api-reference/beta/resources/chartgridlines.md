---
title: Tipo de recurso ChartGridlines
description: Representa las líneas de cuadrícula principales o secundarias del eje de un gráfico.
author: lumine2008
ms.openlocfilehash: 263bbefad519fef8b12080cb7b2bfd74ce1a331f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27319561"
---
# <a name="chartgridlines-resource-type"></a><span data-ttu-id="d4188-103">Tipo de recurso ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="d4188-103">ChartGridlines resource type</span></span>

> <span data-ttu-id="d4188-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d4188-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d4188-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d4188-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d4188-106">Representa las líneas de división principales o secundarias del eje de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="d4188-106">Represents major or minor gridlines on a chart axis.</span></span>


## <a name="methods"></a><span data-ttu-id="d4188-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="d4188-107">Methods</span></span>

| <span data-ttu-id="d4188-108">Método</span><span class="sxs-lookup"><span data-stu-id="d4188-108">Method</span></span>           | <span data-ttu-id="d4188-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4188-109">Return Type</span></span>    |<span data-ttu-id="d4188-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4188-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d4188-111">Get ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="d4188-111">Get ChartGridlines</span></span>](../api/chartgridlines-get.md) | [<span data-ttu-id="d4188-112">ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="d4188-112">ChartGridlines</span></span>](chartgridlines.md) |<span data-ttu-id="d4188-113">Lee las propiedades y relaciones del objeto chartGridlines.</span><span class="sxs-lookup"><span data-stu-id="d4188-113">Read properties and relationships of chartGridlines object.</span></span>|
|[<span data-ttu-id="d4188-114">Actualizar</span><span class="sxs-lookup"><span data-stu-id="d4188-114">Update</span></span>](../api/chartgridlines-update.md) | [<span data-ttu-id="d4188-115">ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="d4188-115">ChartGridlines</span></span>](chartgridlines.md)    |<span data-ttu-id="d4188-116">Actualiza el objeto ChartGridlines.</span><span class="sxs-lookup"><span data-stu-id="d4188-116">Update ChartGridlines object.</span></span> |

## <a name="properties"></a><span data-ttu-id="d4188-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4188-117">Properties</span></span>
| <span data-ttu-id="d4188-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4188-118">Property</span></span>     | <span data-ttu-id="d4188-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4188-119">Type</span></span>   |<span data-ttu-id="d4188-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4188-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d4188-121">visible</span><span class="sxs-lookup"><span data-stu-id="d4188-121">visible</span></span>|<span data-ttu-id="d4188-122">boolean</span><span class="sxs-lookup"><span data-stu-id="d4188-122">boolean</span></span>|<span data-ttu-id="d4188-123">Valor booleano que representa si las líneas de cuadrícula del eje están visibles o no.</span><span class="sxs-lookup"><span data-stu-id="d4188-123">Boolean value representing if the axis gridlines are visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d4188-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d4188-124">Relationships</span></span>
| <span data-ttu-id="d4188-125">Relación</span><span class="sxs-lookup"><span data-stu-id="d4188-125">Relationship</span></span> | <span data-ttu-id="d4188-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4188-126">Type</span></span>   |<span data-ttu-id="d4188-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4188-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d4188-128">format</span><span class="sxs-lookup"><span data-stu-id="d4188-128">format</span></span>|[<span data-ttu-id="d4188-129">ChartGridlinesFormat</span><span class="sxs-lookup"><span data-stu-id="d4188-129">ChartGridlinesFormat</span></span>](chartgridlinesformat.md)|<span data-ttu-id="d4188-p102">Representa el formato de las líneas de cuadrícula del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d4188-p102">Represents the formatting of chart gridlines. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d4188-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d4188-132">JSON representation</span></span>

<span data-ttu-id="d4188-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d4188-133">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartGridLines"
}-->

```json
{
  "visible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartGridlines resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->