---
title: tipo de recurso teamsDeviceUsageUserCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 671dfada02b9c16d3392d0a97023b82020fd1218
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987401"
---
# <a name="teamsdeviceusageusercounts-resource-type"></a><span data-ttu-id="355d8-103">tipo de recurso teamsDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="355d8-103">teamsDeviceUsageUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="355d8-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="355d8-104">Properties</span></span>

| <span data-ttu-id="355d8-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="355d8-105">Property</span></span>          | <span data-ttu-id="355d8-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="355d8-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="355d8-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="355d8-107">reportRefreshDate</span></span> | <span data-ttu-id="355d8-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="355d8-108">Date</span></span>   |
| <span data-ttu-id="355d8-109">web</span><span class="sxs-lookup"><span data-stu-id="355d8-109">web</span></span>               | <span data-ttu-id="355d8-110">Int64</span><span class="sxs-lookup"><span data-stu-id="355d8-110">Int64</span></span>  |
| <span data-ttu-id="355d8-111">windowsPhone</span><span class="sxs-lookup"><span data-stu-id="355d8-111">windowsPhone</span></span>      | <span data-ttu-id="355d8-112">Int64</span><span class="sxs-lookup"><span data-stu-id="355d8-112">Int64</span></span>  |
| <span data-ttu-id="355d8-113">androidPhone</span><span class="sxs-lookup"><span data-stu-id="355d8-113">androidPhone</span></span>      | <span data-ttu-id="355d8-114">Int64</span><span class="sxs-lookup"><span data-stu-id="355d8-114">Int64</span></span>  |
| <span data-ttu-id="355d8-115">IOS</span><span class="sxs-lookup"><span data-stu-id="355d8-115">ios</span></span>               | <span data-ttu-id="355d8-116">Int64</span><span class="sxs-lookup"><span data-stu-id="355d8-116">Int64</span></span>  |
| <span data-ttu-id="355d8-117">mac</span><span class="sxs-lookup"><span data-stu-id="355d8-117">mac</span></span>               | <span data-ttu-id="355d8-118">Int64</span><span class="sxs-lookup"><span data-stu-id="355d8-118">Int64</span></span>  |
| <span data-ttu-id="355d8-119">Windows</span><span class="sxs-lookup"><span data-stu-id="355d8-119">windows</span></span>           | <span data-ttu-id="355d8-120">Int64</span><span class="sxs-lookup"><span data-stu-id="355d8-120">Int64</span></span>  |
| <span data-ttu-id="355d8-121">reportDate</span><span class="sxs-lookup"><span data-stu-id="355d8-121">reportDate</span></span>        | <span data-ttu-id="355d8-122">Fecha</span><span class="sxs-lookup"><span data-stu-id="355d8-122">Date</span></span>   |
| <span data-ttu-id="355d8-123">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="355d8-123">reportPeriod</span></span>      | <span data-ttu-id="355d8-124">String</span><span class="sxs-lookup"><span data-stu-id="355d8-124">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="355d8-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="355d8-125">JSON representation</span></span>

<span data-ttu-id="355d8-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="355d8-126">The following is a JSON representation of the resource.</span></span>

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
