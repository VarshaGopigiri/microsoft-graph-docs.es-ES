---
title: Tipo de recurso Filter
description: Administra el filtrado de la columna de una tabla.
ms.openlocfilehash: 272b4ea0ee91c25ea845217512a12e33b08ed7b8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030240"
---
# <a name="filter-resource-type"></a><span data-ttu-id="3f162-103">Tipo de recurso Filter</span><span class="sxs-lookup"><span data-stu-id="3f162-103">Filter resource type</span></span>

<span data-ttu-id="3f162-104">Administra el filtrado de la columna de una tabla.</span><span class="sxs-lookup"><span data-stu-id="3f162-104">Manages the filtering of a table's column.</span></span>


## <a name="methods"></a><span data-ttu-id="3f162-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f162-105">Methods</span></span>

| <span data-ttu-id="3f162-106">Método</span><span class="sxs-lookup"><span data-stu-id="3f162-106">Method</span></span>           | <span data-ttu-id="3f162-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f162-107">Return Type</span></span>    |<span data-ttu-id="3f162-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f162-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="3f162-109">Apply</span><span class="sxs-lookup"><span data-stu-id="3f162-109">Apply</span></span>](../api/filter-apply.md)|<span data-ttu-id="3f162-110">None</span><span class="sxs-lookup"><span data-stu-id="3f162-110">None</span></span>|<span data-ttu-id="3f162-111">Aplica los criterios de filtro especificados en la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="3f162-111">Apply the given filter criteria on the given column.</span></span>|
|[<span data-ttu-id="3f162-112">Clear</span><span class="sxs-lookup"><span data-stu-id="3f162-112">Clear</span></span>](../api/filter-clear.md)|<span data-ttu-id="3f162-113">None</span><span class="sxs-lookup"><span data-stu-id="3f162-113">None</span></span>|<span data-ttu-id="3f162-114">Borra el filtro de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="3f162-114">Clear the filter on the given column.</span></span>|

## <a name="properties"></a><span data-ttu-id="3f162-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3f162-115">Properties</span></span>

| <span data-ttu-id="3f162-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="3f162-116">Name</span></span> | <span data-ttu-id="3f162-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f162-117">Type</span></span>   |<span data-ttu-id="3f162-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f162-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3f162-119">criterios</span><span class="sxs-lookup"><span data-stu-id="3f162-119">criteria</span></span>|[<span data-ttu-id="3f162-120">WorkbookFilterCriteria</span><span class="sxs-lookup"><span data-stu-id="3f162-120">WorkbookFilterCriteria</span></span>](filtercriteria.md)|<span data-ttu-id="3f162-p101">Filtro aplicado actualmente en la columna especificada. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3f162-p101">The currently applied filter on the given column. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3f162-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3f162-123">JSON representation</span></span>

<span data-ttu-id="3f162-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3f162-124">Here is a JSON representation of the resource.</span></span>

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