---
title: Tipo de recurso Chart
description: Representa un objeto de gráfico de una hoja de cálculo.
ms.openlocfilehash: bada94032dcc00e3f6294b20559f44044570f2ec
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030114"
---
# <a name="chart-resource-type"></a><span data-ttu-id="80170-103">Tipo de recurso Chart</span><span class="sxs-lookup"><span data-stu-id="80170-103">Chart resource type</span></span>

<span data-ttu-id="80170-104">Representa un objeto de gráfico de una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="80170-104">Represents a chart object in a workbook.</span></span>


## <a name="methods"></a><span data-ttu-id="80170-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="80170-105">Methods</span></span>

| <span data-ttu-id="80170-106">Método</span><span class="sxs-lookup"><span data-stu-id="80170-106">Method</span></span>           | <span data-ttu-id="80170-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80170-107">Return Type</span></span>    |<span data-ttu-id="80170-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="80170-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="80170-109">Get Chart</span><span class="sxs-lookup"><span data-stu-id="80170-109">Get Chart</span></span>](../api/chart-get.md) | [<span data-ttu-id="80170-110">WorkbookChart</span><span class="sxs-lookup"><span data-stu-id="80170-110">WorkbookChart</span></span>](chart.md) |<span data-ttu-id="80170-111">Lee las propiedades y relaciones del objeto chart.</span><span class="sxs-lookup"><span data-stu-id="80170-111">Read properties and relationships of chart object.</span></span>|
|[<span data-ttu-id="80170-112">Create ChartSeries</span><span class="sxs-lookup"><span data-stu-id="80170-112">Create ChartSeries</span></span>](../api/chart-post-series.md) |[<span data-ttu-id="80170-113">WorkbookChartSeries</span><span class="sxs-lookup"><span data-stu-id="80170-113">WorkbookChartSeries</span></span>](chartseries.md)| <span data-ttu-id="80170-114">Crea un ChartSeries publicándolo en la colección series.</span><span class="sxs-lookup"><span data-stu-id="80170-114">Create a new ChartSeries by posting to the series collection.</span></span>|
|[<span data-ttu-id="80170-115">List series</span><span class="sxs-lookup"><span data-stu-id="80170-115">List series</span></span>](../api/chart-list-series.md) |<span data-ttu-id="80170-116">Colección de [WorkbookChartSeries](chartseries.md)</span><span class="sxs-lookup"><span data-stu-id="80170-116">[WorkbookChartSeries](chartseries.md) collection</span></span>| <span data-ttu-id="80170-117">Obtiene una colección de objetos ChartSeries.</span><span class="sxs-lookup"><span data-stu-id="80170-117">Get a ChartSeries object collection.</span></span>|
|[<span data-ttu-id="80170-118">Update</span><span class="sxs-lookup"><span data-stu-id="80170-118">Update</span></span>](../api/chart-update.md) | [<span data-ttu-id="80170-119">WorkbookChart</span><span class="sxs-lookup"><span data-stu-id="80170-119">WorkbookChart</span></span>](chart.md)   |<span data-ttu-id="80170-120">Actualiza el objeto Chart.</span><span class="sxs-lookup"><span data-stu-id="80170-120">Update Chart object.</span></span> |
|[<span data-ttu-id="80170-121">Image</span><span class="sxs-lookup"><span data-stu-id="80170-121">Image</span></span>](../api/chart-image.md)|<span data-ttu-id="80170-122">Cadena codificada en base64 de imagen</span><span class="sxs-lookup"><span data-stu-id="80170-122">Image base64 encoded string</span></span>|<span data-ttu-id="80170-123">Representa el gráfico como una imagen con codificación base64 al escalar el gráfico a las dimensiones especificadas.</span><span class="sxs-lookup"><span data-stu-id="80170-123">Renders the chart as a base64-encoded image by scaling the chart to fit the specified dimensions.</span></span>|
|[<span data-ttu-id="80170-124">Delete</span><span class="sxs-lookup"><span data-stu-id="80170-124">Delete</span></span>](../api/chart-delete.md)|<span data-ttu-id="80170-125">None</span><span class="sxs-lookup"><span data-stu-id="80170-125">None</span></span>|<span data-ttu-id="80170-126">Elimina el objeto chart.</span><span class="sxs-lookup"><span data-stu-id="80170-126">Deletes the chart object.</span></span>|
|[<span data-ttu-id="80170-127">Setdata</span><span class="sxs-lookup"><span data-stu-id="80170-127">Setdata</span></span>](../api/chart-setdata.md)|<span data-ttu-id="80170-128">None</span><span class="sxs-lookup"><span data-stu-id="80170-128">None</span></span>|<span data-ttu-id="80170-129">Restablece los datos de origen del gráfico.</span><span class="sxs-lookup"><span data-stu-id="80170-129">Resets the source data for the chart.</span></span>|
|[<span data-ttu-id="80170-130">Setposition</span><span class="sxs-lookup"><span data-stu-id="80170-130">Setposition</span></span>](../api/chart-setposition.md)|<span data-ttu-id="80170-131">None</span><span class="sxs-lookup"><span data-stu-id="80170-131">None</span></span>|<span data-ttu-id="80170-132">Coloca el gráfico con respecto a las celdas de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="80170-132">Positions the chart relative to cells on the worksheet.</span></span>|
|[<span data-ttu-id="80170-133">List</span><span class="sxs-lookup"><span data-stu-id="80170-133">List</span></span>](../api/chart-list.md) | <span data-ttu-id="80170-134">Colección de [WorkbookChart](chart.md)</span><span class="sxs-lookup"><span data-stu-id="80170-134">[WorkbookChart](chart.md) collection</span></span> |<span data-ttu-id="80170-135">Obtiene la colección de objetos chart.</span><span class="sxs-lookup"><span data-stu-id="80170-135">Get chart object collection.</span></span> |
|[<span data-ttu-id="80170-136">Itemat</span><span class="sxs-lookup"><span data-stu-id="80170-136">Itemat</span></span>](../api/chartcollection-itemat.md)|[<span data-ttu-id="80170-137">WorkbookChart</span><span class="sxs-lookup"><span data-stu-id="80170-137">WorkbookChart</span></span>](chart.md)|<span data-ttu-id="80170-138">Obtiene un gráfico en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="80170-138">Gets a chart based on its position in the collection.</span></span>|
|[<span data-ttu-id="80170-139">Add</span><span class="sxs-lookup"><span data-stu-id="80170-139">Add</span></span>](../api/chartcollection-add.md)|[<span data-ttu-id="80170-140">WorkbookChart</span><span class="sxs-lookup"><span data-stu-id="80170-140">WorkbookChart</span></span>](chart.md)|<span data-ttu-id="80170-141">Crea un gráfico.</span><span class="sxs-lookup"><span data-stu-id="80170-141">Creates a new chart.</span></span>|

