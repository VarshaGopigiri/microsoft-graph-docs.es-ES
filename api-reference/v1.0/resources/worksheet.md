---
title: Tipo de recurso Worksheet
description: Una hoja de cálculo de Excel es una cuadrícula de celdas. Puede contener datos, tablas, gráficos, etc.
localization_priority: Priority
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 60e31738329943d96e1a4f3ea8293851e759eaff
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983873"
---
# <a name="worksheet-resource-type"></a><span data-ttu-id="535fa-104">Tipo de recurso Worksheet</span><span class="sxs-lookup"><span data-stu-id="535fa-104">Worksheet resource type</span></span>

<span data-ttu-id="535fa-p102">Una hoja de cálculo de Excel es una cuadrícula de celdas. Puede contener datos, tablas, gráficos, etc.</span><span class="sxs-lookup"><span data-stu-id="535fa-p102">An Excel worksheet is a grid of cells. It can contain data, tables, charts, etc.</span></span>


## <a name="methods"></a><span data-ttu-id="535fa-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="535fa-107">Methods</span></span>

| <span data-ttu-id="535fa-108">Método</span><span class="sxs-lookup"><span data-stu-id="535fa-108">Method</span></span>           | <span data-ttu-id="535fa-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="535fa-109">Return Type</span></span>    |<span data-ttu-id="535fa-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="535fa-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="535fa-111">Get Worksheet</span><span class="sxs-lookup"><span data-stu-id="535fa-111">Get Worksheet</span></span>](../api/worksheet-get.md) | [<span data-ttu-id="535fa-112">WorkbookWorksheet</span><span class="sxs-lookup"><span data-stu-id="535fa-112">WorkbookWorksheet</span></span>](worksheet.md) |<span data-ttu-id="535fa-113">Lee las propiedades y relaciones del objeto worksheet.</span><span class="sxs-lookup"><span data-stu-id="535fa-113">Read properties and relationships of worksheet object.</span></span>|
|[<span data-ttu-id="535fa-114">Create Chart</span><span class="sxs-lookup"><span data-stu-id="535fa-114">Create Chart</span></span>](../api/worksheet-post-charts.md) |[<span data-ttu-id="535fa-115">WorkbookChart</span><span class="sxs-lookup"><span data-stu-id="535fa-115">WorkbookChart</span></span>](chart.md)| <span data-ttu-id="535fa-116">Cree un gráfico publicando en la colección de gráficos.</span><span class="sxs-lookup"><span data-stu-id="535fa-116">Create a new Chart by posting to the charts collection.</span></span>|
|[<span data-ttu-id="535fa-117">List names</span><span class="sxs-lookup"><span data-stu-id="535fa-117">List names</span></span>](../api/worksheet-list-names.md) |<span data-ttu-id="535fa-118">Colección de [WorkbookNamedItem](nameditem.md)</span><span class="sxs-lookup"><span data-stu-id="535fa-118">[WorkbookNamedItem](nameditem.md) collection</span></span>| <span data-ttu-id="535fa-119">Obtenga la colección del elemento con nombre asociada a la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="535fa-119">Get named item collection associated with the worksheet.</span></span>|
|[<span data-ttu-id="535fa-120">List charts</span><span class="sxs-lookup"><span data-stu-id="535fa-120">List charts</span></span>](../api/worksheet-list-charts.md) |<span data-ttu-id="535fa-121">Colección de [WorkbookChart](chart.md)</span><span class="sxs-lookup"><span data-stu-id="535fa-121">[WorkbookChart](chart.md) collection</span></span>| <span data-ttu-id="535fa-122">Obtiene la colección de objetos Chart.</span><span class="sxs-lookup"><span data-stu-id="535fa-122">Get a Chart object collection.</span></span>|
|[<span data-ttu-id="535fa-123">Create Table</span><span class="sxs-lookup"><span data-stu-id="535fa-123">Create Table</span></span>](../api/worksheet-post-tables.md) |[<span data-ttu-id="535fa-124">WorkbookTable</span><span class="sxs-lookup"><span data-stu-id="535fa-124">WorkbookTable</span></span>](table.md)| <span data-ttu-id="535fa-125">Crea un Table publicándolo en la colección tables.</span><span class="sxs-lookup"><span data-stu-id="535fa-125">Create a new Table by posting to the tables collection.</span></span>|
|[<span data-ttu-id="535fa-126">List tables</span><span class="sxs-lookup"><span data-stu-id="535fa-126">List tables</span></span>](../api/worksheet-list-tables.md) |<span data-ttu-id="535fa-127">Colección de [WorkbookTable](table.md)</span><span class="sxs-lookup"><span data-stu-id="535fa-127">[WorkbookTable](table.md) collection</span></span>| <span data-ttu-id="535fa-128">Obtiene una colección de objetos Table.</span><span class="sxs-lookup"><span data-stu-id="535fa-128">Get a Table object collection.</span></span>|
|[<span data-ttu-id="535fa-129">Update</span><span class="sxs-lookup"><span data-stu-id="535fa-129">Update</span></span>](../api/worksheet-update.md) | [<span data-ttu-id="535fa-130">WorkbookWorksheet</span><span class="sxs-lookup"><span data-stu-id="535fa-130">WorkbookWorksheet</span></span>](worksheet.md)   |<span data-ttu-id="535fa-131">Actualiza el objeto Worksheet.</span><span class="sxs-lookup"><span data-stu-id="535fa-131">Update Worksheet object.</span></span> |
|[<span data-ttu-id="535fa-132">Cell</span><span class="sxs-lookup"><span data-stu-id="535fa-132">Cell</span></span>](../api/worksheet-cell.md)|[<span data-ttu-id="535fa-133">Range</span><span class="sxs-lookup"><span data-stu-id="535fa-133">Range</span></span>](range.md)|<span data-ttu-id="535fa-p103">Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="535fa-p103">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid.</span></span>|
|[<span data-ttu-id="535fa-136">Range</span><span class="sxs-lookup"><span data-stu-id="535fa-136">Range</span></span>](../api/worksheet-range.md)|[<span data-ttu-id="535fa-137">Range</span><span class="sxs-lookup"><span data-stu-id="535fa-137">Range</span></span>](range.md)|<span data-ttu-id="535fa-138">Obtiene el objeto de rango especificado por la dirección o el nombre.</span><span class="sxs-lookup"><span data-stu-id="535fa-138">Gets the range object specified by the address or name.</span></span>|
|[<span data-ttu-id="535fa-139">Usedrange</span><span class="sxs-lookup"><span data-stu-id="535fa-139">Usedrange</span></span>](../api/worksheet-usedrange.md)|[<span data-ttu-id="535fa-140">Range</span><span class="sxs-lookup"><span data-stu-id="535fa-140">Range</span></span>](range.md)|<span data-ttu-id="535fa-p104">El rango usado es el rango más pequeño que abarque las celdas que tienen asignado un valor o un formato. Si la hoja de cálculo está en blanco, esta función devolverá la celda superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="535fa-p104">The used range is the smallest range that encompasses any cells that have a value or formatting assigned to them. If the worksheet is blank, this function will return the top left cell.</span></span>|
|[<span data-ttu-id="535fa-143">Delete</span><span class="sxs-lookup"><span data-stu-id="535fa-143">Delete</span></span>](../api/worksheet-delete.md)|<span data-ttu-id="535fa-144">None</span><span class="sxs-lookup"><span data-stu-id="535fa-144">None</span></span>|<span data-ttu-id="535fa-145">Elimina la hoja de cálculo del libro.</span><span class="sxs-lookup"><span data-stu-id="535fa-145">Deletes the worksheet from the workbook.</span></span>|
|[<span data-ttu-id="535fa-146">List</span><span class="sxs-lookup"><span data-stu-id="535fa-146">List</span></span>](../api/worksheet-list.md) | <span data-ttu-id="535fa-147">Colección de [WorkbookWorksheet](worksheet.md)</span><span class="sxs-lookup"><span data-stu-id="535fa-147">[WorkbookWorksheet](worksheet.md) collection</span></span> |<span data-ttu-id="535fa-148">Obtiene la colección de objetos worksheet.</span><span class="sxs-lookup"><span data-stu-id="535fa-148">Get worksheet object collection.</span></span> |
|[<span data-ttu-id="535fa-149">Add</span><span class="sxs-lookup"><span data-stu-id="535fa-149">Add</span></span>](../api/worksheetcollection-add.md)|[<span data-ttu-id="535fa-150">WorkbookWorksheet</span><span class="sxs-lookup"><span data-stu-id="535fa-150">WorkbookWorksheet</span></span>](worksheet.md)|<span data-ttu-id="535fa-p105">Agrega una nueva hoja de cálculo al libro. La hoja de cálculo se agregará al final de las hojas de cálculo existentes.</span><span class="sxs-lookup"><span data-stu-id="535fa-p105">Adds a new worksheet to the workbook. The worksheet will be added at the end of existing worksheets.</span></span> |
|[<span data-ttu-id="535fa-153">List pivotTables</span><span class="sxs-lookup"><span data-stu-id="535fa-153">List pivotTables</span></span>](../api/workbookworksheet-list-pivottables.md) |<span data-ttu-id="535fa-154">Colección [workbookPivotTable](workbookpivottable.md)</span><span class="sxs-lookup"><span data-stu-id="535fa-154">[workbookPivotTable](workbookpivottable.md) collection</span></span>| <span data-ttu-id="535fa-155">Obtiene una colección de objetos workbookPivotTable.</span><span class="sxs-lookup"><span data-stu-id="535fa-155">Get a workbookPivotTable object collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="535fa-156">Propiedades</span><span class="sxs-lookup"><span data-stu-id="535fa-156">Properties</span></span>
| <span data-ttu-id="535fa-157">Propiedad</span><span class="sxs-lookup"><span data-stu-id="535fa-157">Property</span></span>     | <span data-ttu-id="535fa-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="535fa-158">Type</span></span>   |<span data-ttu-id="535fa-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="535fa-159">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="535fa-160">id</span><span class="sxs-lookup"><span data-stu-id="535fa-160">id</span></span>|<span data-ttu-id="535fa-161">string</span><span class="sxs-lookup"><span data-stu-id="535fa-161">string</span></span>|<span data-ttu-id="535fa-p106">Devuelve un valor que identifica de forma única la hoja de cálculo de un libro determinado. El valor del identificador permanece igual, incluso cuando se cambia el nombre de la hoja de cálculo o cuando esta se mueve. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="535fa-p106">Returns a value that uniquely identifies the worksheet in a given workbook. The value of the identifier remains the same even when the worksheet is renamed or moved. Read-only.</span></span>|
|<span data-ttu-id="535fa-165">name</span><span class="sxs-lookup"><span data-stu-id="535fa-165">name</span></span>|<span data-ttu-id="535fa-166">string</span><span class="sxs-lookup"><span data-stu-id="535fa-166">string</span></span>|<span data-ttu-id="535fa-167">Nombre para mostrar de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="535fa-167">The display name of the worksheet.</span></span>|
|<span data-ttu-id="535fa-168">position</span><span class="sxs-lookup"><span data-stu-id="535fa-168">position</span></span>|<span data-ttu-id="535fa-169">entero</span><span class="sxs-lookup"><span data-stu-id="535fa-169">int</span></span>|<span data-ttu-id="535fa-170">Posición de base cero de la hoja de cálculo dentro del libro.</span><span class="sxs-lookup"><span data-stu-id="535fa-170">The zero-based position of the worksheet within the workbook.</span></span>|
|<span data-ttu-id="535fa-171">visibility</span><span class="sxs-lookup"><span data-stu-id="535fa-171">visibility</span></span>|<span data-ttu-id="535fa-172">string</span><span class="sxs-lookup"><span data-stu-id="535fa-172">string</span></span>|<span data-ttu-id="535fa-173">La visibilidad de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="535fa-173">The Visibility of the worksheet.</span></span> <span data-ttu-id="535fa-174">Los valores posibles son: `Visible`, `Hidden`, `VeryHidden`.</span><span class="sxs-lookup"><span data-stu-id="535fa-174">The possible values are: `Visible`, `Hidden`, `VeryHidden`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="535fa-175">Relaciones</span><span class="sxs-lookup"><span data-stu-id="535fa-175">Relationships</span></span>
| <span data-ttu-id="535fa-176">Relación</span><span class="sxs-lookup"><span data-stu-id="535fa-176">Relationship</span></span> | <span data-ttu-id="535fa-177">Tipo</span><span class="sxs-lookup"><span data-stu-id="535fa-177">Type</span></span>   |<span data-ttu-id="535fa-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="535fa-178">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="535fa-179">charts</span><span class="sxs-lookup"><span data-stu-id="535fa-179">charts</span></span>|<span data-ttu-id="535fa-180">Colección de [WorkbookChart](chart.md)</span><span class="sxs-lookup"><span data-stu-id="535fa-180">[WorkbookChart](chart.md) collection</span></span>|<span data-ttu-id="535fa-p108">Devuelve la colección de gráficos que forman parte de la hoja de cálculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="535fa-p108">Returns collection of charts that are part of the worksheet. Read-only.</span></span>|
|<span data-ttu-id="535fa-183">names</span><span class="sxs-lookup"><span data-stu-id="535fa-183">names</span></span>|<span data-ttu-id="535fa-184">Colección de [WorkbookNamedItem](nameditem.md)</span><span class="sxs-lookup"><span data-stu-id="535fa-184">[WorkbookNamedItem](nameditem.md) collection</span></span>|<span data-ttu-id="535fa-p109">Devuelve la colección de los nombres asociados a la hoja de cálculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="535fa-p109">Returns collection of names that are associated with the worksheet. Read-only.</span></span>|
|<span data-ttu-id="535fa-187">pivotTables</span><span class="sxs-lookup"><span data-stu-id="535fa-187">pivotTables</span></span>|<span data-ttu-id="535fa-188">Colección [workbookPivotTable](workbookpivottable.md)</span><span class="sxs-lookup"><span data-stu-id="535fa-188">[workbookPivotTable](workbookpivottable.md) collection</span></span>| <span data-ttu-id="535fa-189">Colección de tablas dinámicas que forman parte de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="535fa-189">Collection of PivotTables that are part of the worksheet.</span></span> |
|<span data-ttu-id="535fa-190">protection</span><span class="sxs-lookup"><span data-stu-id="535fa-190">protection</span></span>|[<span data-ttu-id="535fa-191">WorkbookWorksheetProtection</span><span class="sxs-lookup"><span data-stu-id="535fa-191">WorkbookWorksheetProtection</span></span>](worksheetprotection.md)|<span data-ttu-id="535fa-p110">Devuelve el objeto de protección de hoja de una hoja de cálculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="535fa-p110">Returns sheet protection object for a worksheet. Read-only.</span></span>|
|<span data-ttu-id="535fa-194">tables</span><span class="sxs-lookup"><span data-stu-id="535fa-194">tables</span></span>|<span data-ttu-id="535fa-195">Colección de [WorkbookTable](table.md)</span><span class="sxs-lookup"><span data-stu-id="535fa-195">[WorkbookTable](table.md) collection</span></span>|<span data-ttu-id="535fa-p111">Colección de tablas que forman parte de la hoja de cálculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="535fa-p111">Collection of tables that are part of the worksheet. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="535fa-198">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="535fa-198">JSON representation</span></span>

<span data-ttu-id="535fa-199">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="535fa-199">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookWorksheet"
}-->

```json
{
  "id": "string",
  "name": "string",
  "position": 1024,
  "visibility": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Worksheet resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
