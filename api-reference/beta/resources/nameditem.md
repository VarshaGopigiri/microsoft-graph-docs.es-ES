---
title: Tipo de recurso NamedItem
description: Representa un nombre definido para un rango de celdas o un valor. Los nombres pueden ser objetos primitivos con nombre (como puede verse en el tipo siguiente), un objeto de rango o una referencia a un rango. Este objeto puede usarse para obtener un objeto de rango asociado a nombres.
localization_priority: Normal
ms.openlocfilehash: 5dd093976b2c09ae93c608144c8d6c2b7d7161c2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815375"
---
# <a name="nameditem-resource-type"></a><span data-ttu-id="30747-105">Tipo de recurso NamedItem</span><span class="sxs-lookup"><span data-stu-id="30747-105">NamedItem resource type</span></span>

<span data-ttu-id="30747-p102">Representa un nombre definido para un rango de celdas o un valor. Los nombres pueden ser objetos primitivos con nombre (como puede verse en el tipo siguiente), un objeto de rango o una referencia a un rango. Este objeto puede usarse para obtener un objeto de rango asociado a nombres.</span><span class="sxs-lookup"><span data-stu-id="30747-p102">Represents a defined name for a range of cells or value. Names can be primitive named objects (as seen in the type below), range object, reference to a range. This object can be used to obtain range object associated with names.</span></span>


## <a name="methods"></a><span data-ttu-id="30747-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="30747-109">Methods</span></span>

| <span data-ttu-id="30747-110">Método</span><span class="sxs-lookup"><span data-stu-id="30747-110">Method</span></span>           | <span data-ttu-id="30747-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30747-111">Return Type</span></span>    |<span data-ttu-id="30747-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="30747-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="30747-113">Add</span><span class="sxs-lookup"><span data-stu-id="30747-113">Add</span></span>](../api/nameditem-add.md)|[<span data-ttu-id="30747-114">NamedItem</span><span class="sxs-lookup"><span data-stu-id="30747-114">NamedItem</span></span>](nameditem.md)|<span data-ttu-id="30747-115">Agrega un nuevo nombre a la colección del ámbito especificado.</span><span class="sxs-lookup"><span data-stu-id="30747-115">Adds a new name to the collection of the given scope.</span></span>|
|[<span data-ttu-id="30747-116">AddFormulaLocal</span><span class="sxs-lookup"><span data-stu-id="30747-116">AddFormulaLocal</span></span>](../api/nameditem-addformulalocal.md)|[<span data-ttu-id="30747-117">NamedItem</span><span class="sxs-lookup"><span data-stu-id="30747-117">NamedItem</span></span>](nameditem.md)|<span data-ttu-id="30747-118">Agrega un nuevo nombre a la colección del ámbito especificado empleando la configuración regional del usuario para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="30747-118">Adds a new name to the collection of the given scope using the user's locale for the formula.</span></span>|
|[<span data-ttu-id="30747-119">Get NamedItem</span><span class="sxs-lookup"><span data-stu-id="30747-119">Get NamedItem</span></span>](../api/nameditem-get.md) | [<span data-ttu-id="30747-120">NamedItem</span><span class="sxs-lookup"><span data-stu-id="30747-120">NamedItem</span></span>](nameditem.md) |<span data-ttu-id="30747-121">Lee las propiedades y relaciones del objeto namedItem.</span><span class="sxs-lookup"><span data-stu-id="30747-121">Read properties and relationships of namedItem object.</span></span>|
|[<span data-ttu-id="30747-122">Update</span><span class="sxs-lookup"><span data-stu-id="30747-122">Update</span></span>](../api/nameditem-update.md) | [<span data-ttu-id="30747-123">NamedItem</span><span class="sxs-lookup"><span data-stu-id="30747-123">NamedItem</span></span>](nameditem.md)   |<span data-ttu-id="30747-124">Actualiza el objeto NamedItem.</span><span class="sxs-lookup"><span data-stu-id="30747-124">Update NamedItem object.</span></span> |
|[<span data-ttu-id="30747-125">Range</span><span class="sxs-lookup"><span data-stu-id="30747-125">Range</span></span>](../api/nameditem-range.md)|[<span data-ttu-id="30747-126">Range</span><span class="sxs-lookup"><span data-stu-id="30747-126">Range</span></span>](range.md)|<span data-ttu-id="30747-p103">Devuelve el objeto de intervalo asociado al nombre. Produce una excepción si el tipo del elemento con nombre no es un intervalo.</span><span class="sxs-lookup"><span data-stu-id="30747-p103">Returns the range object that is associated with the name. Throws an exception if the named item's type is not a range.</span></span>|
|[<span data-ttu-id="30747-129">List</span><span class="sxs-lookup"><span data-stu-id="30747-129">List</span></span>](../api/nameditem-list.md) | <span data-ttu-id="30747-130">Colección [NamedItem](nameditem.md)</span><span class="sxs-lookup"><span data-stu-id="30747-130">[NamedItem](nameditem.md) collection</span></span> |<span data-ttu-id="30747-131">Obtiene la colección de objetos namedItem.</span><span class="sxs-lookup"><span data-stu-id="30747-131">Get namedItem object collection.</span></span> |

