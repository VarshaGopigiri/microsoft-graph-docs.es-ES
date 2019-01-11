---
title: Tipo de recurso TableRow
description: Representa una fila de una tabla.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: fe95b62236322451893e3859f9d6599cc637848c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27807178"
---
# <a name="tablerow-resource-type"></a><span data-ttu-id="af2e9-103">Tipo de recurso TableRow</span><span class="sxs-lookup"><span data-stu-id="af2e9-103">TableRow resource type</span></span>

> <span data-ttu-id="af2e9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="af2e9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="af2e9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="af2e9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="af2e9-106">Representa una fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="af2e9-106">Represents a row in a table.</span></span>


## <a name="methods"></a><span data-ttu-id="af2e9-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="af2e9-107">Methods</span></span>

| <span data-ttu-id="af2e9-108">Método</span><span class="sxs-lookup"><span data-stu-id="af2e9-108">Method</span></span>           | <span data-ttu-id="af2e9-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af2e9-109">Return Type</span></span>    |<span data-ttu-id="af2e9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="af2e9-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="af2e9-111">Get TableRow</span><span class="sxs-lookup"><span data-stu-id="af2e9-111">Get TableRow</span></span>](../api/tablerow-get.md) | [<span data-ttu-id="af2e9-112">TableRow</span><span class="sxs-lookup"><span data-stu-id="af2e9-112">TableRow</span></span>](tablerow.md) |<span data-ttu-id="af2e9-113">Lee las propiedades y relaciones del objeto tableRow.</span><span class="sxs-lookup"><span data-stu-id="af2e9-113">Read properties and relationships of tableRow object.</span></span>|
|[<span data-ttu-id="af2e9-114">Update</span><span class="sxs-lookup"><span data-stu-id="af2e9-114">Update</span></span>](../api/tablerow-update.md) | [<span data-ttu-id="af2e9-115">TableRow</span><span class="sxs-lookup"><span data-stu-id="af2e9-115">TableRow</span></span>](tablerow.md)  |<span data-ttu-id="af2e9-116">Actualiza el objeto TableRow.</span><span class="sxs-lookup"><span data-stu-id="af2e9-116">Update TableRow object.</span></span> |
|[<span data-ttu-id="af2e9-117">Range</span><span class="sxs-lookup"><span data-stu-id="af2e9-117">Range</span></span>](../api/tablerow-range.md)|[<span data-ttu-id="af2e9-118">Range</span><span class="sxs-lookup"><span data-stu-id="af2e9-118">Range</span></span>](range.md)|<span data-ttu-id="af2e9-119">Devuelve el objeto de rango asociado a toda la fila.</span><span class="sxs-lookup"><span data-stu-id="af2e9-119">Returns the range object associated with the entire row.</span></span>|
|[<span data-ttu-id="af2e9-120">Delete</span><span class="sxs-lookup"><span data-stu-id="af2e9-120">Delete</span></span>](../api/tablerow-delete.md)|<span data-ttu-id="af2e9-121">None</span><span class="sxs-lookup"><span data-stu-id="af2e9-121">None</span></span>|<span data-ttu-id="af2e9-122">Elimina la fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="af2e9-122">Deletes the row from the table.</span></span>|
|[<span data-ttu-id="af2e9-123">List</span><span class="sxs-lookup"><span data-stu-id="af2e9-123">List</span></span>](../api/tablerow-list.md) | <span data-ttu-id="af2e9-124">Colección [TableRow](tablerow.md)</span><span class="sxs-lookup"><span data-stu-id="af2e9-124">[TableRow](tablerow.md) collection</span></span> |<span data-ttu-id="af2e9-125">Obtiene la colección de objetos tableRow.</span><span class="sxs-lookup"><span data-stu-id="af2e9-125">Get tableRow object collection.</span></span> |
|[<span data-ttu-id="af2e9-126">Itemat</span><span class="sxs-lookup"><span data-stu-id="af2e9-126">Itemat</span></span>](../api/tablerowcollection-itemat.md)|[<span data-ttu-id="af2e9-127">TableRow</span><span class="sxs-lookup"><span data-stu-id="af2e9-127">TableRow</span></span>](tablerow.md)|<span data-ttu-id="af2e9-128">Obtiene una fila en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="af2e9-128">Gets a row based on its position in the collection.</span></span>|
|[<span data-ttu-id="af2e9-129">Add</span><span class="sxs-lookup"><span data-stu-id="af2e9-129">Add</span></span>](../api/tablerowcollection-add.md)|[<span data-ttu-id="af2e9-130">TableRow</span><span class="sxs-lookup"><span data-stu-id="af2e9-130">TableRow</span></span>](tablerow.md)|<span data-ttu-id="af2e9-131">Agrega una nueva fila a la tabla.</span><span class="sxs-lookup"><span data-stu-id="af2e9-131">Adds a new row to the table.</span></span>|

## <a name="properties"></a><span data-ttu-id="af2e9-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="af2e9-132">Properties</span></span>
| <span data-ttu-id="af2e9-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="af2e9-133">Property</span></span>     | <span data-ttu-id="af2e9-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="af2e9-134">Type</span></span>   |<span data-ttu-id="af2e9-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="af2e9-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="af2e9-136">index</span><span class="sxs-lookup"><span data-stu-id="af2e9-136">index</span></span>|<span data-ttu-id="af2e9-137">int</span><span class="sxs-lookup"><span data-stu-id="af2e9-137">int</span></span>|<span data-ttu-id="af2e9-p102">Devuelve el número de índice de la fila dentro de la colección de filas de la tabla. Indizado con cero. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af2e9-p102">Returns the index number of the row within the rows collection of the table. Zero-indexed. Read-only.</span></span>|
|<span data-ttu-id="af2e9-141">values</span><span class="sxs-lookup"><span data-stu-id="af2e9-141">values</span></span>|<span data-ttu-id="af2e9-142">json</span><span class="sxs-lookup"><span data-stu-id="af2e9-142">json</span></span>|<span data-ttu-id="af2e9-p103">Representa los valores sin formato del intervalo especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="af2e9-p103">Represents the raw values of the specified range. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>|

## <a name="relationships"></a><span data-ttu-id="af2e9-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="af2e9-146">Relationships</span></span>
<span data-ttu-id="af2e9-147">Ninguno</span><span class="sxs-lookup"><span data-stu-id="af2e9-147">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="af2e9-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="af2e9-148">JSON representation</span></span>

<span data-ttu-id="af2e9-149">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="af2e9-149">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.tableRow"
}-->

```json
{
  "index": 1024,
  "values": "json"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableRow resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
