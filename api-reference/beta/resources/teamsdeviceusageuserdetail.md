---
title: tipo de recurso teamsDeviceUsageUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 4eeec5f07a0a604249617ac87a62ea12b4052395
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090432"
---
# <a name="teamsdeviceusageuserdetail-resource-type"></a><span data-ttu-id="ab67b-103">tipo de recurso teamsDeviceUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="ab67b-103">teamsDeviceUsageUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="ab67b-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab67b-104">Properties</span></span>

| <span data-ttu-id="ab67b-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab67b-105">Property</span></span>          | <span data-ttu-id="ab67b-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab67b-106">Type</span></span>    |
| :---------------- | :------ |
| <span data-ttu-id="ab67b-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="ab67b-107">reportRefreshDate</span></span> | <span data-ttu-id="ab67b-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="ab67b-108">Date</span></span>    |
| <span data-ttu-id="ab67b-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ab67b-109">userPrincipalName</span></span> | <span data-ttu-id="ab67b-110">String</span><span class="sxs-lookup"><span data-stu-id="ab67b-110">String</span></span>  |
| <span data-ttu-id="ab67b-111">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="ab67b-111">lastActivityDate</span></span>  | <span data-ttu-id="ab67b-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="ab67b-112">Date</span></span>    |
| <span data-ttu-id="ab67b-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="ab67b-113">isDeleted</span></span>         | <span data-ttu-id="ab67b-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="ab67b-114">Boolean</span></span> |
| <span data-ttu-id="ab67b-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="ab67b-115">deletedDate</span></span>       | <span data-ttu-id="ab67b-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="ab67b-116">Date</span></span>    |
| <span data-ttu-id="ab67b-117">usedWeb</span><span class="sxs-lookup"><span data-stu-id="ab67b-117">usedWeb</span></span>           | <span data-ttu-id="ab67b-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="ab67b-118">Boolean</span></span> |
| <span data-ttu-id="ab67b-119">usedWindowsPhone</span><span class="sxs-lookup"><span data-stu-id="ab67b-119">usedWindowsPhone</span></span>  | <span data-ttu-id="ab67b-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="ab67b-120">Boolean</span></span> |
| <span data-ttu-id="ab67b-121">usediOS</span><span class="sxs-lookup"><span data-stu-id="ab67b-121">usediOS</span></span>           | <span data-ttu-id="ab67b-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="ab67b-122">Boolean</span></span> |
| <span data-ttu-id="ab67b-123">usedMac</span><span class="sxs-lookup"><span data-stu-id="ab67b-123">usedMac</span></span>           | <span data-ttu-id="ab67b-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="ab67b-124">Boolean</span></span> |
| <span data-ttu-id="ab67b-125">usedAndroidPhone</span><span class="sxs-lookup"><span data-stu-id="ab67b-125">usedAndroidPhone</span></span>  | <span data-ttu-id="ab67b-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="ab67b-126">Boolean</span></span> |
| <span data-ttu-id="ab67b-127">usedWindows</span><span class="sxs-lookup"><span data-stu-id="ab67b-127">usedWindows</span></span>       | <span data-ttu-id="ab67b-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="ab67b-128">Boolean</span></span> |
| <span data-ttu-id="ab67b-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="ab67b-129">reportPeriod</span></span>      | <span data-ttu-id="ab67b-130">String</span><span class="sxs-lookup"><span data-stu-id="ab67b-130">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="ab67b-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ab67b-131">JSON representation</span></span>

<span data-ttu-id="ab67b-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ab67b-132">The following is a JSON representation of the resource.</span></span>

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
