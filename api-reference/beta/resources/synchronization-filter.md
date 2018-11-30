---
title: tipo de filtro de recurso
description: Determina qué objetos se deben aprovisionar a la aplicación. Por ejemplo, es posible que desee sólo los usuarios de aprovisionamiento que se encuentran en los Estados Unidos. Cuando un filtro de ámbito está presente, se omitirá los objetos que no cumplen con el filtro durante la sincronización.
ms.openlocfilehash: 72885cfbd49083ce80b96cd389286d5c50937ffb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086510"
---
# <a name="filter-resource-type"></a><span data-ttu-id="81826-105">tipo de filtro de recurso</span><span class="sxs-lookup"><span data-stu-id="81826-105">filter resource type</span></span>

> <span data-ttu-id="81826-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="81826-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="81826-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="81826-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="81826-108">Determina qué objetos se deben aprovisionar a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="81826-108">Determines which objects should be provisioned to the application.</span></span> <span data-ttu-id="81826-109">Por ejemplo, es posible que desee sólo los usuarios de aprovisionamiento que se encuentran en los Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="81826-109">For example, you might want to only provision users that are located in the US.</span></span> <span data-ttu-id="81826-110">Cuando un filtro de ámbito está presente, se omitirá los objetos que no cumplen con el filtro durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="81826-110">When a scoping filter is present, objects that do not satisfy the filter will be skipped during synchronization.</span></span>

<span data-ttu-id="81826-111">Filtro de forma parte de la [asignación de objetos](synchronization-objectmapping.md).</span><span class="sxs-lookup"><span data-stu-id="81826-111">Filter is part of [object mapping](synchronization-objectmapping.md).</span></span> <span data-ttu-id="81826-112">Consta de varios conjuntos de grupos de filtro, y cada grupo de filtro contiene una o más cláusulas.</span><span class="sxs-lookup"><span data-stu-id="81826-112">It consists of several sets of filter groups, and each filter group holds one or more clauses.</span></span> <span data-ttu-id="81826-113">Se considera como un objeto en el ámbito del grupo (el grupo se evalúa a `true`) sólo si todas las cláusulas del grupo se evalúan a `true`.</span><span class="sxs-lookup"><span data-stu-id="81826-113">An object is considered in scope for the group (the group is evaluated to `true`) only if all the clauses of the group are evaluated to `true`.</span></span>

<span data-ttu-id="81826-114">Se considera como un objeto en el ámbito para el conjunto de grupo (conjunto de grupos se evalúa a `true`) si cualquiera de los grupos en el conjunto se evalúa a `true`.</span><span class="sxs-lookup"><span data-stu-id="81826-114">An object is considered in scope for the group set (group set is evaluated to `true`) if any of the groups in the set is evaluated to `true`.</span></span>

<span data-ttu-id="81826-115">Para obtener más información, vea [aplicación basada en el atributo de aprovisionamiento con filtros de ámbito](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-saas-scoping-filters)</span><span class="sxs-lookup"><span data-stu-id="81826-115">For more information, see [Attribute-based application provisioning with scoping filters](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-saas-scoping-filters)</span></span>

