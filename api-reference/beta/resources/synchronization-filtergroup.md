---
title: tipo de recurso filterGroup
description: Define un conjunto de cláusulas que debe cumplir un objeto que deben considerarse en ámbito. Se considera como un objeto en el ámbito del grupo (el grupo se evalúa a `true`) sólo si todas las cláusulas del grupo se evalúan a `true`.
localization_priority: Normal
ms.openlocfilehash: 174c02518069e949c49887d9e21e778e8455509a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836116"
---
# <a name="filtergroup-resource-type"></a><span data-ttu-id="8421d-104">tipo de recurso filterGroup</span><span class="sxs-lookup"><span data-stu-id="8421d-104">filterGroup resource type</span></span>

> <span data-ttu-id="8421d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8421d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8421d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8421d-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8421d-107">Define un conjunto de cláusulas que debe cumplir un objeto que deben considerarse en ámbito.</span><span class="sxs-lookup"><span data-stu-id="8421d-107">Defines a set of clauses that an object must satisfy to be considered in scope.</span></span> <span data-ttu-id="8421d-108">Se considera como un objeto en el ámbito del grupo (el grupo se evalúa a `true`) sólo si todas las cláusulas del grupo se evalúan a `true`.</span><span class="sxs-lookup"><span data-stu-id="8421d-108">An object is considered in scope for the group (the group is evaluated to `true`) only if all the clauses of the group are evaluated to `true`.</span></span>

## <a name="properties"></a><span data-ttu-id="8421d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8421d-109">Properties</span></span>
| <span data-ttu-id="8421d-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8421d-110">Property</span></span>     | <span data-ttu-id="8421d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="8421d-111">Type</span></span>   |<span data-ttu-id="8421d-112">Description</span><span class="sxs-lookup"><span data-stu-id="8421d-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8421d-113">cláusulas</span><span class="sxs-lookup"><span data-stu-id="8421d-113">clauses</span></span>|<span data-ttu-id="8421d-114">colección [filterClause](synchronization-filterclause.md)</span><span class="sxs-lookup"><span data-stu-id="8421d-114">[filterClause](synchronization-filterclause.md) collection</span></span>|<span data-ttu-id="8421d-115">Filtrar cláusulas (condiciones) de este grupo.</span><span class="sxs-lookup"><span data-stu-id="8421d-115">Filter clauses (conditions) of this group.</span></span> <span data-ttu-id="8421d-116">Deben cumplirse todas las cláusulas de un grupo en orden para el grupo de filtro evaluar a `true`.</span><span class="sxs-lookup"><span data-stu-id="8421d-116">All clauses in a group must be satisfied in order for the filter group to evaluate to `true`.</span></span>|
|<span data-ttu-id="8421d-117">name</span><span class="sxs-lookup"><span data-stu-id="8421d-117">name</span></span>|<span data-ttu-id="8421d-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="8421d-118">String</span></span>|<span data-ttu-id="8421d-119">Nombre legible del grupo de filtro.</span><span class="sxs-lookup"><span data-stu-id="8421d-119">Human-readable name of the filter group.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8421d-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8421d-120">JSON representation</span></span>

<span data-ttu-id="8421d-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8421d-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.filterGroup"
}-->

```json
{
  "clauses": [{"@odata.type": "microsoft.graph.filterClause"}],
  "name": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "filterGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
