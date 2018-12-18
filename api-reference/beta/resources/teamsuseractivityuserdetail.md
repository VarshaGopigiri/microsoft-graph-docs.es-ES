---
title: tipo de recurso teamsUserActivityUserDetail
description: La siguiente es una representación JSON del recurso.
author: nkramer
ms.openlocfilehash: a1f47bc52c2a0a613598ce663f16023dce208c51
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331944"
---
# <a name="teamsuseractivityuserdetail-resource-type"></a><span data-ttu-id="a8510-103">tipo de recurso teamsUserActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="a8510-103">teamsUserActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="a8510-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a8510-104">Properties</span></span>

| <span data-ttu-id="a8510-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a8510-105">Property</span></span>                | <span data-ttu-id="a8510-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8510-106">Type</span></span>              |
| :---------------------- | :---------------- |
| <span data-ttu-id="a8510-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="a8510-107">reportRefreshDate</span></span>       | <span data-ttu-id="a8510-108">Date</span><span class="sxs-lookup"><span data-stu-id="a8510-108">Date</span></span>              |
| <span data-ttu-id="a8510-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a8510-109">userPrincipalName</span></span>       | <span data-ttu-id="a8510-110">String</span><span class="sxs-lookup"><span data-stu-id="a8510-110">String</span></span>            |
| <span data-ttu-id="a8510-111">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="a8510-111">lastActivityDate</span></span>        | <span data-ttu-id="a8510-112">Date</span><span class="sxs-lookup"><span data-stu-id="a8510-112">Date</span></span>              |
| <span data-ttu-id="a8510-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="a8510-113">isDeleted</span></span>               | <span data-ttu-id="a8510-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="a8510-114">Boolean</span></span>           |
| <span data-ttu-id="a8510-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="a8510-115">deletedDate</span></span>             | <span data-ttu-id="a8510-116">Date</span><span class="sxs-lookup"><span data-stu-id="a8510-116">Date</span></span>              |
| <span data-ttu-id="a8510-117">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="a8510-117">assignedProducts</span></span>        | <span data-ttu-id="a8510-118">Colección String</span><span class="sxs-lookup"><span data-stu-id="a8510-118">String collection</span></span> |
| <span data-ttu-id="a8510-119">teamChatMessageCount</span><span class="sxs-lookup"><span data-stu-id="a8510-119">teamChatMessageCount</span></span>    | <span data-ttu-id="a8510-120">Int64</span><span class="sxs-lookup"><span data-stu-id="a8510-120">Int64</span></span>             |
| <span data-ttu-id="a8510-121">privateChatMessageCount</span><span class="sxs-lookup"><span data-stu-id="a8510-121">privateChatMessageCount</span></span> | <span data-ttu-id="a8510-122">Int64</span><span class="sxs-lookup"><span data-stu-id="a8510-122">Int64</span></span>             |
| <span data-ttu-id="a8510-123">callCount</span><span class="sxs-lookup"><span data-stu-id="a8510-123">callCount</span></span>               | <span data-ttu-id="a8510-124">Int64</span><span class="sxs-lookup"><span data-stu-id="a8510-124">Int64</span></span>             |
| <span data-ttu-id="a8510-125">meetingCount</span><span class="sxs-lookup"><span data-stu-id="a8510-125">meetingCount</span></span>            | <span data-ttu-id="a8510-126">Int64</span><span class="sxs-lookup"><span data-stu-id="a8510-126">Int64</span></span>             |
| <span data-ttu-id="a8510-127">hasOtherAction</span><span class="sxs-lookup"><span data-stu-id="a8510-127">hasOtherAction</span></span>          | <span data-ttu-id="a8510-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="a8510-128">Boolean</span></span>           |
| <span data-ttu-id="a8510-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="a8510-129">reportPeriod</span></span>            | <span data-ttu-id="a8510-130">String</span><span class="sxs-lookup"><span data-stu-id="a8510-130">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="a8510-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a8510-131">JSON representation</span></span>

<span data-ttu-id="a8510-132">La siguiente es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a8510-132">The following is a JSON representaion of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsUserActivityUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "lastActivityDate": "Date", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "assignedProducts": ["String"],
  "teamChatMessageCount": 1024, 
  "privateChatMessageCount": 1024, 
  "callCount": 1024, 
  "meetingCount": 1024, 
  "hasOtherAction": true, 
  "reportPeriod": "String"
}
```
