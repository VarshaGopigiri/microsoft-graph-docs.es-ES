---
title: tipo de recurso oneDriveUsageAccountDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 4b80ebc24aa45be0368dbb59d6d3e99e7adacc8c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088033"
---
# <a name="onedriveusageaccountdetail-resource-type"></a><span data-ttu-id="a7439-103">tipo de recurso oneDriveUsageAccountDetail</span><span class="sxs-lookup"><span data-stu-id="a7439-103">oneDriveUsageAccountDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="a7439-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a7439-104">Properties</span></span>

| <span data-ttu-id="a7439-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7439-105">Property</span></span>                | <span data-ttu-id="a7439-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7439-106">Type</span></span>    |
| :---------------------- | :------ |
| <span data-ttu-id="a7439-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="a7439-107">reportRefreshDate</span></span>       | <span data-ttu-id="a7439-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="a7439-108">Date</span></span>    |
| <span data-ttu-id="a7439-109">siteUrl</span><span class="sxs-lookup"><span data-stu-id="a7439-109">siteUrl</span></span>                 | <span data-ttu-id="a7439-110">String</span><span class="sxs-lookup"><span data-stu-id="a7439-110">String</span></span>  |
| <span data-ttu-id="a7439-111">ownerDisplayName</span><span class="sxs-lookup"><span data-stu-id="a7439-111">ownerDisplayName</span></span>        | <span data-ttu-id="a7439-112">String</span><span class="sxs-lookup"><span data-stu-id="a7439-112">String</span></span>  |
| <span data-ttu-id="a7439-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="a7439-113">isDeleted</span></span>               | <span data-ttu-id="a7439-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="a7439-114">Boolean</span></span> |
| <span data-ttu-id="a7439-115">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="a7439-115">lastActivityDate</span></span>        | <span data-ttu-id="a7439-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="a7439-116">Date</span></span>    |
| <span data-ttu-id="a7439-117">fileCount</span><span class="sxs-lookup"><span data-stu-id="a7439-117">fileCount</span></span>               | <span data-ttu-id="a7439-118">Int64</span><span class="sxs-lookup"><span data-stu-id="a7439-118">Int64</span></span>   |
| <span data-ttu-id="a7439-119">activeFileCount</span><span class="sxs-lookup"><span data-stu-id="a7439-119">activeFileCount</span></span>         | <span data-ttu-id="a7439-120">Int64</span><span class="sxs-lookup"><span data-stu-id="a7439-120">Int64</span></span>   |
| <span data-ttu-id="a7439-121">storageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="a7439-121">storageUsedInBytes</span></span>      | <span data-ttu-id="a7439-122">Int64</span><span class="sxs-lookup"><span data-stu-id="a7439-122">Int64</span></span>   |
| <span data-ttu-id="a7439-123">storageAllocatedInBytes</span><span class="sxs-lookup"><span data-stu-id="a7439-123">storageAllocatedInBytes</span></span> | <span data-ttu-id="a7439-124">Int64</span><span class="sxs-lookup"><span data-stu-id="a7439-124">Int64</span></span>   |
| <span data-ttu-id="a7439-125">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="a7439-125">reportPeriod</span></span>            | <span data-ttu-id="a7439-126">String</span><span class="sxs-lookup"><span data-stu-id="a7439-126">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="a7439-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a7439-127">JSON representation</span></span>

<span data-ttu-id="a7439-128">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a7439-128">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.oneDriveUsageAccountDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "siteUrl": "String", 
  "ownerDisplayName": "String", 
  "isDeleted": true, 
  "lastActivityDate": "Date", 
  "fileCount": 1024, 
  "activeFileCount": 1024, 
  "storageUsedInBytes": 1024, 
  "storageAllocatedInBytes": 1024, 
  "reportPeriod": "String"
}
```
