---
title: Tipo de recurso Chart
description: Representa un objeto de gráfico de una hoja de cálculo.
author: lumine2008
ms.openlocfilehash: cf03a768422fca50e68b88a64b9991aad878466f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27325721"
---
# <a name="chart-resource-type"></a><span data-ttu-id="0ffa5-103">Tipo de recurso Chart</span><span class="sxs-lookup"><span data-stu-id="0ffa5-103">Chart resource type</span></span>

> <span data-ttu-id="0ffa5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0ffa5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0ffa5-106">Representa un objeto de gráfico de una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-106">Represents a chart object in a workbook.</span></span>


## <a name="methods"></a><span data-ttu-id="0ffa5-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="0ffa5-107">Methods</span></span>

| <span data-ttu-id="0ffa5-108">Método</span><span class="sxs-lookup"><span data-stu-id="0ffa5-108">Method</span></span>           | <span data-ttu-id="0ffa5-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ffa5-109">Return Type</span></span>    |<span data-ttu-id="0ffa5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ffa5-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="0ffa5-111">Get Chart</span><span class="sxs-lookup"><span data-stu-id="0ffa5-111">Get Chart</span></span>](../api/chart-get.md) | [<span data-ttu-id="0ffa5-112">Chart</span><span class="sxs-lookup"><span data-stu-id="0ffa5-112">Chart</span></span>](chart.md) |<span data-ttu-id="0ffa5-113">Lee las propiedades y relaciones del objeto chart.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-113">Read properties and relationships of chart object.</span></span>|
|[<span data-ttu-id="0ffa5-114">Create ChartSeries</span><span class="sxs-lookup"><span data-stu-id="0ffa5-114">Create ChartSeries</span></span>](../api/chart-post-series.md) |[<span data-ttu-id="0ffa5-115">ChartSeries</span><span class="sxs-lookup"><span data-stu-id="0ffa5-115">ChartSeries</span></span>](chartseries.md)| <span data-ttu-id="0ffa5-116">Crea un ChartSeries publicándolo en la colección series.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-116">Create a new ChartSeries by posting to the series collection.</span></span>|
|[<span data-ttu-id="0ffa5-117">List series</span><span class="sxs-lookup"><span data-stu-id="0ffa5-117">List series</span></span>](../api/chart-list-series.md) |<span data-ttu-id="0ffa5-118">Colección [ChartSeries](chartseries.md)</span><span class="sxs-lookup"><span data-stu-id="0ffa5-118">[ChartSeries](chartseries.md) collection</span></span>| <span data-ttu-id="0ffa5-119">Obtiene una colección de objetos ChartSeries.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-119">Get a ChartSeries object collection.</span></span>|
|[<span data-ttu-id="0ffa5-120">Actualizar</span><span class="sxs-lookup"><span data-stu-id="0ffa5-120">Update</span></span>](../api/chart-update.md) | [<span data-ttu-id="0ffa5-121">Chart</span><span class="sxs-lookup"><span data-stu-id="0ffa5-121">Chart</span></span>](chart.md)   |<span data-ttu-id="0ffa5-122">Actualiza el objeto Chart.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-122">Update Chart object.</span></span> |
|[<span data-ttu-id="0ffa5-123">Image</span><span class="sxs-lookup"><span data-stu-id="0ffa5-123">Image</span></span>](../api/chart-image.md)|<span data-ttu-id="0ffa5-124">Cadena codificada en base64 de imagen</span><span class="sxs-lookup"><span data-stu-id="0ffa5-124">Image base64 encoded string</span></span>|<span data-ttu-id="0ffa5-125">Representa el gráfico como una imagen con codificación base64 al escalar el gráfico a las dimensiones especificadas.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-125">Renders the chart as a base64-encoded image by scaling the chart to fit the specified dimensions.</span></span>|
|[<span data-ttu-id="0ffa5-126">Eliminar</span><span class="sxs-lookup"><span data-stu-id="0ffa5-126">Delete</span></span>](../api/chart-delete.md)|<span data-ttu-id="0ffa5-127">None</span><span class="sxs-lookup"><span data-stu-id="0ffa5-127">None</span></span>|<span data-ttu-id="0ffa5-128">Elimina el objeto chart.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-128">Deletes the chart object.</span></span>|
|[<span data-ttu-id="0ffa5-129">Setdata</span><span class="sxs-lookup"><span data-stu-id="0ffa5-129">Setdata</span></span>](../api/chart-setdata.md)|<span data-ttu-id="0ffa5-130">None</span><span class="sxs-lookup"><span data-stu-id="0ffa5-130">None</span></span>|<span data-ttu-id="0ffa5-131">Restablece los datos de origen del gráfico.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-131">Resets the source data for the chart.</span></span>|
|[<span data-ttu-id="0ffa5-132">Setposition</span><span class="sxs-lookup"><span data-stu-id="0ffa5-132">Setposition</span></span>](../api/chart-setposition.md)|<span data-ttu-id="0ffa5-133">None</span><span class="sxs-lookup"><span data-stu-id="0ffa5-133">None</span></span>|<span data-ttu-id="0ffa5-134">Coloca el gráfico con respecto a las celdas de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-134">Positions the chart relative to cells on the worksheet.</span></span>|
|[<span data-ttu-id="0ffa5-135">List</span><span class="sxs-lookup"><span data-stu-id="0ffa5-135">List</span></span>](../api/chart-list.md) | <span data-ttu-id="0ffa5-136">Colección [Chart](chart.md)</span><span class="sxs-lookup"><span data-stu-id="0ffa5-136">[Chart](chart.md) collection</span></span> |<span data-ttu-id="0ffa5-137">Obtiene la colección de objetos chart.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-137">Get chart object collection.</span></span> |
|[<span data-ttu-id="0ffa5-138">Itemat</span><span class="sxs-lookup"><span data-stu-id="0ffa5-138">Itemat</span></span>](../api/chartcollection-itemat.md)|[<span data-ttu-id="0ffa5-139">Chart</span><span class="sxs-lookup"><span data-stu-id="0ffa5-139">Chart</span></span>](chart.md)|<span data-ttu-id="0ffa5-140">Obtiene un gráfico basado en su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-140">Gets a chart based on its position in the collection.</span></span>|
|[<span data-ttu-id="0ffa5-141">Add</span><span class="sxs-lookup"><span data-stu-id="0ffa5-141">Add</span></span>](../api/chartcollection-add.md)|[<span data-ttu-id="0ffa5-142">Chart</span><span class="sxs-lookup"><span data-stu-id="0ffa5-142">Chart</span></span>](chart.md)|<span data-ttu-id="0ffa5-143">Crea un gráfico.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-143">Creates a new chart.</span></span>|

