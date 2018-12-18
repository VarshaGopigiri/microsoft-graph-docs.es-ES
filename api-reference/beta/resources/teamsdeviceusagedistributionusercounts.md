---
title: tipo de recurso teamsDeviceUsageDistributionUserCounts
description: La siguiente es una representación JSON del recurso
author: nkramer
ms.openlocfilehash: 01b9f67f30a7b2f13aac65cbcd4795792ee0aaa0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27345853"
---
# <a name="teamsdeviceusagedistributionusercounts-resource-type"></a><span data-ttu-id="61aea-103">tipo de recurso teamsDeviceUsageDistributionUserCounts</span><span class="sxs-lookup"><span data-stu-id="61aea-103">teamsDeviceUsageDistributionUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="61aea-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61aea-104">Properties</span></span>

| <span data-ttu-id="61aea-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="61aea-105">Property</span></span>          | <span data-ttu-id="61aea-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="61aea-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="61aea-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="61aea-107">reportRefreshDate</span></span> | <span data-ttu-id="61aea-108">Date</span><span class="sxs-lookup"><span data-stu-id="61aea-108">Date</span></span>   |
| <span data-ttu-id="61aea-109">web</span><span class="sxs-lookup"><span data-stu-id="61aea-109">web</span></span>               | <span data-ttu-id="61aea-110">Int64</span><span class="sxs-lookup"><span data-stu-id="61aea-110">Int64</span></span>  |
| <span data-ttu-id="61aea-111">windowsPhone</span><span class="sxs-lookup"><span data-stu-id="61aea-111">windowsPhone</span></span>      | <span data-ttu-id="61aea-112">Int64</span><span class="sxs-lookup"><span data-stu-id="61aea-112">Int64</span></span>  |
| <span data-ttu-id="61aea-113">androidPhone</span><span class="sxs-lookup"><span data-stu-id="61aea-113">androidPhone</span></span>      | <span data-ttu-id="61aea-114">Int64</span><span class="sxs-lookup"><span data-stu-id="61aea-114">Int64</span></span>  |
| <span data-ttu-id="61aea-115">IOS</span><span class="sxs-lookup"><span data-stu-id="61aea-115">ios</span></span>               | <span data-ttu-id="61aea-116">Int64</span><span class="sxs-lookup"><span data-stu-id="61aea-116">Int64</span></span>  |
| <span data-ttu-id="61aea-117">mac</span><span class="sxs-lookup"><span data-stu-id="61aea-117">mac</span></span>               | <span data-ttu-id="61aea-118">Int64</span><span class="sxs-lookup"><span data-stu-id="61aea-118">Int64</span></span>  |
| <span data-ttu-id="61aea-119">Windows</span><span class="sxs-lookup"><span data-stu-id="61aea-119">windows</span></span>           | <span data-ttu-id="61aea-120">Int64</span><span class="sxs-lookup"><span data-stu-id="61aea-120">Int64</span></span>  |
| <span data-ttu-id="61aea-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="61aea-121">reportPeriod</span></span>      | <span data-ttu-id="61aea-122">String</span><span class="sxs-lookup"><span data-stu-id="61aea-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="61aea-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="61aea-123">JSON representation</span></span>

<span data-ttu-id="61aea-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="61aea-124">The following is a JSON representation of the resource.</span></span>

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