## <a name="properties"></a><span data-ttu-id="30747-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="30747-132">Properties</span></span>
| <span data-ttu-id="30747-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="30747-133">Property</span></span>     | <span data-ttu-id="30747-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="30747-134">Type</span></span>   |<span data-ttu-id="30747-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="30747-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="30747-136">name</span><span class="sxs-lookup"><span data-stu-id="30747-136">name</span></span>|<span data-ttu-id="30747-137">string</span><span class="sxs-lookup"><span data-stu-id="30747-137">string</span></span>|<span data-ttu-id="30747-p104">Nombre del objeto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="30747-p104">The name of the object. Read-only.</span></span>|
|<span data-ttu-id="30747-140">comment</span><span class="sxs-lookup"><span data-stu-id="30747-140">comment</span></span>|<span data-ttu-id="30747-141">string</span><span class="sxs-lookup"><span data-stu-id="30747-141">string</span></span>|<span data-ttu-id="30747-142">Representa el comentario asociado a este nombre.</span><span class="sxs-lookup"><span data-stu-id="30747-142">Represents the comment associated with this name.</span></span>|
|<span data-ttu-id="30747-143">scope</span><span class="sxs-lookup"><span data-stu-id="30747-143">scope</span></span>|<span data-ttu-id="30747-144">string</span><span class="sxs-lookup"><span data-stu-id="30747-144">string</span></span>|<span data-ttu-id="30747-p105">Indica si el nombre está en el ámbito del libro o de una hoja de cálculo específica. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="30747-p105">Indicates whether the name is scoped to the workbook or to a specific worksheet. Read-only.</span></span>|
|<span data-ttu-id="30747-147">type</span><span class="sxs-lookup"><span data-stu-id="30747-147">type</span></span>|<span data-ttu-id="30747-148">string</span><span class="sxs-lookup"><span data-stu-id="30747-148">string</span></span>|<span data-ttu-id="30747-p106">Indica el tipo de referencia que está asociado al nombre. Valores posibles: `String`, `Integer`, `Double`, `Boolean`, `Range`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="30747-p106">Indicates what type of reference is associated with the name. Possible values are: `String`, `Integer`, `Double`, `Boolean`, `Range`. Read-only.</span></span>|
|<span data-ttu-id="30747-152">value</span><span class="sxs-lookup"><span data-stu-id="30747-152">value</span></span>|<span data-ttu-id="30747-153">string</span><span class="sxs-lookup"><span data-stu-id="30747-153">string</span></span>|<span data-ttu-id="30747-p107">Representa la fórmula a la que debe hacer referencia el nombre, según su definición. Por ejemplo =Sheet14!$B$2:$H$12, =4.75, etc. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="30747-p107">Represents the formula that the name is defined to refer to. E.g. =Sheet14!$B$2:$H$12, =4.75, etc. Read-only.</span></span>|
|<span data-ttu-id="30747-157">visible</span><span class="sxs-lookup"><span data-stu-id="30747-157">visible</span></span>|<span data-ttu-id="30747-158">boolean</span><span class="sxs-lookup"><span data-stu-id="30747-158">boolean</span></span>|<span data-ttu-id="30747-159">Especifica si el objeto está visible o no.</span><span class="sxs-lookup"><span data-stu-id="30747-159">Specifies whether the object is visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="30747-160">Relaciones</span><span class="sxs-lookup"><span data-stu-id="30747-160">Relationships</span></span>
| <span data-ttu-id="30747-161">Relación</span><span class="sxs-lookup"><span data-stu-id="30747-161">Relationship</span></span>     | <span data-ttu-id="30747-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="30747-162">Type</span></span>   |<span data-ttu-id="30747-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="30747-163">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="30747-164">worksheet</span><span class="sxs-lookup"><span data-stu-id="30747-164">worksheet</span></span>|[<span data-ttu-id="30747-165">worksheet</span><span class="sxs-lookup"><span data-stu-id="30747-165">worksheet</span></span>](worksheet.md)|<span data-ttu-id="30747-p108">Devuelve la hoja de cálculo que tiene como ámbito el elemento con nombre. Solo está disponible si el elemento tiene como ámbito la hoja de cálculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="30747-p108">Returns the worksheet on which the named item is scoped to. Available only if the item is scoped to the worksheet. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="30747-169">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="30747-169">JSON representation</span></span>

<span data-ttu-id="30747-170">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="30747-170">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.namedItem"
}-->

```json
{
  "name": "string",
  "comment": "string",
  "scope": "string",
  "type": "string",
  "value": "string",
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
