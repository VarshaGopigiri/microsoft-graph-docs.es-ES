---
title: tipo de recurso emailAppUsageUserCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 7822528aacc9d6f104012d43004fbb9aabba127c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990806"
---
# <a name="emailappusageusercounts-resource-type"></a><span data-ttu-id="59a7b-103">tipo de recurso emailAppUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="59a7b-103">emailAppUsageUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="59a7b-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="59a7b-104">Properties</span></span>

| <span data-ttu-id="59a7b-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="59a7b-105">Property</span></span>          | <span data-ttu-id="59a7b-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="59a7b-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="59a7b-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="59a7b-107">reportRefreshDate</span></span> | <span data-ttu-id="59a7b-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="59a7b-108">Date</span></span>   |
| <span data-ttu-id="59a7b-109">mailForMac</span><span class="sxs-lookup"><span data-stu-id="59a7b-109">mailForMac</span></span>        | <span data-ttu-id="59a7b-110">Int64</span><span class="sxs-lookup"><span data-stu-id="59a7b-110">Int64</span></span>  |
| <span data-ttu-id="59a7b-111">outlookForMac</span><span class="sxs-lookup"><span data-stu-id="59a7b-111">outlookForMac</span></span>     | <span data-ttu-id="59a7b-112">Int64</span><span class="sxs-lookup"><span data-stu-id="59a7b-112">Int64</span></span>  |
| <span data-ttu-id="59a7b-113">outlookForWindows</span><span class="sxs-lookup"><span data-stu-id="59a7b-113">outlookForWindows</span></span> | <span data-ttu-id="59a7b-114">Int64</span><span class="sxs-lookup"><span data-stu-id="59a7b-114">Int64</span></span>  |
| <span data-ttu-id="59a7b-115">outlookForMobile</span><span class="sxs-lookup"><span data-stu-id="59a7b-115">outlookForMobile</span></span>  | <span data-ttu-id="59a7b-116">Int64</span><span class="sxs-lookup"><span data-stu-id="59a7b-116">Int64</span></span>  |
| <span data-ttu-id="59a7b-117">otherForMobile</span><span class="sxs-lookup"><span data-stu-id="59a7b-117">otherForMobile</span></span>    | <span data-ttu-id="59a7b-118">Int64</span><span class="sxs-lookup"><span data-stu-id="59a7b-118">Int64</span></span>  |
| <span data-ttu-id="59a7b-119">outlookForWeb</span><span class="sxs-lookup"><span data-stu-id="59a7b-119">outlookForWeb</span></span>     | <span data-ttu-id="59a7b-120">Int64</span><span class="sxs-lookup"><span data-stu-id="59a7b-120">Int64</span></span>  |
| <span data-ttu-id="59a7b-121">pop3App</span><span class="sxs-lookup"><span data-stu-id="59a7b-121">pop3App</span></span>           | <span data-ttu-id="59a7b-122">Int64</span><span class="sxs-lookup"><span data-stu-id="59a7b-122">Int64</span></span>  |
| <span data-ttu-id="59a7b-123">imap4App</span><span class="sxs-lookup"><span data-stu-id="59a7b-123">imap4App</span></span>          | <span data-ttu-id="59a7b-124">Int64</span><span class="sxs-lookup"><span data-stu-id="59a7b-124">Int64</span></span>  |
| <span data-ttu-id="59a7b-125">smtpApp</span><span class="sxs-lookup"><span data-stu-id="59a7b-125">smtpApp</span></span>           | <span data-ttu-id="59a7b-126">Int64</span><span class="sxs-lookup"><span data-stu-id="59a7b-126">Int64</span></span>  |
| <span data-ttu-id="59a7b-127">reportDate</span><span class="sxs-lookup"><span data-stu-id="59a7b-127">reportDate</span></span>        | <span data-ttu-id="59a7b-128">Fecha</span><span class="sxs-lookup"><span data-stu-id="59a7b-128">Date</span></span>   |
| <span data-ttu-id="59a7b-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="59a7b-129">reportPeriod</span></span>      | <span data-ttu-id="59a7b-130">String</span><span class="sxs-lookup"><span data-stu-id="59a7b-130">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="59a7b-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="59a7b-131">JSON representation</span></span>

<span data-ttu-id="59a7b-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="59a7b-132">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.emailAppUsageUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "mailForMac": 1024, 
  "outlookForMac": 1024, 
  "outlookForWindows": 1024, 
  "outlookForMobile": 1024, 
  "otherForMobile": 1024, 
  "outlookForWeb": 1024, 
  "pop3App": 1024, 
  "imap4App": 1024, 
  "smtpApp": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
