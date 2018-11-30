---
title: Tipo de recurso RangeFormat
description: Objeto de formato que encapsula la fuente, el relleno, los bordes, la alineación y otras propiedades del rango.
ms.openlocfilehash: 8451b1f24f7c0df3842ed390a2a182746a0a7b20
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029662"
---
# <a name="rangeformat-resource-type"></a><span data-ttu-id="e0408-103">Tipo de recurso RangeFormat</span><span class="sxs-lookup"><span data-stu-id="e0408-103">RangeFormat resource type</span></span>

<span data-ttu-id="e0408-104">Objeto de formato que encapsula la fuente, el relleno, los bordes, la alineación y otras propiedades del rango.</span><span class="sxs-lookup"><span data-stu-id="e0408-104">A format object encapsulating the range's font, fill, borders, alignment, and other properties.</span></span>


## <a name="methods"></a><span data-ttu-id="e0408-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="e0408-105">Methods</span></span>

| <span data-ttu-id="e0408-106">Método</span><span class="sxs-lookup"><span data-stu-id="e0408-106">Method</span></span>           | <span data-ttu-id="e0408-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0408-107">Return Type</span></span>    |<span data-ttu-id="e0408-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0408-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e0408-109">Get RangeFormat</span><span class="sxs-lookup"><span data-stu-id="e0408-109">Get RangeFormat</span></span>](../api/rangeformat-get.md) | [<span data-ttu-id="e0408-110">WorkbookRangeFormat</span><span class="sxs-lookup"><span data-stu-id="e0408-110">WorkbookRangeFormat</span></span>](rangeformat.md) |<span data-ttu-id="e0408-111">Lee las propiedades y relaciones del objeto rangeFormat.</span><span class="sxs-lookup"><span data-stu-id="e0408-111">Read properties and relationships of rangeFormat object.</span></span>|
|[<span data-ttu-id="e0408-112">Create RangeBorder</span><span class="sxs-lookup"><span data-stu-id="e0408-112">Create RangeBorder</span></span>](../api/rangeformat-post-borders.md) |[<span data-ttu-id="e0408-113">WorkbookRangeBorder</span><span class="sxs-lookup"><span data-stu-id="e0408-113">WorkbookRangeBorder</span></span>](rangeborder.md)| <span data-ttu-id="e0408-114">Crea un RangeBorder publicándolo en la colección borders.</span><span class="sxs-lookup"><span data-stu-id="e0408-114">Create a new RangeBorder by posting to the borders collection.</span></span>|
|[<span data-ttu-id="e0408-115">List borders</span><span class="sxs-lookup"><span data-stu-id="e0408-115">List borders</span></span>](../api/rangeformat-list-borders.md) |<span data-ttu-id="e0408-116">Colección de [WorkbookRangeBorder](rangeborder.md)</span><span class="sxs-lookup"><span data-stu-id="e0408-116">[WorkbookRangeBorder](rangeborder.md) collection</span></span>| <span data-ttu-id="e0408-117">Obtiene una colección de objetos RangeBorder.</span><span class="sxs-lookup"><span data-stu-id="e0408-117">Get a RangeBorder object collection.</span></span>|
|[<span data-ttu-id="e0408-118">Update</span><span class="sxs-lookup"><span data-stu-id="e0408-118">Update</span></span>](../api/rangeformat-update.md) | [<span data-ttu-id="e0408-119">WorkbookRangeFormat</span><span class="sxs-lookup"><span data-stu-id="e0408-119">WorkbookRangeFormat</span></span>](rangeformat.md) |<span data-ttu-id="e0408-120">Actualiza el objeto RangeFormat.</span><span class="sxs-lookup"><span data-stu-id="e0408-120">Update RangeFormat object.</span></span> |
|[<span data-ttu-id="e0408-121">Autofitcolumns</span><span class="sxs-lookup"><span data-stu-id="e0408-121">Autofitcolumns</span></span>](../api/rangeformat-autofitcolumns.md)|<span data-ttu-id="e0408-122">None</span><span class="sxs-lookup"><span data-stu-id="e0408-122">None</span></span>|<span data-ttu-id="e0408-123">Cambia el ancho de las columnas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).</span><span class="sxs-lookup"><span data-stu-id="e0408-123">Changes the width of the columns of the current range to achieve the best fit, based on the current data in the columns.</span></span>|
|[<span data-ttu-id="e0408-124">Autofitrows</span><span class="sxs-lookup"><span data-stu-id="e0408-124">Autofitrows</span></span>](../api/rangeformat-autofitrows.md)|<span data-ttu-id="e0408-125">None</span><span class="sxs-lookup"><span data-stu-id="e0408-125">None</span></span>|<span data-ttu-id="e0408-126">Cambia el alto de las filas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).</span><span class="sxs-lookup"><span data-stu-id="e0408-126">Changes the height of the rows of the current range to achieve the best fit, based on the current data in the columns.</span></span>|

