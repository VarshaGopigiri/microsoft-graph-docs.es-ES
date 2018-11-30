---
title: tipo de recurso emailAppUsageUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: c8669c8a34987bc1e71152ae717f9be3ba101107
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088549"
---
# <a name="emailappusageusercounts-resource-type"></a><span data-ttu-id="bf522-103">tipo de recurso emailAppUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="bf522-103">emailAppUsageUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="bf522-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf522-104">Properties</span></span>

| <span data-ttu-id="bf522-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bf522-105">Property</span></span>          | <span data-ttu-id="bf522-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf522-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="bf522-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="bf522-107">reportRefreshDate</span></span> | <span data-ttu-id="bf522-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="bf522-108">Date</span></span>   |
| <span data-ttu-id="bf522-109">mailForMac</span><span class="sxs-lookup"><span data-stu-id="bf522-109">mailForMac</span></span>        | <span data-ttu-id="bf522-110">Int64</span><span class="sxs-lookup"><span data-stu-id="bf522-110">Int64</span></span>  |
| <span data-ttu-id="bf522-111">outlookForMac</span><span class="sxs-lookup"><span data-stu-id="bf522-111">outlookForMac</span></span>     | <span data-ttu-id="bf522-112">Int64</span><span class="sxs-lookup"><span data-stu-id="bf522-112">Int64</span></span>  |
| <span data-ttu-id="bf522-113">outlookForWindows</span><span class="sxs-lookup"><span data-stu-id="bf522-113">outlookForWindows</span></span> | <span data-ttu-id="bf522-114">Int64</span><span class="sxs-lookup"><span data-stu-id="bf522-114">Int64</span></span>  |
| <span data-ttu-id="bf522-115">outlookForMobile</span><span class="sxs-lookup"><span data-stu-id="bf522-115">outlookForMobile</span></span>  | <span data-ttu-id="bf522-116">Int64</span><span class="sxs-lookup"><span data-stu-id="bf522-116">Int64</span></span>  |
| <span data-ttu-id="bf522-117">otherForMobile</span><span class="sxs-lookup"><span data-stu-id="bf522-117">otherForMobile</span></span>    | <span data-ttu-id="bf522-118">Int64</span><span class="sxs-lookup"><span data-stu-id="bf522-118">Int64</span></span>  |
| <span data-ttu-id="bf522-119">outlookForWeb</span><span class="sxs-lookup"><span data-stu-id="bf522-119">outlookForWeb</span></span>     | <span data-ttu-id="bf522-120">Int64</span><span class="sxs-lookup"><span data-stu-id="bf522-120">Int64</span></span>  |
| <span data-ttu-id="bf522-121">pop3App</span><span class="sxs-lookup"><span data-stu-id="bf522-121">pop3App</span></span>           | <span data-ttu-id="bf522-122">Int64</span><span class="sxs-lookup"><span data-stu-id="bf522-122">Int64</span></span>  |
| <span data-ttu-id="bf522-123">imap4App</span><span class="sxs-lookup"><span data-stu-id="bf522-123">imap4App</span></span>          | <span data-ttu-id="bf522-124">Int64</span><span class="sxs-lookup"><span data-stu-id="bf522-124">Int64</span></span>  |
| <span data-ttu-id="bf522-125">smtpApp</span><span class="sxs-lookup"><span data-stu-id="bf522-125">smtpApp</span></span>           | <span data-ttu-id="bf522-126">Int64</span><span class="sxs-lookup"><span data-stu-id="bf522-126">Int64</span></span>  |
| <span data-ttu-id="bf522-127">reportDate</span><span class="sxs-lookup"><span data-stu-id="bf522-127">reportDate</span></span>        | <span data-ttu-id="bf522-128">Fecha</span><span class="sxs-lookup"><span data-stu-id="bf522-128">Date</span></span>   |
| <span data-ttu-id="bf522-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="bf522-129">reportPeriod</span></span>      | <span data-ttu-id="bf522-130">String</span><span class="sxs-lookup"><span data-stu-id="bf522-130">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="bf522-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bf522-131">JSON representation</span></span>

<span data-ttu-id="bf522-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="bf522-132">The following is a JSON representation of the resource.</span></span>

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
