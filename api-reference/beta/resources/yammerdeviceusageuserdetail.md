---
title: tipo de recurso yammerDeviceUsageUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 2b74222c1a636fac271268e228c8140e7d1cf33f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912011"
---
# <a name="yammerdeviceusageuserdetail-resource-type"></a><span data-ttu-id="14ec8-103">tipo de recurso yammerDeviceUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="14ec8-103">yammerDeviceUsageUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="14ec8-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14ec8-104">Properties</span></span>

| <span data-ttu-id="14ec8-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="14ec8-105">Property</span></span>          | <span data-ttu-id="14ec8-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="14ec8-106">Type</span></span>    |
| :---------------- | :------ |
| <span data-ttu-id="14ec8-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="14ec8-107">reportRefreshDate</span></span> | <span data-ttu-id="14ec8-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="14ec8-108">Date</span></span>    |
| <span data-ttu-id="14ec8-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="14ec8-109">userPrincipalName</span></span> | <span data-ttu-id="14ec8-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="14ec8-110">String</span></span>  |
| <span data-ttu-id="14ec8-111">displayName</span><span class="sxs-lookup"><span data-stu-id="14ec8-111">displayName</span></span>       | <span data-ttu-id="14ec8-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="14ec8-112">String</span></span>  |
| <span data-ttu-id="14ec8-113">userState</span><span class="sxs-lookup"><span data-stu-id="14ec8-113">userState</span></span>         | <span data-ttu-id="14ec8-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="14ec8-114">String</span></span>  |
| <span data-ttu-id="14ec8-115">stateChangeDate</span><span class="sxs-lookup"><span data-stu-id="14ec8-115">stateChangeDate</span></span>   | <span data-ttu-id="14ec8-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="14ec8-116">Date</span></span>    |
| <span data-ttu-id="14ec8-117">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="14ec8-117">lastActivityDate</span></span>  | <span data-ttu-id="14ec8-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="14ec8-118">Date</span></span>    |
| <span data-ttu-id="14ec8-119">usedWeb</span><span class="sxs-lookup"><span data-stu-id="14ec8-119">usedWeb</span></span>           | <span data-ttu-id="14ec8-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="14ec8-120">Boolean</span></span> |
| <span data-ttu-id="14ec8-121">usedWindowsPhone</span><span class="sxs-lookup"><span data-stu-id="14ec8-121">usedWindowsPhone</span></span>  | <span data-ttu-id="14ec8-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="14ec8-122">Boolean</span></span> |
| <span data-ttu-id="14ec8-123">usedAndroidPhone</span><span class="sxs-lookup"><span data-stu-id="14ec8-123">usedAndroidPhone</span></span>  | <span data-ttu-id="14ec8-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="14ec8-124">Boolean</span></span> |
| <span data-ttu-id="14ec8-125">usediPhone</span><span class="sxs-lookup"><span data-stu-id="14ec8-125">usediPhone</span></span>        | <span data-ttu-id="14ec8-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="14ec8-126">Boolean</span></span> |
| <span data-ttu-id="14ec8-127">usediPad</span><span class="sxs-lookup"><span data-stu-id="14ec8-127">usediPad</span></span>          | <span data-ttu-id="14ec8-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="14ec8-128">Boolean</span></span> |
| <span data-ttu-id="14ec8-129">usedOthers</span><span class="sxs-lookup"><span data-stu-id="14ec8-129">usedOthers</span></span>        | <span data-ttu-id="14ec8-130">Booleano</span><span class="sxs-lookup"><span data-stu-id="14ec8-130">Boolean</span></span> |
| <span data-ttu-id="14ec8-131">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="14ec8-131">reportPeriod</span></span>      | <span data-ttu-id="14ec8-132">String</span><span class="sxs-lookup"><span data-stu-id="14ec8-132">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="14ec8-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="14ec8-133">JSON representation</span></span>

<span data-ttu-id="14ec8-134">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="14ec8-134">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yammerDeviceUsageUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "displayName": "String", 
  "userState": "String", 
  "stateChangeDate": "Date", 
  "lastActivityDate": "Date", 
  "usedWeb": true, 
  "usedWindowsPhone": true, 
  "usedAndroidPhone": true, 
  "usediPhone": true, 
  "usediPad": true, 
  "usedOthers": true, 
  "reportPeriod": "String"
}
```
