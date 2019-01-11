---
title: tipo de recurso teamsDeviceUsageDistributionUserCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
localization_priority: Normal
ms.openlocfilehash: a02dfa5a5036d67a624656d715c0fb0d3c8194ef
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868701"
---
# <a name="teamsdeviceusagedistributionusercounts-resource-type"></a><span data-ttu-id="6cf86-103">tipo de recurso teamsDeviceUsageDistributionUserCounts</span><span class="sxs-lookup"><span data-stu-id="6cf86-103">teamsDeviceUsageDistributionUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="6cf86-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6cf86-104">Properties</span></span>

| <span data-ttu-id="6cf86-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6cf86-105">Property</span></span>          | <span data-ttu-id="6cf86-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="6cf86-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="6cf86-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="6cf86-107">reportRefreshDate</span></span> | <span data-ttu-id="6cf86-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="6cf86-108">Date</span></span>   |
| <span data-ttu-id="6cf86-109">web</span><span class="sxs-lookup"><span data-stu-id="6cf86-109">web</span></span>               | <span data-ttu-id="6cf86-110">Int64</span><span class="sxs-lookup"><span data-stu-id="6cf86-110">Int64</span></span>  |
| <span data-ttu-id="6cf86-111">windowsPhone</span><span class="sxs-lookup"><span data-stu-id="6cf86-111">windowsPhone</span></span>      | <span data-ttu-id="6cf86-112">Int64</span><span class="sxs-lookup"><span data-stu-id="6cf86-112">Int64</span></span>  |
| <span data-ttu-id="6cf86-113">androidPhone</span><span class="sxs-lookup"><span data-stu-id="6cf86-113">androidPhone</span></span>      | <span data-ttu-id="6cf86-114">Int64</span><span class="sxs-lookup"><span data-stu-id="6cf86-114">Int64</span></span>  |
| <span data-ttu-id="6cf86-115">IOS</span><span class="sxs-lookup"><span data-stu-id="6cf86-115">ios</span></span>               | <span data-ttu-id="6cf86-116">Int64</span><span class="sxs-lookup"><span data-stu-id="6cf86-116">Int64</span></span>  |
| <span data-ttu-id="6cf86-117">mac</span><span class="sxs-lookup"><span data-stu-id="6cf86-117">mac</span></span>               | <span data-ttu-id="6cf86-118">Int64</span><span class="sxs-lookup"><span data-stu-id="6cf86-118">Int64</span></span>  |
| <span data-ttu-id="6cf86-119">Windows</span><span class="sxs-lookup"><span data-stu-id="6cf86-119">windows</span></span>           | <span data-ttu-id="6cf86-120">Int64</span><span class="sxs-lookup"><span data-stu-id="6cf86-120">Int64</span></span>  |
| <span data-ttu-id="6cf86-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="6cf86-121">reportPeriod</span></span>      | <span data-ttu-id="6cf86-122">String</span><span class="sxs-lookup"><span data-stu-id="6cf86-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="6cf86-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6cf86-123">JSON representation</span></span>

<span data-ttu-id="6cf86-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6cf86-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsDeviceUsageDistributionUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "web": 1024, 
  "windowsPhone": 1024, 
  "androidPhone": 1024, 
  "ios": 1024, 
  "mac": 1024, 
  "windows": 1024, 
  "reportPeriod": "String"
}
```
