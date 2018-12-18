---
title: tipo de recurso teamsDeviceUsageUserDetail
description: La siguiente es una representación JSON del recurso
author: nkramer
ms.openlocfilehash: 1947b66a59190945e5a6b823b47ef8df7d02683a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27329004"
---
# <a name="teamsdeviceusageuserdetail-resource-type"></a><span data-ttu-id="d6f1e-103">tipo de recurso teamsDeviceUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="d6f1e-103">teamsDeviceUsageUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="d6f1e-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6f1e-104">Properties</span></span>

| <span data-ttu-id="d6f1e-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d6f1e-105">Property</span></span>          | <span data-ttu-id="d6f1e-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6f1e-106">Type</span></span>    |
| :---------------- | :------ |
| <span data-ttu-id="d6f1e-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="d6f1e-107">reportRefreshDate</span></span> | <span data-ttu-id="d6f1e-108">Date</span><span class="sxs-lookup"><span data-stu-id="d6f1e-108">Date</span></span>    |
| <span data-ttu-id="d6f1e-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d6f1e-109">userPrincipalName</span></span> | <span data-ttu-id="d6f1e-110">String</span><span class="sxs-lookup"><span data-stu-id="d6f1e-110">String</span></span>  |
| <span data-ttu-id="d6f1e-111">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="d6f1e-111">lastActivityDate</span></span>  | <span data-ttu-id="d6f1e-112">Date</span><span class="sxs-lookup"><span data-stu-id="d6f1e-112">Date</span></span>    |
| <span data-ttu-id="d6f1e-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="d6f1e-113">isDeleted</span></span>         | <span data-ttu-id="d6f1e-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="d6f1e-114">Boolean</span></span> |
| <span data-ttu-id="d6f1e-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="d6f1e-115">deletedDate</span></span>       | <span data-ttu-id="d6f1e-116">Date</span><span class="sxs-lookup"><span data-stu-id="d6f1e-116">Date</span></span>    |
| <span data-ttu-id="d6f1e-117">usedWeb</span><span class="sxs-lookup"><span data-stu-id="d6f1e-117">usedWeb</span></span>           | <span data-ttu-id="d6f1e-118">Boolean</span><span class="sxs-lookup"><span data-stu-id="d6f1e-118">Boolean</span></span> |
| <span data-ttu-id="d6f1e-119">usedWindowsPhone</span><span class="sxs-lookup"><span data-stu-id="d6f1e-119">usedWindowsPhone</span></span>  | <span data-ttu-id="d6f1e-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="d6f1e-120">Boolean</span></span> |
| <span data-ttu-id="d6f1e-121">usediOS</span><span class="sxs-lookup"><span data-stu-id="d6f1e-121">usediOS</span></span>           | <span data-ttu-id="d6f1e-122">Boolean</span><span class="sxs-lookup"><span data-stu-id="d6f1e-122">Boolean</span></span> |
| <span data-ttu-id="d6f1e-123">usedMac</span><span class="sxs-lookup"><span data-stu-id="d6f1e-123">usedMac</span></span>           | <span data-ttu-id="d6f1e-124">Boolean</span><span class="sxs-lookup"><span data-stu-id="d6f1e-124">Boolean</span></span> |
| <span data-ttu-id="d6f1e-125">usedAndroidPhone</span><span class="sxs-lookup"><span data-stu-id="d6f1e-125">usedAndroidPhone</span></span>  | <span data-ttu-id="d6f1e-126">Boolean</span><span class="sxs-lookup"><span data-stu-id="d6f1e-126">Boolean</span></span> |
| <span data-ttu-id="d6f1e-127">usedWindows</span><span class="sxs-lookup"><span data-stu-id="d6f1e-127">usedWindows</span></span>       | <span data-ttu-id="d6f1e-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="d6f1e-128">Boolean</span></span> |
| <span data-ttu-id="d6f1e-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="d6f1e-129">reportPeriod</span></span>      | <span data-ttu-id="d6f1e-130">String</span><span class="sxs-lookup"><span data-stu-id="d6f1e-130">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="d6f1e-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d6f1e-131">JSON representation</span></span>

<span data-ttu-id="d6f1e-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d6f1e-132">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsDeviceUsageUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "lastActivityDate": "Date", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "usedWeb": true, 
  "usedWindowsPhone": true, 
  "usediOS": true, 
  "usedMac": true, 
  "usedAndroidPhone": true, 
  "usedWindows": true, 
  "reportPeriod": "String"
}
```
