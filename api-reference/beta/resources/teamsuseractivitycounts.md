---
title: tipo de recurso teamsUserActivityCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 39e90b4c9dc6b9929959139ba67ddb090d143e38
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089801"
---
# <a name="teamsuseractivitycounts-resource-type"></a><span data-ttu-id="fce0c-103">tipo de recurso teamsUserActivityCounts</span><span class="sxs-lookup"><span data-stu-id="fce0c-103">teamsUserActivityCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="fce0c-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fce0c-104">Properties</span></span>

| <span data-ttu-id="fce0c-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fce0c-105">Property</span></span>            | <span data-ttu-id="fce0c-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="fce0c-106">Type</span></span>   |
| :------------------ | :----- |
| <span data-ttu-id="fce0c-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="fce0c-107">reportRefreshDate</span></span>   | <span data-ttu-id="fce0c-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="fce0c-108">Date</span></span>   |
| <span data-ttu-id="fce0c-109">reportDate</span><span class="sxs-lookup"><span data-stu-id="fce0c-109">reportDate</span></span>          | <span data-ttu-id="fce0c-110">Fecha</span><span class="sxs-lookup"><span data-stu-id="fce0c-110">Date</span></span>   |
| <span data-ttu-id="fce0c-111">teamChatMessages</span><span class="sxs-lookup"><span data-stu-id="fce0c-111">teamChatMessages</span></span>    | <span data-ttu-id="fce0c-112">Int64</span><span class="sxs-lookup"><span data-stu-id="fce0c-112">Int64</span></span>  |
| <span data-ttu-id="fce0c-113">privateChatMessages</span><span class="sxs-lookup"><span data-stu-id="fce0c-113">privateChatMessages</span></span> | <span data-ttu-id="fce0c-114">Int64</span><span class="sxs-lookup"><span data-stu-id="fce0c-114">Int64</span></span>  |
| <span data-ttu-id="fce0c-115">llamadas</span><span class="sxs-lookup"><span data-stu-id="fce0c-115">calls</span></span>               | <span data-ttu-id="fce0c-116">Int64</span><span class="sxs-lookup"><span data-stu-id="fce0c-116">Int64</span></span>  |
| <span data-ttu-id="fce0c-117">reuniones</span><span class="sxs-lookup"><span data-stu-id="fce0c-117">meetings</span></span>            | <span data-ttu-id="fce0c-118">Int64</span><span class="sxs-lookup"><span data-stu-id="fce0c-118">Int64</span></span>  |
| <span data-ttu-id="fce0c-119">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="fce0c-119">reportPeriod</span></span>        | <span data-ttu-id="fce0c-120">String</span><span class="sxs-lookup"><span data-stu-id="fce0c-120">String</span></span> |


## <a name="json-representation"></a><span data-ttu-id="fce0c-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fce0c-121">JSON representation</span></span>

<span data-ttu-id="fce0c-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fce0c-122">The following is a JSON representation of the resource.</span></span>

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
