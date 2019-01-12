---
title: Tipo de recurso ChartSeries
description: Representa una serie de un gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: b9a857f127848f1ed0da8de673902527e3858ffe
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970391"
---
# <a name="chartseries-resource-type"></a><span data-ttu-id="40dda-103">Tipo de recurso ChartSeries</span><span class="sxs-lookup"><span data-stu-id="40dda-103">ChartSeries resource type</span></span>

<span data-ttu-id="40dda-104">Representa una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="40dda-104">Represents a series in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="40dda-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="40dda-105">Methods</span></span>

| <span data-ttu-id="40dda-106">Método</span><span class="sxs-lookup"><span data-stu-id="40dda-106">Method</span></span>           | <span data-ttu-id="40dda-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40dda-107">Return Type</span></span>    |<span data-ttu-id="40dda-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="40dda-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="40dda-109">Get ChartSeries</span><span class="sxs-lookup"><span data-stu-id="40dda-109">Get ChartSeries</span></span>](../api/chartseries-get.md) | [<span data-ttu-id="40dda-110">WorkbookChartSeries</span><span class="sxs-lookup"><span data-stu-id="40dda-110">WorkbookChartSeries</span></span>](chartseries.md) |<span data-ttu-id="40dda-111">Lee las propiedades y relaciones del objeto chartSeries.</span><span class="sxs-lookup"><span data-stu-id="40dda-111">Read properties and relationships of chartSeries object.</span></span>|
|[<span data-ttu-id="40dda-112">Create ChartPoints</span><span class="sxs-lookup"><span data-stu-id="40dda-112">Create ChartPoints</span></span>](../api/chartseries-post-points.md) |[<span data-ttu-id="40dda-113">ChartPoints</span><span class="sxs-lookup"><span data-stu-id="40dda-113">ChartPoints</span></span>](chartpoint.md)| <span data-ttu-id="40dda-114">Crea un nuevo ChartPoints publicándolo en la colección points.</span><span class="sxs-lookup"><span data-stu-id="40dda-114">Create a new ChartPoints by posting to the points collection.</span></span>|
|[<span data-ttu-id="40dda-115">List points</span><span class="sxs-lookup"><span data-stu-id="40dda-115">List points</span></span>](../api/chartseries-list-points.md) |<span data-ttu-id="40dda-116">Colección [ChartPoints](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="40dda-116">[ChartPoints](chartpoint.md) collection</span></span>| <span data-ttu-id="40dda-117">Obtiene la colección de objetos ChartPoints.</span><span class="sxs-lookup"><span data-stu-id="40dda-117">Get a ChartPoints object collection.</span></span>|
|[<span data-ttu-id="40dda-118">Update</span><span class="sxs-lookup"><span data-stu-id="40dda-118">Update</span></span>](../api/chartseries-update.md) | [<span data-ttu-id="40dda-119">WorkbookChartSeries</span><span class="sxs-lookup"><span data-stu-id="40dda-119">WorkbookChartSeries</span></span>](chartseries.md) |<span data-ttu-id="40dda-120">Actualiza el objeto ChartSeries.</span><span class="sxs-lookup"><span data-stu-id="40dda-120">Update ChartSeries object.</span></span> |
|[<span data-ttu-id="40dda-121">List</span><span class="sxs-lookup"><span data-stu-id="40dda-121">List</span></span>](../api/chartseries-list.md) | <span data-ttu-id="40dda-122">Colección de [WorkbookChartSeries](chartseries.md)</span><span class="sxs-lookup"><span data-stu-id="40dda-122">[WorkbookChartSeries](chartseries.md) collection</span></span> |<span data-ttu-id="40dda-123">Obtiene la colección de objetos chartSeries.</span><span class="sxs-lookup"><span data-stu-id="40dda-123">Get chartSeries object collection.</span></span> |
|[<span data-ttu-id="40dda-124">ItemAt</span><span class="sxs-lookup"><span data-stu-id="40dda-124">ItemAt</span></span>](../api/chartseriescollection-itemat.md)|[<span data-ttu-id="40dda-125">WorkbookChartSeries</span><span class="sxs-lookup"><span data-stu-id="40dda-125">WorkbookChartSeries</span></span>](chartseries.md)|<span data-ttu-id="40dda-126">Recupera una serie en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="40dda-126">Retrieves a series based on its position in the collection</span></span>|

## <a name="properties"></a><span data-ttu-id="40dda-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40dda-127">Properties</span></span>
| <span data-ttu-id="40dda-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="40dda-128">Property</span></span>     | <span data-ttu-id="40dda-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="40dda-129">Type</span></span>   |<span data-ttu-id="40dda-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="40dda-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="40dda-131">name</span><span class="sxs-lookup"><span data-stu-id="40dda-131">name</span></span>|<span data-ttu-id="40dda-132">string</span><span class="sxs-lookup"><span data-stu-id="40dda-132">string</span></span>|<span data-ttu-id="40dda-133">Representa el nombre de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="40dda-133">Represents the name of a series in a chart.</span></span>|

## <a name="relationships"></a><span data-ttu-id="40dda-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="40dda-134">Relationships</span></span>
| <span data-ttu-id="40dda-135">Relación</span><span class="sxs-lookup"><span data-stu-id="40dda-135">Relationship</span></span> | <span data-ttu-id="40dda-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="40dda-136">Type</span></span>   |<span data-ttu-id="40dda-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="40dda-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="40dda-138">format</span><span class="sxs-lookup"><span data-stu-id="40dda-138">format</span></span>|[<span data-ttu-id="40dda-139">WorkbookChartSeriesFormat</span><span class="sxs-lookup"><span data-stu-id="40dda-139">WorkbookChartSeriesFormat</span></span>](chartseriesformat.md)|<span data-ttu-id="40dda-p101">Representa el formato de una serie del gráfico, que incluye el formato de relleno y de línea. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="40dda-p101">Represents the formatting of a chart series, which includes fill and line formatting. Read-only.</span></span>|
|<span data-ttu-id="40dda-142">points</span><span class="sxs-lookup"><span data-stu-id="40dda-142">points</span></span>|<span data-ttu-id="40dda-143">Colección de [WorkbookChartPoint](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="40dda-143">[WorkbookChartPoint](chartpoint.md) collection</span></span>|<span data-ttu-id="40dda-p102">Representa una colección de todos los puntos de la serie. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="40dda-p102">Represents a collection of all points in the series. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="40dda-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="40dda-146">JSON representation</span></span>

<span data-ttu-id="40dda-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="40dda-147">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartSeries"
}-->

```json
{
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartSeries resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
