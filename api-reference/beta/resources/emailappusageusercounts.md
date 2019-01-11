---
title: tipo de recurso emailAppUsageUserCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: a018776f092e9b7f378e8069666d015e1cd3e4a0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27835451"
---
# <a name="emailappusageusercounts-resource-type"></a><span data-ttu-id="38cb9-103">tipo de recurso emailAppUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="38cb9-103">emailAppUsageUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="38cb9-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38cb9-104">Properties</span></span>

| <span data-ttu-id="38cb9-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="38cb9-105">Property</span></span>          | <span data-ttu-id="38cb9-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="38cb9-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="38cb9-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="38cb9-107">reportRefreshDate</span></span> | <span data-ttu-id="38cb9-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="38cb9-108">Date</span></span>   |
| <span data-ttu-id="38cb9-109">mailForMac</span><span class="sxs-lookup"><span data-stu-id="38cb9-109">mailForMac</span></span>        | <span data-ttu-id="38cb9-110">Int64</span><span class="sxs-lookup"><span data-stu-id="38cb9-110">Int64</span></span>  |
| <span data-ttu-id="38cb9-111">outlookForMac</span><span class="sxs-lookup"><span data-stu-id="38cb9-111">outlookForMac</span></span>     | <span data-ttu-id="38cb9-112">Int64</span><span class="sxs-lookup"><span data-stu-id="38cb9-112">Int64</span></span>  |
| <span data-ttu-id="38cb9-113">outlookForWindows</span><span class="sxs-lookup"><span data-stu-id="38cb9-113">outlookForWindows</span></span> | <span data-ttu-id="38cb9-114">Int64</span><span class="sxs-lookup"><span data-stu-id="38cb9-114">Int64</span></span>  |
| <span data-ttu-id="38cb9-115">outlookForMobile</span><span class="sxs-lookup"><span data-stu-id="38cb9-115">outlookForMobile</span></span>  | <span data-ttu-id="38cb9-116">Int64</span><span class="sxs-lookup"><span data-stu-id="38cb9-116">Int64</span></span>  |
| <span data-ttu-id="38cb9-117">otherForMobile</span><span class="sxs-lookup"><span data-stu-id="38cb9-117">otherForMobile</span></span>    | <span data-ttu-id="38cb9-118">Int64</span><span class="sxs-lookup"><span data-stu-id="38cb9-118">Int64</span></span>  |
| <span data-ttu-id="38cb9-119">outlookForWeb</span><span class="sxs-lookup"><span data-stu-id="38cb9-119">outlookForWeb</span></span>     | <span data-ttu-id="38cb9-120">Int64</span><span class="sxs-lookup"><span data-stu-id="38cb9-120">Int64</span></span>  |
| <span data-ttu-id="38cb9-121">pop3App</span><span class="sxs-lookup"><span data-stu-id="38cb9-121">pop3App</span></span>           | <span data-ttu-id="38cb9-122">Int64</span><span class="sxs-lookup"><span data-stu-id="38cb9-122">Int64</span></span>  |
| <span data-ttu-id="38cb9-123">imap4App</span><span class="sxs-lookup"><span data-stu-id="38cb9-123">imap4App</span></span>          | <span data-ttu-id="38cb9-124">Int64</span><span class="sxs-lookup"><span data-stu-id="38cb9-124">Int64</span></span>  |
| <span data-ttu-id="38cb9-125">smtpApp</span><span class="sxs-lookup"><span data-stu-id="38cb9-125">smtpApp</span></span>           | <span data-ttu-id="38cb9-126">Int64</span><span class="sxs-lookup"><span data-stu-id="38cb9-126">Int64</span></span>  |
| <span data-ttu-id="38cb9-127">reportDate</span><span class="sxs-lookup"><span data-stu-id="38cb9-127">reportDate</span></span>        | <span data-ttu-id="38cb9-128">Fecha</span><span class="sxs-lookup"><span data-stu-id="38cb9-128">Date</span></span>   |
| <span data-ttu-id="38cb9-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="38cb9-129">reportPeriod</span></span>      | <span data-ttu-id="38cb9-130">String</span><span class="sxs-lookup"><span data-stu-id="38cb9-130">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="38cb9-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="38cb9-131">JSON representation</span></span>

<span data-ttu-id="38cb9-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="38cb9-132">The following is a JSON representation of the resource.</span></span>

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
