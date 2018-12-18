---
title: tipo de recurso teamsDeviceUsageUserCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
ms.openlocfilehash: 1255a8e1e92bb461d5c100c72e9030f57db5f8fa
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306513"
---
# <a name="teamsdeviceusageusercounts-resource-type"></a><span data-ttu-id="5bae4-103">tipo de recurso teamsDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="5bae4-103">teamsDeviceUsageUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="5bae4-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5bae4-104">Properties</span></span>

| <span data-ttu-id="5bae4-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5bae4-105">Property</span></span>          | <span data-ttu-id="5bae4-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="5bae4-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="5bae4-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="5bae4-107">reportRefreshDate</span></span> | <span data-ttu-id="5bae4-108">Date</span><span class="sxs-lookup"><span data-stu-id="5bae4-108">Date</span></span>   |
| <span data-ttu-id="5bae4-109">web</span><span class="sxs-lookup"><span data-stu-id="5bae4-109">web</span></span>               | <span data-ttu-id="5bae4-110">Int64</span><span class="sxs-lookup"><span data-stu-id="5bae4-110">Int64</span></span>  |
| <span data-ttu-id="5bae4-111">windowsPhone</span><span class="sxs-lookup"><span data-stu-id="5bae4-111">windowsPhone</span></span>      | <span data-ttu-id="5bae4-112">Int64</span><span class="sxs-lookup"><span data-stu-id="5bae4-112">Int64</span></span>  |
| <span data-ttu-id="5bae4-113">androidPhone</span><span class="sxs-lookup"><span data-stu-id="5bae4-113">androidPhone</span></span>      | <span data-ttu-id="5bae4-114">Int64</span><span class="sxs-lookup"><span data-stu-id="5bae4-114">Int64</span></span>  |
| <span data-ttu-id="5bae4-115">IOS</span><span class="sxs-lookup"><span data-stu-id="5bae4-115">ios</span></span>               | <span data-ttu-id="5bae4-116">Int64</span><span class="sxs-lookup"><span data-stu-id="5bae4-116">Int64</span></span>  |
| <span data-ttu-id="5bae4-117">mac</span><span class="sxs-lookup"><span data-stu-id="5bae4-117">mac</span></span>               | <span data-ttu-id="5bae4-118">Int64</span><span class="sxs-lookup"><span data-stu-id="5bae4-118">Int64</span></span>  |
| <span data-ttu-id="5bae4-119">Windows</span><span class="sxs-lookup"><span data-stu-id="5bae4-119">windows</span></span>           | <span data-ttu-id="5bae4-120">Int64</span><span class="sxs-lookup"><span data-stu-id="5bae4-120">Int64</span></span>  |
| <span data-ttu-id="5bae4-121">reportDate</span><span class="sxs-lookup"><span data-stu-id="5bae4-121">reportDate</span></span>        | <span data-ttu-id="5bae4-122">Date</span><span class="sxs-lookup"><span data-stu-id="5bae4-122">Date</span></span>   |
| <span data-ttu-id="5bae4-123">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="5bae4-123">reportPeriod</span></span>      | <span data-ttu-id="5bae4-124">String</span><span class="sxs-lookup"><span data-stu-id="5bae4-124">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="5bae4-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5bae4-125">JSON representation</span></span>

<span data-ttu-id="5bae4-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5bae4-126">The following is a JSON representation of the resource.</span></span>

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
