---
title: Tipo de recurso TableColumn
description: Representa una columna en una tabla.
ms.openlocfilehash: 0195bde59ee2116b064b47b9659f682877efc16b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086687"
---
# <a name="tablecolumn-resource-type"></a><span data-ttu-id="c5bb7-103">Tipo de recurso TableColumn</span><span class="sxs-lookup"><span data-stu-id="c5bb7-103">TableColumn resource type</span></span>

> <span data-ttu-id="c5bb7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c5bb7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c5bb7-106">Representa una columna en una tabla.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-106">Represents a column in a table.</span></span>


## <a name="methods"></a><span data-ttu-id="c5bb7-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5bb7-107">Methods</span></span>

| <span data-ttu-id="c5bb7-108">Método</span><span class="sxs-lookup"><span data-stu-id="c5bb7-108">Method</span></span>           | <span data-ttu-id="c5bb7-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5bb7-109">Return Type</span></span>    |<span data-ttu-id="c5bb7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5bb7-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c5bb7-111">Get TableColumn</span><span class="sxs-lookup"><span data-stu-id="c5bb7-111">Get TableColumn</span></span>](../api/tablecolumn-get.md) | [<span data-ttu-id="c5bb7-112">TableColumn</span><span class="sxs-lookup"><span data-stu-id="c5bb7-112">TableColumn</span></span>](tablecolumn.md) |<span data-ttu-id="c5bb7-113">Lee las propiedades y relaciones del objeto tableColumn.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-113">Read properties and relationships of tableColumn object.</span></span>|
|[<span data-ttu-id="c5bb7-114">Update</span><span class="sxs-lookup"><span data-stu-id="c5bb7-114">Update</span></span>](../api/tablecolumn-update.md) | [<span data-ttu-id="c5bb7-115">TableColumn</span><span class="sxs-lookup"><span data-stu-id="c5bb7-115">TableColumn</span></span>](tablecolumn.md) |<span data-ttu-id="c5bb7-116">Actualiza el objeto TableColumn.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-116">Update TableColumn object.</span></span> |
|[<span data-ttu-id="c5bb7-117">Databodyrange</span><span class="sxs-lookup"><span data-stu-id="c5bb7-117">Databodyrange</span></span>](../api/tablecolumn-databodyrange.md)|[<span data-ttu-id="c5bb7-118">Range</span><span class="sxs-lookup"><span data-stu-id="c5bb7-118">Range</span></span>](range.md)|<span data-ttu-id="c5bb7-119">Obtiene el objeto de rango asociado al cuerpo de datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-119">Gets the range object associated with the data body of the column.</span></span>|
|[<span data-ttu-id="c5bb7-120">Headerrowrange</span><span class="sxs-lookup"><span data-stu-id="c5bb7-120">Headerrowrange</span></span>](../api/tablecolumn-headerrowrange.md)|[<span data-ttu-id="c5bb7-121">Range</span><span class="sxs-lookup"><span data-stu-id="c5bb7-121">Range</span></span>](range.md)|<span data-ttu-id="c5bb7-122">Obtiene el objeto de rango asociado a la fila de encabezado de la columna.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-122">Gets the range object associated with the header row of the column.</span></span>|
|[<span data-ttu-id="c5bb7-123">Range</span><span class="sxs-lookup"><span data-stu-id="c5bb7-123">Range</span></span>](../api/tablecolumn-range.md)|[<span data-ttu-id="c5bb7-124">Range</span><span class="sxs-lookup"><span data-stu-id="c5bb7-124">Range</span></span>](range.md)|<span data-ttu-id="c5bb7-125">Obtiene el objeto de rango asociado a toda la columna.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-125">Gets the range object associated with the entire column.</span></span>|
|[<span data-ttu-id="c5bb7-126">Totalrowrange</span><span class="sxs-lookup"><span data-stu-id="c5bb7-126">Totalrowrange</span></span>](../api/tablecolumn-totalrowrange.md)|[<span data-ttu-id="c5bb7-127">Range</span><span class="sxs-lookup"><span data-stu-id="c5bb7-127">Range</span></span>](range.md)|<span data-ttu-id="c5bb7-128">Obtiene el objeto de rango asociado a la fila de totales de la columna.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-128">Gets the range object associated with the totals row of the column.</span></span>|
|[<span data-ttu-id="c5bb7-129">Delete</span><span class="sxs-lookup"><span data-stu-id="c5bb7-129">Delete</span></span>](../api/tablecolumn-delete.md)|<span data-ttu-id="c5bb7-130">None</span><span class="sxs-lookup"><span data-stu-id="c5bb7-130">None</span></span>|<span data-ttu-id="c5bb7-131">Elimina la columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-131">Deletes the column from the table.</span></span>|
|[<span data-ttu-id="c5bb7-132">List</span><span class="sxs-lookup"><span data-stu-id="c5bb7-132">List</span></span>](../api/tablecolumn-list.md) | <span data-ttu-id="c5bb7-133">Colección [TableColumn](tablecolumn.md)</span><span class="sxs-lookup"><span data-stu-id="c5bb7-133">[TableColumn](tablecolumn.md) collection</span></span> |<span data-ttu-id="c5bb7-134">Obtiene la colección de objetos tableColumn.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-134">Get tableColumn object collection.</span></span> |
|[<span data-ttu-id="c5bb7-135">Itemat</span><span class="sxs-lookup"><span data-stu-id="c5bb7-135">Itemat</span></span>](../api/tablecolumncollection-itemat.md)|[<span data-ttu-id="c5bb7-136">TableColumn</span><span class="sxs-lookup"><span data-stu-id="c5bb7-136">TableColumn</span></span>](tablecolumn.md)|<span data-ttu-id="c5bb7-137">Obtiene una columna en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-137">Gets a column based on its position in the collection.</span></span>|
|[<span data-ttu-id="c5bb7-138">Add</span><span class="sxs-lookup"><span data-stu-id="c5bb7-138">Add</span></span>](../api/tablecolumncollection-add.md)|[<span data-ttu-id="c5bb7-139">TableColumn</span><span class="sxs-lookup"><span data-stu-id="c5bb7-139">TableColumn</span></span>](tablecolumn.md)|<span data-ttu-id="c5bb7-140">Agrega una nueva columna a la tabla.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-140">Adds a new column to the table.</span></span>|

