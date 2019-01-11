---
title: Tipo de recurso NamedItem
description: Representa un nombre definido para un rango de celdas o un valor. Los nombres pueden ser objetos primitivos con nombre (como puede verse en el tipo siguiente), un objeto de rango o una referencia a un rango. Este objeto puede usarse para obtener un objeto de rango asociado a nombres.
localization_priority: Normal
ms.openlocfilehash: e413361cc42a0f8f65e23e12d36b49d2c7bcebb3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883828"
---
# <a name="nameditem-resource-type"></a><span data-ttu-id="76722-105">Tipo de recurso NamedItem</span><span class="sxs-lookup"><span data-stu-id="76722-105">NamedItem resource type</span></span>

<span data-ttu-id="76722-p102">Representa un nombre definido para un rango de celdas o un valor. Los nombres pueden ser objetos primitivos con nombre (como puede verse en el tipo siguiente), un objeto de rango o una referencia a un rango. Este objeto puede usarse para obtener un objeto de rango asociado a nombres.</span><span class="sxs-lookup"><span data-stu-id="76722-p102">Represents a defined name for a range of cells or value. Names can be primitive named objects (as seen in the type below), range object, reference to a range. This object can be used to obtain range object associated with names.</span></span>


## <a name="methods"></a><span data-ttu-id="76722-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="76722-109">Methods</span></span>

| <span data-ttu-id="76722-110">Método</span><span class="sxs-lookup"><span data-stu-id="76722-110">Method</span></span>           | <span data-ttu-id="76722-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76722-111">Return Type</span></span>    |<span data-ttu-id="76722-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="76722-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="76722-113">Add</span><span class="sxs-lookup"><span data-stu-id="76722-113">Add</span></span>](../api/nameditem-add.md)|[<span data-ttu-id="76722-114">WorkbookNamedItem</span><span class="sxs-lookup"><span data-stu-id="76722-114">WorkbookNamedItem</span></span>](nameditem.md)|<span data-ttu-id="76722-115">Agrega un nuevo nombre a la colección del ámbito especificado.</span><span class="sxs-lookup"><span data-stu-id="76722-115">Adds a new name to the collection of the given scope.</span></span>|
|[<span data-ttu-id="76722-116">AddFormulaLocal</span><span class="sxs-lookup"><span data-stu-id="76722-116">AddFormulaLocal</span></span>](../api/nameditem-addformulalocal.md)|[<span data-ttu-id="76722-117">WorkbookNamedItem</span><span class="sxs-lookup"><span data-stu-id="76722-117">WorkbookNamedItem</span></span>](nameditem.md)|<span data-ttu-id="76722-118">Agrega un nuevo nombre a la colección del ámbito especificado empleando la configuración regional del usuario para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="76722-118">Adds a new name to the collection of the given scope using the user's locale for the formula.</span></span>|
|[<span data-ttu-id="76722-119">Get NamedItem</span><span class="sxs-lookup"><span data-stu-id="76722-119">Get NamedItem</span></span>](../api/nameditem-get.md) | [<span data-ttu-id="76722-120">WorkbookNamedItem</span><span class="sxs-lookup"><span data-stu-id="76722-120">WorkbookNamedItem</span></span>](nameditem.md) |<span data-ttu-id="76722-121">Lee las propiedades y relaciones del objeto namedItem.</span><span class="sxs-lookup"><span data-stu-id="76722-121">Read properties and relationships of namedItem object.</span></span>|
|[<span data-ttu-id="76722-122">Update</span><span class="sxs-lookup"><span data-stu-id="76722-122">Update</span></span>](../api/nameditem-update.md) | [<span data-ttu-id="76722-123">WorkbookNamedItem</span><span class="sxs-lookup"><span data-stu-id="76722-123">WorkbookNamedItem</span></span>](nameditem.md)   |<span data-ttu-id="76722-124">Actualiza el objeto NamedItem.</span><span class="sxs-lookup"><span data-stu-id="76722-124">Update NamedItem object.</span></span> |
|[<span data-ttu-id="76722-125">Range</span><span class="sxs-lookup"><span data-stu-id="76722-125">Range</span></span>](../api/nameditem-range.md)|[<span data-ttu-id="76722-126">Range</span><span class="sxs-lookup"><span data-stu-id="76722-126">Range</span></span>](range.md)|<span data-ttu-id="76722-p103">Devuelve el objeto de intervalo asociado al nombre. Produce una excepción si el tipo del elemento con nombre no es un intervalo.</span><span class="sxs-lookup"><span data-stu-id="76722-p103">Returns the range object that is associated with the name. Throws an exception if the named item's type is not a range.</span></span>|
|[<span data-ttu-id="76722-129">List</span><span class="sxs-lookup"><span data-stu-id="76722-129">List</span></span>](../api/nameditem-list.md) | <span data-ttu-id="76722-130">Colección de [WorkbookNamedItem](nameditem.md)</span><span class="sxs-lookup"><span data-stu-id="76722-130">[WorkbookNamedItem](nameditem.md) collection</span></span> |<span data-ttu-id="76722-131">Obtiene la colección de objetos namedItem.</span><span class="sxs-lookup"><span data-stu-id="76722-131">Get namedItem object collection.</span></span> |

