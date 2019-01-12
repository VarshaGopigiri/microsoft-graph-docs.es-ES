---
title: tipo de recurso teamsUserActivityCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: bcc0e9d1ed5c93c3d9f4ba97165d0413025a89cd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987527"
---
# <a name="teamsuseractivitycounts-resource-type"></a><span data-ttu-id="241d1-103">tipo de recurso teamsUserActivityCounts</span><span class="sxs-lookup"><span data-stu-id="241d1-103">teamsUserActivityCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="241d1-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="241d1-104">Properties</span></span>

| <span data-ttu-id="241d1-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="241d1-105">Property</span></span>            | <span data-ttu-id="241d1-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="241d1-106">Type</span></span>   |
| :------------------ | :----- |
| <span data-ttu-id="241d1-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="241d1-107">reportRefreshDate</span></span>   | <span data-ttu-id="241d1-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="241d1-108">Date</span></span>   |
| <span data-ttu-id="241d1-109">reportDate</span><span class="sxs-lookup"><span data-stu-id="241d1-109">reportDate</span></span>          | <span data-ttu-id="241d1-110">Fecha</span><span class="sxs-lookup"><span data-stu-id="241d1-110">Date</span></span>   |
| <span data-ttu-id="241d1-111">teamChatMessages</span><span class="sxs-lookup"><span data-stu-id="241d1-111">teamChatMessages</span></span>    | <span data-ttu-id="241d1-112">Int64</span><span class="sxs-lookup"><span data-stu-id="241d1-112">Int64</span></span>  |
| <span data-ttu-id="241d1-113">privateChatMessages</span><span class="sxs-lookup"><span data-stu-id="241d1-113">privateChatMessages</span></span> | <span data-ttu-id="241d1-114">Int64</span><span class="sxs-lookup"><span data-stu-id="241d1-114">Int64</span></span>  |
| <span data-ttu-id="241d1-115">llamadas</span><span class="sxs-lookup"><span data-stu-id="241d1-115">calls</span></span>               | <span data-ttu-id="241d1-116">Int64</span><span class="sxs-lookup"><span data-stu-id="241d1-116">Int64</span></span>  |
| <span data-ttu-id="241d1-117">reuniones</span><span class="sxs-lookup"><span data-stu-id="241d1-117">meetings</span></span>            | <span data-ttu-id="241d1-118">Int64</span><span class="sxs-lookup"><span data-stu-id="241d1-118">Int64</span></span>  |
| <span data-ttu-id="241d1-119">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="241d1-119">reportPeriod</span></span>        | <span data-ttu-id="241d1-120">String</span><span class="sxs-lookup"><span data-stu-id="241d1-120">String</span></span> |


## <a name="json-representation"></a><span data-ttu-id="241d1-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="241d1-121">JSON representation</span></span>

<span data-ttu-id="241d1-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="241d1-122">The following is a JSON representation of the resource.</span></span>

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