## <a name="properties"></a><span data-ttu-id="c5bb7-141">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5bb7-141">Properties</span></span>
| <span data-ttu-id="c5bb7-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c5bb7-142">Property</span></span>     | <span data-ttu-id="c5bb7-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5bb7-143">Type</span></span>   |<span data-ttu-id="c5bb7-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5bb7-144">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c5bb7-145">id</span><span class="sxs-lookup"><span data-stu-id="c5bb7-145">id</span></span>|<span data-ttu-id="c5bb7-146">int</span><span class="sxs-lookup"><span data-stu-id="c5bb7-146">int</span></span>|<span data-ttu-id="c5bb7-p102">Devuelve una clave única que identifica la columna de la tabla. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-p102">Returns a unique key that identifies the column within the table. Read-only.</span></span>|
|<span data-ttu-id="c5bb7-149">Index</span><span class="sxs-lookup"><span data-stu-id="c5bb7-149">index</span></span>|<span data-ttu-id="c5bb7-150">int</span><span class="sxs-lookup"><span data-stu-id="c5bb7-150">int</span></span>|<span data-ttu-id="c5bb7-p103">Devuelve el número de índice de la columna dentro de la colección de columnas de la tabla. Indizado con cero. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-p103">Returns the index number of the column within the columns collection of the table. Zero-indexed. Read-only.</span></span>|
|<span data-ttu-id="c5bb7-154">name</span><span class="sxs-lookup"><span data-stu-id="c5bb7-154">name</span></span>|<span data-ttu-id="c5bb7-155">string</span><span class="sxs-lookup"><span data-stu-id="c5bb7-155">string</span></span>|<span data-ttu-id="c5bb7-p104">Devuelve el nombre de la columna de la tabla. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-p104">Returns the name of the table column. Read-only.</span></span>|
|<span data-ttu-id="c5bb7-158">values</span><span class="sxs-lookup"><span data-stu-id="c5bb7-158">values</span></span>|<span data-ttu-id="c5bb7-159">json</span><span class="sxs-lookup"><span data-stu-id="c5bb7-159">json</span></span>|<span data-ttu-id="c5bb7-p105">Representa los valores sin formato del intervalo especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-p105">Represents the raw values of the specified range. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c5bb7-163">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c5bb7-163">Relationships</span></span>
| <span data-ttu-id="c5bb7-164">Relación</span><span class="sxs-lookup"><span data-stu-id="c5bb7-164">Relationship</span></span> | <span data-ttu-id="c5bb7-165">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5bb7-165">Type</span></span>   |<span data-ttu-id="c5bb7-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5bb7-166">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c5bb7-167">filter</span><span class="sxs-lookup"><span data-stu-id="c5bb7-167">filter</span></span>|[<span data-ttu-id="c5bb7-168">Filter</span><span class="sxs-lookup"><span data-stu-id="c5bb7-168">Filter</span></span>](filter.md)|<span data-ttu-id="c5bb7-p106">Recupera el filtro aplicado a la columna. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-p106">Retrieve the filter applied to the column. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c5bb7-171">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c5bb7-171">JSON representation</span></span>

<span data-ttu-id="c5bb7-172">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c5bb7-172">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.tableColumn"
}-->

```json
{
  "id": 1024,
  "index": 1024,
  "name": "string",
  "values": "json"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableColumn resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->