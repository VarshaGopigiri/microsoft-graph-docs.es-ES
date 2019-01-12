---
title: tipo de recurso teamsUserActivityUserDetail
description: La siguiente es una representación JSON del recurso.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 32b611ee9ec01b0339389256b8c8dff9eac99fa9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27913432"
---
# <a name="teamsuseractivityuserdetail-resource-type"></a><span data-ttu-id="51428-103">tipo de recurso teamsUserActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="51428-103">teamsUserActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="51428-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51428-104">Properties</span></span>

| <span data-ttu-id="51428-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51428-105">Property</span></span>                | <span data-ttu-id="51428-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="51428-106">Type</span></span>              |
| :---------------------- | :---------------- |
| <span data-ttu-id="51428-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="51428-107">reportRefreshDate</span></span>       | <span data-ttu-id="51428-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="51428-108">Date</span></span>              |
| <span data-ttu-id="51428-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="51428-109">userPrincipalName</span></span>       | <span data-ttu-id="51428-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="51428-110">String</span></span>            |
| <span data-ttu-id="51428-111">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="51428-111">lastActivityDate</span></span>        | <span data-ttu-id="51428-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="51428-112">Date</span></span>              |
| <span data-ttu-id="51428-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="51428-113">isDeleted</span></span>               | <span data-ttu-id="51428-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="51428-114">Boolean</span></span>           |
| <span data-ttu-id="51428-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="51428-115">deletedDate</span></span>             | <span data-ttu-id="51428-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="51428-116">Date</span></span>              |
| <span data-ttu-id="51428-117">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="51428-117">assignedProducts</span></span>        | <span data-ttu-id="51428-118">Colección String</span><span class="sxs-lookup"><span data-stu-id="51428-118">String collection</span></span> |
| <span data-ttu-id="51428-119">teamChatMessageCount</span><span class="sxs-lookup"><span data-stu-id="51428-119">teamChatMessageCount</span></span>    | <span data-ttu-id="51428-120">Int64</span><span class="sxs-lookup"><span data-stu-id="51428-120">Int64</span></span>             |
| <span data-ttu-id="51428-121">privateChatMessageCount</span><span class="sxs-lookup"><span data-stu-id="51428-121">privateChatMessageCount</span></span> | <span data-ttu-id="51428-122">Int64</span><span class="sxs-lookup"><span data-stu-id="51428-122">Int64</span></span>             |
| <span data-ttu-id="51428-123">callCount</span><span class="sxs-lookup"><span data-stu-id="51428-123">callCount</span></span>               | <span data-ttu-id="51428-124">Int64</span><span class="sxs-lookup"><span data-stu-id="51428-124">Int64</span></span>             |
| <span data-ttu-id="51428-125">meetingCount</span><span class="sxs-lookup"><span data-stu-id="51428-125">meetingCount</span></span>            | <span data-ttu-id="51428-126">Int64</span><span class="sxs-lookup"><span data-stu-id="51428-126">Int64</span></span>             |
| <span data-ttu-id="51428-127">hasOtherAction</span><span class="sxs-lookup"><span data-stu-id="51428-127">hasOtherAction</span></span>          | <span data-ttu-id="51428-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="51428-128">Boolean</span></span>           |
| <span data-ttu-id="51428-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="51428-129">reportPeriod</span></span>            | <span data-ttu-id="51428-130">String</span><span class="sxs-lookup"><span data-stu-id="51428-130">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="51428-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="51428-131">JSON representation</span></span>

<span data-ttu-id="51428-132">La siguiente es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="51428-132">The following is a JSON representaion of the resource.</span></span>

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
