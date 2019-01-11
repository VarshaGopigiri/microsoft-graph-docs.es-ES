---
title: tipo de recurso teamsUserActivityCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
localization_priority: Normal
ms.openlocfilehash: c7351795f6b3dafbac996844fc1ac11cd24bbc03
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886593"
---
# <a name="teamsuseractivitycounts-resource-type"></a><span data-ttu-id="19f66-103">tipo de recurso teamsUserActivityCounts</span><span class="sxs-lookup"><span data-stu-id="19f66-103">teamsUserActivityCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="19f66-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19f66-104">Properties</span></span>

| <span data-ttu-id="19f66-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="19f66-105">Property</span></span>            | <span data-ttu-id="19f66-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="19f66-106">Type</span></span>   |
| :------------------ | :----- |
| <span data-ttu-id="19f66-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="19f66-107">reportRefreshDate</span></span>   | <span data-ttu-id="19f66-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="19f66-108">Date</span></span>   |
| <span data-ttu-id="19f66-109">reportDate</span><span class="sxs-lookup"><span data-stu-id="19f66-109">reportDate</span></span>          | <span data-ttu-id="19f66-110">Fecha</span><span class="sxs-lookup"><span data-stu-id="19f66-110">Date</span></span>   |
| <span data-ttu-id="19f66-111">teamChatMessages</span><span class="sxs-lookup"><span data-stu-id="19f66-111">teamChatMessages</span></span>    | <span data-ttu-id="19f66-112">Int64</span><span class="sxs-lookup"><span data-stu-id="19f66-112">Int64</span></span>  |
| <span data-ttu-id="19f66-113">privateChatMessages</span><span class="sxs-lookup"><span data-stu-id="19f66-113">privateChatMessages</span></span> | <span data-ttu-id="19f66-114">Int64</span><span class="sxs-lookup"><span data-stu-id="19f66-114">Int64</span></span>  |
| <span data-ttu-id="19f66-115">llamadas</span><span class="sxs-lookup"><span data-stu-id="19f66-115">calls</span></span>               | <span data-ttu-id="19f66-116">Int64</span><span class="sxs-lookup"><span data-stu-id="19f66-116">Int64</span></span>  |
| <span data-ttu-id="19f66-117">reuniones</span><span class="sxs-lookup"><span data-stu-id="19f66-117">meetings</span></span>            | <span data-ttu-id="19f66-118">Int64</span><span class="sxs-lookup"><span data-stu-id="19f66-118">Int64</span></span>  |
| <span data-ttu-id="19f66-119">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="19f66-119">reportPeriod</span></span>        | <span data-ttu-id="19f66-120">String</span><span class="sxs-lookup"><span data-stu-id="19f66-120">String</span></span> |


## <a name="json-representation"></a><span data-ttu-id="19f66-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="19f66-121">JSON representation</span></span>

<span data-ttu-id="19f66-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="19f66-122">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsUserActivityCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "teamChatMessages": 1024, 
  "privateChatMessages": 1024, 
  "calls": 1024, 
  "meetings": 1024, 
  "reportPeriod": "String"
}
```
