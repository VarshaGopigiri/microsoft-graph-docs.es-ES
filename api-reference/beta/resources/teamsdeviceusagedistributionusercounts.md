---
title: tipo de recurso teamsDeviceUsageDistributionUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: b039320e389e1a61832089991b2368b27e51c475
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083404"
---
# <a name="teamsdeviceusagedistributionusercounts-resource-type"></a><span data-ttu-id="a54fe-103">tipo de recurso teamsDeviceUsageDistributionUserCounts</span><span class="sxs-lookup"><span data-stu-id="a54fe-103">teamsDeviceUsageDistributionUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="a54fe-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a54fe-104">Properties</span></span>

| <span data-ttu-id="a54fe-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a54fe-105">Property</span></span>          | <span data-ttu-id="a54fe-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a54fe-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="a54fe-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="a54fe-107">reportRefreshDate</span></span> | <span data-ttu-id="a54fe-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="a54fe-108">Date</span></span>   |
| <span data-ttu-id="a54fe-109">web</span><span class="sxs-lookup"><span data-stu-id="a54fe-109">web</span></span>               | <span data-ttu-id="a54fe-110">Int64</span><span class="sxs-lookup"><span data-stu-id="a54fe-110">Int64</span></span>  |
| <span data-ttu-id="a54fe-111">windowsPhone</span><span class="sxs-lookup"><span data-stu-id="a54fe-111">windowsPhone</span></span>      | <span data-ttu-id="a54fe-112">Int64</span><span class="sxs-lookup"><span data-stu-id="a54fe-112">Int64</span></span>  |
| <span data-ttu-id="a54fe-113">androidPhone</span><span class="sxs-lookup"><span data-stu-id="a54fe-113">androidPhone</span></span>      | <span data-ttu-id="a54fe-114">Int64</span><span class="sxs-lookup"><span data-stu-id="a54fe-114">Int64</span></span>  |
| <span data-ttu-id="a54fe-115">IOS</span><span class="sxs-lookup"><span data-stu-id="a54fe-115">ios</span></span>               | <span data-ttu-id="a54fe-116">Int64</span><span class="sxs-lookup"><span data-stu-id="a54fe-116">Int64</span></span>  |
| <span data-ttu-id="a54fe-117">mac</span><span class="sxs-lookup"><span data-stu-id="a54fe-117">mac</span></span>               | <span data-ttu-id="a54fe-118">Int64</span><span class="sxs-lookup"><span data-stu-id="a54fe-118">Int64</span></span>  |
| <span data-ttu-id="a54fe-119">Windows</span><span class="sxs-lookup"><span data-stu-id="a54fe-119">windows</span></span>           | <span data-ttu-id="a54fe-120">Int64</span><span class="sxs-lookup"><span data-stu-id="a54fe-120">Int64</span></span>  |
| <span data-ttu-id="a54fe-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="a54fe-121">reportPeriod</span></span>      | <span data-ttu-id="a54fe-122">String</span><span class="sxs-lookup"><span data-stu-id="a54fe-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="a54fe-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a54fe-123">JSON representation</span></span>

<span data-ttu-id="a54fe-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a54fe-124">The following is a JSON representation of the resource.</span></span>

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
