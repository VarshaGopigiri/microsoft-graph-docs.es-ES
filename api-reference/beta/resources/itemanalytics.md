---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemAnalytics
localization_priority: Normal
ms.openlocfilehash: 03626b5dad041181558af076b5dc0ac05b684e13
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842416"
---
# <a name="itemanalytics-resource-type"></a><span data-ttu-id="79047-102">tipo de recurso itemAnalytics</span><span class="sxs-lookup"><span data-stu-id="79047-102">itemAnalytics resource type</span></span>

> <span data-ttu-id="79047-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="79047-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="79047-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="79047-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="79047-105">El recurso **itemAnalytics** proporciona análisis acerca de las actividades que tuvieron lugar en un elemento.</span><span class="sxs-lookup"><span data-stu-id="79047-105">The **itemAnalytics** resource provides analytics about activities that took place on an item.</span></span> <span data-ttu-id="79047-106">Actualmente, este recurso sólo está disponible en SharePoint y OneDrive para la empresa.</span><span class="sxs-lookup"><span data-stu-id="79047-106">This resource is currently only available on SharePoint and OneDrive for Business.</span></span>

<span data-ttu-id="79047-107">También puede usar la API [getActivitiesByInterval][] para recuperar análisis a través de un intervalo de tiempo personalizado o un intervalo.</span><span class="sxs-lookup"><span data-stu-id="79047-107">You can also use the [getActivitiesByInterval][] API to retrieve analytics over a custom time range or interval.</span></span>

><span data-ttu-id="79047-108">**Nota:** El recurso **itemAnalytics** aún no está disponible en todas las [implementaciones nacionales](/graph/deployments).</span><span class="sxs-lookup"><span data-stu-id="79047-108">**Note:** The **itemAnalytics** resource is not yet available in all [national deployments](/graph/deployments).</span></span>

## <a name="json-representation"></a><span data-ttu-id="79047-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="79047-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="79047-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79047-110">Properties</span></span>

| <span data-ttu-id="79047-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="79047-111">Property</span></span>      | <span data-ttu-id="79047-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="79047-112">Type</span></span>                 | <span data-ttu-id="79047-113">Description</span><span class="sxs-lookup"><span data-stu-id="79047-113">Description</span></span>
|:--------------|:---------------------|:--------------------------------------
| <span data-ttu-id="79047-114">allTime</span><span class="sxs-lookup"><span data-stu-id="79047-114">allTime</span></span>       | <span data-ttu-id="79047-115">[itemActivityStat][]</span><span class="sxs-lookup"><span data-stu-id="79047-115">[itemActivityStat][]</span></span> | <span data-ttu-id="79047-116">Análisis a través de la vida útil del elemento.</span><span class="sxs-lookup"><span data-stu-id="79047-116">Analytics over the the item's lifespan.</span></span>
| <span data-ttu-id="79047-117">lastSevenDays</span><span class="sxs-lookup"><span data-stu-id="79047-117">lastSevenDays</span></span> | <span data-ttu-id="79047-118">[itemActivityStat][]</span><span class="sxs-lookup"><span data-stu-id="79047-118">[itemActivityStat][]</span></span> | <span data-ttu-id="79047-119">Análisis de los últimos siete días.</span><span class="sxs-lookup"><span data-stu-id="79047-119">Analytics for the last seven days.</span></span>

[itemActivityStat]: itemactivitystat.md


[getActivitiesByInterval]: ../api/itemactivity-getbyinterval.md

<!-- {
  "type": "#page.annotation",
  "description": "The ItemAnalytics object provides analytics about activities that took place on an item.",
  "keywords": "activities,activity,action,analytics",
  "section": "documentation",
  "tocPath": "Resources/ItemAnalytics"
} -->