## <a name="properties"></a><span data-ttu-id="81826-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81826-116">Properties</span></span>
| <span data-ttu-id="81826-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="81826-117">Property</span></span>     | <span data-ttu-id="81826-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="81826-118">Type</span></span>   |<span data-ttu-id="81826-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="81826-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="81826-120">categoryFilterGroups</span><span class="sxs-lookup"><span data-stu-id="81826-120">categoryFilterGroups</span></span>|<span data-ttu-id="81826-121">colección de [filterGroup](synchronization-filtergroup.md)</span><span class="sxs-lookup"><span data-stu-id="81826-121">[filterGroup](synchronization-filtergroup.md) collection</span></span>|<span data-ttu-id="81826-122">`*Experimental*`Filtrar conjunto de grupo que se usa para decidir si objeto dado pertenece y se debe procesar como parte de este objeto de asignación.</span><span class="sxs-lookup"><span data-stu-id="81826-122">`*Experimental*` Filter group set used to decide whether given object belongs and should be processed as part of this object mapping.</span></span> <span data-ttu-id="81826-123">Se considera como un objeto en el ámbito \*Si cualquiera de los grupos de la colección se evalúa a `true` \*.</span><span class="sxs-lookup"><span data-stu-id="81826-123">An object is considered in scope *if ANY of the groups in the collection is evaluated to `true`*.</span></span>|
|<span data-ttu-id="81826-124">grupos</span><span class="sxs-lookup"><span data-stu-id="81826-124">groups</span></span>|<span data-ttu-id="81826-125">colección de [filterGroup](synchronization-filtergroup.md)</span><span class="sxs-lookup"><span data-stu-id="81826-125">[filterGroup](synchronization-filtergroup.md) collection</span></span>|<span data-ttu-id="81826-126">Filtrar conjunto de grupo que se usa para decidir si el objeto dado es en el ámbito de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="81826-126">Filter group set used to decide whether given object is in scope for provisioning.</span></span> <span data-ttu-id="81826-127">**Éste es el filtro que debe usarse en la mayoría de los casos**.</span><span class="sxs-lookup"><span data-stu-id="81826-127">**This is the filter which should be used in most cases**.</span></span> <span data-ttu-id="81826-128">Si un objeto que se utiliza para satisfacer este filtro en un momento dado y, a continuación, el objeto o el filtro se ha cambiado por lo que el filtro no satisfecho, ya existe el objeto \* obtener aprovisionará desaprovisionamiento ".</span><span class="sxs-lookup"><span data-stu-id="81826-128">If an object used to satisfy this filter at a given moment, and then the object or the filter was changed so that filter is not satisfied any longer, such object \*will get de-provisioned".</span></span> <span data-ttu-id="81826-129">Se considera como un objeto en el ámbito \*Si cualquiera de los grupos de la colección se evalúa a `true` \*.</span><span class="sxs-lookup"><span data-stu-id="81826-129">An object is considered in scope *if ANY of the groups in the collection is evaluated to `true`*.</span></span>|
|<span data-ttu-id="81826-130">inputFilterGroups</span><span class="sxs-lookup"><span data-stu-id="81826-130">inputFilterGroups</span></span>|<span data-ttu-id="81826-131">colección de [filterGroup](synchronization-filtergroup.md)</span><span class="sxs-lookup"><span data-stu-id="81826-131">[filterGroup](synchronization-filtergroup.md) collection</span></span>|<span data-ttu-id="81826-132">`*Experimental*`Filtrar conjunto de grupo que se usa para filtrar objetos en la fase temprana de leerlos desde el directorio.</span><span class="sxs-lookup"><span data-stu-id="81826-132">`*Experimental*` Filter group set used to filter out objects at the early stage of reading them from the directory.</span></span> <span data-ttu-id="81826-133">Si un objeto no satisface este filtro no se procesarán aún más.</span><span class="sxs-lookup"><span data-stu-id="81826-133">If an object doesn't satisfy this filter it will not be processed further.</span></span> <span data-ttu-id="81826-134">Es importante comprender que, si utiliza un objeto para satisfacer este filtro en un momento dado y, a continuación, el objeto o el filtro se cambió lo ese filtro está ya no se cumple, por ejemplo, objeto *no obtener aprovisionará desaprovisionamiento*.</span><span class="sxs-lookup"><span data-stu-id="81826-134">Important to understand is that if an object used to satisfy this filter at a given moment, and then the object or the filter was changed so that filter is no longer satisfied, such object *will NOT get de-provisioned*.</span></span> <span data-ttu-id="81826-135">Se considera como un objeto en el ámbito \*Si cualquiera de los grupos de la colección se evalúa a `true` \*.</span><span class="sxs-lookup"><span data-stu-id="81826-135">An object is considered in scope *if ANY of the groups in the collection is evaluated to `true`*.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="81826-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="81826-136">JSON representation</span></span>

<span data-ttu-id="81826-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="81826-137">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.filter"
}-->

```json
{
  "categoryFilterGroups": [{"@odata.type": "microsoft.graph.filterGroup"}],
  "groups": [{"@odata.type": "microsoft.graph.filterGroup"}],
  "inputFilterGroups": [{"@odata.type": "microsoft.graph.filterGroup"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "filter resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->