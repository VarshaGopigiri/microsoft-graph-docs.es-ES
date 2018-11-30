---
title: tipo de recurso teamsUserActivityUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: f6478175252e99af2bfe5561d29eebe75b638eb2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084097"
---
# <a name="teamsuseractivityusercounts-resource-type"></a><span data-ttu-id="4abc1-103">tipo de recurso teamsUserActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="4abc1-103">teamsUserActivityUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="4abc1-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4abc1-104">Properties</span></span>

| <span data-ttu-id="4abc1-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4abc1-105">Property</span></span>            | <span data-ttu-id="4abc1-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4abc1-106">Type</span></span>   |
| :------------------ | :----- |
| <span data-ttu-id="4abc1-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="4abc1-107">reportRefreshDate</span></span>   | <span data-ttu-id="4abc1-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="4abc1-108">Date</span></span>   |
| <span data-ttu-id="4abc1-109">reportDate</span><span class="sxs-lookup"><span data-stu-id="4abc1-109">reportDate</span></span>          | <span data-ttu-id="4abc1-110">Fecha</span><span class="sxs-lookup"><span data-stu-id="4abc1-110">Date</span></span>   |
| <span data-ttu-id="4abc1-111">teamChatMessages</span><span class="sxs-lookup"><span data-stu-id="4abc1-111">teamChatMessages</span></span>    | <span data-ttu-id="4abc1-112">Int64</span><span class="sxs-lookup"><span data-stu-id="4abc1-112">Int64</span></span>  |
| <span data-ttu-id="4abc1-113">privateChatMessages</span><span class="sxs-lookup"><span data-stu-id="4abc1-113">privateChatMessages</span></span> | <span data-ttu-id="4abc1-114">Int64</span><span class="sxs-lookup"><span data-stu-id="4abc1-114">Int64</span></span>  |
| <span data-ttu-id="4abc1-115">llamadas</span><span class="sxs-lookup"><span data-stu-id="4abc1-115">calls</span></span>               | <span data-ttu-id="4abc1-116">Int64</span><span class="sxs-lookup"><span data-stu-id="4abc1-116">Int64</span></span>  |
| <span data-ttu-id="4abc1-117">reuniones</span><span class="sxs-lookup"><span data-stu-id="4abc1-117">meetings</span></span>            | <span data-ttu-id="4abc1-118">Int64</span><span class="sxs-lookup"><span data-stu-id="4abc1-118">Int64</span></span>  |
| <span data-ttu-id="4abc1-119">otherActions</span><span class="sxs-lookup"><span data-stu-id="4abc1-119">otherActions</span></span>        | <span data-ttu-id="4abc1-120">Int64</span><span class="sxs-lookup"><span data-stu-id="4abc1-120">Int64</span></span>  |
| <span data-ttu-id="4abc1-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="4abc1-121">reportPeriod</span></span>        | <span data-ttu-id="4abc1-122">String</span><span class="sxs-lookup"><span data-stu-id="4abc1-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="4abc1-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4abc1-123">JSON representation</span></span>

<span data-ttu-id="4abc1-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4abc1-124">The following is a JSON representation of the resource.</span></span>

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
