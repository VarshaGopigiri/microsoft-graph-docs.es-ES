---
title: tipo de recurso emailAppUsageAppsUserCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 220770fab755c0e345af23f3fc3113732af63ff0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970385"
---
# <a name="emailappusageappsusercounts-resource-type"></a><span data-ttu-id="de3b3-103">tipo de recurso emailAppUsageAppsUserCounts</span><span class="sxs-lookup"><span data-stu-id="de3b3-103">emailAppUsageAppsUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="de3b3-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="de3b3-104">Properties</span></span>

| <span data-ttu-id="de3b3-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="de3b3-105">Property</span></span>          | <span data-ttu-id="de3b3-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="de3b3-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="de3b3-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="de3b3-107">reportRefreshDate</span></span> | <span data-ttu-id="de3b3-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="de3b3-108">Date</span></span>   |
| <span data-ttu-id="de3b3-109">mailForMac</span><span class="sxs-lookup"><span data-stu-id="de3b3-109">mailForMac</span></span>        | <span data-ttu-id="de3b3-110">Int64</span><span class="sxs-lookup"><span data-stu-id="de3b3-110">Int64</span></span>  |
| <span data-ttu-id="de3b3-111">outlookForMac</span><span class="sxs-lookup"><span data-stu-id="de3b3-111">outlookForMac</span></span>     | <span data-ttu-id="de3b3-112">Int64</span><span class="sxs-lookup"><span data-stu-id="de3b3-112">Int64</span></span>  |
| <span data-ttu-id="de3b3-113">outlookForWindows</span><span class="sxs-lookup"><span data-stu-id="de3b3-113">outlookForWindows</span></span> | <span data-ttu-id="de3b3-114">Int64</span><span class="sxs-lookup"><span data-stu-id="de3b3-114">Int64</span></span>  |
| <span data-ttu-id="de3b3-115">outlookForMobile</span><span class="sxs-lookup"><span data-stu-id="de3b3-115">outlookForMobile</span></span>  | <span data-ttu-id="de3b3-116">Int64</span><span class="sxs-lookup"><span data-stu-id="de3b3-116">Int64</span></span>  |
| <span data-ttu-id="de3b3-117">otherForMobile</span><span class="sxs-lookup"><span data-stu-id="de3b3-117">otherForMobile</span></span>    | <span data-ttu-id="de3b3-118">Int64</span><span class="sxs-lookup"><span data-stu-id="de3b3-118">Int64</span></span>  |
| <span data-ttu-id="de3b3-119">outlookForWeb</span><span class="sxs-lookup"><span data-stu-id="de3b3-119">outlookForWeb</span></span>     | <span data-ttu-id="de3b3-120">Int64</span><span class="sxs-lookup"><span data-stu-id="de3b3-120">Int64</span></span>  |
| <span data-ttu-id="de3b3-121">pop3App</span><span class="sxs-lookup"><span data-stu-id="de3b3-121">pop3App</span></span>           | <span data-ttu-id="de3b3-122">Int64</span><span class="sxs-lookup"><span data-stu-id="de3b3-122">Int64</span></span>  |
| <span data-ttu-id="de3b3-123">imap4App</span><span class="sxs-lookup"><span data-stu-id="de3b3-123">imap4App</span></span>          | <span data-ttu-id="de3b3-124">Int64</span><span class="sxs-lookup"><span data-stu-id="de3b3-124">Int64</span></span>  |
| <span data-ttu-id="de3b3-125">smtpApp</span><span class="sxs-lookup"><span data-stu-id="de3b3-125">smtpApp</span></span>           | <span data-ttu-id="de3b3-126">Int64</span><span class="sxs-lookup"><span data-stu-id="de3b3-126">Int64</span></span>  |
| <span data-ttu-id="de3b3-127">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="de3b3-127">reportPeriod</span></span>      | <span data-ttu-id="de3b3-128">String</span><span class="sxs-lookup"><span data-stu-id="de3b3-128">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="de3b3-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="de3b3-129">JSON representation</span></span>

<span data-ttu-id="de3b3-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="de3b3-130">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.emailAppUsageAppsUserCounts"
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
  "reportPeriod": "String"
}
```
