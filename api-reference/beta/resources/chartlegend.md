---
title: Tipo de recurso ChartLegend
description: Representa la leyenda de un gráfico.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: db5c4531143df52c86e310c1d3670ab72b6e938c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853777"
---
# <a name="chartlegend-resource-type"></a><span data-ttu-id="7315d-103">Tipo de recurso ChartLegend</span><span class="sxs-lookup"><span data-stu-id="7315d-103">ChartLegend resource type</span></span>

> <span data-ttu-id="7315d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7315d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7315d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7315d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7315d-106">Representa la leyenda de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="7315d-106">Represents the legend in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="7315d-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="7315d-107">Methods</span></span>

| <span data-ttu-id="7315d-108">Método</span><span class="sxs-lookup"><span data-stu-id="7315d-108">Method</span></span>           | <span data-ttu-id="7315d-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7315d-109">Return Type</span></span>    |<span data-ttu-id="7315d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7315d-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="7315d-111">Get ChartLegend</span><span class="sxs-lookup"><span data-stu-id="7315d-111">Get ChartLegend</span></span>](../api/chartlegend-get.md) | [<span data-ttu-id="7315d-112">ChartLegend</span><span class="sxs-lookup"><span data-stu-id="7315d-112">ChartLegend</span></span>](chartlegend.md) |<span data-ttu-id="7315d-113">Lee las propiedades y relaciones del objeto chartLegend.</span><span class="sxs-lookup"><span data-stu-id="7315d-113">Read properties and relationships of chartLegend object.</span></span>|
|[<span data-ttu-id="7315d-114">Update</span><span class="sxs-lookup"><span data-stu-id="7315d-114">Update</span></span>](../api/chartlegend-update.md) | [<span data-ttu-id="7315d-115">ChartLegend</span><span class="sxs-lookup"><span data-stu-id="7315d-115">ChartLegend</span></span>](chartlegend.md) |<span data-ttu-id="7315d-116">Actualiza el objeto ChartLegend.</span><span class="sxs-lookup"><span data-stu-id="7315d-116">Update ChartLegend object.</span></span> |

## <a name="properties"></a><span data-ttu-id="7315d-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7315d-117">Properties</span></span>
| <span data-ttu-id="7315d-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7315d-118">Property</span></span>     | <span data-ttu-id="7315d-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="7315d-119">Type</span></span>   |<span data-ttu-id="7315d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="7315d-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7315d-121">overlay</span><span class="sxs-lookup"><span data-stu-id="7315d-121">overlay</span></span>|<span data-ttu-id="7315d-122">boolean</span><span class="sxs-lookup"><span data-stu-id="7315d-122">boolean</span></span>|<span data-ttu-id="7315d-123">Valor booleano que indica si la leyenda del gráfico debe superponerse al cuerpo principal del gráfico.</span><span class="sxs-lookup"><span data-stu-id="7315d-123">Boolean value for whether the chart legend should overlap with the main body of the chart.</span></span>|
|<span data-ttu-id="7315d-124">position</span><span class="sxs-lookup"><span data-stu-id="7315d-124">position</span></span>|<span data-ttu-id="7315d-125">string</span><span class="sxs-lookup"><span data-stu-id="7315d-125">string</span></span>|<span data-ttu-id="7315d-p102">Representa la posición de la leyenda del gráfico. Valores posibles: `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`.</span><span class="sxs-lookup"><span data-stu-id="7315d-p102">Represents the position of the legend on the chart. Possible values are: `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`.</span></span>|
|<span data-ttu-id="7315d-128">visible</span><span class="sxs-lookup"><span data-stu-id="7315d-128">visible</span></span>|<span data-ttu-id="7315d-129">boolean</span><span class="sxs-lookup"><span data-stu-id="7315d-129">boolean</span></span>|<span data-ttu-id="7315d-130">Valor booleano que representa la visibilidad de un objeto ChartLegend.</span><span class="sxs-lookup"><span data-stu-id="7315d-130">A boolean value the represents the visibility of a ChartLegend object.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7315d-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7315d-131">Relationships</span></span>
| <span data-ttu-id="7315d-132">Relación</span><span class="sxs-lookup"><span data-stu-id="7315d-132">Relationship</span></span> | <span data-ttu-id="7315d-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="7315d-133">Type</span></span>   |<span data-ttu-id="7315d-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="7315d-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7315d-135">format</span><span class="sxs-lookup"><span data-stu-id="7315d-135">format</span></span>|[<span data-ttu-id="7315d-136">ChartLegendFormat</span><span class="sxs-lookup"><span data-stu-id="7315d-136">ChartLegendFormat</span></span>](chartlegendformat.md)|<span data-ttu-id="7315d-p103">Representa el formato de una leyenda del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7315d-p103">Represents the formatting of a chart legend, which includes fill and font formatting. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7315d-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7315d-139">JSON representation</span></span>

<span data-ttu-id="7315d-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7315d-140">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartLegend"
}-->

```json
{
  "overlay": true,
  "position": "string",
  "visible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartLegend resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
