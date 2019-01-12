---
title: Tipo de recurso ChartAxis
description: Representa un solo eje de un gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: c6344f2bbb102e2e2402dba267538cb46d4c0fbe
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27914195"
---
# <a name="chartaxis-resource-type"></a><span data-ttu-id="a6342-103">Tipo de recurso ChartAxis</span><span class="sxs-lookup"><span data-stu-id="a6342-103">ChartAxis resource type</span></span>

> <span data-ttu-id="a6342-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a6342-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a6342-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a6342-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a6342-106">Representa un solo eje de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="a6342-106">Represents a single axis in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="a6342-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="a6342-107">Methods</span></span>

| <span data-ttu-id="a6342-108">Método</span><span class="sxs-lookup"><span data-stu-id="a6342-108">Method</span></span>           | <span data-ttu-id="a6342-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6342-109">Return Type</span></span>    |<span data-ttu-id="a6342-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6342-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a6342-111">Get ChartAxis</span><span class="sxs-lookup"><span data-stu-id="a6342-111">Get ChartAxis</span></span>](../api/chartaxis-get.md) | [<span data-ttu-id="a6342-112">ChartAxis</span><span class="sxs-lookup"><span data-stu-id="a6342-112">ChartAxis</span></span>](chartaxis.md) |<span data-ttu-id="a6342-113">Lee las propiedades y relaciones del objeto chartAxis.</span><span class="sxs-lookup"><span data-stu-id="a6342-113">Read properties and relationships of chartAxis object.</span></span>|
|[<span data-ttu-id="a6342-114">Update</span><span class="sxs-lookup"><span data-stu-id="a6342-114">Update</span></span>](../api/chartaxis-update.md) | [<span data-ttu-id="a6342-115">ChartAxis</span><span class="sxs-lookup"><span data-stu-id="a6342-115">ChartAxis</span></span>](chartaxis.md)   |<span data-ttu-id="a6342-116">Actualiza el objeto ChartAxis.</span><span class="sxs-lookup"><span data-stu-id="a6342-116">Update ChartAxis object.</span></span> |

## <a name="properties"></a><span data-ttu-id="a6342-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a6342-117">Properties</span></span>
| <span data-ttu-id="a6342-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a6342-118">Property</span></span>     | <span data-ttu-id="a6342-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6342-119">Type</span></span>   |<span data-ttu-id="a6342-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6342-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a6342-121">majorUnit</span><span class="sxs-lookup"><span data-stu-id="a6342-121">majorUnit</span></span>|<span data-ttu-id="a6342-122">object</span><span class="sxs-lookup"><span data-stu-id="a6342-122">object</span></span>|<span data-ttu-id="a6342-p102">Representa el intervalo entre dos marcas de graduación principales. Puede establecerse en un valor numérico o en una cadena vacía.  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="a6342-p102">Represents the interval between two major tick marks. Can be set to a numeric value or an empty string.  The returned value is always a number.</span></span>|
|<span data-ttu-id="a6342-126">maximum</span><span class="sxs-lookup"><span data-stu-id="a6342-126">maximum</span></span>|<span data-ttu-id="a6342-127">object</span><span class="sxs-lookup"><span data-stu-id="a6342-127">object</span></span>|<span data-ttu-id="a6342-p103">Representa el valor máximo del eje de valores.  Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos).  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="a6342-p103">Represents the maximum value on the value axis.  Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="a6342-131">minimum</span><span class="sxs-lookup"><span data-stu-id="a6342-131">minimum</span></span>|<span data-ttu-id="a6342-132">object</span><span class="sxs-lookup"><span data-stu-id="a6342-132">object</span></span>|<span data-ttu-id="a6342-p104">Representa el valor mínimo del eje de valores. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="a6342-p104">Represents the minimum value on the value axis. Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="a6342-136">minorUnit</span><span class="sxs-lookup"><span data-stu-id="a6342-136">minorUnit</span></span>|<span data-ttu-id="a6342-137">object</span><span class="sxs-lookup"><span data-stu-id="a6342-137">object</span></span>|<span data-ttu-id="a6342-p105">Representa el rango entre dos marcas de graduación secundarias. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="a6342-p105">Represents the interval between two minor tick marks. "Can be set to a numeric value or an empty string (for automatic axis values). The returned value is always a number.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a6342-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a6342-141">Relationships</span></span>
| <span data-ttu-id="a6342-142">Relación</span><span class="sxs-lookup"><span data-stu-id="a6342-142">Relationship</span></span> | <span data-ttu-id="a6342-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6342-143">Type</span></span>   |<span data-ttu-id="a6342-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6342-144">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a6342-145">format</span><span class="sxs-lookup"><span data-stu-id="a6342-145">format</span></span>|[<span data-ttu-id="a6342-146">ChartAxisFormat</span><span class="sxs-lookup"><span data-stu-id="a6342-146">ChartAxisFormat</span></span>](chartaxisformat.md)|<span data-ttu-id="a6342-p106">Representa el formato de un objeto de gráfico, que incluye el formato de línea y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a6342-p106">Represents the formatting of a chart object, which includes line and font formatting. Read-only.</span></span>|
|<span data-ttu-id="a6342-149">majorGridlines</span><span class="sxs-lookup"><span data-stu-id="a6342-149">majorGridlines</span></span>|[<span data-ttu-id="a6342-150">ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="a6342-150">ChartGridlines</span></span>](chartgridlines.md)|<span data-ttu-id="a6342-p107">Devuelve un objeto de línea de cuadrícula que representa las líneas de cuadrícula principales del eje especificado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a6342-p107">Returns a gridlines object that represents the major gridlines for the specified axis. Read-only.</span></span>|
|<span data-ttu-id="a6342-153">minorGridlines</span><span class="sxs-lookup"><span data-stu-id="a6342-153">minorGridlines</span></span>|[<span data-ttu-id="a6342-154">ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="a6342-154">ChartGridlines</span></span>](chartgridlines.md)|<span data-ttu-id="a6342-p108">Devuelve un objeto de línea de cuadrícula que representa las líneas de cuadrícula secundarias del eje especificado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a6342-p108">Returns a Gridlines object that represents the minor gridlines for the specified axis. Read-only.</span></span>|
|<span data-ttu-id="a6342-157">title</span><span class="sxs-lookup"><span data-stu-id="a6342-157">title</span></span>|[<span data-ttu-id="a6342-158">ChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="a6342-158">ChartAxisTitle</span></span>](chartaxistitle.md)|<span data-ttu-id="a6342-p109">Representa el título del eje. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a6342-p109">Represents the axis title. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a6342-161">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a6342-161">JSON representation</span></span>

<span data-ttu-id="a6342-162">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a6342-162">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartaxis"
}-->

```json
{
  "majorUnit": "string",
  "maximum": "string",
  "minimum": "string",
  "minorUnit": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxis resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
