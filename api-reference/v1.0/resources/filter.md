---
title: Tipo de recurso Filter
description: Administra el filtrado de la columna de una tabla.
localization_priority: Normal
ms.openlocfilehash: cc4b1b105c2049b36fa27cb88b41102366648fa8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834667"
---
# <a name="filter-resource-type"></a><span data-ttu-id="dfe57-103">Tipo de recurso Filter</span><span class="sxs-lookup"><span data-stu-id="dfe57-103">Filter resource type</span></span>

<span data-ttu-id="dfe57-104">Administra el filtrado de la columna de una tabla.</span><span class="sxs-lookup"><span data-stu-id="dfe57-104">Manages the filtering of a table's column.</span></span>


## <a name="methods"></a><span data-ttu-id="dfe57-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="dfe57-105">Methods</span></span>

| <span data-ttu-id="dfe57-106">Método</span><span class="sxs-lookup"><span data-stu-id="dfe57-106">Method</span></span>           | <span data-ttu-id="dfe57-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfe57-107">Return Type</span></span>    |<span data-ttu-id="dfe57-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfe57-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="dfe57-109">Apply</span><span class="sxs-lookup"><span data-stu-id="dfe57-109">Apply</span></span>](../api/filter-apply.md)|<span data-ttu-id="dfe57-110">None</span><span class="sxs-lookup"><span data-stu-id="dfe57-110">None</span></span>|<span data-ttu-id="dfe57-111">Aplica los criterios de filtro especificados en la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="dfe57-111">Apply the given filter criteria on the given column.</span></span>|
|[<span data-ttu-id="dfe57-112">Clear</span><span class="sxs-lookup"><span data-stu-id="dfe57-112">Clear</span></span>](../api/filter-clear.md)|<span data-ttu-id="dfe57-113">None</span><span class="sxs-lookup"><span data-stu-id="dfe57-113">None</span></span>|<span data-ttu-id="dfe57-114">Borra el filtro de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="dfe57-114">Clear the filter on the given column.</span></span>|

## <a name="properties"></a><span data-ttu-id="dfe57-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dfe57-115">Properties</span></span>

| <span data-ttu-id="dfe57-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="dfe57-116">Name</span></span> | <span data-ttu-id="dfe57-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="dfe57-117">Type</span></span>   |<span data-ttu-id="dfe57-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfe57-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dfe57-119">criterios</span><span class="sxs-lookup"><span data-stu-id="dfe57-119">criteria</span></span>|[<span data-ttu-id="dfe57-120">WorkbookFilterCriteria</span><span class="sxs-lookup"><span data-stu-id="dfe57-120">WorkbookFilterCriteria</span></span>](filtercriteria.md)|<span data-ttu-id="dfe57-p101">Filtro aplicado actualmente en la columna especificada. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dfe57-p101">The currently applied filter on the given column. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="dfe57-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dfe57-123">JSON representation</span></span>

<span data-ttu-id="dfe57-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="dfe57-124">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookFilter"
}-->

```json
{
  "criteria": {"@odata.type": "microsoft.graph.workbookFilterCriteria" }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Filter resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
