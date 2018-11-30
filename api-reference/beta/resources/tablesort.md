---
title: Tipo de recurso TableSort
description: Administra operaciones de ordenación en objetos Table.
ms.openlocfilehash: 02ee1f72bc53a3097c76cf9bab62a165fe3c56f8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091064"
---
# <a name="tablesort-resource-type"></a><span data-ttu-id="92ada-103">Tipo de recurso TableSort</span><span class="sxs-lookup"><span data-stu-id="92ada-103">TableSort resource type</span></span>

> <span data-ttu-id="92ada-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="92ada-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="92ada-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="92ada-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="92ada-106">Administra operaciones de ordenación en objetos Table.</span><span class="sxs-lookup"><span data-stu-id="92ada-106">Manages sorting operations on Table objects.</span></span>


## <a name="methods"></a><span data-ttu-id="92ada-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="92ada-107">Methods</span></span>

| <span data-ttu-id="92ada-108">Método</span><span class="sxs-lookup"><span data-stu-id="92ada-108">Method</span></span>           | <span data-ttu-id="92ada-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92ada-109">Return Type</span></span>    |<span data-ttu-id="92ada-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="92ada-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="92ada-111">Get TableSort</span><span class="sxs-lookup"><span data-stu-id="92ada-111">Get TableSort</span></span>](../api/tablesort-get.md) | [<span data-ttu-id="92ada-112">TableSort</span><span class="sxs-lookup"><span data-stu-id="92ada-112">TableSort</span></span>](tablesort.md) |<span data-ttu-id="92ada-113">Lee las propiedades y relaciones del objeto tableSort.</span><span class="sxs-lookup"><span data-stu-id="92ada-113">Read properties and relationships of tableSort object.</span></span>|
|[<span data-ttu-id="92ada-114">Apply</span><span class="sxs-lookup"><span data-stu-id="92ada-114">Apply</span></span>](../api/tablesort-apply.md)|<span data-ttu-id="92ada-115">None</span><span class="sxs-lookup"><span data-stu-id="92ada-115">None</span></span>|<span data-ttu-id="92ada-116">Realiza una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="92ada-116">Perform a sort operation.</span></span>|
|[<span data-ttu-id="92ada-117">Clear</span><span class="sxs-lookup"><span data-stu-id="92ada-117">Clear</span></span>](../api/tablesort-clear.md)|<span data-ttu-id="92ada-118">None</span><span class="sxs-lookup"><span data-stu-id="92ada-118">None</span></span>|<span data-ttu-id="92ada-p102">Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.</span><span class="sxs-lookup"><span data-stu-id="92ada-p102">Clears the sorting that is currently on the table. While this doesn't modify the table's ordering, it clears the state of the header buttons.</span></span>|
|[<span data-ttu-id="92ada-121">Reapply</span><span class="sxs-lookup"><span data-stu-id="92ada-121">Reapply</span></span>](../api/tablesort-reapply.md)|<span data-ttu-id="92ada-122">None</span><span class="sxs-lookup"><span data-stu-id="92ada-122">None</span></span>|<span data-ttu-id="92ada-123">Vuelve a aplicar los parámetros de ordenación actuales a la tabla.</span><span class="sxs-lookup"><span data-stu-id="92ada-123">Reapplies the current sorting parameters to the table.</span></span>|

## <a name="properties"></a><span data-ttu-id="92ada-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="92ada-124">Properties</span></span>
| <span data-ttu-id="92ada-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="92ada-125">Property</span></span>     | <span data-ttu-id="92ada-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="92ada-126">Type</span></span>   |<span data-ttu-id="92ada-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="92ada-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="92ada-128">matchCase</span><span class="sxs-lookup"><span data-stu-id="92ada-128">matchCase</span></span>|<span data-ttu-id="92ada-129">boolean</span><span class="sxs-lookup"><span data-stu-id="92ada-129">boolean</span></span>|<span data-ttu-id="92ada-p103">Indica si última ordenación de la tabla distinguía mayúsculas de minúsculas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="92ada-p103">Represents whether the casing impacted the last sort of the table. Read-only.</span></span>|
|<span data-ttu-id="92ada-132">method</span><span class="sxs-lookup"><span data-stu-id="92ada-132">method</span></span>|<span data-ttu-id="92ada-133">string</span><span class="sxs-lookup"><span data-stu-id="92ada-133">string</span></span>|<span data-ttu-id="92ada-p104">Representa el método de ordenación de caracteres chinos usado por última vez para ordenar la tabla. Valores posibles: `PinYin`, `StrokeCount`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="92ada-p104">Represents Chinese character ordering method last used to sort the table. Possible values are: `PinYin`, `StrokeCount`. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="92ada-137">Relaciones</span><span class="sxs-lookup"><span data-stu-id="92ada-137">Relationships</span></span>
| <span data-ttu-id="92ada-138">Relación</span><span class="sxs-lookup"><span data-stu-id="92ada-138">Relationship</span></span> | <span data-ttu-id="92ada-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="92ada-139">Type</span></span>   |<span data-ttu-id="92ada-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="92ada-140">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="92ada-141">fields</span><span class="sxs-lookup"><span data-stu-id="92ada-141">fields</span></span>|[<span data-ttu-id="92ada-142">SortField</span><span class="sxs-lookup"><span data-stu-id="92ada-142">SortField</span></span>](sortfield.md)|<span data-ttu-id="92ada-p105">Representa las condiciones actuales que se usaron por última vez para ordenar la tabla. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="92ada-p105">Represents the current conditions used to last sort the table. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="92ada-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="92ada-145">JSON representation</span></span>

<span data-ttu-id="92ada-146">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="92ada-146">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.tableSort"
}-->

```json
{
  "matchCase": true,
  "method": "string"
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