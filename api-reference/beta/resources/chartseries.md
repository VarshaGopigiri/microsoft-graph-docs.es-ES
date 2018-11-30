---
title: Tipo de recurso ChartSeries
description: Representa una serie de un gráfico.
ms.openlocfilehash: 301fd3ba3c299108836bbd92497f4d6f6af94b0a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091052"
---
# <a name="chartseries-resource-type"></a><span data-ttu-id="da66a-103">Tipo de recurso ChartSeries</span><span class="sxs-lookup"><span data-stu-id="da66a-103">ChartSeries resource type</span></span>

> <span data-ttu-id="da66a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="da66a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="da66a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="da66a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="da66a-106">Representa una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="da66a-106">Represents a series in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="da66a-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="da66a-107">Methods</span></span>

| <span data-ttu-id="da66a-108">Método</span><span class="sxs-lookup"><span data-stu-id="da66a-108">Method</span></span>           | <span data-ttu-id="da66a-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da66a-109">Return Type</span></span>    |<span data-ttu-id="da66a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="da66a-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="da66a-111">Get ChartSeries</span><span class="sxs-lookup"><span data-stu-id="da66a-111">Get ChartSeries</span></span>](../api/chartseries-get.md) | [<span data-ttu-id="da66a-112">ChartSeries</span><span class="sxs-lookup"><span data-stu-id="da66a-112">ChartSeries</span></span>](chartseries.md) |<span data-ttu-id="da66a-113">Lee las propiedades y relaciones del objeto chartSeries.</span><span class="sxs-lookup"><span data-stu-id="da66a-113">Read properties and relationships of chartSeries object.</span></span>|
|[<span data-ttu-id="da66a-114">Create ChartPoints</span><span class="sxs-lookup"><span data-stu-id="da66a-114">Create ChartPoints</span></span>](../api/chartseries-post-points.md) |[<span data-ttu-id="da66a-115">ChartPoints</span><span class="sxs-lookup"><span data-stu-id="da66a-115">ChartPoints</span></span>](chartpoint.md)| <span data-ttu-id="da66a-116">Crea un nuevo ChartPoints publicándolo en la colección points.</span><span class="sxs-lookup"><span data-stu-id="da66a-116">Create a new ChartPoints by posting to the points collection.</span></span>|
|[<span data-ttu-id="da66a-117">List points</span><span class="sxs-lookup"><span data-stu-id="da66a-117">List points</span></span>](../api/chartseries-list-points.md) |<span data-ttu-id="da66a-118">Colección [ChartPoints](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="da66a-118">[ChartPoints](chartpoint.md) collection</span></span>| <span data-ttu-id="da66a-119">Obtiene la colección de objetos ChartPoints.</span><span class="sxs-lookup"><span data-stu-id="da66a-119">Get a ChartPoints object collection.</span></span>|
|[<span data-ttu-id="da66a-120">Update</span><span class="sxs-lookup"><span data-stu-id="da66a-120">Update</span></span>](../api/chartseries-update.md) | [<span data-ttu-id="da66a-121">ChartSeries</span><span class="sxs-lookup"><span data-stu-id="da66a-121">ChartSeries</span></span>](chartseries.md) |<span data-ttu-id="da66a-122">Actualiza el objeto ChartSeries.</span><span class="sxs-lookup"><span data-stu-id="da66a-122">Update ChartSeries object.</span></span> |
|[<span data-ttu-id="da66a-123">List</span><span class="sxs-lookup"><span data-stu-id="da66a-123">List</span></span>](../api/chartseries-list.md) | <span data-ttu-id="da66a-124">Colección [ChartSeries](chartseries.md)</span><span class="sxs-lookup"><span data-stu-id="da66a-124">[ChartSeries](chartseries.md) collection</span></span> |<span data-ttu-id="da66a-125">Obtiene la colección de objetos chartSeries.</span><span class="sxs-lookup"><span data-stu-id="da66a-125">Get chartSeries object collection.</span></span> |
|[<span data-ttu-id="da66a-126">Itemat</span><span class="sxs-lookup"><span data-stu-id="da66a-126">Itemat</span></span>](../api/chartseriescollection-itemat.md)|[<span data-ttu-id="da66a-127">ChartSeries</span><span class="sxs-lookup"><span data-stu-id="da66a-127">ChartSeries</span></span>](chartseries.md)|<span data-ttu-id="da66a-128">Recupera una serie en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="da66a-128">Retrieves a series based on its position in the collection</span></span>|

## <a name="properties"></a><span data-ttu-id="da66a-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="da66a-129">Properties</span></span>
| <span data-ttu-id="da66a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="da66a-130">Property</span></span>     | <span data-ttu-id="da66a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="da66a-131">Type</span></span>   |<span data-ttu-id="da66a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="da66a-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="da66a-133">name</span><span class="sxs-lookup"><span data-stu-id="da66a-133">name</span></span>|<span data-ttu-id="da66a-134">string</span><span class="sxs-lookup"><span data-stu-id="da66a-134">string</span></span>|<span data-ttu-id="da66a-135">Representa el nombre de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="da66a-135">Represents the name of a series in a chart.</span></span>|

## <a name="relationships"></a><span data-ttu-id="da66a-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="da66a-136">Relationships</span></span>
| <span data-ttu-id="da66a-137">Relación</span><span class="sxs-lookup"><span data-stu-id="da66a-137">Relationship</span></span> | <span data-ttu-id="da66a-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="da66a-138">Type</span></span>   |<span data-ttu-id="da66a-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="da66a-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="da66a-140">format</span><span class="sxs-lookup"><span data-stu-id="da66a-140">format</span></span>|[<span data-ttu-id="da66a-141">ChartSeriesFormat</span><span class="sxs-lookup"><span data-stu-id="da66a-141">ChartSeriesFormat</span></span>](chartseriesformat.md)|<span data-ttu-id="da66a-p102">Representa el formato de una serie del gráfico, que incluye el formato de relleno y de línea. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="da66a-p102">Represents the formatting of a chart series, which includes fill and line formatting. Read-only.</span></span>|
|<span data-ttu-id="da66a-144">points</span><span class="sxs-lookup"><span data-stu-id="da66a-144">points</span></span>|<span data-ttu-id="da66a-145">Colección [ChartPoints](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="da66a-145">[ChartPoints](chartpoint.md) collection</span></span>|<span data-ttu-id="da66a-p103">Representa una colección de todos los puntos de la serie. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="da66a-p103">Represents a collection of all points in the series. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="da66a-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="da66a-148">JSON representation</span></span>

<span data-ttu-id="da66a-149">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="da66a-149">Here is a JSON representation of the resource.</span></span>

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