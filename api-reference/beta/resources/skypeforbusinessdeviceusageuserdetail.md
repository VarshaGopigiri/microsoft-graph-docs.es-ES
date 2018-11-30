---
title: tipo de recurso skypeForBusinessDeviceUsageUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: b62920d124fd52e0f653c128eeb0956cdfe0c680
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084716"
---
# <a name="skypeforbusinessdeviceusageuserdetail-resource-type"></a><span data-ttu-id="72a06-103">tipo de recurso skypeForBusinessDeviceUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="72a06-103">skypeForBusinessDeviceUsageUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="72a06-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72a06-104">Properties</span></span>

| <span data-ttu-id="72a06-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72a06-105">Property</span></span>          | <span data-ttu-id="72a06-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="72a06-106">Type</span></span>    |
| :---------------- | :------ |
| <span data-ttu-id="72a06-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="72a06-107">reportRefreshDate</span></span> | <span data-ttu-id="72a06-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="72a06-108">Date</span></span>    |
| <span data-ttu-id="72a06-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="72a06-109">userPrincipalName</span></span> | <span data-ttu-id="72a06-110">String</span><span class="sxs-lookup"><span data-stu-id="72a06-110">String</span></span>  |
| <span data-ttu-id="72a06-111">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="72a06-111">lastActivityDate</span></span>  | <span data-ttu-id="72a06-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="72a06-112">Date</span></span>    |
| <span data-ttu-id="72a06-113">usedWindows</span><span class="sxs-lookup"><span data-stu-id="72a06-113">usedWindows</span></span>       | <span data-ttu-id="72a06-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="72a06-114">Boolean</span></span> |
| <span data-ttu-id="72a06-115">usedWindowsPhone</span><span class="sxs-lookup"><span data-stu-id="72a06-115">usedWindowsPhone</span></span>  | <span data-ttu-id="72a06-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="72a06-116">Boolean</span></span> |
| <span data-ttu-id="72a06-117">usedAndroidPhone</span><span class="sxs-lookup"><span data-stu-id="72a06-117">usedAndroidPhone</span></span>  | <span data-ttu-id="72a06-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="72a06-118">Boolean</span></span> |
| <span data-ttu-id="72a06-119">usediPhone</span><span class="sxs-lookup"><span data-stu-id="72a06-119">usediPhone</span></span>        | <span data-ttu-id="72a06-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="72a06-120">Boolean</span></span> |
| <span data-ttu-id="72a06-121">usediPad</span><span class="sxs-lookup"><span data-stu-id="72a06-121">usediPad</span></span>          | <span data-ttu-id="72a06-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="72a06-122">Boolean</span></span> |
| <span data-ttu-id="72a06-123">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="72a06-123">reportPeriod</span></span>      | <span data-ttu-id="72a06-124">String</span><span class="sxs-lookup"><span data-stu-id="72a06-124">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="72a06-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="72a06-125">JSON representation</span></span>

<span data-ttu-id="72a06-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="72a06-126">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessDeviceUsageUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "lastActivityDate": "Date", 
  "usedWindows": true, 
  "usedWindowsPhone": true, 
  "usedAndroidPhone": true, 
  "usediPhone": true, 
  "usediPad": true, 
  "reportPeriod": "String"
}
```
