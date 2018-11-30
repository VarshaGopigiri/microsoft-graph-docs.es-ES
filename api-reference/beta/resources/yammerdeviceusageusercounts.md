---
title: tipo de recurso yammerDeviceUsageUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 7faec83d113da3f412c913177a717fdc69504310
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086639"
---
# <a name="yammerdeviceusageusercounts-resource-type"></a><span data-ttu-id="6c38e-103">tipo de recurso yammerDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="6c38e-103">yammerDeviceUsageUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="6c38e-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6c38e-104">Properties</span></span>

| <span data-ttu-id="6c38e-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c38e-105">Property</span></span>          | <span data-ttu-id="6c38e-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c38e-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="6c38e-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="6c38e-107">reportRefreshDate</span></span> | <span data-ttu-id="6c38e-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="6c38e-108">Date</span></span>   |
| <span data-ttu-id="6c38e-109">web</span><span class="sxs-lookup"><span data-stu-id="6c38e-109">web</span></span>               | <span data-ttu-id="6c38e-110">Int32</span><span class="sxs-lookup"><span data-stu-id="6c38e-110">Int32</span></span>  |
| <span data-ttu-id="6c38e-111">windowsPhone</span><span class="sxs-lookup"><span data-stu-id="6c38e-111">windowsPhone</span></span>      | <span data-ttu-id="6c38e-112">Int32</span><span class="sxs-lookup"><span data-stu-id="6c38e-112">Int32</span></span>  |
| <span data-ttu-id="6c38e-113">androidPhone</span><span class="sxs-lookup"><span data-stu-id="6c38e-113">androidPhone</span></span>      | <span data-ttu-id="6c38e-114">Int32</span><span class="sxs-lookup"><span data-stu-id="6c38e-114">Int32</span></span>  |
| <span data-ttu-id="6c38e-115">iPhone</span><span class="sxs-lookup"><span data-stu-id="6c38e-115">iPhone</span></span>            | <span data-ttu-id="6c38e-116">Int32</span><span class="sxs-lookup"><span data-stu-id="6c38e-116">Int32</span></span>  |
| <span data-ttu-id="6c38e-117">iPad</span><span class="sxs-lookup"><span data-stu-id="6c38e-117">iPad</span></span>              | <span data-ttu-id="6c38e-118">Int32</span><span class="sxs-lookup"><span data-stu-id="6c38e-118">Int32</span></span>  |
| <span data-ttu-id="6c38e-119">otros</span><span class="sxs-lookup"><span data-stu-id="6c38e-119">other</span></span>             | <span data-ttu-id="6c38e-120">Int32</span><span class="sxs-lookup"><span data-stu-id="6c38e-120">Int32</span></span>  |
| <span data-ttu-id="6c38e-121">reportDate</span><span class="sxs-lookup"><span data-stu-id="6c38e-121">reportDate</span></span>        | <span data-ttu-id="6c38e-122">Fecha</span><span class="sxs-lookup"><span data-stu-id="6c38e-122">Date</span></span>   |
| <span data-ttu-id="6c38e-123">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="6c38e-123">reportPeriod</span></span>      | <span data-ttu-id="6c38e-124">String</span><span class="sxs-lookup"><span data-stu-id="6c38e-124">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="6c38e-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6c38e-125">JSON representation</span></span>

<span data-ttu-id="6c38e-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6c38e-126">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yammerDeviceUsageUserCounts"
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
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```