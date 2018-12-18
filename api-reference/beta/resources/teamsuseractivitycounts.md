---
title: tipo de recurso teamsUserActivityCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
ms.openlocfilehash: f67540f4172993b1076d9590438262b0d4da1846
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334520"
---
# <a name="teamsuseractivitycounts-resource-type"></a><span data-ttu-id="e0423-103">tipo de recurso teamsUserActivityCounts</span><span class="sxs-lookup"><span data-stu-id="e0423-103">teamsUserActivityCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="e0423-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e0423-104">Properties</span></span>

| <span data-ttu-id="e0423-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e0423-105">Property</span></span>            | <span data-ttu-id="e0423-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0423-106">Type</span></span>   |
| :------------------ | :----- |
| <span data-ttu-id="e0423-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="e0423-107">reportRefreshDate</span></span>   | <span data-ttu-id="e0423-108">Date</span><span class="sxs-lookup"><span data-stu-id="e0423-108">Date</span></span>   |
| <span data-ttu-id="e0423-109">reportDate</span><span class="sxs-lookup"><span data-stu-id="e0423-109">reportDate</span></span>          | <span data-ttu-id="e0423-110">Date</span><span class="sxs-lookup"><span data-stu-id="e0423-110">Date</span></span>   |
| <span data-ttu-id="e0423-111">teamChatMessages</span><span class="sxs-lookup"><span data-stu-id="e0423-111">teamChatMessages</span></span>    | <span data-ttu-id="e0423-112">Int64</span><span class="sxs-lookup"><span data-stu-id="e0423-112">Int64</span></span>  |
| <span data-ttu-id="e0423-113">privateChatMessages</span><span class="sxs-lookup"><span data-stu-id="e0423-113">privateChatMessages</span></span> | <span data-ttu-id="e0423-114">Int64</span><span class="sxs-lookup"><span data-stu-id="e0423-114">Int64</span></span>  |
| <span data-ttu-id="e0423-115">llamadas</span><span class="sxs-lookup"><span data-stu-id="e0423-115">calls</span></span>               | <span data-ttu-id="e0423-116">Int64</span><span class="sxs-lookup"><span data-stu-id="e0423-116">Int64</span></span>  |
| <span data-ttu-id="e0423-117">reuniones</span><span class="sxs-lookup"><span data-stu-id="e0423-117">meetings</span></span>            | <span data-ttu-id="e0423-118">Int64</span><span class="sxs-lookup"><span data-stu-id="e0423-118">Int64</span></span>  |
| <span data-ttu-id="e0423-119">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="e0423-119">reportPeriod</span></span>        | <span data-ttu-id="e0423-120">String</span><span class="sxs-lookup"><span data-stu-id="e0423-120">String</span></span> |


## <a name="json-representation"></a><span data-ttu-id="e0423-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e0423-121">JSON representation</span></span>

<span data-ttu-id="e0423-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e0423-122">The following is a JSON representation of the resource.</span></span>

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
