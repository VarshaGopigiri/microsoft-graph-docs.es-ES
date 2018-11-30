---
title: Tipo de recurso RangeFormat
description: Objeto de formato que encapsula la fuente, el relleno, los bordes, la alineación y otras propiedades del rango.
ms.openlocfilehash: dc1eb1fd06370dff554e1245245ec24cdf5a6658
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086465"
---
# <a name="rangeformat-resource-type"></a><span data-ttu-id="1ef48-103">Tipo de recurso RangeFormat</span><span class="sxs-lookup"><span data-stu-id="1ef48-103">RangeFormat resource type</span></span>

> <span data-ttu-id="1ef48-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1ef48-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1ef48-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1ef48-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1ef48-106">Objeto de formato que encapsula la fuente, el relleno, los bordes, la alineación y otras propiedades del rango.</span><span class="sxs-lookup"><span data-stu-id="1ef48-106">A format object encapsulating the range's font, fill, borders, alignment, and other properties.</span></span>


## <a name="methods"></a><span data-ttu-id="1ef48-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="1ef48-107">Methods</span></span>

| <span data-ttu-id="1ef48-108">Método</span><span class="sxs-lookup"><span data-stu-id="1ef48-108">Method</span></span>           | <span data-ttu-id="1ef48-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ef48-109">Return Type</span></span>    |<span data-ttu-id="1ef48-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ef48-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="1ef48-111">Get RangeFormat</span><span class="sxs-lookup"><span data-stu-id="1ef48-111">Get RangeFormat</span></span>](../api/rangeformat-get.md) | [<span data-ttu-id="1ef48-112">RangeFormat</span><span class="sxs-lookup"><span data-stu-id="1ef48-112">RangeFormat</span></span>](rangeformat.md) |<span data-ttu-id="1ef48-113">Lee las propiedades y relaciones del objeto rangeFormat.</span><span class="sxs-lookup"><span data-stu-id="1ef48-113">Read properties and relationships of rangeFormat object.</span></span>|
|[<span data-ttu-id="1ef48-114">Create RangeBorder</span><span class="sxs-lookup"><span data-stu-id="1ef48-114">Create RangeBorder</span></span>](../api/rangeformat-post-borders.md) |[<span data-ttu-id="1ef48-115">RangeBorder</span><span class="sxs-lookup"><span data-stu-id="1ef48-115">RangeBorder</span></span>](rangeborder.md)| <span data-ttu-id="1ef48-116">Crea un RangeBorder publicándolo en la colección borders.</span><span class="sxs-lookup"><span data-stu-id="1ef48-116">Create a new RangeBorder by posting to the borders collection.</span></span>|
|[<span data-ttu-id="1ef48-117">List borders</span><span class="sxs-lookup"><span data-stu-id="1ef48-117">List borders</span></span>](../api/rangeformat-list-borders.md) |<span data-ttu-id="1ef48-118">Colección [RangeBorder](rangeborder.md)</span><span class="sxs-lookup"><span data-stu-id="1ef48-118">[RangeBorder](rangeborder.md) collection</span></span>| <span data-ttu-id="1ef48-119">Obtiene una colección de objetos RangeBorder.</span><span class="sxs-lookup"><span data-stu-id="1ef48-119">Get a RangeBorder object collection.</span></span>|
|[<span data-ttu-id="1ef48-120">Update</span><span class="sxs-lookup"><span data-stu-id="1ef48-120">Update</span></span>](../api/rangeformat-update.md) | [<span data-ttu-id="1ef48-121">RangeFormat</span><span class="sxs-lookup"><span data-stu-id="1ef48-121">RangeFormat</span></span>](rangeformat.md) |<span data-ttu-id="1ef48-122">Actualiza el objeto RangeFormat.</span><span class="sxs-lookup"><span data-stu-id="1ef48-122">Update RangeFormat object.</span></span> |
|[<span data-ttu-id="1ef48-123">Autofitcolumns</span><span class="sxs-lookup"><span data-stu-id="1ef48-123">Autofitcolumns</span></span>](../api/rangeformat-autofitcolumns.md)|<span data-ttu-id="1ef48-124">None</span><span class="sxs-lookup"><span data-stu-id="1ef48-124">None</span></span>|<span data-ttu-id="1ef48-125">Cambia el ancho de las columnas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).</span><span class="sxs-lookup"><span data-stu-id="1ef48-125">Changes the width of the columns of the current range to achieve the best fit, based on the current data in the columns.</span></span>|
|[<span data-ttu-id="1ef48-126">Autofitrows</span><span class="sxs-lookup"><span data-stu-id="1ef48-126">Autofitrows</span></span>](../api/rangeformat-autofitrows.md)|<span data-ttu-id="1ef48-127">None</span><span class="sxs-lookup"><span data-stu-id="1ef48-127">None</span></span>|<span data-ttu-id="1ef48-128">Cambia el alto de las filas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).</span><span class="sxs-lookup"><span data-stu-id="1ef48-128">Changes the height of the rows of the current range to achieve the best fit, based on the current data in the columns.</span></span>|

