---
title: tipo de recurso sharePointActivityUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: a5b6de8a4a9b82d9e6d34a2ae289f0c7589798ee
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083811"
---
# <a name="sharepointactivityuserdetail-resource-type"></a><span data-ttu-id="ef40d-103">tipo de recurso sharePointActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="ef40d-103">sharePointActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="ef40d-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ef40d-104">Properties</span></span>

| <span data-ttu-id="ef40d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ef40d-105">Property</span></span>                  | <span data-ttu-id="ef40d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef40d-106">Type</span></span>              |
| :------------------------ | :---------------- |
| <span data-ttu-id="ef40d-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="ef40d-107">reportRefreshDate</span></span>         | <span data-ttu-id="ef40d-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="ef40d-108">Date</span></span>              |
| <span data-ttu-id="ef40d-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ef40d-109">userPrincipalName</span></span>         | <span data-ttu-id="ef40d-110">String</span><span class="sxs-lookup"><span data-stu-id="ef40d-110">String</span></span>            |
| <span data-ttu-id="ef40d-111">isDeleted</span><span class="sxs-lookup"><span data-stu-id="ef40d-111">isDeleted</span></span>                 | <span data-ttu-id="ef40d-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="ef40d-112">Boolean</span></span>           |
| <span data-ttu-id="ef40d-113">deletedDate</span><span class="sxs-lookup"><span data-stu-id="ef40d-113">deletedDate</span></span>               | <span data-ttu-id="ef40d-114">Fecha</span><span class="sxs-lookup"><span data-stu-id="ef40d-114">Date</span></span>              |
| <span data-ttu-id="ef40d-115">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="ef40d-115">lastActivityDate</span></span>          | <span data-ttu-id="ef40d-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="ef40d-116">Date</span></span>              |
| <span data-ttu-id="ef40d-117">viewedOrEditedFileCount</span><span class="sxs-lookup"><span data-stu-id="ef40d-117">viewedOrEditedFileCount</span></span>   | <span data-ttu-id="ef40d-118">Int64</span><span class="sxs-lookup"><span data-stu-id="ef40d-118">Int64</span></span>             |
| <span data-ttu-id="ef40d-119">syncedFileCount</span><span class="sxs-lookup"><span data-stu-id="ef40d-119">syncedFileCount</span></span>           | <span data-ttu-id="ef40d-120">Int64</span><span class="sxs-lookup"><span data-stu-id="ef40d-120">Int64</span></span>             |
| <span data-ttu-id="ef40d-121">sharedInternallyFileCount</span><span class="sxs-lookup"><span data-stu-id="ef40d-121">sharedInternallyFileCount</span></span> | <span data-ttu-id="ef40d-122">Int64</span><span class="sxs-lookup"><span data-stu-id="ef40d-122">Int64</span></span>             |
| <span data-ttu-id="ef40d-123">sharedExternallyFileCount</span><span class="sxs-lookup"><span data-stu-id="ef40d-123">sharedExternallyFileCount</span></span> | <span data-ttu-id="ef40d-124">Int64</span><span class="sxs-lookup"><span data-stu-id="ef40d-124">Int64</span></span>             |
| <span data-ttu-id="ef40d-125">visitedPageCount</span><span class="sxs-lookup"><span data-stu-id="ef40d-125">visitedPageCount</span></span>          | <span data-ttu-id="ef40d-126">Int64</span><span class="sxs-lookup"><span data-stu-id="ef40d-126">Int64</span></span>             |
| <span data-ttu-id="ef40d-127">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="ef40d-127">assignedProducts</span></span>          | <span data-ttu-id="ef40d-128">Colección String</span><span class="sxs-lookup"><span data-stu-id="ef40d-128">String collection</span></span> |
| <span data-ttu-id="ef40d-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="ef40d-129">reportPeriod</span></span>              | <span data-ttu-id="ef40d-130">String</span><span class="sxs-lookup"><span data-stu-id="ef40d-130">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="ef40d-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ef40d-131">JSON representation</span></span>

<span data-ttu-id="ef40d-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ef40d-132">The following is a JSON representation of the resource.</span></span>

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
