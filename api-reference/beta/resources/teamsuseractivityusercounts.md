---
title: tipo de recurso teamsUserActivityUserCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: bcb69c09d621ce3cce006fd9130afa0a70e4cdb8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912823"
---
# <a name="teamsuseractivityusercounts-resource-type"></a><span data-ttu-id="6ffa2-103">tipo de recurso teamsUserActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="6ffa2-103">teamsUserActivityUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="6ffa2-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ffa2-104">Properties</span></span>

| <span data-ttu-id="6ffa2-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6ffa2-105">Property</span></span>            | <span data-ttu-id="6ffa2-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ffa2-106">Type</span></span>   |
| :------------------ | :----- |
| <span data-ttu-id="6ffa2-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="6ffa2-107">reportRefreshDate</span></span>   | <span data-ttu-id="6ffa2-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="6ffa2-108">Date</span></span>   |
| <span data-ttu-id="6ffa2-109">reportDate</span><span class="sxs-lookup"><span data-stu-id="6ffa2-109">reportDate</span></span>          | <span data-ttu-id="6ffa2-110">Fecha</span><span class="sxs-lookup"><span data-stu-id="6ffa2-110">Date</span></span>   |
| <span data-ttu-id="6ffa2-111">teamChatMessages</span><span class="sxs-lookup"><span data-stu-id="6ffa2-111">teamChatMessages</span></span>    | <span data-ttu-id="6ffa2-112">Int64</span><span class="sxs-lookup"><span data-stu-id="6ffa2-112">Int64</span></span>  |
| <span data-ttu-id="6ffa2-113">privateChatMessages</span><span class="sxs-lookup"><span data-stu-id="6ffa2-113">privateChatMessages</span></span> | <span data-ttu-id="6ffa2-114">Int64</span><span class="sxs-lookup"><span data-stu-id="6ffa2-114">Int64</span></span>  |
| <span data-ttu-id="6ffa2-115">llamadas</span><span class="sxs-lookup"><span data-stu-id="6ffa2-115">calls</span></span>               | <span data-ttu-id="6ffa2-116">Int64</span><span class="sxs-lookup"><span data-stu-id="6ffa2-116">Int64</span></span>  |
| <span data-ttu-id="6ffa2-117">reuniones</span><span class="sxs-lookup"><span data-stu-id="6ffa2-117">meetings</span></span>            | <span data-ttu-id="6ffa2-118">Int64</span><span class="sxs-lookup"><span data-stu-id="6ffa2-118">Int64</span></span>  |
| <span data-ttu-id="6ffa2-119">otherActions</span><span class="sxs-lookup"><span data-stu-id="6ffa2-119">otherActions</span></span>        | <span data-ttu-id="6ffa2-120">Int64</span><span class="sxs-lookup"><span data-stu-id="6ffa2-120">Int64</span></span>  |
| <span data-ttu-id="6ffa2-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="6ffa2-121">reportPeriod</span></span>        | <span data-ttu-id="6ffa2-122">String</span><span class="sxs-lookup"><span data-stu-id="6ffa2-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="6ffa2-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6ffa2-123">JSON representation</span></span>

<span data-ttu-id="6ffa2-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6ffa2-124">The following is a JSON representation of the resource.</span></span>

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