## <a name="properties"></a><span data-ttu-id="0ffa5-144">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0ffa5-144">Properties</span></span>
| <span data-ttu-id="0ffa5-145">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0ffa5-145">Property</span></span>     | <span data-ttu-id="0ffa5-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ffa5-146">Type</span></span>   |<span data-ttu-id="0ffa5-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ffa5-147">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0ffa5-148">height</span><span class="sxs-lookup"><span data-stu-id="0ffa5-148">height</span></span>|<span data-ttu-id="0ffa5-149">Double</span><span class="sxs-lookup"><span data-stu-id="0ffa5-149">double</span></span>|<span data-ttu-id="0ffa5-150">Representa el alto, en puntos, del objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-150">Represents the height, in points, of the chart object.</span></span>|
|<span data-ttu-id="0ffa5-151">id</span><span class="sxs-lookup"><span data-stu-id="0ffa5-151">id</span></span>|<span data-ttu-id="0ffa5-152">string</span><span class="sxs-lookup"><span data-stu-id="0ffa5-152">string</span></span>|<span data-ttu-id="0ffa5-p102">Obtiene un gráfico en función de su posición en la colección. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-p102">Gets a chart based on its position in the collection. Read-only.</span></span>|
|<span data-ttu-id="0ffa5-155">left</span><span class="sxs-lookup"><span data-stu-id="0ffa5-155">left</span></span>|<span data-ttu-id="0ffa5-156">Double</span><span class="sxs-lookup"><span data-stu-id="0ffa5-156">double</span></span>|<span data-ttu-id="0ffa5-157">Distancia, en puntos, desde el lado izquierdo del gráfico hasta el origen de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-157">The distance, in points, from the left side of the chart to the worksheet origin.</span></span>|
|<span data-ttu-id="0ffa5-158">name</span><span class="sxs-lookup"><span data-stu-id="0ffa5-158">name</span></span>|<span data-ttu-id="0ffa5-159">string</span><span class="sxs-lookup"><span data-stu-id="0ffa5-159">string</span></span>|<span data-ttu-id="0ffa5-160">Representa el nombre de un objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-160">Represents the name of a chart object.</span></span>|
|<span data-ttu-id="0ffa5-161">top</span><span class="sxs-lookup"><span data-stu-id="0ffa5-161">top</span></span>|<span data-ttu-id="0ffa5-162">Double</span><span class="sxs-lookup"><span data-stu-id="0ffa5-162">double</span></span>|<span data-ttu-id="0ffa5-163">Representa la distancia, en puntos, desde el borde superior del objeto hasta la parte superior de la fila 1 (en una hoja de cálculo) o la parte superior del área del gráfico (en un gráfico).</span><span class="sxs-lookup"><span data-stu-id="0ffa5-163">Represents the distance, in points, from the top edge of the object to the top of row 1 (on a worksheet) or the top of the chart area (on a chart).</span></span>|
|<span data-ttu-id="0ffa5-164">width</span><span class="sxs-lookup"><span data-stu-id="0ffa5-164">width</span></span>|<span data-ttu-id="0ffa5-165">double</span><span class="sxs-lookup"><span data-stu-id="0ffa5-165">double</span></span>|<span data-ttu-id="0ffa5-166">Representa el ancho, en puntos, del objeto graph.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-166">Represents the width, in points, of the chart object.</span></span>|

