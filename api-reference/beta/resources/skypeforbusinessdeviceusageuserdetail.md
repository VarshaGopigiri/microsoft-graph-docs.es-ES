---
title: tipo de recurso skypeForBusinessDeviceUsageUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 95f2f6cf1f3f6c54c4b6b4b39a7118cd8a94b224
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858383"
---
# <a name="skypeforbusinessdeviceusageuserdetail-resource-type"></a><span data-ttu-id="83983-103">tipo de recurso skypeForBusinessDeviceUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="83983-103">skypeForBusinessDeviceUsageUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="83983-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83983-104">Properties</span></span>

| <span data-ttu-id="83983-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="83983-105">Property</span></span>          | <span data-ttu-id="83983-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="83983-106">Type</span></span>    |
| :---------------- | :------ |
| <span data-ttu-id="83983-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="83983-107">reportRefreshDate</span></span> | <span data-ttu-id="83983-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="83983-108">Date</span></span>    |
| <span data-ttu-id="83983-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="83983-109">userPrincipalName</span></span> | <span data-ttu-id="83983-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="83983-110">String</span></span>  |
| <span data-ttu-id="83983-111">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="83983-111">lastActivityDate</span></span>  | <span data-ttu-id="83983-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="83983-112">Date</span></span>    |
| <span data-ttu-id="83983-113">usedWindows</span><span class="sxs-lookup"><span data-stu-id="83983-113">usedWindows</span></span>       | <span data-ttu-id="83983-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="83983-114">Boolean</span></span> |
| <span data-ttu-id="83983-115">usedWindowsPhone</span><span class="sxs-lookup"><span data-stu-id="83983-115">usedWindowsPhone</span></span>  | <span data-ttu-id="83983-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="83983-116">Boolean</span></span> |
| <span data-ttu-id="83983-117">usedAndroidPhone</span><span class="sxs-lookup"><span data-stu-id="83983-117">usedAndroidPhone</span></span>  | <span data-ttu-id="83983-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="83983-118">Boolean</span></span> |
| <span data-ttu-id="83983-119">usediPhone</span><span class="sxs-lookup"><span data-stu-id="83983-119">usediPhone</span></span>        | <span data-ttu-id="83983-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="83983-120">Boolean</span></span> |
| <span data-ttu-id="83983-121">usediPad</span><span class="sxs-lookup"><span data-stu-id="83983-121">usediPad</span></span>          | <span data-ttu-id="83983-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="83983-122">Boolean</span></span> |
| <span data-ttu-id="83983-123">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="83983-123">reportPeriod</span></span>      | <span data-ttu-id="83983-124">String</span><span class="sxs-lookup"><span data-stu-id="83983-124">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="83983-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="83983-125">JSON representation</span></span>

<span data-ttu-id="83983-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="83983-126">The following is a JSON representation of the resource.</span></span>

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