## <a name="properties"></a><span data-ttu-id="e0408-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e0408-127">Properties</span></span>
| <span data-ttu-id="e0408-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e0408-128">Property</span></span>     | <span data-ttu-id="e0408-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0408-129">Type</span></span>   |<span data-ttu-id="e0408-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0408-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e0408-131">columnWidth</span><span class="sxs-lookup"><span data-stu-id="e0408-131">columnWidth</span></span>|<span data-ttu-id="e0408-132">double</span><span class="sxs-lookup"><span data-stu-id="e0408-132">double</span></span>|<span data-ttu-id="e0408-p101">Obtiene o establece el ancho de todas las columnas del rango. Si los anchos de columna no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="e0408-p101">Gets or sets the width of all colums within the range. If the column widths are not uniform, null will be returned.</span></span>|
|<span data-ttu-id="e0408-135">horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="e0408-135">horizontalAlignment</span></span>|<span data-ttu-id="e0408-136">string</span><span class="sxs-lookup"><span data-stu-id="e0408-136">string</span></span>|<span data-ttu-id="e0408-137">Representa la alineación horizontal del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="e0408-137">Represents the horizontal alignment for the specified object.</span></span> <span data-ttu-id="e0408-138">Los valores posibles son: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="e0408-138">The possible values are: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span></span>|
|<span data-ttu-id="e0408-139">rowHeight</span><span class="sxs-lookup"><span data-stu-id="e0408-139">rowHeight</span></span>|<span data-ttu-id="e0408-140">double</span><span class="sxs-lookup"><span data-stu-id="e0408-140">double</span></span>|<span data-ttu-id="e0408-p103">Obtiene o establece el alto de todas las filas del rango. Si los altos de fila no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="e0408-p103">Gets or sets the height of all rows in the range. If the row heights are not uniform null will be returned.</span></span>|
|<span data-ttu-id="e0408-143">verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="e0408-143">verticalAlignment</span></span>|<span data-ttu-id="e0408-144">string</span><span class="sxs-lookup"><span data-stu-id="e0408-144">string</span></span>|<span data-ttu-id="e0408-145">Representa la alineación vertical del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="e0408-145">Represents the vertical alignment for the specified object.</span></span> <span data-ttu-id="e0408-146">Los valores posibles son: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="e0408-146">The possible values are: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span></span>|
|<span data-ttu-id="e0408-147">wrapText</span><span class="sxs-lookup"><span data-stu-id="e0408-147">wrapText</span></span>|<span data-ttu-id="e0408-148">boolean</span><span class="sxs-lookup"><span data-stu-id="e0408-148">boolean</span></span>|<span data-ttu-id="e0408-p105">Indica si Excel ajusta el texto del objeto. Un valor null indica que el intervalo no tiene una configuración de ajuste uniforme.</span><span class="sxs-lookup"><span data-stu-id="e0408-p105">Indicates if Excel wraps the text in the object. A null value indicates that the entire range doesn't have uniform wrap setting</span></span>|

## <a name="relationships"></a><span data-ttu-id="e0408-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e0408-151">Relationships</span></span>
| <span data-ttu-id="e0408-152">Relación</span><span class="sxs-lookup"><span data-stu-id="e0408-152">Relationship</span></span> | <span data-ttu-id="e0408-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0408-153">Type</span></span>   |<span data-ttu-id="e0408-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0408-154">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e0408-155">borders</span><span class="sxs-lookup"><span data-stu-id="e0408-155">borders</span></span>|<span data-ttu-id="e0408-156">Colección de [WorkbookRangeBorder](rangeborder.md)</span><span class="sxs-lookup"><span data-stu-id="e0408-156">[WorkbookRangeBorder](rangeborder.md) collection</span></span>|<span data-ttu-id="e0408-157">Colección de objetos border que se aplican al rango global seleccionado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e0408-157">Collection of border objects that apply to the overall range selected Read-only.</span></span>|
|<span data-ttu-id="e0408-158">fill</span><span class="sxs-lookup"><span data-stu-id="e0408-158">fill</span></span>|[<span data-ttu-id="e0408-159">WorkbookRangeFill</span><span class="sxs-lookup"><span data-stu-id="e0408-159">WorkbookRangeFill</span></span>](rangefill.md)|<span data-ttu-id="e0408-p106">Devuelve el objeto de relleno definido en el rango global. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e0408-p106">Returns the fill object defined on the overall range. Read-only.</span></span>|
|<span data-ttu-id="e0408-162">font</span><span class="sxs-lookup"><span data-stu-id="e0408-162">font</span></span>|[<span data-ttu-id="e0408-163">WorkbookRangeFont</span><span class="sxs-lookup"><span data-stu-id="e0408-163">WorkbookRangeFont</span></span>](rangefont.md)|<span data-ttu-id="e0408-164">Devuelve el objeto de fuente definido en el intervalo global seleccionado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e0408-164">Returns the font object defined on the overall range selected Read-only.</span></span>|
|<span data-ttu-id="e0408-165">protection</span><span class="sxs-lookup"><span data-stu-id="e0408-165">protection</span></span>|[<span data-ttu-id="e0408-166">WorkbookFormatProtection</span><span class="sxs-lookup"><span data-stu-id="e0408-166">WorkbookFormatProtection</span></span>](formatprotection.md)|<span data-ttu-id="e0408-p107">Devuelve el objeto de protección de formato de un rango. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e0408-p107">Returns the format protection object for a range. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e0408-169">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e0408-169">JSON representation</span></span>

<span data-ttu-id="e0408-170">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e0408-170">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookRangeFormat"
}-->

```json
{
  "columnWidth": 1024,
  "horizontalAlignment": "string",
  "rowHeight": 1024,
  "verticalAlignment": "string",
  "wrapText": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->