## <a name="properties"></a><span data-ttu-id="80170-142">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80170-142">Properties</span></span>
| <span data-ttu-id="80170-143">Propiedad</span><span class="sxs-lookup"><span data-stu-id="80170-143">Property</span></span>     | <span data-ttu-id="80170-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="80170-144">Type</span></span>   |<span data-ttu-id="80170-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="80170-145">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="80170-146">height</span><span class="sxs-lookup"><span data-stu-id="80170-146">height</span></span>|<span data-ttu-id="80170-147">Double</span><span class="sxs-lookup"><span data-stu-id="80170-147">double</span></span>|<span data-ttu-id="80170-148">Representa el alto, en puntos, del objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="80170-148">Represents the height, in points, of the chart object.</span></span>|
|<span data-ttu-id="80170-149">id</span><span class="sxs-lookup"><span data-stu-id="80170-149">id</span></span>|<span data-ttu-id="80170-150">string</span><span class="sxs-lookup"><span data-stu-id="80170-150">string</span></span>|<span data-ttu-id="80170-p101">Obtiene un gráfico en función de su posición en la colección. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="80170-p101">Gets a chart based on its position in the collection. Read-only.</span></span>|
|<span data-ttu-id="80170-153">left</span><span class="sxs-lookup"><span data-stu-id="80170-153">left</span></span>|<span data-ttu-id="80170-154">Double</span><span class="sxs-lookup"><span data-stu-id="80170-154">double</span></span>|<span data-ttu-id="80170-155">Distancia, en puntos, desde el lado izquierdo del gráfico hasta el origen de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="80170-155">The distance, in points, from the left side of the chart to the worksheet origin.</span></span>|
|<span data-ttu-id="80170-156">name</span><span class="sxs-lookup"><span data-stu-id="80170-156">name</span></span>|<span data-ttu-id="80170-157">string</span><span class="sxs-lookup"><span data-stu-id="80170-157">string</span></span>|<span data-ttu-id="80170-158">Representa el nombre de un objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="80170-158">Represents the name of a chart object.</span></span>|
|<span data-ttu-id="80170-159">top</span><span class="sxs-lookup"><span data-stu-id="80170-159">top</span></span>|<span data-ttu-id="80170-160">Double</span><span class="sxs-lookup"><span data-stu-id="80170-160">double</span></span>|<span data-ttu-id="80170-161">Representa la distancia, en puntos, desde el borde superior del objeto hasta la parte superior de la fila 1 (en una hoja de cálculo) o la parte superior del área del gráfico (en un gráfico).</span><span class="sxs-lookup"><span data-stu-id="80170-161">Represents the distance, in points, from the top edge of the object to the top of row 1 (on a worksheet) or the top of the chart area (on a chart).</span></span>|
|<span data-ttu-id="80170-162">width</span><span class="sxs-lookup"><span data-stu-id="80170-162">width</span></span>|<span data-ttu-id="80170-163">double</span><span class="sxs-lookup"><span data-stu-id="80170-163">double</span></span>|<span data-ttu-id="80170-164">Representa el ancho, en puntos, del objeto graph.</span><span class="sxs-lookup"><span data-stu-id="80170-164">Represents the width, in points, of the chart object.</span></span>|