## <a name="relationships"></a><span data-ttu-id="0ffa5-167">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0ffa5-167">Relationships</span></span>
| <span data-ttu-id="0ffa5-168">Relación</span><span class="sxs-lookup"><span data-stu-id="0ffa5-168">Relationship</span></span> | <span data-ttu-id="0ffa5-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ffa5-169">Type</span></span>   |<span data-ttu-id="0ffa5-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ffa5-170">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0ffa5-171">axes</span><span class="sxs-lookup"><span data-stu-id="0ffa5-171">axes</span></span>|[<span data-ttu-id="0ffa5-172">ChartAxes</span><span class="sxs-lookup"><span data-stu-id="0ffa5-172">ChartAxes</span></span>](chartaxes.md)|<span data-ttu-id="0ffa5-p103">Representa los ejes del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-p103">Represents chart axes. Read-only.</span></span>|
|<span data-ttu-id="0ffa5-175">dataLabels</span><span class="sxs-lookup"><span data-stu-id="0ffa5-175">dataLabels</span></span>|[<span data-ttu-id="0ffa5-176">ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="0ffa5-176">ChartDataLabels</span></span>](chartdatalabels.md)|<span data-ttu-id="0ffa5-p104">Representa la clase DataLabels del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-p104">Represents the datalabels on the chart. Read-only.</span></span>|
|<span data-ttu-id="0ffa5-179">format</span><span class="sxs-lookup"><span data-stu-id="0ffa5-179">format</span></span>|[<span data-ttu-id="0ffa5-180">ChartAreaFormat</span><span class="sxs-lookup"><span data-stu-id="0ffa5-180">ChartAreaFormat</span></span>](chartareaformat.md)|<span data-ttu-id="0ffa5-p105">Encapsula las propiedades de formato del área del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-p105">Encapsulates the format properties for the chart area. Read-only.</span></span>|
|<span data-ttu-id="0ffa5-183">legend</span><span class="sxs-lookup"><span data-stu-id="0ffa5-183">legend</span></span>|[<span data-ttu-id="0ffa5-184">ChartLegend</span><span class="sxs-lookup"><span data-stu-id="0ffa5-184">ChartLegend</span></span>](chartlegend.md)|<span data-ttu-id="0ffa5-p106">Representa la leyenda del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-p106">Represents the legend for the chart. Read-only.</span></span>|
|<span data-ttu-id="0ffa5-187">series</span><span class="sxs-lookup"><span data-stu-id="0ffa5-187">series</span></span>|<span data-ttu-id="0ffa5-188">Colección [ChartSeries](chartseries.md)</span><span class="sxs-lookup"><span data-stu-id="0ffa5-188">[ChartSeries](chartseries.md) collection</span></span>|<span data-ttu-id="0ffa5-p107">Representa una sola serie o una colección de series del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-p107">Represents either a single series or collection of series in the chart. Read-only.</span></span>|
|<span data-ttu-id="0ffa5-191">title</span><span class="sxs-lookup"><span data-stu-id="0ffa5-191">title</span></span>|[<span data-ttu-id="0ffa5-192">ChartTitle</span><span class="sxs-lookup"><span data-stu-id="0ffa5-192">ChartTitle</span></span>](charttitle.md)|<span data-ttu-id="0ffa5-p108">Representa el título del gráfico especificado, incluido el texto, la visibilidad, la posición y el formato del título. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-p108">Represents the title of the specified chart, including the text, visibility, position and formating of the title. Read-only.</span></span>|
|<span data-ttu-id="0ffa5-195">worksheet</span><span class="sxs-lookup"><span data-stu-id="0ffa5-195">worksheet</span></span>|[<span data-ttu-id="0ffa5-196">Worksheet</span><span class="sxs-lookup"><span data-stu-id="0ffa5-196">Worksheet</span></span>](worksheet.md)|<span data-ttu-id="0ffa5-p109">La hoja de cálculo que contiene el gráfico actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-p109">The worksheet containing the current chart. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0ffa5-199">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0ffa5-199">JSON representation</span></span>

<span data-ttu-id="0ffa5-200">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-200">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chart"
}-->

```json
{
  "height": 1024,
  "id": "string",
  "left": 1024,
  "name": "string",
  "top": 1024,
  "width": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Chart resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->