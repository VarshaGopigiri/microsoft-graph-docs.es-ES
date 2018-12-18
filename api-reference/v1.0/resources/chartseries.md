---
title: Tipo de recurso ChartSeries
description: Representa una serie de un gráfico.
author: lumine2008
ms.openlocfilehash: 60cd3e29f1b2c2f106fae0fdfb76b18657d68120
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314493"
---
# <a name="chartseries-resource-type"></a><span data-ttu-id="ff942-103">Tipo de recurso ChartSeries</span><span class="sxs-lookup"><span data-stu-id="ff942-103">ChartSeries resource type</span></span>

<span data-ttu-id="ff942-104">Representa una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="ff942-104">Represents a series in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="ff942-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="ff942-105">Methods</span></span>

| <span data-ttu-id="ff942-106">Método</span><span class="sxs-lookup"><span data-stu-id="ff942-106">Method</span></span>           | <span data-ttu-id="ff942-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff942-107">Return Type</span></span>    |<span data-ttu-id="ff942-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff942-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ff942-109">Get ChartSeries</span><span class="sxs-lookup"><span data-stu-id="ff942-109">Get ChartSeries</span></span>](../api/chartseries-get.md) | [<span data-ttu-id="ff942-110">WorkbookChartSeries</span><span class="sxs-lookup"><span data-stu-id="ff942-110">WorkbookChartSeries</span></span>](chartseries.md) |<span data-ttu-id="ff942-111">Lee las propiedades y relaciones del objeto chartSeries.</span><span class="sxs-lookup"><span data-stu-id="ff942-111">Read properties and relationships of chartSeries object.</span></span>|
|[<span data-ttu-id="ff942-112">Create ChartPoints</span><span class="sxs-lookup"><span data-stu-id="ff942-112">Create ChartPoints</span></span>](../api/chartseries-post-points.md) |[<span data-ttu-id="ff942-113">ChartPoints</span><span class="sxs-lookup"><span data-stu-id="ff942-113">ChartPoints</span></span>](chartpoint.md)| <span data-ttu-id="ff942-114">Crea un nuevo ChartPoints publicándolo en la colección points.</span><span class="sxs-lookup"><span data-stu-id="ff942-114">Create a new ChartPoints by posting to the points collection.</span></span>|
|[<span data-ttu-id="ff942-115">List points</span><span class="sxs-lookup"><span data-stu-id="ff942-115">List points</span></span>](../api/chartseries-list-points.md) |<span data-ttu-id="ff942-116">Colección [ChartPoints](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="ff942-116">[ChartPoints](chartpoint.md) collection</span></span>| <span data-ttu-id="ff942-117">Obtiene la colección de objetos ChartPoints.</span><span class="sxs-lookup"><span data-stu-id="ff942-117">Get a ChartPoints object collection.</span></span>|
|[<span data-ttu-id="ff942-118">Actualizar</span><span class="sxs-lookup"><span data-stu-id="ff942-118">Update</span></span>](../api/chartseries-update.md) | [<span data-ttu-id="ff942-119">WorkbookChartSeries</span><span class="sxs-lookup"><span data-stu-id="ff942-119">WorkbookChartSeries</span></span>](chartseries.md) |<span data-ttu-id="ff942-120">Actualiza el objeto ChartSeries.</span><span class="sxs-lookup"><span data-stu-id="ff942-120">Update ChartSeries object.</span></span> |
|[<span data-ttu-id="ff942-121">List</span><span class="sxs-lookup"><span data-stu-id="ff942-121">List</span></span>](../api/chartseries-list.md) | <span data-ttu-id="ff942-122">Colección de [WorkbookChartSeries](chartseries.md)</span><span class="sxs-lookup"><span data-stu-id="ff942-122">[WorkbookChartSeries](chartseries.md) collection</span></span> |<span data-ttu-id="ff942-123">Obtiene la colección de objetos chartSeries.</span><span class="sxs-lookup"><span data-stu-id="ff942-123">Get chartSeries object collection.</span></span> |
|[<span data-ttu-id="ff942-124">ItemAt</span><span class="sxs-lookup"><span data-stu-id="ff942-124">ItemAt</span></span>](../api/chartseriescollection-itemat.md)|[<span data-ttu-id="ff942-125">WorkbookChartSeries</span><span class="sxs-lookup"><span data-stu-id="ff942-125">WorkbookChartSeries</span></span>](chartseries.md)|<span data-ttu-id="ff942-126">Recupera una serie en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="ff942-126">Retrieves a series based on its position in the collection</span></span>|

## <a name="properties"></a><span data-ttu-id="ff942-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff942-127">Properties</span></span>
| <span data-ttu-id="ff942-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ff942-128">Property</span></span>     | <span data-ttu-id="ff942-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff942-129">Type</span></span>   |<span data-ttu-id="ff942-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff942-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ff942-131">name</span><span class="sxs-lookup"><span data-stu-id="ff942-131">name</span></span>|<span data-ttu-id="ff942-132">string</span><span class="sxs-lookup"><span data-stu-id="ff942-132">string</span></span>|<span data-ttu-id="ff942-133">Representa el nombre de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="ff942-133">Represents the name of a series in a chart.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ff942-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ff942-134">Relationships</span></span>
| <span data-ttu-id="ff942-135">Relación</span><span class="sxs-lookup"><span data-stu-id="ff942-135">Relationship</span></span> | <span data-ttu-id="ff942-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff942-136">Type</span></span>   |<span data-ttu-id="ff942-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff942-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ff942-138">format</span><span class="sxs-lookup"><span data-stu-id="ff942-138">format</span></span>|[<span data-ttu-id="ff942-139">WorkbookChartSeriesFormat</span><span class="sxs-lookup"><span data-stu-id="ff942-139">WorkbookChartSeriesFormat</span></span>](chartseriesformat.md)|<span data-ttu-id="ff942-p101">Representa el formato de una serie del gráfico, que incluye el formato de relleno y de línea. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff942-p101">Represents the formatting of a chart series, which includes fill and line formatting. Read-only.</span></span>|
|<span data-ttu-id="ff942-142">points</span><span class="sxs-lookup"><span data-stu-id="ff942-142">points</span></span>|<span data-ttu-id="ff942-143">Colección de [WorkbookChartPoint](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="ff942-143">[WorkbookChartPoint](chartpoint.md) collection</span></span>|<span data-ttu-id="ff942-p102">Representa una colección de todos los puntos de la serie. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff942-p102">Represents a collection of all points in the series. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ff942-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ff942-146">JSON representation</span></span>

<span data-ttu-id="ff942-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ff942-147">Here is a JSON representation of the resource.</span></span>

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