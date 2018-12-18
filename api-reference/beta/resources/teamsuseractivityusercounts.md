---
title: tipo de recurso teamsUserActivityUserCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
ms.openlocfilehash: f4e10f1e34d4c6bdbed83279b98632c504630bc7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330460"
---
# <a name="teamsuseractivityusercounts-resource-type"></a><span data-ttu-id="42329-103">tipo de recurso teamsUserActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="42329-103">teamsUserActivityUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="42329-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42329-104">Properties</span></span>

| <span data-ttu-id="42329-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="42329-105">Property</span></span>            | <span data-ttu-id="42329-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="42329-106">Type</span></span>   |
| :------------------ | :----- |
| <span data-ttu-id="42329-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="42329-107">reportRefreshDate</span></span>   | <span data-ttu-id="42329-108">Date</span><span class="sxs-lookup"><span data-stu-id="42329-108">Date</span></span>   |
| <span data-ttu-id="42329-109">reportDate</span><span class="sxs-lookup"><span data-stu-id="42329-109">reportDate</span></span>          | <span data-ttu-id="42329-110">Date</span><span class="sxs-lookup"><span data-stu-id="42329-110">Date</span></span>   |
| <span data-ttu-id="42329-111">teamChatMessages</span><span class="sxs-lookup"><span data-stu-id="42329-111">teamChatMessages</span></span>    | <span data-ttu-id="42329-112">Int64</span><span class="sxs-lookup"><span data-stu-id="42329-112">Int64</span></span>  |
| <span data-ttu-id="42329-113">privateChatMessages</span><span class="sxs-lookup"><span data-stu-id="42329-113">privateChatMessages</span></span> | <span data-ttu-id="42329-114">Int64</span><span class="sxs-lookup"><span data-stu-id="42329-114">Int64</span></span>  |
| <span data-ttu-id="42329-115">llamadas</span><span class="sxs-lookup"><span data-stu-id="42329-115">calls</span></span>               | <span data-ttu-id="42329-116">Int64</span><span class="sxs-lookup"><span data-stu-id="42329-116">Int64</span></span>  |
| <span data-ttu-id="42329-117">reuniones</span><span class="sxs-lookup"><span data-stu-id="42329-117">meetings</span></span>            | <span data-ttu-id="42329-118">Int64</span><span class="sxs-lookup"><span data-stu-id="42329-118">Int64</span></span>  |
| <span data-ttu-id="42329-119">otherActions</span><span class="sxs-lookup"><span data-stu-id="42329-119">otherActions</span></span>        | <span data-ttu-id="42329-120">Int64</span><span class="sxs-lookup"><span data-stu-id="42329-120">Int64</span></span>  |
| <span data-ttu-id="42329-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="42329-121">reportPeriod</span></span>        | <span data-ttu-id="42329-122">String</span><span class="sxs-lookup"><span data-stu-id="42329-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="42329-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="42329-123">JSON representation</span></span>

<span data-ttu-id="42329-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="42329-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsUserActivityUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "teamChatMessages": 1024, 
  "privateChatMessages": 1024, 
  "calls": 1024, 
  "meetings": 1024, 
  "otherActions": 1024, 
  "reportPeriod": "String"
}
```
