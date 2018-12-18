---
title: Tipo de recurso ChartAxis
description: Representa un solo eje de un gráfico.
author: lumine2008
ms.openlocfilehash: 39c71e9fa832ffb967a1ef147ccd7e07d6b9aaec
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344369"
---
# <a name="chartaxis-resource-type"></a><span data-ttu-id="19e36-103">Tipo de recurso ChartAxis</span><span class="sxs-lookup"><span data-stu-id="19e36-103">ChartAxis resource type</span></span>

<span data-ttu-id="19e36-104">Representa un solo eje de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="19e36-104">Represents a single axis in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="19e36-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="19e36-105">Methods</span></span>

| <span data-ttu-id="19e36-106">Método</span><span class="sxs-lookup"><span data-stu-id="19e36-106">Method</span></span>           | <span data-ttu-id="19e36-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19e36-107">Return Type</span></span>    |<span data-ttu-id="19e36-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="19e36-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="19e36-109">Get ChartAxis</span><span class="sxs-lookup"><span data-stu-id="19e36-109">Get ChartAxis</span></span>](../api/chartaxis-get.md) | [<span data-ttu-id="19e36-110">WorkbookChartAxis</span><span class="sxs-lookup"><span data-stu-id="19e36-110">WorkbookChartAxis</span></span>](chartaxis.md) |<span data-ttu-id="19e36-111">Lee las propiedades y relaciones del objeto chartAxis.</span><span class="sxs-lookup"><span data-stu-id="19e36-111">Read properties and relationships of chartAxis object.</span></span>|
|[<span data-ttu-id="19e36-112">Actualizar</span><span class="sxs-lookup"><span data-stu-id="19e36-112">Update</span></span>](../api/chartaxis-update.md) | [<span data-ttu-id="19e36-113">WorkbookChartAxis</span><span class="sxs-lookup"><span data-stu-id="19e36-113">WorkbookChartAxis</span></span>](chartaxis.md)   |<span data-ttu-id="19e36-114">Actualiza el objeto ChartAxis.</span><span class="sxs-lookup"><span data-stu-id="19e36-114">Update ChartAxis object.</span></span> |

## <a name="properties"></a><span data-ttu-id="19e36-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19e36-115">Properties</span></span>
| <span data-ttu-id="19e36-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="19e36-116">Property</span></span>     | <span data-ttu-id="19e36-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="19e36-117">Type</span></span>   |<span data-ttu-id="19e36-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="19e36-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="19e36-119">id</span><span class="sxs-lookup"><span data-stu-id="19e36-119">id</span></span>       |<span data-ttu-id="19e36-120">string</span><span class="sxs-lookup"><span data-stu-id="19e36-120">string</span></span>   | <span data-ttu-id="19e36-121">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="19e36-121">Unique identifier.</span></span> <span data-ttu-id="19e36-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19e36-122">Read-only.</span></span>|
|<span data-ttu-id="19e36-123">majorUnit</span><span class="sxs-lookup"><span data-stu-id="19e36-123">majorUnit</span></span>|<span data-ttu-id="19e36-124">Json</span><span class="sxs-lookup"><span data-stu-id="19e36-124">Json</span></span>|<span data-ttu-id="19e36-p102">Representa el intervalo entre dos marcas de graduación principales. Puede establecerse en un valor numérico o en una cadena vacía.  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="19e36-p102">Represents the interval between two major tick marks. Can be set to a numeric value or an empty string.  The returned value is always a number.</span></span>|
|<span data-ttu-id="19e36-128">maximum</span><span class="sxs-lookup"><span data-stu-id="19e36-128">maximum</span></span>|<span data-ttu-id="19e36-129">Json</span><span class="sxs-lookup"><span data-stu-id="19e36-129">Json</span></span>|<span data-ttu-id="19e36-p103">Representa el valor máximo del eje de valores.  Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos).  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="19e36-p103">Represents the maximum value on the value axis.  Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="19e36-133">minimum</span><span class="sxs-lookup"><span data-stu-id="19e36-133">minimum</span></span>|<span data-ttu-id="19e36-134">Json</span><span class="sxs-lookup"><span data-stu-id="19e36-134">Json</span></span>|<span data-ttu-id="19e36-p104">Representa el valor mínimo del eje de valores. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="19e36-p104">Represents the minimum value on the value axis. Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="19e36-138">minorUnit</span><span class="sxs-lookup"><span data-stu-id="19e36-138">minorUnit</span></span>|<span data-ttu-id="19e36-139">Json</span><span class="sxs-lookup"><span data-stu-id="19e36-139">Json</span></span>|<span data-ttu-id="19e36-p105">Representa el rango entre dos marcas de graduación secundarias. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="19e36-p105">Represents the interval between two minor tick marks. "Can be set to a numeric value or an empty string (for automatic axis values). The returned value is always a number.</span></span>|

