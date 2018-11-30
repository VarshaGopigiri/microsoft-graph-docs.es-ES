---
title: tipo de recurso emailAppUsageAppsUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: e588a671129c6aa131bce781e3a6db0d44128f6d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086010"
---
# <a name="emailappusageappsusercounts-resource-type"></a><span data-ttu-id="e4708-103">tipo de recurso emailAppUsageAppsUserCounts</span><span class="sxs-lookup"><span data-stu-id="e4708-103">emailAppUsageAppsUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="e4708-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4708-104">Properties</span></span>

| <span data-ttu-id="e4708-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e4708-105">Property</span></span>          | <span data-ttu-id="e4708-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4708-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="e4708-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="e4708-107">reportRefreshDate</span></span> | <span data-ttu-id="e4708-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="e4708-108">Date</span></span>   |
| <span data-ttu-id="e4708-109">mailForMac</span><span class="sxs-lookup"><span data-stu-id="e4708-109">mailForMac</span></span>        | <span data-ttu-id="e4708-110">Int64</span><span class="sxs-lookup"><span data-stu-id="e4708-110">Int64</span></span>  |
| <span data-ttu-id="e4708-111">outlookForMac</span><span class="sxs-lookup"><span data-stu-id="e4708-111">outlookForMac</span></span>     | <span data-ttu-id="e4708-112">Int64</span><span class="sxs-lookup"><span data-stu-id="e4708-112">Int64</span></span>  |
| <span data-ttu-id="e4708-113">outlookForWindows</span><span class="sxs-lookup"><span data-stu-id="e4708-113">outlookForWindows</span></span> | <span data-ttu-id="e4708-114">Int64</span><span class="sxs-lookup"><span data-stu-id="e4708-114">Int64</span></span>  |
| <span data-ttu-id="e4708-115">outlookForMobile</span><span class="sxs-lookup"><span data-stu-id="e4708-115">outlookForMobile</span></span>  | <span data-ttu-id="e4708-116">Int64</span><span class="sxs-lookup"><span data-stu-id="e4708-116">Int64</span></span>  |
| <span data-ttu-id="e4708-117">otherForMobile</span><span class="sxs-lookup"><span data-stu-id="e4708-117">otherForMobile</span></span>    | <span data-ttu-id="e4708-118">Int64</span><span class="sxs-lookup"><span data-stu-id="e4708-118">Int64</span></span>  |
| <span data-ttu-id="e4708-119">outlookForWeb</span><span class="sxs-lookup"><span data-stu-id="e4708-119">outlookForWeb</span></span>     | <span data-ttu-id="e4708-120">Int64</span><span class="sxs-lookup"><span data-stu-id="e4708-120">Int64</span></span>  |
| <span data-ttu-id="e4708-121">pop3App</span><span class="sxs-lookup"><span data-stu-id="e4708-121">pop3App</span></span>           | <span data-ttu-id="e4708-122">Int64</span><span class="sxs-lookup"><span data-stu-id="e4708-122">Int64</span></span>  |
| <span data-ttu-id="e4708-123">imap4App</span><span class="sxs-lookup"><span data-stu-id="e4708-123">imap4App</span></span>          | <span data-ttu-id="e4708-124">Int64</span><span class="sxs-lookup"><span data-stu-id="e4708-124">Int64</span></span>  |
| <span data-ttu-id="e4708-125">smtpApp</span><span class="sxs-lookup"><span data-stu-id="e4708-125">smtpApp</span></span>           | <span data-ttu-id="e4708-126">Int64</span><span class="sxs-lookup"><span data-stu-id="e4708-126">Int64</span></span>  |
| <span data-ttu-id="e4708-127">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="e4708-127">reportPeriod</span></span>      | <span data-ttu-id="e4708-128">String</span><span class="sxs-lookup"><span data-stu-id="e4708-128">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="e4708-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e4708-129">JSON representation</span></span>

<span data-ttu-id="e4708-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e4708-130">The following is a JSON representation of the resource.</span></span>

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
