---
title: Tipo de recurso ChartDataLabels
description: Representa una colección de todas las etiquetas de datos en un punto del gráfico.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 7e45db4129422c32af809d46c076b2f6d82eff89
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876198"
---
# <a name="chartdatalabels-resource-type"></a><span data-ttu-id="18e74-103">Tipo de recurso ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="18e74-103">ChartDataLabels resource type</span></span>

> <span data-ttu-id="18e74-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="18e74-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="18e74-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="18e74-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="18e74-106">Representa una colección de todas las etiquetas de datos en un punto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="18e74-106">Represents a collection of all the data labels on a chart point.</span></span>


## <a name="methods"></a><span data-ttu-id="18e74-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="18e74-107">Methods</span></span>

| <span data-ttu-id="18e74-108">Método</span><span class="sxs-lookup"><span data-stu-id="18e74-108">Method</span></span>           | <span data-ttu-id="18e74-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18e74-109">Return Type</span></span>    |<span data-ttu-id="18e74-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="18e74-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="18e74-111">Get ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="18e74-111">Get ChartDataLabels</span></span>](../api/chartdatalabels-get.md) | [<span data-ttu-id="18e74-112">ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="18e74-112">ChartDataLabels</span></span>](chartdatalabels.md) |<span data-ttu-id="18e74-113">Lee las propiedades y relaciones del objeto chartDataLabels.</span><span class="sxs-lookup"><span data-stu-id="18e74-113">Read properties and relationships of chartDataLabels object.</span></span>|
|[<span data-ttu-id="18e74-114">Update</span><span class="sxs-lookup"><span data-stu-id="18e74-114">Update</span></span>](../api/chartdatalabels-update.md) | [<span data-ttu-id="18e74-115">ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="18e74-115">ChartDataLabels</span></span>](chartdatalabels.md) |<span data-ttu-id="18e74-116">Actualiza el objeto ChartDataLabels.</span><span class="sxs-lookup"><span data-stu-id="18e74-116">Update ChartDataLabels object.</span></span> |

## <a name="properties"></a><span data-ttu-id="18e74-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="18e74-117">Properties</span></span>
| <span data-ttu-id="18e74-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="18e74-118">Property</span></span>     | <span data-ttu-id="18e74-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="18e74-119">Type</span></span>   |<span data-ttu-id="18e74-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="18e74-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="18e74-121">position</span><span class="sxs-lookup"><span data-stu-id="18e74-121">position</span></span>|<span data-ttu-id="18e74-122">string</span><span class="sxs-lookup"><span data-stu-id="18e74-122">string</span></span>|<span data-ttu-id="18e74-p102">Valor DataLabelPosition que representa la posición de la etiqueta de datos. Valores posibles: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span><span class="sxs-lookup"><span data-stu-id="18e74-p102">DataLabelPosition value that represents the position of the data label. Possible values are: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span></span>|
|<span data-ttu-id="18e74-125">separator</span><span class="sxs-lookup"><span data-stu-id="18e74-125">separator</span></span>|<span data-ttu-id="18e74-126">string</span><span class="sxs-lookup"><span data-stu-id="18e74-126">string</span></span>|<span data-ttu-id="18e74-127">Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="18e74-127">String representing the separator used for the data labels on a chart.</span></span>|
|<span data-ttu-id="18e74-128">showBubbleSize</span><span class="sxs-lookup"><span data-stu-id="18e74-128">showBubbleSize</span></span>|<span data-ttu-id="18e74-129">boolean</span><span class="sxs-lookup"><span data-stu-id="18e74-129">boolean</span></span>|<span data-ttu-id="18e74-130">Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="18e74-130">Boolean value representing if the data label bubble size is visible or not.</span></span>|
|<span data-ttu-id="18e74-131">showCategoryName</span><span class="sxs-lookup"><span data-stu-id="18e74-131">showCategoryName</span></span>|<span data-ttu-id="18e74-132">boolean</span><span class="sxs-lookup"><span data-stu-id="18e74-132">boolean</span></span>|<span data-ttu-id="18e74-133">Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="18e74-133">Boolean value representing if the data label category name is visible or not.</span></span>|
|<span data-ttu-id="18e74-134">showLegendKey</span><span class="sxs-lookup"><span data-stu-id="18e74-134">showLegendKey</span></span>|<span data-ttu-id="18e74-135">boolean</span><span class="sxs-lookup"><span data-stu-id="18e74-135">boolean</span></span>|<span data-ttu-id="18e74-136">Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="18e74-136">Boolean value representing if the data label legend key is visible or not.</span></span>|
|<span data-ttu-id="18e74-137">showPercentage</span><span class="sxs-lookup"><span data-stu-id="18e74-137">showPercentage</span></span>|<span data-ttu-id="18e74-138">boolean</span><span class="sxs-lookup"><span data-stu-id="18e74-138">boolean</span></span>|<span data-ttu-id="18e74-139">Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="18e74-139">Boolean value representing if the data label percentage is visible or not.</span></span>|
|<span data-ttu-id="18e74-140">showSeriesName</span><span class="sxs-lookup"><span data-stu-id="18e74-140">showSeriesName</span></span>|<span data-ttu-id="18e74-141">boolean</span><span class="sxs-lookup"><span data-stu-id="18e74-141">boolean</span></span>|<span data-ttu-id="18e74-142">Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="18e74-142">Boolean value representing if the data label series name is visible or not.</span></span>|
|<span data-ttu-id="18e74-143">showValue</span><span class="sxs-lookup"><span data-stu-id="18e74-143">showValue</span></span>|<span data-ttu-id="18e74-144">boolean</span><span class="sxs-lookup"><span data-stu-id="18e74-144">boolean</span></span>|<span data-ttu-id="18e74-145">Valor booleano que representa si el valor de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="18e74-145">Boolean value representing if the data label value is visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="18e74-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="18e74-146">Relationships</span></span>
| <span data-ttu-id="18e74-147">Relación</span><span class="sxs-lookup"><span data-stu-id="18e74-147">Relationship</span></span> | <span data-ttu-id="18e74-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="18e74-148">Type</span></span>   |<span data-ttu-id="18e74-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="18e74-149">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="18e74-150">format</span><span class="sxs-lookup"><span data-stu-id="18e74-150">format</span></span>|[<span data-ttu-id="18e74-151">ChartDataLabelFormat</span><span class="sxs-lookup"><span data-stu-id="18e74-151">ChartDataLabelFormat</span></span>](chartdatalabelformat.md)|<span data-ttu-id="18e74-p103">Representa el formato de las etiquetas de datos del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="18e74-p103">Represents the format of chart data labels, which includes fill and font formatting. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="18e74-154">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="18e74-154">JSON representation</span></span>

<span data-ttu-id="18e74-155">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="18e74-155">Here is a JSON representation of the resource.</span></span>

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
