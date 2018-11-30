---
title: tipo de recurso yammerDeviceUsageDistributionUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: f98c8831c147a82985d1e59b5559d88e1a4824c6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086637"
---
# <a name="yammerdeviceusagedistributionusercounts-resource-type"></a><span data-ttu-id="d353f-103">tipo de recurso yammerDeviceUsageDistributionUserCounts</span><span class="sxs-lookup"><span data-stu-id="d353f-103">yammerDeviceUsageDistributionUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="d353f-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d353f-104">Properties</span></span>

| <span data-ttu-id="d353f-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d353f-105">Property</span></span>          | <span data-ttu-id="d353f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="d353f-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="d353f-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="d353f-107">reportRefreshDate</span></span> | <span data-ttu-id="d353f-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="d353f-108">Date</span></span>   |
| <span data-ttu-id="d353f-109">web</span><span class="sxs-lookup"><span data-stu-id="d353f-109">web</span></span>               | <span data-ttu-id="d353f-110">Int32</span><span class="sxs-lookup"><span data-stu-id="d353f-110">Int32</span></span>  |
| <span data-ttu-id="d353f-111">windowsPhone</span><span class="sxs-lookup"><span data-stu-id="d353f-111">windowsPhone</span></span>      | <span data-ttu-id="d353f-112">Int32</span><span class="sxs-lookup"><span data-stu-id="d353f-112">Int32</span></span>  |
| <span data-ttu-id="d353f-113">androidPhone</span><span class="sxs-lookup"><span data-stu-id="d353f-113">androidPhone</span></span>      | <span data-ttu-id="d353f-114">Int32</span><span class="sxs-lookup"><span data-stu-id="d353f-114">Int32</span></span>  |
| <span data-ttu-id="d353f-115">iPhone</span><span class="sxs-lookup"><span data-stu-id="d353f-115">iPhone</span></span>            | <span data-ttu-id="d353f-116">Int32</span><span class="sxs-lookup"><span data-stu-id="d353f-116">Int32</span></span>  |
| <span data-ttu-id="d353f-117">iPad</span><span class="sxs-lookup"><span data-stu-id="d353f-117">iPad</span></span>              | <span data-ttu-id="d353f-118">Int32</span><span class="sxs-lookup"><span data-stu-id="d353f-118">Int32</span></span>  |
| <span data-ttu-id="d353f-119">otros</span><span class="sxs-lookup"><span data-stu-id="d353f-119">other</span></span>             | <span data-ttu-id="d353f-120">Int32</span><span class="sxs-lookup"><span data-stu-id="d353f-120">Int32</span></span>  |
| <span data-ttu-id="d353f-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="d353f-121">reportPeriod</span></span>      | <span data-ttu-id="d353f-122">String</span><span class="sxs-lookup"><span data-stu-id="d353f-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="d353f-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d353f-123">JSON representation</span></span>

<span data-ttu-id="d353f-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d353f-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yammerDeviceUsageDistributionUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "web": 1024, 
  "windowsPhone": 1024, 
  "androidPhone": 1024, 
  "iPhone": 1024, 
  "iPad": 1024, 
  "other": 1024, 
  "reportPeriod": "String"
}
```
