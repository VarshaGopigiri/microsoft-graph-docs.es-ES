---
title: Tipo de recurso ChartDataLabels
description: Representa una colección de todas las etiquetas de datos en un punto del gráfico.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: add7ef03b4779cae799949c6eb5901fcd1e3ddaf
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809012"
---
# <a name="chartdatalabels-resource-type"></a><span data-ttu-id="c58fb-103">Tipo de recurso ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="c58fb-103">ChartDataLabels resource type</span></span>

<span data-ttu-id="c58fb-104">Representa una colección de todas las etiquetas de datos en un punto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="c58fb-104">Represents a collection of all the data labels on a chart point.</span></span>


## <a name="methods"></a><span data-ttu-id="c58fb-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="c58fb-105">Methods</span></span>

| <span data-ttu-id="c58fb-106">Método</span><span class="sxs-lookup"><span data-stu-id="c58fb-106">Method</span></span>           | <span data-ttu-id="c58fb-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c58fb-107">Return Type</span></span>    |<span data-ttu-id="c58fb-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c58fb-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c58fb-109">Get ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="c58fb-109">Get ChartDataLabels</span></span>](../api/chartdatalabels-get.md) | [<span data-ttu-id="c58fb-110">WorkbookChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="c58fb-110">WorkbookChartDataLabels</span></span>](chartdatalabels.md) |<span data-ttu-id="c58fb-111">Lee las propiedades y relaciones del objeto chartDataLabels.</span><span class="sxs-lookup"><span data-stu-id="c58fb-111">Read properties and relationships of chartDataLabels object.</span></span>|
|[<span data-ttu-id="c58fb-112">Update</span><span class="sxs-lookup"><span data-stu-id="c58fb-112">Update</span></span>](../api/chartdatalabels-update.md) | [<span data-ttu-id="c58fb-113">WorkbookChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="c58fb-113">WorkbookChartDataLabels</span></span>](chartdatalabels.md) |<span data-ttu-id="c58fb-114">Actualiza el objeto ChartDataLabels.</span><span class="sxs-lookup"><span data-stu-id="c58fb-114">Update ChartDataLabels object.</span></span> |

## <a name="properties"></a><span data-ttu-id="c58fb-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c58fb-115">Properties</span></span>
| <span data-ttu-id="c58fb-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c58fb-116">Property</span></span>     | <span data-ttu-id="c58fb-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="c58fb-117">Type</span></span>   |<span data-ttu-id="c58fb-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c58fb-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c58fb-119">position</span><span class="sxs-lookup"><span data-stu-id="c58fb-119">position</span></span>|<span data-ttu-id="c58fb-120">string</span><span class="sxs-lookup"><span data-stu-id="c58fb-120">string</span></span>|<span data-ttu-id="c58fb-121">Valor de DataLabelPosition que representa la posición de la etiqueta de datos.</span><span class="sxs-lookup"><span data-stu-id="c58fb-121">DataLabelPosition value that represents the position of the data label.</span></span> <span data-ttu-id="c58fb-122">Los valores posibles son: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span><span class="sxs-lookup"><span data-stu-id="c58fb-122">The possible values are: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span></span>|
|<span data-ttu-id="c58fb-123">separator</span><span class="sxs-lookup"><span data-stu-id="c58fb-123">separator</span></span>|<span data-ttu-id="c58fb-124">string</span><span class="sxs-lookup"><span data-stu-id="c58fb-124">string</span></span>|<span data-ttu-id="c58fb-125">Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="c58fb-125">String representing the separator used for the data labels on a chart.</span></span>|
|<span data-ttu-id="c58fb-126">showBubbleSize</span><span class="sxs-lookup"><span data-stu-id="c58fb-126">showBubbleSize</span></span>|<span data-ttu-id="c58fb-127">boolean</span><span class="sxs-lookup"><span data-stu-id="c58fb-127">boolean</span></span>|<span data-ttu-id="c58fb-128">Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="c58fb-128">Boolean value representing if the data label bubble size is visible or not.</span></span>|
|<span data-ttu-id="c58fb-129">showCategoryName</span><span class="sxs-lookup"><span data-stu-id="c58fb-129">showCategoryName</span></span>|<span data-ttu-id="c58fb-130">boolean</span><span class="sxs-lookup"><span data-stu-id="c58fb-130">boolean</span></span>|<span data-ttu-id="c58fb-131">Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="c58fb-131">Boolean value representing if the data label category name is visible or not.</span></span>|
|<span data-ttu-id="c58fb-132">showLegendKey</span><span class="sxs-lookup"><span data-stu-id="c58fb-132">showLegendKey</span></span>|<span data-ttu-id="c58fb-133">boolean</span><span class="sxs-lookup"><span data-stu-id="c58fb-133">boolean</span></span>|<span data-ttu-id="c58fb-134">Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="c58fb-134">Boolean value representing if the data label legend key is visible or not.</span></span>|
|<span data-ttu-id="c58fb-135">showPercentage</span><span class="sxs-lookup"><span data-stu-id="c58fb-135">showPercentage</span></span>|<span data-ttu-id="c58fb-136">boolean</span><span class="sxs-lookup"><span data-stu-id="c58fb-136">boolean</span></span>|<span data-ttu-id="c58fb-137">Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="c58fb-137">Boolean value representing if the data label percentage is visible or not.</span></span>|
|<span data-ttu-id="c58fb-138">showSeriesName</span><span class="sxs-lookup"><span data-stu-id="c58fb-138">showSeriesName</span></span>|<span data-ttu-id="c58fb-139">boolean</span><span class="sxs-lookup"><span data-stu-id="c58fb-139">boolean</span></span>|<span data-ttu-id="c58fb-140">Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="c58fb-140">Boolean value representing if the data label series name is visible or not.</span></span>|
|<span data-ttu-id="c58fb-141">showValue</span><span class="sxs-lookup"><span data-stu-id="c58fb-141">showValue</span></span>|<span data-ttu-id="c58fb-142">boolean</span><span class="sxs-lookup"><span data-stu-id="c58fb-142">boolean</span></span>|<span data-ttu-id="c58fb-143">Valor booleano que representa si el valor de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="c58fb-143">Boolean value representing if the data label value is visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c58fb-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c58fb-144">Relationships</span></span>
| <span data-ttu-id="c58fb-145">Relación</span><span class="sxs-lookup"><span data-stu-id="c58fb-145">Relationship</span></span> | <span data-ttu-id="c58fb-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="c58fb-146">Type</span></span>   |<span data-ttu-id="c58fb-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="c58fb-147">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c58fb-148">format</span><span class="sxs-lookup"><span data-stu-id="c58fb-148">format</span></span>|[<span data-ttu-id="c58fb-149">WorkbookChartDataLabelFormat</span><span class="sxs-lookup"><span data-stu-id="c58fb-149">WorkbookChartDataLabelFormat</span></span>](chartdatalabelformat.md)|<span data-ttu-id="c58fb-p102">Representa el formato de las etiquetas de datos del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c58fb-p102">Represents the format of chart data labels, which includes fill and font formatting. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c58fb-152">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c58fb-152">JSON representation</span></span>

<span data-ttu-id="c58fb-153">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c58fb-153">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartDataLabels"
}-->

```json
{
  "position": "string",
  "separator": "string",
  "showBubbleSize": true,
  "showCategoryName": true,
  "showLegendKey": true,
  "showPercentage": true,
  "showSeriesName": true,
  "showValue": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartDataLabels resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
