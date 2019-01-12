---
title: tipo de recurso sharePointActivityUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: a7dc324d821dca26ff1083f1e48c258e1955d72f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979946"
---
# <a name="sharepointactivityuserdetail-resource-type"></a><span data-ttu-id="14ab5-103">tipo de recurso sharePointActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="14ab5-103">sharePointActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="14ab5-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14ab5-104">Properties</span></span>

| <span data-ttu-id="14ab5-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="14ab5-105">Property</span></span>                  | <span data-ttu-id="14ab5-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="14ab5-106">Type</span></span>              |
| :------------------------ | :---------------- |
| <span data-ttu-id="14ab5-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="14ab5-107">reportRefreshDate</span></span>         | <span data-ttu-id="14ab5-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="14ab5-108">Date</span></span>              |
| <span data-ttu-id="14ab5-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="14ab5-109">userPrincipalName</span></span>         | <span data-ttu-id="14ab5-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="14ab5-110">String</span></span>            |
| <span data-ttu-id="14ab5-111">isDeleted</span><span class="sxs-lookup"><span data-stu-id="14ab5-111">isDeleted</span></span>                 | <span data-ttu-id="14ab5-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="14ab5-112">Boolean</span></span>           |
| <span data-ttu-id="14ab5-113">deletedDate</span><span class="sxs-lookup"><span data-stu-id="14ab5-113">deletedDate</span></span>               | <span data-ttu-id="14ab5-114">Fecha</span><span class="sxs-lookup"><span data-stu-id="14ab5-114">Date</span></span>              |
| <span data-ttu-id="14ab5-115">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="14ab5-115">lastActivityDate</span></span>          | <span data-ttu-id="14ab5-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="14ab5-116">Date</span></span>              |
| <span data-ttu-id="14ab5-117">viewedOrEditedFileCount</span><span class="sxs-lookup"><span data-stu-id="14ab5-117">viewedOrEditedFileCount</span></span>   | <span data-ttu-id="14ab5-118">Int64</span><span class="sxs-lookup"><span data-stu-id="14ab5-118">Int64</span></span>             |
| <span data-ttu-id="14ab5-119">syncedFileCount</span><span class="sxs-lookup"><span data-stu-id="14ab5-119">syncedFileCount</span></span>           | <span data-ttu-id="14ab5-120">Int64</span><span class="sxs-lookup"><span data-stu-id="14ab5-120">Int64</span></span>             |
| <span data-ttu-id="14ab5-121">sharedInternallyFileCount</span><span class="sxs-lookup"><span data-stu-id="14ab5-121">sharedInternallyFileCount</span></span> | <span data-ttu-id="14ab5-122">Int64</span><span class="sxs-lookup"><span data-stu-id="14ab5-122">Int64</span></span>             |
| <span data-ttu-id="14ab5-123">sharedExternallyFileCount</span><span class="sxs-lookup"><span data-stu-id="14ab5-123">sharedExternallyFileCount</span></span> | <span data-ttu-id="14ab5-124">Int64</span><span class="sxs-lookup"><span data-stu-id="14ab5-124">Int64</span></span>             |
| <span data-ttu-id="14ab5-125">visitedPageCount</span><span class="sxs-lookup"><span data-stu-id="14ab5-125">visitedPageCount</span></span>          | <span data-ttu-id="14ab5-126">Int64</span><span class="sxs-lookup"><span data-stu-id="14ab5-126">Int64</span></span>             |
| <span data-ttu-id="14ab5-127">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="14ab5-127">assignedProducts</span></span>          | <span data-ttu-id="14ab5-128">Colección String</span><span class="sxs-lookup"><span data-stu-id="14ab5-128">String collection</span></span> |
| <span data-ttu-id="14ab5-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="14ab5-129">reportPeriod</span></span>              | <span data-ttu-id="14ab5-130">String</span><span class="sxs-lookup"><span data-stu-id="14ab5-130">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="14ab5-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="14ab5-131">JSON representation</span></span>

<span data-ttu-id="14ab5-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="14ab5-132">The following is a JSON representation of the resource.</span></span>

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
