---
title: Tipo de recurso ChartAxes
description: Representa los ejes del gráfico.
ms.openlocfilehash: 4fc801ecdba147a26b30f07a2487eabe11acfb3c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029508"
---
# <a name="chartaxes-resource-type"></a><span data-ttu-id="d0a86-103">Tipo de recurso ChartAxes</span><span class="sxs-lookup"><span data-stu-id="d0a86-103">ChartAxes resource type</span></span>

<span data-ttu-id="d0a86-104">Representa los ejes del gráfico.</span><span class="sxs-lookup"><span data-stu-id="d0a86-104">Represents the chart axes.</span></span>


## <a name="methods"></a><span data-ttu-id="d0a86-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="d0a86-105">Methods</span></span>
<span data-ttu-id="d0a86-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d0a86-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="d0a86-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0a86-107">Properties</span></span>
<span data-ttu-id="d0a86-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d0a86-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="d0a86-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d0a86-109">Relationships</span></span>
| <span data-ttu-id="d0a86-110">Relación</span><span class="sxs-lookup"><span data-stu-id="d0a86-110">Relationship</span></span> | <span data-ttu-id="d0a86-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0a86-111">Type</span></span>   |<span data-ttu-id="d0a86-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0a86-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d0a86-113">categoryAxis</span><span class="sxs-lookup"><span data-stu-id="d0a86-113">categoryAxis</span></span>|[<span data-ttu-id="d0a86-114">WorkbookChartAxis</span><span class="sxs-lookup"><span data-stu-id="d0a86-114">WorkbookChartAxis</span></span>](chartaxis.md)|<span data-ttu-id="d0a86-p101">Representa el eje de categorías de un gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d0a86-p101">Represents the category axis in a chart. Read-only.</span></span>|
|<span data-ttu-id="d0a86-117">seriesAxis</span><span class="sxs-lookup"><span data-stu-id="d0a86-117">seriesAxis</span></span>|[<span data-ttu-id="d0a86-118">WorkbookChartAxis</span><span class="sxs-lookup"><span data-stu-id="d0a86-118">WorkbookChartAxis</span></span>](chartaxis.md)|<span data-ttu-id="d0a86-p102">Representa el eje de series de un gráfico tridimensional. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d0a86-p102">Represents the series axis of a 3-dimensional chart. Read-only.</span></span>|
|<span data-ttu-id="d0a86-121">valueAxis</span><span class="sxs-lookup"><span data-stu-id="d0a86-121">valueAxis</span></span>|[<span data-ttu-id="d0a86-122">WorkbookChartAxis</span><span class="sxs-lookup"><span data-stu-id="d0a86-122">WorkbookChartAxis</span></span>](chartaxis.md)|<span data-ttu-id="d0a86-p103">Representa el eje de valores de un eje. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d0a86-p103">Represents the value axis in an axis. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d0a86-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d0a86-125">JSON representation</span></span>

<span data-ttu-id="d0a86-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d0a86-126">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartAxes"
}-->

```json
{
  "categoryAxis": {"@odata.type": "microsoft.graph.workbookChartAxis"},
  "seriesAxis": {"@odata.type": "microsoft.graph.workbookChartAxis"},
  "valueAxis": {"@odata.type": "microsoft.graph.workbookChartAxis"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxes resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->