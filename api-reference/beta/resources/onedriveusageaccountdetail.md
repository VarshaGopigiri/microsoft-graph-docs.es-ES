---
title: tipo de recurso oneDriveUsageAccountDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 9c13e03d1170b0ebbc53394541c4564c60c67e78
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957399"
---
# <a name="onedriveusageaccountdetail-resource-type"></a><span data-ttu-id="6e201-103">tipo de recurso oneDriveUsageAccountDetail</span><span class="sxs-lookup"><span data-stu-id="6e201-103">oneDriveUsageAccountDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="6e201-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e201-104">Properties</span></span>

| <span data-ttu-id="6e201-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6e201-105">Property</span></span>                | <span data-ttu-id="6e201-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e201-106">Type</span></span>    |
| :---------------------- | :------ |
| <span data-ttu-id="6e201-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="6e201-107">reportRefreshDate</span></span>       | <span data-ttu-id="6e201-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="6e201-108">Date</span></span>    |
| <span data-ttu-id="6e201-109">siteUrl</span><span class="sxs-lookup"><span data-stu-id="6e201-109">siteUrl</span></span>                 | <span data-ttu-id="6e201-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="6e201-110">String</span></span>  |
| <span data-ttu-id="6e201-111">ownerDisplayName</span><span class="sxs-lookup"><span data-stu-id="6e201-111">ownerDisplayName</span></span>        | <span data-ttu-id="6e201-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="6e201-112">String</span></span>  |
| <span data-ttu-id="6e201-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="6e201-113">isDeleted</span></span>               | <span data-ttu-id="6e201-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="6e201-114">Boolean</span></span> |
| <span data-ttu-id="6e201-115">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="6e201-115">lastActivityDate</span></span>        | <span data-ttu-id="6e201-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="6e201-116">Date</span></span>    |
| <span data-ttu-id="6e201-117">fileCount</span><span class="sxs-lookup"><span data-stu-id="6e201-117">fileCount</span></span>               | <span data-ttu-id="6e201-118">Int64</span><span class="sxs-lookup"><span data-stu-id="6e201-118">Int64</span></span>   |
| <span data-ttu-id="6e201-119">activeFileCount</span><span class="sxs-lookup"><span data-stu-id="6e201-119">activeFileCount</span></span>         | <span data-ttu-id="6e201-120">Int64</span><span class="sxs-lookup"><span data-stu-id="6e201-120">Int64</span></span>   |
| <span data-ttu-id="6e201-121">storageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="6e201-121">storageUsedInBytes</span></span>      | <span data-ttu-id="6e201-122">Int64</span><span class="sxs-lookup"><span data-stu-id="6e201-122">Int64</span></span>   |
| <span data-ttu-id="6e201-123">storageAllocatedInBytes</span><span class="sxs-lookup"><span data-stu-id="6e201-123">storageAllocatedInBytes</span></span> | <span data-ttu-id="6e201-124">Int64</span><span class="sxs-lookup"><span data-stu-id="6e201-124">Int64</span></span>   |
| <span data-ttu-id="6e201-125">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="6e201-125">reportPeriod</span></span>            | <span data-ttu-id="6e201-126">String</span><span class="sxs-lookup"><span data-stu-id="6e201-126">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="6e201-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6e201-127">JSON representation</span></span>

<span data-ttu-id="6e201-128">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6e201-128">The following is a JSON representation of the resource.</span></span>

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
