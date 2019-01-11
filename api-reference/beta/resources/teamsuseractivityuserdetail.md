---
title: tipo de recurso teamsUserActivityUserDetail
description: La siguiente es una representación JSON del recurso.
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 2e3f64c7065343712f6a9d9c6a114bf95f24c171
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823656"
---
# <a name="teamsuseractivityuserdetail-resource-type"></a><span data-ttu-id="4521f-103">tipo de recurso teamsUserActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="4521f-103">teamsUserActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="4521f-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4521f-104">Properties</span></span>

| <span data-ttu-id="4521f-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4521f-105">Property</span></span>                | <span data-ttu-id="4521f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4521f-106">Type</span></span>              |
| :---------------------- | :---------------- |
| <span data-ttu-id="4521f-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="4521f-107">reportRefreshDate</span></span>       | <span data-ttu-id="4521f-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="4521f-108">Date</span></span>              |
| <span data-ttu-id="4521f-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4521f-109">userPrincipalName</span></span>       | <span data-ttu-id="4521f-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="4521f-110">String</span></span>            |
| <span data-ttu-id="4521f-111">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="4521f-111">lastActivityDate</span></span>        | <span data-ttu-id="4521f-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="4521f-112">Date</span></span>              |
| <span data-ttu-id="4521f-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="4521f-113">isDeleted</span></span>               | <span data-ttu-id="4521f-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="4521f-114">Boolean</span></span>           |
| <span data-ttu-id="4521f-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="4521f-115">deletedDate</span></span>             | <span data-ttu-id="4521f-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="4521f-116">Date</span></span>              |
| <span data-ttu-id="4521f-117">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="4521f-117">assignedProducts</span></span>        | <span data-ttu-id="4521f-118">Colección String</span><span class="sxs-lookup"><span data-stu-id="4521f-118">String collection</span></span> |
| <span data-ttu-id="4521f-119">teamChatMessageCount</span><span class="sxs-lookup"><span data-stu-id="4521f-119">teamChatMessageCount</span></span>    | <span data-ttu-id="4521f-120">Int64</span><span class="sxs-lookup"><span data-stu-id="4521f-120">Int64</span></span>             |
| <span data-ttu-id="4521f-121">privateChatMessageCount</span><span class="sxs-lookup"><span data-stu-id="4521f-121">privateChatMessageCount</span></span> | <span data-ttu-id="4521f-122">Int64</span><span class="sxs-lookup"><span data-stu-id="4521f-122">Int64</span></span>             |
| <span data-ttu-id="4521f-123">callCount</span><span class="sxs-lookup"><span data-stu-id="4521f-123">callCount</span></span>               | <span data-ttu-id="4521f-124">Int64</span><span class="sxs-lookup"><span data-stu-id="4521f-124">Int64</span></span>             |
| <span data-ttu-id="4521f-125">meetingCount</span><span class="sxs-lookup"><span data-stu-id="4521f-125">meetingCount</span></span>            | <span data-ttu-id="4521f-126">Int64</span><span class="sxs-lookup"><span data-stu-id="4521f-126">Int64</span></span>             |
| <span data-ttu-id="4521f-127">hasOtherAction</span><span class="sxs-lookup"><span data-stu-id="4521f-127">hasOtherAction</span></span>          | <span data-ttu-id="4521f-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="4521f-128">Boolean</span></span>           |
| <span data-ttu-id="4521f-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="4521f-129">reportPeriod</span></span>            | <span data-ttu-id="4521f-130">String</span><span class="sxs-lookup"><span data-stu-id="4521f-130">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="4521f-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4521f-131">JSON representation</span></span>

<span data-ttu-id="4521f-132">La siguiente es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4521f-132">The following is a JSON representaion of the resource.</span></span>

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
