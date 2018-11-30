---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemAnalytics
ms.openlocfilehash: b50df7d1fdf67cffd508c3b5891d07c599521c8a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085489"
---
# <a name="itemanalytics-resource-type"></a><span data-ttu-id="3f2e4-102">tipo de recurso itemAnalytics</span><span class="sxs-lookup"><span data-stu-id="3f2e4-102">itemAnalytics resource type</span></span>

> <span data-ttu-id="3f2e4-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3f2e4-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3f2e4-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3f2e4-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3f2e4-105">El recurso **itemAnalytics** proporciona análisis acerca de las actividades que tuvieron lugar en un elemento.</span><span class="sxs-lookup"><span data-stu-id="3f2e4-105">The **itemAnalytics** resource provides analytics about activities that took place on an item.</span></span> <span data-ttu-id="3f2e4-106">Actualmente, este recurso sólo está disponible en SharePoint y OneDrive para la empresa.</span><span class="sxs-lookup"><span data-stu-id="3f2e4-106">This resource is currently only available on SharePoint and OneDrive for Business.</span></span>

<span data-ttu-id="3f2e4-107">También puede usar la API [getActivitiesByInterval][] para recuperar análisis a través de un intervalo de tiempo personalizado o un intervalo.</span><span class="sxs-lookup"><span data-stu-id="3f2e4-107">You can also use the [getActivitiesByInterval][] API to retrieve analytics over a custom time range or interval.</span></span>

><span data-ttu-id="3f2e4-108">**Nota:** El recurso **itemAnalytics** aún no está disponible en todas las [implementaciones nacionales](/graph/deployments).</span><span class="sxs-lookup"><span data-stu-id="3f2e4-108">**Note:** The **itemAnalytics** resource is not yet available in all [national deployments](/graph/deployments).</span></span>

## <a name="json-representation"></a><span data-ttu-id="3f2e4-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3f2e4-109">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.itemAnalytics",
  "@type.aka": "oneDrive.analytics"
}-->

```json
{
  "allTime": {"@odata.type": "microsoft.graph.itemActivityStat"},
  "lastSevenDays": {"@odata.type": "microsoft.graph.itemActivityStat"}
}
```

## <a name="properties"></a><span data-ttu-id="3f2e4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3f2e4-110">Properties</span></span>

| <span data-ttu-id="3f2e4-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3f2e4-111">Property</span></span>      | <span data-ttu-id="3f2e4-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f2e4-112">Type</span></span>                 | <span data-ttu-id="3f2e4-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f2e4-113">Description</span></span>
|:--------------|:---------------------|:--------------------------------------
| <span data-ttu-id="3f2e4-114">allTime</span><span class="sxs-lookup"><span data-stu-id="3f2e4-114">allTime</span></span>       | <span data-ttu-id="3f2e4-115">[itemActivityStat][]</span><span class="sxs-lookup"><span data-stu-id="3f2e4-115">[itemActivityStat][]</span></span> | <span data-ttu-id="3f2e4-116">Análisis a través de la vida útil del elemento.</span><span class="sxs-lookup"><span data-stu-id="3f2e4-116">Analytics over the the item's lifespan.</span></span>
| <span data-ttu-id="3f2e4-117">lastSevenDays</span><span class="sxs-lookup"><span data-stu-id="3f2e4-117">lastSevenDays</span></span> | <span data-ttu-id="3f2e4-118">[itemActivityStat][]</span><span class="sxs-lookup"><span data-stu-id="3f2e4-118">[itemActivityStat][]</span></span> | <span data-ttu-id="3f2e4-119">Análisis de los últimos siete días.</span><span class="sxs-lookup"><span data-stu-id="3f2e4-119">Analytics for the last seven days.</span></span>

[itemActivityStat]: itemactivitystat.md


[getActivitiesByInterval]: ../api/itemactivity-getbyinterval.md

<!-- {
  "type": "#page.annotation",
  "description": "The ItemAnalytics object provides analytics about activities that took place on an item.",
  "keywords": "activities,activity,action,analytics",
  "section": "documentation",
  "tocPath": "Resources/ItemAnalytics"
} -->
