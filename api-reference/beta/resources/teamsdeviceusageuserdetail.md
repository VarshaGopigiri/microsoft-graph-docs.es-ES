---
title: tipo de recurso teamsDeviceUsageUserDetail
description: La siguiente es una representación JSON del recurso
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 06e2cea1154c608b61642b07adbd96aae1710903
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27807108"
---
# <a name="teamsdeviceusageuserdetail-resource-type"></a><span data-ttu-id="5f397-103">tipo de recurso teamsDeviceUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="5f397-103">teamsDeviceUsageUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="5f397-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f397-104">Properties</span></span>

| <span data-ttu-id="5f397-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f397-105">Property</span></span>          | <span data-ttu-id="5f397-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f397-106">Type</span></span>    |
| :---------------- | :------ |
| <span data-ttu-id="5f397-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="5f397-107">reportRefreshDate</span></span> | <span data-ttu-id="5f397-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="5f397-108">Date</span></span>    |
| <span data-ttu-id="5f397-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5f397-109">userPrincipalName</span></span> | <span data-ttu-id="5f397-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="5f397-110">String</span></span>  |
| <span data-ttu-id="5f397-111">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="5f397-111">lastActivityDate</span></span>  | <span data-ttu-id="5f397-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="5f397-112">Date</span></span>    |
| <span data-ttu-id="5f397-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="5f397-113">isDeleted</span></span>         | <span data-ttu-id="5f397-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f397-114">Boolean</span></span> |
| <span data-ttu-id="5f397-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="5f397-115">deletedDate</span></span>       | <span data-ttu-id="5f397-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="5f397-116">Date</span></span>    |
| <span data-ttu-id="5f397-117">usedWeb</span><span class="sxs-lookup"><span data-stu-id="5f397-117">usedWeb</span></span>           | <span data-ttu-id="5f397-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f397-118">Boolean</span></span> |
| <span data-ttu-id="5f397-119">usedWindowsPhone</span><span class="sxs-lookup"><span data-stu-id="5f397-119">usedWindowsPhone</span></span>  | <span data-ttu-id="5f397-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f397-120">Boolean</span></span> |
| <span data-ttu-id="5f397-121">usediOS</span><span class="sxs-lookup"><span data-stu-id="5f397-121">usediOS</span></span>           | <span data-ttu-id="5f397-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f397-122">Boolean</span></span> |
| <span data-ttu-id="5f397-123">usedMac</span><span class="sxs-lookup"><span data-stu-id="5f397-123">usedMac</span></span>           | <span data-ttu-id="5f397-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f397-124">Boolean</span></span> |
| <span data-ttu-id="5f397-125">usedAndroidPhone</span><span class="sxs-lookup"><span data-stu-id="5f397-125">usedAndroidPhone</span></span>  | <span data-ttu-id="5f397-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f397-126">Boolean</span></span> |
| <span data-ttu-id="5f397-127">usedWindows</span><span class="sxs-lookup"><span data-stu-id="5f397-127">usedWindows</span></span>       | <span data-ttu-id="5f397-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f397-128">Boolean</span></span> |
| <span data-ttu-id="5f397-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="5f397-129">reportPeriod</span></span>      | <span data-ttu-id="5f397-130">String</span><span class="sxs-lookup"><span data-stu-id="5f397-130">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="5f397-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5f397-131">JSON representation</span></span>

<span data-ttu-id="5f397-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5f397-132">The following is a JSON representation of the resource.</span></span>

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