## <a name="relationships"></a><span data-ttu-id="80170-165">Relaciones</span><span class="sxs-lookup"><span data-stu-id="80170-165">Relationships</span></span>
| <span data-ttu-id="80170-166">Relación</span><span class="sxs-lookup"><span data-stu-id="80170-166">Relationship</span></span> | <span data-ttu-id="80170-167">Tipo</span><span class="sxs-lookup"><span data-stu-id="80170-167">Type</span></span>   |<span data-ttu-id="80170-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="80170-168">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="80170-169">axes</span><span class="sxs-lookup"><span data-stu-id="80170-169">axes</span></span>|[<span data-ttu-id="80170-170">WorkbookChartAxes</span><span class="sxs-lookup"><span data-stu-id="80170-170">WorkbookChartAxes</span></span>](chartaxes.md)|<span data-ttu-id="80170-p102">Representa los ejes del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="80170-p102">Represents chart axes. Read-only.</span></span>|
|<span data-ttu-id="80170-173">dataLabels</span><span class="sxs-lookup"><span data-stu-id="80170-173">dataLabels</span></span>|[<span data-ttu-id="80170-174">WorkbookChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="80170-174">WorkbookChartDataLabels</span></span>](chartdatalabels.md)|<span data-ttu-id="80170-p103">Representa la clase DataLabels del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="80170-p103">Represents the datalabels on the chart. Read-only.</span></span>|
|<span data-ttu-id="80170-177">format</span><span class="sxs-lookup"><span data-stu-id="80170-177">format</span></span>|[<span data-ttu-id="80170-178">WorkbookChartAreaFormat</span><span class="sxs-lookup"><span data-stu-id="80170-178">WorkbookChartAreaFormat</span></span>](chartareaformat.md)|<span data-ttu-id="80170-p104">Encapsula las propiedades de formato del área del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="80170-p104">Encapsulates the format properties for the chart area. Read-only.</span></span>|
|<span data-ttu-id="80170-181">legend</span><span class="sxs-lookup"><span data-stu-id="80170-181">legend</span></span>|[<span data-ttu-id="80170-182">WorkbookChartLegend</span><span class="sxs-lookup"><span data-stu-id="80170-182">WorkbookChartLegend</span></span>](chartlegend.md)|<span data-ttu-id="80170-p105">Representa la leyenda del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="80170-p105">Represents the legend for the chart. Read-only.</span></span>|
|<span data-ttu-id="80170-185">series</span><span class="sxs-lookup"><span data-stu-id="80170-185">series</span></span>|<span data-ttu-id="80170-186">Colección de [WorkbookChartSeries](chartseries.md)</span><span class="sxs-lookup"><span data-stu-id="80170-186">[WorkbookChartSeries](chartseries.md) collection</span></span>|<span data-ttu-id="80170-p106">Representa una sola serie o una colección de series del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="80170-p106">Represents either a single series or collection of series in the chart. Read-only.</span></span>|
|<span data-ttu-id="80170-189">title</span><span class="sxs-lookup"><span data-stu-id="80170-189">title</span></span>|[<span data-ttu-id="80170-190">WorkbookChartTitle</span><span class="sxs-lookup"><span data-stu-id="80170-190">WorkbookChartTitle</span></span>](charttitle.md)|<span data-ttu-id="80170-p107">Representa el título del gráfico especificado, incluido el texto, la visibilidad, la posición y el formato del título. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="80170-p107">Represents the title of the specified chart, including the text, visibility, position and formating of the title. Read-only.</span></span>|
|<span data-ttu-id="80170-193">worksheet</span><span class="sxs-lookup"><span data-stu-id="80170-193">worksheet</span></span>|[<span data-ttu-id="80170-194">WorkbookWorksheet</span><span class="sxs-lookup"><span data-stu-id="80170-194">WorkbookWorksheet</span></span>](worksheet.md)|<span data-ttu-id="80170-p108">La hoja de cálculo que contiene el gráfico actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="80170-p108">The worksheet containing the current chart. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="80170-197">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="80170-197">JSON representation</span></span>

<span data-ttu-id="80170-198">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="80170-198">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChart"
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