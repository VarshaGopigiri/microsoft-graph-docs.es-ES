---
title: Tipo de recurso Filter
description: Administra el filtrado de la columna de una tabla.
localization_priority: Normal
ms.openlocfilehash: 5bbc4eff85f40e116ea513c27fa2966dd28a5493
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852790"
---
# <a name="filter-resource-type"></a><span data-ttu-id="53dcf-103">Tipo de recurso Filter</span><span class="sxs-lookup"><span data-stu-id="53dcf-103">Filter resource type</span></span>

> <span data-ttu-id="53dcf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="53dcf-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="53dcf-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="53dcf-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="53dcf-106">Administra el filtrado de la columna de una tabla.</span><span class="sxs-lookup"><span data-stu-id="53dcf-106">Manages the filtering of a table's column.</span></span>


## <a name="methods"></a><span data-ttu-id="53dcf-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="53dcf-107">Methods</span></span>

| <span data-ttu-id="53dcf-108">Método</span><span class="sxs-lookup"><span data-stu-id="53dcf-108">Method</span></span>           | <span data-ttu-id="53dcf-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53dcf-109">Return Type</span></span>    |<span data-ttu-id="53dcf-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="53dcf-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="53dcf-111">Apply</span><span class="sxs-lookup"><span data-stu-id="53dcf-111">Apply</span></span>](../api/filter-apply.md)|<span data-ttu-id="53dcf-112">None</span><span class="sxs-lookup"><span data-stu-id="53dcf-112">None</span></span>|<span data-ttu-id="53dcf-113">Aplica los criterios de filtro especificados en la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="53dcf-113">Apply the given filter criteria on the given column.</span></span>|
|[<span data-ttu-id="53dcf-114">Clear</span><span class="sxs-lookup"><span data-stu-id="53dcf-114">Clear</span></span>](../api/filter-clear.md)|<span data-ttu-id="53dcf-115">None</span><span class="sxs-lookup"><span data-stu-id="53dcf-115">None</span></span>|<span data-ttu-id="53dcf-116">Borra el filtro de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="53dcf-116">Clear the filter on the given column.</span></span>|

## <a name="properties"></a><span data-ttu-id="53dcf-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53dcf-117">Properties</span></span>
<span data-ttu-id="53dcf-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="53dcf-118">None</span></span>

## <a name="relationships"></a><span data-ttu-id="53dcf-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="53dcf-119">Relationships</span></span>
| <span data-ttu-id="53dcf-120">Relación</span><span class="sxs-lookup"><span data-stu-id="53dcf-120">Relationship</span></span> | <span data-ttu-id="53dcf-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="53dcf-121">Type</span></span>   |<span data-ttu-id="53dcf-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="53dcf-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="53dcf-123">criterios</span><span class="sxs-lookup"><span data-stu-id="53dcf-123">criteria</span></span>|[<span data-ttu-id="53dcf-124">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="53dcf-124">FilterCriteria</span></span>](filtercriteria.md)|<span data-ttu-id="53dcf-p102">Filtro aplicado actualmente en la columna especificada. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53dcf-p102">The currently applied filter on the given column. Read-only.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Filter resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
