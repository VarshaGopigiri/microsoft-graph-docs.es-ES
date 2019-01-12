---
title: tipo de recurso emailActivityUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: b871bf5dbaedd961fad09bf97be868f46e7430a1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938310"
---
# <a name="emailactivityuserdetail-resource-type"></a><span data-ttu-id="1f598-103">tipo de recurso emailActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="1f598-103">emailActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="1f598-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1f598-104">Properties</span></span>

| <span data-ttu-id="1f598-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1f598-105">Property</span></span>          | <span data-ttu-id="1f598-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f598-106">Type</span></span>              |
| :---------------- | :---------------- |
| <span data-ttu-id="1f598-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="1f598-107">reportRefreshDate</span></span> | <span data-ttu-id="1f598-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="1f598-108">Date</span></span>              |
| <span data-ttu-id="1f598-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1f598-109">userPrincipalName</span></span> | <span data-ttu-id="1f598-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="1f598-110">String</span></span>            |
| <span data-ttu-id="1f598-111">displayName</span><span class="sxs-lookup"><span data-stu-id="1f598-111">displayName</span></span>       | <span data-ttu-id="1f598-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="1f598-112">String</span></span>            |
| <span data-ttu-id="1f598-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="1f598-113">isDeleted</span></span>         | <span data-ttu-id="1f598-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="1f598-114">Boolean</span></span>           |
| <span data-ttu-id="1f598-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="1f598-115">deletedDate</span></span>       | <span data-ttu-id="1f598-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="1f598-116">Date</span></span>              |
| <span data-ttu-id="1f598-117">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="1f598-117">lastActivityDate</span></span>  | <span data-ttu-id="1f598-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="1f598-118">Date</span></span>              |
| <span data-ttu-id="1f598-119">sendCount</span><span class="sxs-lookup"><span data-stu-id="1f598-119">sendCount</span></span>         | <span data-ttu-id="1f598-120">Int64</span><span class="sxs-lookup"><span data-stu-id="1f598-120">Int64</span></span>             |
| <span data-ttu-id="1f598-121">receiveCount</span><span class="sxs-lookup"><span data-stu-id="1f598-121">receiveCount</span></span>      | <span data-ttu-id="1f598-122">Int64</span><span class="sxs-lookup"><span data-stu-id="1f598-122">Int64</span></span>             |
| <span data-ttu-id="1f598-123">readCount</span><span class="sxs-lookup"><span data-stu-id="1f598-123">readCount</span></span>         | <span data-ttu-id="1f598-124">Int64</span><span class="sxs-lookup"><span data-stu-id="1f598-124">Int64</span></span>             |
| <span data-ttu-id="1f598-125">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="1f598-125">assignedProducts</span></span>  | <span data-ttu-id="1f598-126">Colección String</span><span class="sxs-lookup"><span data-stu-id="1f598-126">String collection</span></span> |
| <span data-ttu-id="1f598-127">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="1f598-127">reportPeriod</span></span>      | <span data-ttu-id="1f598-128">String</span><span class="sxs-lookup"><span data-stu-id="1f598-128">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="1f598-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1f598-129">JSON representation</span></span>

<span data-ttu-id="1f598-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1f598-130">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.emailActivityUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "displayName": "String", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "lastActivityDate": "Date", 
  "sendCount": 1024, 
  "receiveCount": 1024, 
  "readCount": 1024, 
  "assignedProducts": ["String"], 
  "reportPeriod": "String"
}
```
