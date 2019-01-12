---
title: Tipo de recurso ChartDataLabels
description: Representa una colección de todas las etiquetas de datos en un punto del gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 16e2e3acafc98a4066b8620f41f15c7cae1667cc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27954683"
---
# <a name="chartdatalabels-resource-type"></a><span data-ttu-id="ffda2-103">Tipo de recurso ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="ffda2-103">ChartDataLabels resource type</span></span>

> <span data-ttu-id="ffda2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ffda2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ffda2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ffda2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ffda2-106">Representa una colección de todas las etiquetas de datos en un punto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="ffda2-106">Represents a collection of all the data labels on a chart point.</span></span>


## <a name="methods"></a><span data-ttu-id="ffda2-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="ffda2-107">Methods</span></span>

| <span data-ttu-id="ffda2-108">Método</span><span class="sxs-lookup"><span data-stu-id="ffda2-108">Method</span></span>           | <span data-ttu-id="ffda2-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffda2-109">Return Type</span></span>    |<span data-ttu-id="ffda2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffda2-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ffda2-111">Get ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="ffda2-111">Get ChartDataLabels</span></span>](../api/chartdatalabels-get.md) | [<span data-ttu-id="ffda2-112">ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="ffda2-112">ChartDataLabels</span></span>](chartdatalabels.md) |<span data-ttu-id="ffda2-113">Lee las propiedades y relaciones del objeto chartDataLabels.</span><span class="sxs-lookup"><span data-stu-id="ffda2-113">Read properties and relationships of chartDataLabels object.</span></span>|
|[<span data-ttu-id="ffda2-114">Update</span><span class="sxs-lookup"><span data-stu-id="ffda2-114">Update</span></span>](../api/chartdatalabels-update.md) | [<span data-ttu-id="ffda2-115">ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="ffda2-115">ChartDataLabels</span></span>](chartdatalabels.md) |<span data-ttu-id="ffda2-116">Actualiza el objeto ChartDataLabels.</span><span class="sxs-lookup"><span data-stu-id="ffda2-116">Update ChartDataLabels object.</span></span> |

## <a name="properties"></a><span data-ttu-id="ffda2-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ffda2-117">Properties</span></span>
| <span data-ttu-id="ffda2-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ffda2-118">Property</span></span>     | <span data-ttu-id="ffda2-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffda2-119">Type</span></span>   |<span data-ttu-id="ffda2-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffda2-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ffda2-121">position</span><span class="sxs-lookup"><span data-stu-id="ffda2-121">position</span></span>|<span data-ttu-id="ffda2-122">string</span><span class="sxs-lookup"><span data-stu-id="ffda2-122">string</span></span>|<span data-ttu-id="ffda2-p102">Valor DataLabelPosition que representa la posición de la etiqueta de datos. Valores posibles: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span><span class="sxs-lookup"><span data-stu-id="ffda2-p102">DataLabelPosition value that represents the position of the data label. Possible values are: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span></span>|
|<span data-ttu-id="ffda2-125">separator</span><span class="sxs-lookup"><span data-stu-id="ffda2-125">separator</span></span>|<span data-ttu-id="ffda2-126">string</span><span class="sxs-lookup"><span data-stu-id="ffda2-126">string</span></span>|<span data-ttu-id="ffda2-127">Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="ffda2-127">String representing the separator used for the data labels on a chart.</span></span>|
|<span data-ttu-id="ffda2-128">showBubbleSize</span><span class="sxs-lookup"><span data-stu-id="ffda2-128">showBubbleSize</span></span>|<span data-ttu-id="ffda2-129">boolean</span><span class="sxs-lookup"><span data-stu-id="ffda2-129">boolean</span></span>|<span data-ttu-id="ffda2-130">Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ffda2-130">Boolean value representing if the data label bubble size is visible or not.</span></span>|
|<span data-ttu-id="ffda2-131">showCategoryName</span><span class="sxs-lookup"><span data-stu-id="ffda2-131">showCategoryName</span></span>|<span data-ttu-id="ffda2-132">boolean</span><span class="sxs-lookup"><span data-stu-id="ffda2-132">boolean</span></span>|<span data-ttu-id="ffda2-133">Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ffda2-133">Boolean value representing if the data label category name is visible or not.</span></span>|
|<span data-ttu-id="ffda2-134">showLegendKey</span><span class="sxs-lookup"><span data-stu-id="ffda2-134">showLegendKey</span></span>|<span data-ttu-id="ffda2-135">boolean</span><span class="sxs-lookup"><span data-stu-id="ffda2-135">boolean</span></span>|<span data-ttu-id="ffda2-136">Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ffda2-136">Boolean value representing if the data label legend key is visible or not.</span></span>|
|<span data-ttu-id="ffda2-137">showPercentage</span><span class="sxs-lookup"><span data-stu-id="ffda2-137">showPercentage</span></span>|<span data-ttu-id="ffda2-138">boolean</span><span class="sxs-lookup"><span data-stu-id="ffda2-138">boolean</span></span>|<span data-ttu-id="ffda2-139">Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ffda2-139">Boolean value representing if the data label percentage is visible or not.</span></span>|
|<span data-ttu-id="ffda2-140">showSeriesName</span><span class="sxs-lookup"><span data-stu-id="ffda2-140">showSeriesName</span></span>|<span data-ttu-id="ffda2-141">boolean</span><span class="sxs-lookup"><span data-stu-id="ffda2-141">boolean</span></span>|<span data-ttu-id="ffda2-142">Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ffda2-142">Boolean value representing if the data label series name is visible or not.</span></span>|
|<span data-ttu-id="ffda2-143">showValue</span><span class="sxs-lookup"><span data-stu-id="ffda2-143">showValue</span></span>|<span data-ttu-id="ffda2-144">boolean</span><span class="sxs-lookup"><span data-stu-id="ffda2-144">boolean</span></span>|<span data-ttu-id="ffda2-145">Valor booleano que representa si el valor de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ffda2-145">Boolean value representing if the data label value is visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ffda2-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ffda2-146">Relationships</span></span>
| <span data-ttu-id="ffda2-147">Relación</span><span class="sxs-lookup"><span data-stu-id="ffda2-147">Relationship</span></span> | <span data-ttu-id="ffda2-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffda2-148">Type</span></span>   |<span data-ttu-id="ffda2-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffda2-149">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ffda2-150">format</span><span class="sxs-lookup"><span data-stu-id="ffda2-150">format</span></span>|[<span data-ttu-id="ffda2-151">ChartDataLabelFormat</span><span class="sxs-lookup"><span data-stu-id="ffda2-151">ChartDataLabelFormat</span></span>](chartdatalabelformat.md)|<span data-ttu-id="ffda2-p103">Representa el formato de las etiquetas de datos del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ffda2-p103">Represents the format of chart data labels, which includes fill and font formatting. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ffda2-154">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ffda2-154">JSON representation</span></span>

<span data-ttu-id="ffda2-155">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ffda2-155">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartDataLabels"
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
