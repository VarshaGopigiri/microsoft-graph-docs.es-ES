---
title: tipo de recurso teamsDeviceUsageUserCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 07a43b024d133e5ac1d8eb8a2665fd3027001edb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857354"
---
# <a name="teamsdeviceusageusercounts-resource-type"></a><span data-ttu-id="bc536-103">tipo de recurso teamsDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="bc536-103">teamsDeviceUsageUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="bc536-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bc536-104">Properties</span></span>

| <span data-ttu-id="bc536-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bc536-105">Property</span></span>          | <span data-ttu-id="bc536-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc536-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="bc536-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="bc536-107">reportRefreshDate</span></span> | <span data-ttu-id="bc536-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="bc536-108">Date</span></span>   |
| <span data-ttu-id="bc536-109">web</span><span class="sxs-lookup"><span data-stu-id="bc536-109">web</span></span>               | <span data-ttu-id="bc536-110">Int64</span><span class="sxs-lookup"><span data-stu-id="bc536-110">Int64</span></span>  |
| <span data-ttu-id="bc536-111">windowsPhone</span><span class="sxs-lookup"><span data-stu-id="bc536-111">windowsPhone</span></span>      | <span data-ttu-id="bc536-112">Int64</span><span class="sxs-lookup"><span data-stu-id="bc536-112">Int64</span></span>  |
| <span data-ttu-id="bc536-113">androidPhone</span><span class="sxs-lookup"><span data-stu-id="bc536-113">androidPhone</span></span>      | <span data-ttu-id="bc536-114">Int64</span><span class="sxs-lookup"><span data-stu-id="bc536-114">Int64</span></span>  |
| <span data-ttu-id="bc536-115">IOS</span><span class="sxs-lookup"><span data-stu-id="bc536-115">ios</span></span>               | <span data-ttu-id="bc536-116">Int64</span><span class="sxs-lookup"><span data-stu-id="bc536-116">Int64</span></span>  |
| <span data-ttu-id="bc536-117">mac</span><span class="sxs-lookup"><span data-stu-id="bc536-117">mac</span></span>               | <span data-ttu-id="bc536-118">Int64</span><span class="sxs-lookup"><span data-stu-id="bc536-118">Int64</span></span>  |
| <span data-ttu-id="bc536-119">Windows</span><span class="sxs-lookup"><span data-stu-id="bc536-119">windows</span></span>           | <span data-ttu-id="bc536-120">Int64</span><span class="sxs-lookup"><span data-stu-id="bc536-120">Int64</span></span>  |
| <span data-ttu-id="bc536-121">reportDate</span><span class="sxs-lookup"><span data-stu-id="bc536-121">reportDate</span></span>        | <span data-ttu-id="bc536-122">Fecha</span><span class="sxs-lookup"><span data-stu-id="bc536-122">Date</span></span>   |
| <span data-ttu-id="bc536-123">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="bc536-123">reportPeriod</span></span>      | <span data-ttu-id="bc536-124">String</span><span class="sxs-lookup"><span data-stu-id="bc536-124">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="bc536-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bc536-125">JSON representation</span></span>

<span data-ttu-id="bc536-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="bc536-126">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsDeviceUsageUserCounts"
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
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
