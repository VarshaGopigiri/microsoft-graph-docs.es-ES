---
title: Tipo de recurso ChartDataLabels
description: Representa una colección de todas las etiquetas de datos en un punto del gráfico.
author: lumine2008
ms.openlocfilehash: 39c95d0849d398df7d57f676cc392c157e6f43f5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339056"
---
# <a name="chartdatalabels-resource-type"></a><span data-ttu-id="51264-103">Tipo de recurso ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="51264-103">ChartDataLabels resource type</span></span>

<span data-ttu-id="51264-104">Representa una colección de todas las etiquetas de datos en un punto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="51264-104">Represents a collection of all the data labels on a chart point.</span></span>


## <a name="methods"></a><span data-ttu-id="51264-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="51264-105">Methods</span></span>

| <span data-ttu-id="51264-106">Método</span><span class="sxs-lookup"><span data-stu-id="51264-106">Method</span></span>           | <span data-ttu-id="51264-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51264-107">Return Type</span></span>    |<span data-ttu-id="51264-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="51264-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="51264-109">Get ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="51264-109">Get ChartDataLabels</span></span>](../api/chartdatalabels-get.md) | [<span data-ttu-id="51264-110">WorkbookChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="51264-110">WorkbookChartDataLabels</span></span>](chartdatalabels.md) |<span data-ttu-id="51264-111">Lee las propiedades y relaciones del objeto chartDataLabels.</span><span class="sxs-lookup"><span data-stu-id="51264-111">Read properties and relationships of chartDataLabels object.</span></span>|
|[<span data-ttu-id="51264-112">Actualizar</span><span class="sxs-lookup"><span data-stu-id="51264-112">Update</span></span>](../api/chartdatalabels-update.md) | [<span data-ttu-id="51264-113">WorkbookChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="51264-113">WorkbookChartDataLabels</span></span>](chartdatalabels.md) |<span data-ttu-id="51264-114">Actualiza el objeto ChartDataLabels.</span><span class="sxs-lookup"><span data-stu-id="51264-114">Update ChartDataLabels object.</span></span> |

## <a name="properties"></a><span data-ttu-id="51264-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51264-115">Properties</span></span>
| <span data-ttu-id="51264-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51264-116">Property</span></span>     | <span data-ttu-id="51264-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="51264-117">Type</span></span>   |<span data-ttu-id="51264-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="51264-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="51264-119">position</span><span class="sxs-lookup"><span data-stu-id="51264-119">position</span></span>|<span data-ttu-id="51264-120">string</span><span class="sxs-lookup"><span data-stu-id="51264-120">string</span></span>|<span data-ttu-id="51264-121">Valor de DataLabelPosition que representa la posición de la etiqueta de datos.</span><span class="sxs-lookup"><span data-stu-id="51264-121">DataLabelPosition value that represents the position of the data label.</span></span> <span data-ttu-id="51264-122">Los valores posibles son: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span><span class="sxs-lookup"><span data-stu-id="51264-122">The possible values are: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span></span>|
|<span data-ttu-id="51264-123">separator</span><span class="sxs-lookup"><span data-stu-id="51264-123">separator</span></span>|<span data-ttu-id="51264-124">string</span><span class="sxs-lookup"><span data-stu-id="51264-124">string</span></span>|<span data-ttu-id="51264-125">Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="51264-125">String representing the separator used for the data labels on a chart.</span></span>|
|<span data-ttu-id="51264-126">showBubbleSize</span><span class="sxs-lookup"><span data-stu-id="51264-126">showBubbleSize</span></span>|<span data-ttu-id="51264-127">boolean</span><span class="sxs-lookup"><span data-stu-id="51264-127">boolean</span></span>|<span data-ttu-id="51264-128">Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="51264-128">Boolean value representing if the data label bubble size is visible or not.</span></span>|
|<span data-ttu-id="51264-129">showCategoryName</span><span class="sxs-lookup"><span data-stu-id="51264-129">showCategoryName</span></span>|<span data-ttu-id="51264-130">boolean</span><span class="sxs-lookup"><span data-stu-id="51264-130">boolean</span></span>|<span data-ttu-id="51264-131">Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="51264-131">Boolean value representing if the data label category name is visible or not.</span></span>|
|<span data-ttu-id="51264-132">showLegendKey</span><span class="sxs-lookup"><span data-stu-id="51264-132">showLegendKey</span></span>|<span data-ttu-id="51264-133">boolean</span><span class="sxs-lookup"><span data-stu-id="51264-133">boolean</span></span>|<span data-ttu-id="51264-134">Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="51264-134">Boolean value representing if the data label legend key is visible or not.</span></span>|
|<span data-ttu-id="51264-135">showPercentage</span><span class="sxs-lookup"><span data-stu-id="51264-135">showPercentage</span></span>|<span data-ttu-id="51264-136">boolean</span><span class="sxs-lookup"><span data-stu-id="51264-136">boolean</span></span>|<span data-ttu-id="51264-137">Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="51264-137">Boolean value representing if the data label percentage is visible or not.</span></span>|
|<span data-ttu-id="51264-138">showSeriesName</span><span class="sxs-lookup"><span data-stu-id="51264-138">showSeriesName</span></span>|<span data-ttu-id="51264-139">boolean</span><span class="sxs-lookup"><span data-stu-id="51264-139">boolean</span></span>|<span data-ttu-id="51264-140">Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="51264-140">Boolean value representing if the data label series name is visible or not.</span></span>|
|<span data-ttu-id="51264-141">showValue</span><span class="sxs-lookup"><span data-stu-id="51264-141">showValue</span></span>|<span data-ttu-id="51264-142">boolean</span><span class="sxs-lookup"><span data-stu-id="51264-142">boolean</span></span>|<span data-ttu-id="51264-143">Valor booleano que representa si el valor de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="51264-143">Boolean value representing if the data label value is visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="51264-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="51264-144">Relationships</span></span>
| <span data-ttu-id="51264-145">Relación</span><span class="sxs-lookup"><span data-stu-id="51264-145">Relationship</span></span> | <span data-ttu-id="51264-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="51264-146">Type</span></span>   |<span data-ttu-id="51264-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="51264-147">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="51264-148">format</span><span class="sxs-lookup"><span data-stu-id="51264-148">format</span></span>|[<span data-ttu-id="51264-149">WorkbookChartDataLabelFormat</span><span class="sxs-lookup"><span data-stu-id="51264-149">WorkbookChartDataLabelFormat</span></span>](chartdatalabelformat.md)|<span data-ttu-id="51264-p102">Representa el formato de las etiquetas de datos del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="51264-p102">Represents the format of chart data labels, which includes fill and font formatting. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="51264-152">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="51264-152">JSON representation</span></span>

<span data-ttu-id="51264-153">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="51264-153">Here is a JSON representation of the resource.</span></span>

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