---
title: tipo de recurso emailAppUsageAppsUserCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: efbc4ce75293237813e9a835cb45ff0bf0ec4b26
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27807822"
---
# <a name="emailappusageappsusercounts-resource-type"></a><span data-ttu-id="fb2bf-103">tipo de recurso emailAppUsageAppsUserCounts</span><span class="sxs-lookup"><span data-stu-id="fb2bf-103">emailAppUsageAppsUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="fb2bf-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb2bf-104">Properties</span></span>

| <span data-ttu-id="fb2bf-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb2bf-105">Property</span></span>          | <span data-ttu-id="fb2bf-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb2bf-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="fb2bf-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="fb2bf-107">reportRefreshDate</span></span> | <span data-ttu-id="fb2bf-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="fb2bf-108">Date</span></span>   |
| <span data-ttu-id="fb2bf-109">mailForMac</span><span class="sxs-lookup"><span data-stu-id="fb2bf-109">mailForMac</span></span>        | <span data-ttu-id="fb2bf-110">Int64</span><span class="sxs-lookup"><span data-stu-id="fb2bf-110">Int64</span></span>  |
| <span data-ttu-id="fb2bf-111">outlookForMac</span><span class="sxs-lookup"><span data-stu-id="fb2bf-111">outlookForMac</span></span>     | <span data-ttu-id="fb2bf-112">Int64</span><span class="sxs-lookup"><span data-stu-id="fb2bf-112">Int64</span></span>  |
| <span data-ttu-id="fb2bf-113">outlookForWindows</span><span class="sxs-lookup"><span data-stu-id="fb2bf-113">outlookForWindows</span></span> | <span data-ttu-id="fb2bf-114">Int64</span><span class="sxs-lookup"><span data-stu-id="fb2bf-114">Int64</span></span>  |
| <span data-ttu-id="fb2bf-115">outlookForMobile</span><span class="sxs-lookup"><span data-stu-id="fb2bf-115">outlookForMobile</span></span>  | <span data-ttu-id="fb2bf-116">Int64</span><span class="sxs-lookup"><span data-stu-id="fb2bf-116">Int64</span></span>  |
| <span data-ttu-id="fb2bf-117">otherForMobile</span><span class="sxs-lookup"><span data-stu-id="fb2bf-117">otherForMobile</span></span>    | <span data-ttu-id="fb2bf-118">Int64</span><span class="sxs-lookup"><span data-stu-id="fb2bf-118">Int64</span></span>  |
| <span data-ttu-id="fb2bf-119">outlookForWeb</span><span class="sxs-lookup"><span data-stu-id="fb2bf-119">outlookForWeb</span></span>     | <span data-ttu-id="fb2bf-120">Int64</span><span class="sxs-lookup"><span data-stu-id="fb2bf-120">Int64</span></span>  |
| <span data-ttu-id="fb2bf-121">pop3App</span><span class="sxs-lookup"><span data-stu-id="fb2bf-121">pop3App</span></span>           | <span data-ttu-id="fb2bf-122">Int64</span><span class="sxs-lookup"><span data-stu-id="fb2bf-122">Int64</span></span>  |
| <span data-ttu-id="fb2bf-123">imap4App</span><span class="sxs-lookup"><span data-stu-id="fb2bf-123">imap4App</span></span>          | <span data-ttu-id="fb2bf-124">Int64</span><span class="sxs-lookup"><span data-stu-id="fb2bf-124">Int64</span></span>  |
| <span data-ttu-id="fb2bf-125">smtpApp</span><span class="sxs-lookup"><span data-stu-id="fb2bf-125">smtpApp</span></span>           | <span data-ttu-id="fb2bf-126">Int64</span><span class="sxs-lookup"><span data-stu-id="fb2bf-126">Int64</span></span>  |
| <span data-ttu-id="fb2bf-127">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="fb2bf-127">reportPeriod</span></span>      | <span data-ttu-id="fb2bf-128">String</span><span class="sxs-lookup"><span data-stu-id="fb2bf-128">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="fb2bf-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fb2bf-129">JSON representation</span></span>

<span data-ttu-id="fb2bf-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fb2bf-130">The following is a JSON representation of the resource.</span></span>

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
