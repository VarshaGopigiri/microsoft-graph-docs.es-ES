---
title: tipo de recurso teamsDeviceUsageUserDetail
description: La siguiente es una representación JSON del recurso
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 8cdd2fe1a212bb1d36846b80fc1b558c576deb47
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953788"
---
# <a name="teamsdeviceusageuserdetail-resource-type"></a><span data-ttu-id="5b026-103">tipo de recurso teamsDeviceUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="5b026-103">teamsDeviceUsageUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="5b026-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5b026-104">Properties</span></span>

| <span data-ttu-id="5b026-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5b026-105">Property</span></span>          | <span data-ttu-id="5b026-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="5b026-106">Type</span></span>    |
| :---------------- | :------ |
| <span data-ttu-id="5b026-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="5b026-107">reportRefreshDate</span></span> | <span data-ttu-id="5b026-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="5b026-108">Date</span></span>    |
| <span data-ttu-id="5b026-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5b026-109">userPrincipalName</span></span> | <span data-ttu-id="5b026-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="5b026-110">String</span></span>  |
| <span data-ttu-id="5b026-111">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="5b026-111">lastActivityDate</span></span>  | <span data-ttu-id="5b026-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="5b026-112">Date</span></span>    |
| <span data-ttu-id="5b026-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="5b026-113">isDeleted</span></span>         | <span data-ttu-id="5b026-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="5b026-114">Boolean</span></span> |
| <span data-ttu-id="5b026-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="5b026-115">deletedDate</span></span>       | <span data-ttu-id="5b026-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="5b026-116">Date</span></span>    |
| <span data-ttu-id="5b026-117">usedWeb</span><span class="sxs-lookup"><span data-stu-id="5b026-117">usedWeb</span></span>           | <span data-ttu-id="5b026-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="5b026-118">Boolean</span></span> |
| <span data-ttu-id="5b026-119">usedWindowsPhone</span><span class="sxs-lookup"><span data-stu-id="5b026-119">usedWindowsPhone</span></span>  | <span data-ttu-id="5b026-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="5b026-120">Boolean</span></span> |
| <span data-ttu-id="5b026-121">usediOS</span><span class="sxs-lookup"><span data-stu-id="5b026-121">usediOS</span></span>           | <span data-ttu-id="5b026-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="5b026-122">Boolean</span></span> |
| <span data-ttu-id="5b026-123">usedMac</span><span class="sxs-lookup"><span data-stu-id="5b026-123">usedMac</span></span>           | <span data-ttu-id="5b026-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="5b026-124">Boolean</span></span> |
| <span data-ttu-id="5b026-125">usedAndroidPhone</span><span class="sxs-lookup"><span data-stu-id="5b026-125">usedAndroidPhone</span></span>  | <span data-ttu-id="5b026-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="5b026-126">Boolean</span></span> |
| <span data-ttu-id="5b026-127">usedWindows</span><span class="sxs-lookup"><span data-stu-id="5b026-127">usedWindows</span></span>       | <span data-ttu-id="5b026-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="5b026-128">Boolean</span></span> |
| <span data-ttu-id="5b026-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="5b026-129">reportPeriod</span></span>      | <span data-ttu-id="5b026-130">String</span><span class="sxs-lookup"><span data-stu-id="5b026-130">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="5b026-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5b026-131">JSON representation</span></span>

<span data-ttu-id="5b026-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5b026-132">The following is a JSON representation of the resource.</span></span>

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