## <a name="relationships"></a><span data-ttu-id="19e36-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="19e36-143">Relationships</span></span>
| <span data-ttu-id="19e36-144">Relación</span><span class="sxs-lookup"><span data-stu-id="19e36-144">Relationship</span></span> | <span data-ttu-id="19e36-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="19e36-145">Type</span></span>   |<span data-ttu-id="19e36-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="19e36-146">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="19e36-147">format</span><span class="sxs-lookup"><span data-stu-id="19e36-147">format</span></span>|[<span data-ttu-id="19e36-148">WorkbookChartAxisFormat</span><span class="sxs-lookup"><span data-stu-id="19e36-148">WorkbookChartAxisFormat</span></span>](chartaxisformat.md)|<span data-ttu-id="19e36-p106">Representa el formato de un objeto de gráfico, que incluye el formato de línea y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19e36-p106">Represents the formatting of a chart object, which includes line and font formatting. Read-only.</span></span>|
|<span data-ttu-id="19e36-151">majorGridlines</span><span class="sxs-lookup"><span data-stu-id="19e36-151">majorGridlines</span></span>|[<span data-ttu-id="19e36-152">WorkbookChartGridlines</span><span class="sxs-lookup"><span data-stu-id="19e36-152">WorkbookChartGridlines</span></span>](chartgridlines.md)|<span data-ttu-id="19e36-p107">Devuelve un objeto de línea de cuadrícula que representa las líneas de cuadrícula principales del eje especificado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19e36-p107">Returns a gridlines object that represents the major gridlines for the specified axis. Read-only.</span></span>|
|<span data-ttu-id="19e36-155">minorGridlines</span><span class="sxs-lookup"><span data-stu-id="19e36-155">minorGridlines</span></span>|[<span data-ttu-id="19e36-156">WorkbookChartGridlines</span><span class="sxs-lookup"><span data-stu-id="19e36-156">WorkbookChartGridlines</span></span>](chartgridlines.md)|<span data-ttu-id="19e36-p108">Devuelve un objeto de línea de cuadrícula que representa las líneas de cuadrícula secundarias del eje especificado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19e36-p108">Returns a Gridlines object that represents the minor gridlines for the specified axis. Read-only.</span></span>|
|<span data-ttu-id="19e36-159">title</span><span class="sxs-lookup"><span data-stu-id="19e36-159">title</span></span>|[<span data-ttu-id="19e36-160">WorkbookChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="19e36-160">WorkbookChartAxisTitle</span></span>](chartaxistitle.md)|<span data-ttu-id="19e36-p109">Representa el título del eje. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19e36-p109">Represents the axis title. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="19e36-163">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="19e36-163">JSON representation</span></span>

<span data-ttu-id="19e36-164">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="19e36-164">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartAxis"
}-->

```json
{
  "id": "string",
  "majorUnit": "string",
  "maximum": "string",
  "minimum": "string",
  "minorUnit": "string",
   "format": {"@odata.type": "microsoft.graph.workbookChartAxisFormat"},
  "majorGridlines": {"@odata.type": "microsoft.graph.workbookChartGridlines"},
  "minorGridlines": {"@odata.type": "microsoft.graph.workbookChartGridlines"},
  "title": {"@odata.type": "microsoft.graph.workbookChartAxisTitle"}
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