---
title: tipo de recurso oneDriveUsageAccountDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 92695f509302ede4b3ce64320e8f4ed42418f7e5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842612"
---
# <a name="onedriveusageaccountdetail-resource-type"></a><span data-ttu-id="fc549-103">tipo de recurso oneDriveUsageAccountDetail</span><span class="sxs-lookup"><span data-stu-id="fc549-103">oneDriveUsageAccountDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="fc549-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc549-104">Properties</span></span>

| <span data-ttu-id="fc549-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fc549-105">Property</span></span>                | <span data-ttu-id="fc549-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc549-106">Type</span></span>    |
| :---------------------- | :------ |
| <span data-ttu-id="fc549-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="fc549-107">reportRefreshDate</span></span>       | <span data-ttu-id="fc549-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="fc549-108">Date</span></span>    |
| <span data-ttu-id="fc549-109">siteUrl</span><span class="sxs-lookup"><span data-stu-id="fc549-109">siteUrl</span></span>                 | <span data-ttu-id="fc549-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="fc549-110">String</span></span>  |
| <span data-ttu-id="fc549-111">ownerDisplayName</span><span class="sxs-lookup"><span data-stu-id="fc549-111">ownerDisplayName</span></span>        | <span data-ttu-id="fc549-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="fc549-112">String</span></span>  |
| <span data-ttu-id="fc549-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="fc549-113">isDeleted</span></span>               | <span data-ttu-id="fc549-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="fc549-114">Boolean</span></span> |
| <span data-ttu-id="fc549-115">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="fc549-115">lastActivityDate</span></span>        | <span data-ttu-id="fc549-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="fc549-116">Date</span></span>    |
| <span data-ttu-id="fc549-117">fileCount</span><span class="sxs-lookup"><span data-stu-id="fc549-117">fileCount</span></span>               | <span data-ttu-id="fc549-118">Int64</span><span class="sxs-lookup"><span data-stu-id="fc549-118">Int64</span></span>   |
| <span data-ttu-id="fc549-119">activeFileCount</span><span class="sxs-lookup"><span data-stu-id="fc549-119">activeFileCount</span></span>         | <span data-ttu-id="fc549-120">Int64</span><span class="sxs-lookup"><span data-stu-id="fc549-120">Int64</span></span>   |
| <span data-ttu-id="fc549-121">storageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="fc549-121">storageUsedInBytes</span></span>      | <span data-ttu-id="fc549-122">Int64</span><span class="sxs-lookup"><span data-stu-id="fc549-122">Int64</span></span>   |
| <span data-ttu-id="fc549-123">storageAllocatedInBytes</span><span class="sxs-lookup"><span data-stu-id="fc549-123">storageAllocatedInBytes</span></span> | <span data-ttu-id="fc549-124">Int64</span><span class="sxs-lookup"><span data-stu-id="fc549-124">Int64</span></span>   |
| <span data-ttu-id="fc549-125">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="fc549-125">reportPeriod</span></span>            | <span data-ttu-id="fc549-126">String</span><span class="sxs-lookup"><span data-stu-id="fc549-126">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="fc549-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fc549-127">JSON representation</span></span>

<span data-ttu-id="fc549-128">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fc549-128">The following is a JSON representation of the resource.</span></span>

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
