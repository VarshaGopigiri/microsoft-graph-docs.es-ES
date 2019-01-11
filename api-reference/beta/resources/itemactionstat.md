---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemActionStat
localization_priority: Normal
ms.openlocfilehash: 1d2ab438e7aaf5b0a6aede99290394a9a4ea7f0e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879530"
---
# <a name="itemactionstat-resource-type"></a><span data-ttu-id="58a1a-102">tipo de recurso itemActionStat</span><span class="sxs-lookup"><span data-stu-id="58a1a-102">itemActionStat resource type</span></span>

> <span data-ttu-id="58a1a-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="58a1a-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="58a1a-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="58a1a-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="58a1a-105">El recurso **itemActionStat** proporciona agregados detalles sobre una acción durante un período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="58a1a-105">The **itemActionStat** resource provides aggregate details about an action over a period of time.</span></span>

## <a name="json-representation"></a><span data-ttu-id="58a1a-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="58a1a-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.itemActionStat",
}-->

```json
{
  "actionCount": 123,
  "actorCount": 60
}
```

## <a name="properties"></a><span data-ttu-id="58a1a-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="58a1a-107">Properties</span></span>

| <span data-ttu-id="58a1a-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="58a1a-108">Property</span></span>    | <span data-ttu-id="58a1a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="58a1a-109">Type</span></span>  | <span data-ttu-id="58a1a-110">Description</span><span class="sxs-lookup"><span data-stu-id="58a1a-110">Description</span></span>
|:------------|:------|:-------------------------------------------------------
| <span data-ttu-id="58a1a-111">CuentaAcción</span><span class="sxs-lookup"><span data-stu-id="58a1a-111">actionCount</span></span> | <span data-ttu-id="58a1a-112">Int32</span><span class="sxs-lookup"><span data-stu-id="58a1a-112">Int32</span></span> | <span data-ttu-id="58a1a-113">El número de veces que tuvo lugar la acción.</span><span class="sxs-lookup"><span data-stu-id="58a1a-113">The number of times the action took place.</span></span> <span data-ttu-id="58a1a-114">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="58a1a-114">Read-only.</span></span>
| <span data-ttu-id="58a1a-115">actorCount</span><span class="sxs-lookup"><span data-stu-id="58a1a-115">actorCount</span></span>  | <span data-ttu-id="58a1a-116">Int32</span><span class="sxs-lookup"><span data-stu-id="58a1a-116">Int32</span></span> | <span data-ttu-id="58a1a-117">El número de distintos actores que realizó la acción.</span><span class="sxs-lookup"><span data-stu-id="58a1a-117">The number of distinct actors that performed the action.</span></span> <span data-ttu-id="58a1a-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="58a1a-118">Read-only.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The ItemActionStat object provides aggregate details about an action over a period of time.",
  "keywords": "activities,activity,action,analytics",
  "section": "documentation",
  "tocPath": "Resources/ItemActionStat"
} -->
