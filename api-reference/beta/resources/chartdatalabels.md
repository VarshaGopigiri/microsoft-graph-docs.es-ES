---
title: Tipo de recurso ChartDataLabels
description: Representa una colección de todas las etiquetas de datos en un punto del gráfico.
ms.openlocfilehash: d226c5edb3fecc3a2e27fae32060f786f790d7e7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088353"
---
# <a name="chartdatalabels-resource-type"></a><span data-ttu-id="9a697-103">Tipo de recurso ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="9a697-103">ChartDataLabels resource type</span></span>

> <span data-ttu-id="9a697-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9a697-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9a697-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9a697-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9a697-106">Representa una colección de todas las etiquetas de datos en un punto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="9a697-106">Represents a collection of all the data labels on a chart point.</span></span>


## <a name="methods"></a><span data-ttu-id="9a697-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="9a697-107">Methods</span></span>

| <span data-ttu-id="9a697-108">Método</span><span class="sxs-lookup"><span data-stu-id="9a697-108">Method</span></span>           | <span data-ttu-id="9a697-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a697-109">Return Type</span></span>    |<span data-ttu-id="9a697-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a697-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9a697-111">Get ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="9a697-111">Get ChartDataLabels</span></span>](../api/chartdatalabels-get.md) | [<span data-ttu-id="9a697-112">ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="9a697-112">ChartDataLabels</span></span>](chartdatalabels.md) |<span data-ttu-id="9a697-113">Lee las propiedades y relaciones del objeto chartDataLabels.</span><span class="sxs-lookup"><span data-stu-id="9a697-113">Read properties and relationships of chartDataLabels object.</span></span>|
|[<span data-ttu-id="9a697-114">Update</span><span class="sxs-lookup"><span data-stu-id="9a697-114">Update</span></span>](../api/chartdatalabels-update.md) | [<span data-ttu-id="9a697-115">ChartDataLabels</span><span class="sxs-lookup"><span data-stu-id="9a697-115">ChartDataLabels</span></span>](chartdatalabels.md) |<span data-ttu-id="9a697-116">Actualiza el objeto ChartDataLabels.</span><span class="sxs-lookup"><span data-stu-id="9a697-116">Update ChartDataLabels object.</span></span> |

## <a name="properties"></a><span data-ttu-id="9a697-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a697-117">Properties</span></span>
| <span data-ttu-id="9a697-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9a697-118">Property</span></span>     | <span data-ttu-id="9a697-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a697-119">Type</span></span>   |<span data-ttu-id="9a697-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a697-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9a697-121">position</span><span class="sxs-lookup"><span data-stu-id="9a697-121">position</span></span>|<span data-ttu-id="9a697-122">string</span><span class="sxs-lookup"><span data-stu-id="9a697-122">string</span></span>|<span data-ttu-id="9a697-p102">Valor DataLabelPosition que representa la posición de la etiqueta de datos. Valores posibles: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span><span class="sxs-lookup"><span data-stu-id="9a697-p102">DataLabelPosition value that represents the position of the data label. Possible values are: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span></span>|
|<span data-ttu-id="9a697-125">separator</span><span class="sxs-lookup"><span data-stu-id="9a697-125">separator</span></span>|<span data-ttu-id="9a697-126">string</span><span class="sxs-lookup"><span data-stu-id="9a697-126">string</span></span>|<span data-ttu-id="9a697-127">Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="9a697-127">String representing the separator used for the data labels on a chart.</span></span>|
|<span data-ttu-id="9a697-128">showBubbleSize</span><span class="sxs-lookup"><span data-stu-id="9a697-128">showBubbleSize</span></span>|<span data-ttu-id="9a697-129">boolean</span><span class="sxs-lookup"><span data-stu-id="9a697-129">boolean</span></span>|<span data-ttu-id="9a697-130">Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="9a697-130">Boolean value representing if the data label bubble size is visible or not.</span></span>|
|<span data-ttu-id="9a697-131">showCategoryName</span><span class="sxs-lookup"><span data-stu-id="9a697-131">showCategoryName</span></span>|<span data-ttu-id="9a697-132">boolean</span><span class="sxs-lookup"><span data-stu-id="9a697-132">boolean</span></span>|<span data-ttu-id="9a697-133">Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="9a697-133">Boolean value representing if the data label category name is visible or not.</span></span>|
|<span data-ttu-id="9a697-134">showLegendKey</span><span class="sxs-lookup"><span data-stu-id="9a697-134">showLegendKey</span></span>|<span data-ttu-id="9a697-135">boolean</span><span class="sxs-lookup"><span data-stu-id="9a697-135">boolean</span></span>|<span data-ttu-id="9a697-136">Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="9a697-136">Boolean value representing if the data label legend key is visible or not.</span></span>|
|<span data-ttu-id="9a697-137">showPercentage</span><span class="sxs-lookup"><span data-stu-id="9a697-137">showPercentage</span></span>|<span data-ttu-id="9a697-138">boolean</span><span class="sxs-lookup"><span data-stu-id="9a697-138">boolean</span></span>|<span data-ttu-id="9a697-139">Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="9a697-139">Boolean value representing if the data label percentage is visible or not.</span></span>|
|<span data-ttu-id="9a697-140">showSeriesName</span><span class="sxs-lookup"><span data-stu-id="9a697-140">showSeriesName</span></span>|<span data-ttu-id="9a697-141">boolean</span><span class="sxs-lookup"><span data-stu-id="9a697-141">boolean</span></span>|<span data-ttu-id="9a697-142">Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="9a697-142">Boolean value representing if the data label series name is visible or not.</span></span>|
|<span data-ttu-id="9a697-143">showValue</span><span class="sxs-lookup"><span data-stu-id="9a697-143">showValue</span></span>|<span data-ttu-id="9a697-144">boolean</span><span class="sxs-lookup"><span data-stu-id="9a697-144">boolean</span></span>|<span data-ttu-id="9a697-145">Valor booleano que representa si el valor de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="9a697-145">Boolean value representing if the data label value is visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9a697-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9a697-146">Relationships</span></span>
| <span data-ttu-id="9a697-147">Relación</span><span class="sxs-lookup"><span data-stu-id="9a697-147">Relationship</span></span> | <span data-ttu-id="9a697-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a697-148">Type</span></span>   |<span data-ttu-id="9a697-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a697-149">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9a697-150">format</span><span class="sxs-lookup"><span data-stu-id="9a697-150">format</span></span>|[<span data-ttu-id="9a697-151">ChartDataLabelFormat</span><span class="sxs-lookup"><span data-stu-id="9a697-151">ChartDataLabelFormat</span></span>](chartdatalabelformat.md)|<span data-ttu-id="9a697-p103">Representa el formato de las etiquetas de datos del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a697-p103">Represents the format of chart data labels, which includes fill and font formatting. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9a697-154">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9a697-154">JSON representation</span></span>

<span data-ttu-id="9a697-155">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9a697-155">Here is a JSON representation of the resource.</span></span>

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