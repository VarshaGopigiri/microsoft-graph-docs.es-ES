---
title: tipo de recurso sharePointActivityUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 4503739a7b2e13cade72951ae56ab410f22608b9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880699"
---
# <a name="sharepointactivityuserdetail-resource-type"></a><span data-ttu-id="c8142-103">tipo de recurso sharePointActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="c8142-103">sharePointActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="c8142-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8142-104">Properties</span></span>

| <span data-ttu-id="c8142-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c8142-105">Property</span></span>                  | <span data-ttu-id="c8142-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8142-106">Type</span></span>              |
| :------------------------ | :---------------- |
| <span data-ttu-id="c8142-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="c8142-107">reportRefreshDate</span></span>         | <span data-ttu-id="c8142-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="c8142-108">Date</span></span>              |
| <span data-ttu-id="c8142-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c8142-109">userPrincipalName</span></span>         | <span data-ttu-id="c8142-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8142-110">String</span></span>            |
| <span data-ttu-id="c8142-111">isDeleted</span><span class="sxs-lookup"><span data-stu-id="c8142-111">isDeleted</span></span>                 | <span data-ttu-id="c8142-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8142-112">Boolean</span></span>           |
| <span data-ttu-id="c8142-113">deletedDate</span><span class="sxs-lookup"><span data-stu-id="c8142-113">deletedDate</span></span>               | <span data-ttu-id="c8142-114">Fecha</span><span class="sxs-lookup"><span data-stu-id="c8142-114">Date</span></span>              |
| <span data-ttu-id="c8142-115">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="c8142-115">lastActivityDate</span></span>          | <span data-ttu-id="c8142-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="c8142-116">Date</span></span>              |
| <span data-ttu-id="c8142-117">viewedOrEditedFileCount</span><span class="sxs-lookup"><span data-stu-id="c8142-117">viewedOrEditedFileCount</span></span>   | <span data-ttu-id="c8142-118">Int64</span><span class="sxs-lookup"><span data-stu-id="c8142-118">Int64</span></span>             |
| <span data-ttu-id="c8142-119">syncedFileCount</span><span class="sxs-lookup"><span data-stu-id="c8142-119">syncedFileCount</span></span>           | <span data-ttu-id="c8142-120">Int64</span><span class="sxs-lookup"><span data-stu-id="c8142-120">Int64</span></span>             |
| <span data-ttu-id="c8142-121">sharedInternallyFileCount</span><span class="sxs-lookup"><span data-stu-id="c8142-121">sharedInternallyFileCount</span></span> | <span data-ttu-id="c8142-122">Int64</span><span class="sxs-lookup"><span data-stu-id="c8142-122">Int64</span></span>             |
| <span data-ttu-id="c8142-123">sharedExternallyFileCount</span><span class="sxs-lookup"><span data-stu-id="c8142-123">sharedExternallyFileCount</span></span> | <span data-ttu-id="c8142-124">Int64</span><span class="sxs-lookup"><span data-stu-id="c8142-124">Int64</span></span>             |
| <span data-ttu-id="c8142-125">visitedPageCount</span><span class="sxs-lookup"><span data-stu-id="c8142-125">visitedPageCount</span></span>          | <span data-ttu-id="c8142-126">Int64</span><span class="sxs-lookup"><span data-stu-id="c8142-126">Int64</span></span>             |
| <span data-ttu-id="c8142-127">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="c8142-127">assignedProducts</span></span>          | <span data-ttu-id="c8142-128">Colección String</span><span class="sxs-lookup"><span data-stu-id="c8142-128">String collection</span></span> |
| <span data-ttu-id="c8142-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="c8142-129">reportPeriod</span></span>              | <span data-ttu-id="c8142-130">String</span><span class="sxs-lookup"><span data-stu-id="c8142-130">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="c8142-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c8142-131">JSON representation</span></span>

<span data-ttu-id="c8142-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="c8142-132">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.sharePointActivityUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "lastActivityDate": "Date", 
  "viewedOrEditedFileCount": 1024, 
  "syncedFileCount": 1024, 
  "sharedInternallyFileCount": 1024, 
  "sharedExternallyFileCount": 1024, 
  "visitedPageCount": 1024, 
  "assignedProducts": ["String"], 
  "reportPeriod": "String"
}
```
