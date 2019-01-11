---
title: Tipo de recurso Worksheet
description: Una hoja de cálculo de Excel es una cuadrícula de celdas. Puede contener datos, tablas, gráficos, etc.
localization_priority: Normal
ms.openlocfilehash: 690596bfe6df5f6bfd98f7f5bd37021e47132152
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27807801"
---
# <a name="worksheet-resource-type"></a><span data-ttu-id="7b053-104">Tipo de recurso Worksheet</span><span class="sxs-lookup"><span data-stu-id="7b053-104">Worksheet resource type</span></span>

> <span data-ttu-id="7b053-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7b053-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7b053-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7b053-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7b053-p103">Una hoja de cálculo de Excel es una cuadrícula de celdas. Puede contener datos, tablas, gráficos, etc.</span><span class="sxs-lookup"><span data-stu-id="7b053-p103">An Excel worksheet is a grid of cells. It can contain data, tables, charts, etc.</span></span>


## <a name="methods"></a><span data-ttu-id="7b053-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="7b053-109">Methods</span></span>

| <span data-ttu-id="7b053-110">Método</span><span class="sxs-lookup"><span data-stu-id="7b053-110">Method</span></span>           | <span data-ttu-id="7b053-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b053-111">Return Type</span></span>    |<span data-ttu-id="7b053-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b053-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="7b053-113">Get Worksheet</span><span class="sxs-lookup"><span data-stu-id="7b053-113">Get Worksheet</span></span>](../api/worksheet-get.md) | [<span data-ttu-id="7b053-114">Worksheet</span><span class="sxs-lookup"><span data-stu-id="7b053-114">Worksheet</span></span>](worksheet.md) |<span data-ttu-id="7b053-115">Lee las propiedades y relaciones del objeto worksheet.</span><span class="sxs-lookup"><span data-stu-id="7b053-115">Read properties and relationships of worksheet object.</span></span>|
|[<span data-ttu-id="7b053-116">Create Chart</span><span class="sxs-lookup"><span data-stu-id="7b053-116">Create Chart</span></span>](../api/worksheet-post-charts.md) |[<span data-ttu-id="7b053-117">Chart</span><span class="sxs-lookup"><span data-stu-id="7b053-117">Chart</span></span>](chart.md)| <span data-ttu-id="7b053-118">Cree un gráfico publicando en la colección de gráficos.</span><span class="sxs-lookup"><span data-stu-id="7b053-118">Create a new Chart by posting to the charts collection.</span></span>|
|[<span data-ttu-id="7b053-119">List names</span><span class="sxs-lookup"><span data-stu-id="7b053-119">List names</span></span>](../api/worksheet-list-names.md) |<span data-ttu-id="7b053-120">Colección [NamedItem](nameditem.md)</span><span class="sxs-lookup"><span data-stu-id="7b053-120">[NamedItem](nameditem.md) collection</span></span>| <span data-ttu-id="7b053-121">Obtenga la colección del elemento con nombre asociada a la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="7b053-121">Get named item collection associated with the worksheet.</span></span>|
|[<span data-ttu-id="7b053-122">List charts</span><span class="sxs-lookup"><span data-stu-id="7b053-122">List charts</span></span>](../api/worksheet-list-charts.md) |<span data-ttu-id="7b053-123">Colección [Chart](chart.md)</span><span class="sxs-lookup"><span data-stu-id="7b053-123">[Chart](chart.md) collection</span></span>| <span data-ttu-id="7b053-124">Obtiene la colección de objetos Chart.</span><span class="sxs-lookup"><span data-stu-id="7b053-124">Get a Chart object collection.</span></span>|
|[<span data-ttu-id="7b053-125">Create Table</span><span class="sxs-lookup"><span data-stu-id="7b053-125">Create Table</span></span>](../api/worksheet-post-tables.md) |[<span data-ttu-id="7b053-126">Tabla</span><span class="sxs-lookup"><span data-stu-id="7b053-126">Table</span></span>](table.md)| <span data-ttu-id="7b053-127">Crea un Table publicándolo en la colección tables.</span><span class="sxs-lookup"><span data-stu-id="7b053-127">Create a new Table by posting to the tables collection.</span></span>|
|[<span data-ttu-id="7b053-128">List tables</span><span class="sxs-lookup"><span data-stu-id="7b053-128">List tables</span></span>](../api/worksheet-list-tables.md) |<span data-ttu-id="7b053-129">Colección [Table](table.md)</span><span class="sxs-lookup"><span data-stu-id="7b053-129">[Table](table.md) collection</span></span>| <span data-ttu-id="7b053-130">Obtiene una colección de objetos Table.</span><span class="sxs-lookup"><span data-stu-id="7b053-130">Get a Table object collection.</span></span>|
|[<span data-ttu-id="7b053-131">Update</span><span class="sxs-lookup"><span data-stu-id="7b053-131">Update</span></span>](../api/worksheet-update.md) | [<span data-ttu-id="7b053-132">Worksheet</span><span class="sxs-lookup"><span data-stu-id="7b053-132">Worksheet</span></span>](worksheet.md)   |<span data-ttu-id="7b053-133">Actualiza el objeto Worksheet.</span><span class="sxs-lookup"><span data-stu-id="7b053-133">Update Worksheet object.</span></span> |
|[<span data-ttu-id="7b053-134">Cell</span><span class="sxs-lookup"><span data-stu-id="7b053-134">Cell</span></span>](../api/worksheet-cell.md)|[<span data-ttu-id="7b053-135">Range</span><span class="sxs-lookup"><span data-stu-id="7b053-135">Range</span></span>](range.md)|<span data-ttu-id="7b053-p104">Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="7b053-p104">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid.</span></span>|
|[<span data-ttu-id="7b053-138">Range</span><span class="sxs-lookup"><span data-stu-id="7b053-138">Range</span></span>](../api/worksheet-range.md)|[<span data-ttu-id="7b053-139">Range</span><span class="sxs-lookup"><span data-stu-id="7b053-139">Range</span></span>](range.md)|<span data-ttu-id="7b053-140">Obtiene el objeto de rango especificado por la dirección o el nombre.</span><span class="sxs-lookup"><span data-stu-id="7b053-140">Gets the range object specified by the address or name.</span></span>|
|[<span data-ttu-id="7b053-141">Usedrange</span><span class="sxs-lookup"><span data-stu-id="7b053-141">Usedrange</span></span>](../api/worksheet-usedrange.md)|[<span data-ttu-id="7b053-142">Range</span><span class="sxs-lookup"><span data-stu-id="7b053-142">Range</span></span>](range.md)|<span data-ttu-id="7b053-p105">El rango usado es el rango más pequeño que abarque las celdas que tienen asignado un valor o un formato. Si la hoja de cálculo está en blanco, esta función devolverá la celda superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="7b053-p105">The used range is the smallest range that encompasses any cells that have a value or formatting assigned to them. If the worksheet is blank, this function will return the top left cell.</span></span>|
|[<span data-ttu-id="7b053-145">Delete</span><span class="sxs-lookup"><span data-stu-id="7b053-145">Delete</span></span>](../api/worksheet-delete.md)|<span data-ttu-id="7b053-146">None</span><span class="sxs-lookup"><span data-stu-id="7b053-146">None</span></span>|<span data-ttu-id="7b053-147">Elimina la hoja de cálculo del libro.</span><span class="sxs-lookup"><span data-stu-id="7b053-147">Deletes the worksheet from the workbook.</span></span>|
|[<span data-ttu-id="7b053-148">List</span><span class="sxs-lookup"><span data-stu-id="7b053-148">List</span></span>](../api/worksheet-list.md) | <span data-ttu-id="7b053-149">Colección [Worksheet](worksheet.md)</span><span class="sxs-lookup"><span data-stu-id="7b053-149">[Worksheet](worksheet.md) collection</span></span> |<span data-ttu-id="7b053-150">Obtiene la colección de objetos worksheet.</span><span class="sxs-lookup"><span data-stu-id="7b053-150">Get worksheet object collection.</span></span> |
|[<span data-ttu-id="7b053-151">Add</span><span class="sxs-lookup"><span data-stu-id="7b053-151">Add</span></span>](../api/worksheetcollection-add.md)|[<span data-ttu-id="7b053-152">Worksheet</span><span class="sxs-lookup"><span data-stu-id="7b053-152">Worksheet</span></span>](worksheet.md)|<span data-ttu-id="7b053-p106">Agrega una nueva hoja de cálculo al libro. La hoja de cálculo se agregará al final de las hojas de cálculo existentes.</span><span class="sxs-lookup"><span data-stu-id="7b053-p106">Adds a new worksheet to the workbook. The worksheet will be added at the end of existing worksheets.</span></span> |
|[<span data-ttu-id="7b053-155">List pivotTables</span><span class="sxs-lookup"><span data-stu-id="7b053-155">List pivotTables</span></span>](../api/workbookworksheet-list-pivottables.md) |<span data-ttu-id="7b053-156">Colección [workbookPivotTable](workbookpivottable.md)</span><span class="sxs-lookup"><span data-stu-id="7b053-156">[workbookPivotTable](workbookpivottable.md) collection</span></span>| <span data-ttu-id="7b053-157">Obtiene una colección de objetos workbookPivotTable.</span><span class="sxs-lookup"><span data-stu-id="7b053-157">Get a workbookPivotTable object collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="7b053-158">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b053-158">Properties</span></span>
| <span data-ttu-id="7b053-159">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7b053-159">Property</span></span>     | <span data-ttu-id="7b053-160">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b053-160">Type</span></span>   |<span data-ttu-id="7b053-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b053-161">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7b053-162">id</span><span class="sxs-lookup"><span data-stu-id="7b053-162">id</span></span>|<span data-ttu-id="7b053-163">string</span><span class="sxs-lookup"><span data-stu-id="7b053-163">string</span></span>|<span data-ttu-id="7b053-p107">Devuelve un valor que identifica de forma única la hoja de cálculo de un libro determinado. El valor del identificador permanece igual, incluso cuando se cambia el nombre de la hoja de cálculo o cuando esta se mueve. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7b053-p107">Returns a value that uniquely identifies the worksheet in a given workbook. The value of the identifier remains the same even when the worksheet is renamed or moved. Read-only.</span></span>|
|<span data-ttu-id="7b053-167">name</span><span class="sxs-lookup"><span data-stu-id="7b053-167">name</span></span>|<span data-ttu-id="7b053-168">string</span><span class="sxs-lookup"><span data-stu-id="7b053-168">string</span></span>|<span data-ttu-id="7b053-169">Nombre para mostrar de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="7b053-169">The display name of the worksheet.</span></span>|
|<span data-ttu-id="7b053-170">position</span><span class="sxs-lookup"><span data-stu-id="7b053-170">position</span></span>|<span data-ttu-id="7b053-171">entero</span><span class="sxs-lookup"><span data-stu-id="7b053-171">int</span></span>|<span data-ttu-id="7b053-172">Posición de base cero de la hoja de cálculo dentro del libro.</span><span class="sxs-lookup"><span data-stu-id="7b053-172">The zero-based position of the worksheet within the workbook.</span></span>|
|<span data-ttu-id="7b053-173">visibility</span><span class="sxs-lookup"><span data-stu-id="7b053-173">visibility</span></span>|<span data-ttu-id="7b053-174">string</span><span class="sxs-lookup"><span data-stu-id="7b053-174">string</span></span>|<span data-ttu-id="7b053-p108">Visibilidad de la hoja de cálculo. Valores posibles: `Visible`, `Hidden`, `VeryHidden`.</span><span class="sxs-lookup"><span data-stu-id="7b053-p108">The Visibility of the worksheet. Possible values are: `Visible`, `Hidden`, `VeryHidden`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7b053-177">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7b053-177">Relationships</span></span>
| <span data-ttu-id="7b053-178">Relación</span><span class="sxs-lookup"><span data-stu-id="7b053-178">Relationship</span></span> | <span data-ttu-id="7b053-179">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b053-179">Type</span></span>   |<span data-ttu-id="7b053-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b053-180">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7b053-181">charts</span><span class="sxs-lookup"><span data-stu-id="7b053-181">charts</span></span>|<span data-ttu-id="7b053-182">Colección [Chart](chart.md)</span><span class="sxs-lookup"><span data-stu-id="7b053-182">[Chart](chart.md) collection</span></span>|<span data-ttu-id="7b053-p109">Devuelve la colección de gráficos que forman parte de la hoja de cálculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7b053-p109">Returns collection of charts that are part of the worksheet. Read-only.</span></span>|
|<span data-ttu-id="7b053-185">names</span><span class="sxs-lookup"><span data-stu-id="7b053-185">names</span></span>|<span data-ttu-id="7b053-186">Colección [NamedItem](nameditem.md)</span><span class="sxs-lookup"><span data-stu-id="7b053-186">[NamedItem](nameditem.md) collection</span></span>|<span data-ttu-id="7b053-p110">Devuelve la colección de los nombres asociados a la hoja de cálculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7b053-p110">Returns collection of names that are associated with the worksheet. Read-only.</span></span>|
|<span data-ttu-id="7b053-189">pivotTables</span><span class="sxs-lookup"><span data-stu-id="7b053-189">pivotTables</span></span>|<span data-ttu-id="7b053-190">Colección [workbookPivotTable](workbookpivottable.md)</span><span class="sxs-lookup"><span data-stu-id="7b053-190">[workbookPivotTable](workbookpivottable.md) collection</span></span>| <span data-ttu-id="7b053-191">Colección de tablas dinámicas que forman parte de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="7b053-191">Collection of PivotTables that are part of the worksheet.</span></span> |
|<span data-ttu-id="7b053-192">protection</span><span class="sxs-lookup"><span data-stu-id="7b053-192">protection</span></span>|[<span data-ttu-id="7b053-193">WorksheetProtection</span><span class="sxs-lookup"><span data-stu-id="7b053-193">WorksheetProtection</span></span>](worksheetprotection.md)|<span data-ttu-id="7b053-p111">Devuelve el objeto de protección de hoja de una hoja de cálculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7b053-p111">Returns sheet protection object for a worksheet. Read-only.</span></span>|
|<span data-ttu-id="7b053-196">tables</span><span class="sxs-lookup"><span data-stu-id="7b053-196">tables</span></span>|<span data-ttu-id="7b053-197">Colección [Table](table.md)</span><span class="sxs-lookup"><span data-stu-id="7b053-197">[Table](table.md) collection</span></span>|<span data-ttu-id="7b053-p112">Colección de tablas que forman parte de la hoja de cálculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7b053-p112">Collection of tables that are part of the worksheet. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7b053-200">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7b053-200">JSON representation</span></span>

<span data-ttu-id="7b053-201">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7b053-201">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.worksheet"
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
