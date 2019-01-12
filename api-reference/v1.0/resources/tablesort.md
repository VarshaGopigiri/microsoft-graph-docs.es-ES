---
title: Tipo de recurso TableSort
description: Administra operaciones de ordenación en objetos Table.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: be607832be82b99853b4cd44cfa5b60449a2c432
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27929476"
---
# <a name="tablesort-resource-type"></a><span data-ttu-id="1b64a-103">Tipo de recurso TableSort</span><span class="sxs-lookup"><span data-stu-id="1b64a-103">TableSort resource type</span></span>

<span data-ttu-id="1b64a-104">Administra operaciones de ordenación en objetos Table.</span><span class="sxs-lookup"><span data-stu-id="1b64a-104">Manages sorting operations on Table objects.</span></span>


## <a name="methods"></a><span data-ttu-id="1b64a-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="1b64a-105">Methods</span></span>

| <span data-ttu-id="1b64a-106">Método</span><span class="sxs-lookup"><span data-stu-id="1b64a-106">Method</span></span>           | <span data-ttu-id="1b64a-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b64a-107">Return Type</span></span>    |<span data-ttu-id="1b64a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b64a-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="1b64a-109">Get TableSort</span><span class="sxs-lookup"><span data-stu-id="1b64a-109">Get TableSort</span></span>](../api/tablesort-get.md) | [<span data-ttu-id="1b64a-110">WorkbookTableSort</span><span class="sxs-lookup"><span data-stu-id="1b64a-110">WorkbookTableSort</span></span>](tablesort.md) |<span data-ttu-id="1b64a-111">Lee las propiedades y relaciones del objeto tableSort.</span><span class="sxs-lookup"><span data-stu-id="1b64a-111">Read properties and relationships of tableSort object.</span></span>|
|[<span data-ttu-id="1b64a-112">Apply</span><span class="sxs-lookup"><span data-stu-id="1b64a-112">Apply</span></span>](../api/tablesort-apply.md)|<span data-ttu-id="1b64a-113">None</span><span class="sxs-lookup"><span data-stu-id="1b64a-113">None</span></span>|<span data-ttu-id="1b64a-114">Realiza una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="1b64a-114">Perform a sort operation.</span></span>|
|[<span data-ttu-id="1b64a-115">Clear</span><span class="sxs-lookup"><span data-stu-id="1b64a-115">Clear</span></span>](../api/tablesort-clear.md)|<span data-ttu-id="1b64a-116">None</span><span class="sxs-lookup"><span data-stu-id="1b64a-116">None</span></span>|<span data-ttu-id="1b64a-p101">Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.</span><span class="sxs-lookup"><span data-stu-id="1b64a-p101">Clears the sorting that is currently on the table. While this doesn't modify the table's ordering, it clears the state of the header buttons.</span></span>|
|[<span data-ttu-id="1b64a-119">Reapply</span><span class="sxs-lookup"><span data-stu-id="1b64a-119">Reapply</span></span>](../api/tablesort-reapply.md)|<span data-ttu-id="1b64a-120">None</span><span class="sxs-lookup"><span data-stu-id="1b64a-120">None</span></span>|<span data-ttu-id="1b64a-121">Vuelve a aplicar los parámetros de ordenación actuales a la tabla.</span><span class="sxs-lookup"><span data-stu-id="1b64a-121">Reapplies the current sorting parameters to the table.</span></span>|

## <a name="properties"></a><span data-ttu-id="1b64a-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1b64a-122">Properties</span></span>
| <span data-ttu-id="1b64a-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1b64a-123">Property</span></span>     | <span data-ttu-id="1b64a-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b64a-124">Type</span></span>   |<span data-ttu-id="1b64a-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b64a-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1b64a-126">fields</span><span class="sxs-lookup"><span data-stu-id="1b64a-126">fields</span></span>|<span data-ttu-id="1b64a-127">Colección de [WorkbookSortField](sortfield.md)</span><span class="sxs-lookup"><span data-stu-id="1b64a-127">[WorkbookSortField](sortfield.md) collection</span></span>|<span data-ttu-id="1b64a-p102">Representa las condiciones actuales que se usaron por última vez para ordenar la tabla. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1b64a-p102">Represents the current conditions used to last sort the table. Read-only.</span></span>|
|<span data-ttu-id="1b64a-130">matchCase</span><span class="sxs-lookup"><span data-stu-id="1b64a-130">matchCase</span></span>|<span data-ttu-id="1b64a-131">boolean</span><span class="sxs-lookup"><span data-stu-id="1b64a-131">boolean</span></span>|<span data-ttu-id="1b64a-p103">Indica si última ordenación de la tabla distinguía mayúsculas de minúsculas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1b64a-p103">Represents whether the casing impacted the last sort of the table. Read-only.</span></span>|
|<span data-ttu-id="1b64a-134">method</span><span class="sxs-lookup"><span data-stu-id="1b64a-134">method</span></span>|<span data-ttu-id="1b64a-135">string</span><span class="sxs-lookup"><span data-stu-id="1b64a-135">string</span></span>|<span data-ttu-id="1b64a-136">Representa el método utilizado por última vez para ordenar la tabla de orden de los caracteres chinos.</span><span class="sxs-lookup"><span data-stu-id="1b64a-136">Represents Chinese character ordering method last used to sort the table.</span></span> <span data-ttu-id="1b64a-137">Los valores posibles son: `PinYin`, `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="1b64a-137">The possible values are: `PinYin`, `StrokeCount`.</span></span> <span data-ttu-id="1b64a-138">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1b64a-138">Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1b64a-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1b64a-139">JSON representation</span></span>

<span data-ttu-id="1b64a-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1b64a-140">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookTableSort"
}-->

```json
{
  "matchCase": true,
  "method": "string",
  "fields": [{ "@odata.type": "microsoft.graph.workbookSortField" }]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableSort resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
