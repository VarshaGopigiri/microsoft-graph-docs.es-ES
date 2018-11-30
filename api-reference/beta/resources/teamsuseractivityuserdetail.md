---
title: tipo de recurso teamsUserActivityUserDetail
description: La siguiente es una representación JSON del recurso.
ms.openlocfilehash: 4e40ea4adf07450e6b51555df47579955a2a0286
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089813"
---
# <a name="teamsuseractivityuserdetail-resource-type"></a><span data-ttu-id="7eea1-103">tipo de recurso teamsUserActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="7eea1-103">teamsUserActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="7eea1-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7eea1-104">Properties</span></span>

| <span data-ttu-id="7eea1-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7eea1-105">Property</span></span>                | <span data-ttu-id="7eea1-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="7eea1-106">Type</span></span>              |
| :---------------------- | :---------------- |
| <span data-ttu-id="7eea1-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="7eea1-107">reportRefreshDate</span></span>       | <span data-ttu-id="7eea1-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="7eea1-108">Date</span></span>              |
| <span data-ttu-id="7eea1-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7eea1-109">userPrincipalName</span></span>       | <span data-ttu-id="7eea1-110">String</span><span class="sxs-lookup"><span data-stu-id="7eea1-110">String</span></span>            |
| <span data-ttu-id="7eea1-111">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="7eea1-111">lastActivityDate</span></span>        | <span data-ttu-id="7eea1-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="7eea1-112">Date</span></span>              |
| <span data-ttu-id="7eea1-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="7eea1-113">isDeleted</span></span>               | <span data-ttu-id="7eea1-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="7eea1-114">Boolean</span></span>           |
| <span data-ttu-id="7eea1-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="7eea1-115">deletedDate</span></span>             | <span data-ttu-id="7eea1-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="7eea1-116">Date</span></span>              |
| <span data-ttu-id="7eea1-117">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="7eea1-117">assignedProducts</span></span>        | <span data-ttu-id="7eea1-118">Colección String</span><span class="sxs-lookup"><span data-stu-id="7eea1-118">String collection</span></span> |
| <span data-ttu-id="7eea1-119">teamChatMessageCount</span><span class="sxs-lookup"><span data-stu-id="7eea1-119">teamChatMessageCount</span></span>    | <span data-ttu-id="7eea1-120">Int64</span><span class="sxs-lookup"><span data-stu-id="7eea1-120">Int64</span></span>             |
| <span data-ttu-id="7eea1-121">privateChatMessageCount</span><span class="sxs-lookup"><span data-stu-id="7eea1-121">privateChatMessageCount</span></span> | <span data-ttu-id="7eea1-122">Int64</span><span class="sxs-lookup"><span data-stu-id="7eea1-122">Int64</span></span>             |
| <span data-ttu-id="7eea1-123">callCount</span><span class="sxs-lookup"><span data-stu-id="7eea1-123">callCount</span></span>               | <span data-ttu-id="7eea1-124">Int64</span><span class="sxs-lookup"><span data-stu-id="7eea1-124">Int64</span></span>             |
| <span data-ttu-id="7eea1-125">meetingCount</span><span class="sxs-lookup"><span data-stu-id="7eea1-125">meetingCount</span></span>            | <span data-ttu-id="7eea1-126">Int64</span><span class="sxs-lookup"><span data-stu-id="7eea1-126">Int64</span></span>             |
| <span data-ttu-id="7eea1-127">hasOtherAction</span><span class="sxs-lookup"><span data-stu-id="7eea1-127">hasOtherAction</span></span>          | <span data-ttu-id="7eea1-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="7eea1-128">Boolean</span></span>           |
| <span data-ttu-id="7eea1-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="7eea1-129">reportPeriod</span></span>            | <span data-ttu-id="7eea1-130">String</span><span class="sxs-lookup"><span data-stu-id="7eea1-130">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="7eea1-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7eea1-131">JSON representation</span></span>

<span data-ttu-id="7eea1-132">La siguiente es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7eea1-132">The following is a JSON representaion of the resource.</span></span>

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
