---
title: Tipo de recurso ChartGridlines
description: Representa las líneas de cuadrícula principales o secundarias del eje de un gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 7347ac1b7ff251b12764534df217cd883ba730b3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956951"
---
# <a name="chartgridlines-resource-type"></a><span data-ttu-id="d506b-103">Tipo de recurso ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="d506b-103">ChartGridlines resource type</span></span>

<span data-ttu-id="d506b-104">Representa las líneas de cuadrícula principales o secundarias del eje de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="d506b-104">Represents major or minor gridlines on a chart axis.</span></span>


## <a name="methods"></a><span data-ttu-id="d506b-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="d506b-105">Methods</span></span>

| <span data-ttu-id="d506b-106">Método</span><span class="sxs-lookup"><span data-stu-id="d506b-106">Method</span></span>           | <span data-ttu-id="d506b-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d506b-107">Return Type</span></span>    |<span data-ttu-id="d506b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d506b-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d506b-109">Get ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="d506b-109">Get ChartGridlines</span></span>](../api/chartgridlines-get.md) | [<span data-ttu-id="d506b-110">WorkbookChartGridlines</span><span class="sxs-lookup"><span data-stu-id="d506b-110">WorkbookChartGridlines</span></span>](chartgridlines.md) |<span data-ttu-id="d506b-111">Lee las propiedades y relaciones del objeto chartGridlines.</span><span class="sxs-lookup"><span data-stu-id="d506b-111">Read properties and relationships of chartGridlines object.</span></span>|
|[<span data-ttu-id="d506b-112">Update</span><span class="sxs-lookup"><span data-stu-id="d506b-112">Update</span></span>](../api/chartgridlines-update.md) | [<span data-ttu-id="d506b-113">WorkbookChartGridlines</span><span class="sxs-lookup"><span data-stu-id="d506b-113">WorkbookChartGridlines</span></span>](chartgridlines.md)    |<span data-ttu-id="d506b-114">Actualiza el objeto ChartGridlines.</span><span class="sxs-lookup"><span data-stu-id="d506b-114">Update ChartGridlines object.</span></span> |

## <a name="properties"></a><span data-ttu-id="d506b-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d506b-115">Properties</span></span>
| <span data-ttu-id="d506b-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d506b-116">Property</span></span>     | <span data-ttu-id="d506b-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="d506b-117">Type</span></span>   |<span data-ttu-id="d506b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d506b-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d506b-119">visible</span><span class="sxs-lookup"><span data-stu-id="d506b-119">visible</span></span>|<span data-ttu-id="d506b-120">boolean</span><span class="sxs-lookup"><span data-stu-id="d506b-120">boolean</span></span>|<span data-ttu-id="d506b-121">Valor booleano que representa si las líneas de cuadrícula del eje están visibles o no.</span><span class="sxs-lookup"><span data-stu-id="d506b-121">Boolean value representing if the axis gridlines are visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d506b-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d506b-122">Relationships</span></span>
| <span data-ttu-id="d506b-123">Relación</span><span class="sxs-lookup"><span data-stu-id="d506b-123">Relationship</span></span> | <span data-ttu-id="d506b-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="d506b-124">Type</span></span>   |<span data-ttu-id="d506b-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="d506b-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d506b-126">format</span><span class="sxs-lookup"><span data-stu-id="d506b-126">format</span></span>|[<span data-ttu-id="d506b-127">WorkbookChartGridlinesFormat</span><span class="sxs-lookup"><span data-stu-id="d506b-127">WorkbookChartGridlinesFormat</span></span>](chartgridlinesformat.md)|<span data-ttu-id="d506b-p101">Representa el formato de las líneas de cuadrícula del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d506b-p101">Represents the formatting of chart gridlines. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d506b-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d506b-130">JSON representation</span></span>

<span data-ttu-id="d506b-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d506b-131">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartGridlines"
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
