---
title: Tipo de recurso ChartSeries
description: Representa una serie de un gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 5a299c7140c2032a57cd47fb0880ae34620a920b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915819"
---
# <a name="chartseries-resource-type"></a><span data-ttu-id="75915-103">Tipo de recurso ChartSeries</span><span class="sxs-lookup"><span data-stu-id="75915-103">ChartSeries resource type</span></span>

> <span data-ttu-id="75915-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="75915-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="75915-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="75915-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="75915-106">Representa una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="75915-106">Represents a series in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="75915-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="75915-107">Methods</span></span>

| <span data-ttu-id="75915-108">Método</span><span class="sxs-lookup"><span data-stu-id="75915-108">Method</span></span>           | <span data-ttu-id="75915-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75915-109">Return Type</span></span>    |<span data-ttu-id="75915-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="75915-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="75915-111">Get ChartSeries</span><span class="sxs-lookup"><span data-stu-id="75915-111">Get ChartSeries</span></span>](../api/chartseries-get.md) | [<span data-ttu-id="75915-112">ChartSeries</span><span class="sxs-lookup"><span data-stu-id="75915-112">ChartSeries</span></span>](chartseries.md) |<span data-ttu-id="75915-113">Lee las propiedades y relaciones del objeto chartSeries.</span><span class="sxs-lookup"><span data-stu-id="75915-113">Read properties and relationships of chartSeries object.</span></span>|
|[<span data-ttu-id="75915-114">Create ChartPoints</span><span class="sxs-lookup"><span data-stu-id="75915-114">Create ChartPoints</span></span>](../api/chartseries-post-points.md) |[<span data-ttu-id="75915-115">ChartPoints</span><span class="sxs-lookup"><span data-stu-id="75915-115">ChartPoints</span></span>](chartpoint.md)| <span data-ttu-id="75915-116">Crea un nuevo ChartPoints publicándolo en la colección points.</span><span class="sxs-lookup"><span data-stu-id="75915-116">Create a new ChartPoints by posting to the points collection.</span></span>|
|[<span data-ttu-id="75915-117">List points</span><span class="sxs-lookup"><span data-stu-id="75915-117">List points</span></span>](../api/chartseries-list-points.md) |<span data-ttu-id="75915-118">Colección [ChartPoints](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="75915-118">[ChartPoints](chartpoint.md) collection</span></span>| <span data-ttu-id="75915-119">Obtiene la colección de objetos ChartPoints.</span><span class="sxs-lookup"><span data-stu-id="75915-119">Get a ChartPoints object collection.</span></span>|
|[<span data-ttu-id="75915-120">Update</span><span class="sxs-lookup"><span data-stu-id="75915-120">Update</span></span>](../api/chartseries-update.md) | [<span data-ttu-id="75915-121">ChartSeries</span><span class="sxs-lookup"><span data-stu-id="75915-121">ChartSeries</span></span>](chartseries.md) |<span data-ttu-id="75915-122">Actualiza el objeto ChartSeries.</span><span class="sxs-lookup"><span data-stu-id="75915-122">Update ChartSeries object.</span></span> |
|[<span data-ttu-id="75915-123">List</span><span class="sxs-lookup"><span data-stu-id="75915-123">List</span></span>](../api/chartseries-list.md) | <span data-ttu-id="75915-124">Colección [ChartSeries](chartseries.md)</span><span class="sxs-lookup"><span data-stu-id="75915-124">[ChartSeries](chartseries.md) collection</span></span> |<span data-ttu-id="75915-125">Obtiene la colección de objetos chartSeries.</span><span class="sxs-lookup"><span data-stu-id="75915-125">Get chartSeries object collection.</span></span> |
|[<span data-ttu-id="75915-126">Itemat</span><span class="sxs-lookup"><span data-stu-id="75915-126">Itemat</span></span>](../api/chartseriescollection-itemat.md)|[<span data-ttu-id="75915-127">ChartSeries</span><span class="sxs-lookup"><span data-stu-id="75915-127">ChartSeries</span></span>](chartseries.md)|<span data-ttu-id="75915-128">Recupera una serie en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="75915-128">Retrieves a series based on its position in the collection</span></span>|

## <a name="properties"></a><span data-ttu-id="75915-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75915-129">Properties</span></span>
| <span data-ttu-id="75915-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75915-130">Property</span></span>     | <span data-ttu-id="75915-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="75915-131">Type</span></span>   |<span data-ttu-id="75915-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="75915-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="75915-133">name</span><span class="sxs-lookup"><span data-stu-id="75915-133">name</span></span>|<span data-ttu-id="75915-134">string</span><span class="sxs-lookup"><span data-stu-id="75915-134">string</span></span>|<span data-ttu-id="75915-135">Representa el nombre de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="75915-135">Represents the name of a series in a chart.</span></span>|

## <a name="relationships"></a><span data-ttu-id="75915-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="75915-136">Relationships</span></span>
| <span data-ttu-id="75915-137">Relación</span><span class="sxs-lookup"><span data-stu-id="75915-137">Relationship</span></span> | <span data-ttu-id="75915-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="75915-138">Type</span></span>   |<span data-ttu-id="75915-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="75915-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="75915-140">format</span><span class="sxs-lookup"><span data-stu-id="75915-140">format</span></span>|[<span data-ttu-id="75915-141">ChartSeriesFormat</span><span class="sxs-lookup"><span data-stu-id="75915-141">ChartSeriesFormat</span></span>](chartseriesformat.md)|<span data-ttu-id="75915-p102">Representa el formato de una serie del gráfico, que incluye el formato de relleno y de línea. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="75915-p102">Represents the formatting of a chart series, which includes fill and line formatting. Read-only.</span></span>|
|<span data-ttu-id="75915-144">points</span><span class="sxs-lookup"><span data-stu-id="75915-144">points</span></span>|<span data-ttu-id="75915-145">Colección [ChartPoints](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="75915-145">[ChartPoints](chartpoint.md) collection</span></span>|<span data-ttu-id="75915-p103">Representa una colección de todos los puntos de la serie. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="75915-p103">Represents a collection of all points in the series. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="75915-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="75915-148">JSON representation</span></span>

<span data-ttu-id="75915-149">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="75915-149">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartSeries"
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