## <a name="properties"></a><span data-ttu-id="1ef48-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1ef48-129">Properties</span></span>
| <span data-ttu-id="1ef48-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1ef48-130">Property</span></span>     | <span data-ttu-id="1ef48-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1ef48-131">Type</span></span>   |<span data-ttu-id="1ef48-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ef48-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1ef48-133">columnWidth</span><span class="sxs-lookup"><span data-stu-id="1ef48-133">columnWidth</span></span>|<span data-ttu-id="1ef48-134">double</span><span class="sxs-lookup"><span data-stu-id="1ef48-134">double</span></span>|<span data-ttu-id="1ef48-p102">Obtiene o establece el ancho de todas las columnas del rango. Si los anchos de columna no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="1ef48-p102">Gets or sets the width of all colums within the range. If the column widths are not uniform, null will be returned.</span></span>|
|<span data-ttu-id="1ef48-137">horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="1ef48-137">horizontalAlignment</span></span>|<span data-ttu-id="1ef48-138">string</span><span class="sxs-lookup"><span data-stu-id="1ef48-138">string</span></span>|<span data-ttu-id="1ef48-p103">Representa la alineación horizontal del objeto especificado. Valores posibles: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="1ef48-p103">Represents the horizontal alignment for the specified object. Possible values are: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span></span>|
|<span data-ttu-id="1ef48-141">rowHeight</span><span class="sxs-lookup"><span data-stu-id="1ef48-141">rowHeight</span></span>|<span data-ttu-id="1ef48-142">double</span><span class="sxs-lookup"><span data-stu-id="1ef48-142">double</span></span>|<span data-ttu-id="1ef48-p104">Obtiene o establece el alto de todas las filas del rango. Si los altos de fila no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="1ef48-p104">Gets or sets the height of all rows in the range. If the row heights are not uniform null will be returned.</span></span>|
|<span data-ttu-id="1ef48-145">verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="1ef48-145">verticalAlignment</span></span>|<span data-ttu-id="1ef48-146">string</span><span class="sxs-lookup"><span data-stu-id="1ef48-146">string</span></span>|<span data-ttu-id="1ef48-p105">Representa la alineación vertical del objeto especificado. Valores posibles: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="1ef48-p105">Represents the vertical alignment for the specified object. Possible values are: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span></span>|
|<span data-ttu-id="1ef48-149">wrapText</span><span class="sxs-lookup"><span data-stu-id="1ef48-149">wrapText</span></span>|<span data-ttu-id="1ef48-150">boolean</span><span class="sxs-lookup"><span data-stu-id="1ef48-150">boolean</span></span>|<span data-ttu-id="1ef48-p106">Indica si Excel ajusta el texto del objeto. Un valor null indica que el intervalo no tiene una configuración de ajuste uniforme.</span><span class="sxs-lookup"><span data-stu-id="1ef48-p106">Indicates if Excel wraps the text in the object. A null value indicates that the entire range doesn't have uniform wrap setting</span></span>|

## <a name="relationships"></a><span data-ttu-id="1ef48-153">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1ef48-153">Relationships</span></span>
| <span data-ttu-id="1ef48-154">Relación</span><span class="sxs-lookup"><span data-stu-id="1ef48-154">Relationship</span></span> | <span data-ttu-id="1ef48-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="1ef48-155">Type</span></span>   |<span data-ttu-id="1ef48-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ef48-156">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1ef48-157">borders</span><span class="sxs-lookup"><span data-stu-id="1ef48-157">borders</span></span>|<span data-ttu-id="1ef48-158">Colección [RangeBorder](rangeborder.md)</span><span class="sxs-lookup"><span data-stu-id="1ef48-158">[RangeBorder](rangeborder.md) collection</span></span>|<span data-ttu-id="1ef48-159">Colección de objetos border que se aplican al rango global seleccionado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1ef48-159">Collection of border objects that apply to the overall range selected Read-only.</span></span>|
|<span data-ttu-id="1ef48-160">fill</span><span class="sxs-lookup"><span data-stu-id="1ef48-160">fill</span></span>|[<span data-ttu-id="1ef48-161">RangeFill</span><span class="sxs-lookup"><span data-stu-id="1ef48-161">RangeFill</span></span>](rangefill.md)|<span data-ttu-id="1ef48-p107">Devuelve el objeto de relleno definido en el rango global. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1ef48-p107">Returns the fill object defined on the overall range. Read-only.</span></span>|
|<span data-ttu-id="1ef48-164">font</span><span class="sxs-lookup"><span data-stu-id="1ef48-164">font</span></span>|[<span data-ttu-id="1ef48-165">RangeFont</span><span class="sxs-lookup"><span data-stu-id="1ef48-165">RangeFont</span></span>](rangefont.md)|<span data-ttu-id="1ef48-166">Devuelve el objeto de fuente definido en el intervalo global seleccionado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1ef48-166">Returns the font object defined on the overall range selected Read-only.</span></span>|
|<span data-ttu-id="1ef48-167">protection</span><span class="sxs-lookup"><span data-stu-id="1ef48-167">protection</span></span>|[<span data-ttu-id="1ef48-168">FormatProtection</span><span class="sxs-lookup"><span data-stu-id="1ef48-168">FormatProtection</span></span>](formatprotection.md)|<span data-ttu-id="1ef48-p108">Devuelve el objeto de protección de formato de un rango. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1ef48-p108">Returns the format protection object for a range. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1ef48-171">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1ef48-171">JSON representation</span></span>

<span data-ttu-id="1ef48-172">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1ef48-172">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rangeFormat"
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