## <a name="properties"></a><span data-ttu-id="76722-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="76722-132">Properties</span></span>
| <span data-ttu-id="76722-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="76722-133">Property</span></span>     | <span data-ttu-id="76722-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="76722-134">Type</span></span>   |<span data-ttu-id="76722-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="76722-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="76722-136">name</span><span class="sxs-lookup"><span data-stu-id="76722-136">name</span></span>|<span data-ttu-id="76722-137">string</span><span class="sxs-lookup"><span data-stu-id="76722-137">string</span></span>|<span data-ttu-id="76722-p104">Nombre del objeto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="76722-p104">The name of the object. Read-only.</span></span>|
|<span data-ttu-id="76722-140">comment</span><span class="sxs-lookup"><span data-stu-id="76722-140">comment</span></span>|<span data-ttu-id="76722-141">string</span><span class="sxs-lookup"><span data-stu-id="76722-141">string</span></span>|<span data-ttu-id="76722-142">Representa el comentario asociado a este nombre.</span><span class="sxs-lookup"><span data-stu-id="76722-142">Represents the comment associated with this name.</span></span>|
|<span data-ttu-id="76722-143">scope</span><span class="sxs-lookup"><span data-stu-id="76722-143">scope</span></span>|<span data-ttu-id="76722-144">string</span><span class="sxs-lookup"><span data-stu-id="76722-144">string</span></span>|<span data-ttu-id="76722-p105">Indica si el nombre está en el ámbito del libro o de una hoja de cálculo específica. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="76722-p105">Indicates whether the name is scoped to the workbook or to a specific worksheet. Read-only.</span></span>|
|<span data-ttu-id="76722-147">type</span><span class="sxs-lookup"><span data-stu-id="76722-147">type</span></span>|<span data-ttu-id="76722-148">string</span><span class="sxs-lookup"><span data-stu-id="76722-148">string</span></span>|<span data-ttu-id="76722-149">Indica qué tipo de referencia está asociado con el nombre.</span><span class="sxs-lookup"><span data-stu-id="76722-149">Indicates what type of reference is associated with the name.</span></span> <span data-ttu-id="76722-150">Los valores posibles son: `String`, `Integer`, `Double`, `Boolean`, `Range`.</span><span class="sxs-lookup"><span data-stu-id="76722-150">The possible values are: `String`, `Integer`, `Double`, `Boolean`, `Range`.</span></span> <span data-ttu-id="76722-151">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="76722-151">Read-only.</span></span>|
|<span data-ttu-id="76722-152">valor</span><span class="sxs-lookup"><span data-stu-id="76722-152">value</span></span>|<span data-ttu-id="76722-153">Json</span><span class="sxs-lookup"><span data-stu-id="76722-153">Json</span></span>|<span data-ttu-id="76722-p107">Representa la fórmula a la que debe hacer referencia el nombre, según su definición. Por ejemplo =Sheet14!$B$2:$H$12, =4.75, etc. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="76722-p107">Represents the formula that the name is defined to refer to. E.g. =Sheet14!$B$2:$H$12, =4.75, etc. Read-only.</span></span>|
|<span data-ttu-id="76722-157">visible</span><span class="sxs-lookup"><span data-stu-id="76722-157">visible</span></span>|<span data-ttu-id="76722-158">boolean</span><span class="sxs-lookup"><span data-stu-id="76722-158">boolean</span></span>|<span data-ttu-id="76722-159">Especifica si el objeto está visible o no.</span><span class="sxs-lookup"><span data-stu-id="76722-159">Specifies whether the object is visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="76722-160">Relaciones</span><span class="sxs-lookup"><span data-stu-id="76722-160">Relationships</span></span>
| <span data-ttu-id="76722-161">Relación</span><span class="sxs-lookup"><span data-stu-id="76722-161">Relationship</span></span>     | <span data-ttu-id="76722-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="76722-162">Type</span></span>   |<span data-ttu-id="76722-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="76722-163">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="76722-164">worksheet</span><span class="sxs-lookup"><span data-stu-id="76722-164">worksheet</span></span>|[<span data-ttu-id="76722-165">WorkbookWorksheet</span><span class="sxs-lookup"><span data-stu-id="76722-165">WorkbookWorksheet</span></span>](worksheet.md)|<span data-ttu-id="76722-p108">Devuelve la hoja de cálculo que tiene como ámbito el elemento con nombre. Solo está disponible si el elemento tiene como ámbito la hoja de cálculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="76722-p108">Returns the worksheet on which the named item is scoped to. Available only if the item is scoped to the worksheet. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="76722-169">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="76722-169">JSON representation</span></span>

<span data-ttu-id="76722-170">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="76722-170">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookNamedItem"
}-->

```json
{
  "name": "string",
  "comment": "string",
  "scope": "string",
  "type": "string",
  "value": {"@odata.type": "microsoft.graph.Json"},
  "visible": true
  
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "NamedItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
