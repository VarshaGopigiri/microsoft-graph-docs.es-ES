---
title: tipo de recurso oneDriveActivityUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 29c9c8b723d4f87fa9858e26906878c973b37b09
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948250"
---
# <a name="onedriveactivityuserdetail-resource-type"></a><span data-ttu-id="f476d-103">tipo de recurso oneDriveActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="f476d-103">oneDriveActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="f476d-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f476d-104">Properties</span></span>

| <span data-ttu-id="f476d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f476d-105">Property</span></span>                  | <span data-ttu-id="f476d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f476d-106">Type</span></span>              |
| :------------------------ | :---------------- |
| <span data-ttu-id="f476d-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="f476d-107">reportRefreshDate</span></span>         | <span data-ttu-id="f476d-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="f476d-108">Date</span></span>              |
| <span data-ttu-id="f476d-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f476d-109">userPrincipalName</span></span>         | <span data-ttu-id="f476d-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="f476d-110">String</span></span>            |
| <span data-ttu-id="f476d-111">isDeleted</span><span class="sxs-lookup"><span data-stu-id="f476d-111">isDeleted</span></span>                 | <span data-ttu-id="f476d-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="f476d-112">Boolean</span></span>           |
| <span data-ttu-id="f476d-113">deletedDate</span><span class="sxs-lookup"><span data-stu-id="f476d-113">deletedDate</span></span>               | <span data-ttu-id="f476d-114">Fecha</span><span class="sxs-lookup"><span data-stu-id="f476d-114">Date</span></span>              |
| <span data-ttu-id="f476d-115">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="f476d-115">lastActivityDate</span></span>          | <span data-ttu-id="f476d-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="f476d-116">Date</span></span>              |
| <span data-ttu-id="f476d-117">viewedOrEditedFileCount</span><span class="sxs-lookup"><span data-stu-id="f476d-117">viewedOrEditedFileCount</span></span>   | <span data-ttu-id="f476d-118">Int64</span><span class="sxs-lookup"><span data-stu-id="f476d-118">Int64</span></span>             |
| <span data-ttu-id="f476d-119">syncedFileCount</span><span class="sxs-lookup"><span data-stu-id="f476d-119">syncedFileCount</span></span>           | <span data-ttu-id="f476d-120">Int64</span><span class="sxs-lookup"><span data-stu-id="f476d-120">Int64</span></span>             |
| <span data-ttu-id="f476d-121">sharedInternallyFileCount</span><span class="sxs-lookup"><span data-stu-id="f476d-121">sharedInternallyFileCount</span></span> | <span data-ttu-id="f476d-122">Int64</span><span class="sxs-lookup"><span data-stu-id="f476d-122">Int64</span></span>             |
| <span data-ttu-id="f476d-123">sharedExternallyFileCount</span><span class="sxs-lookup"><span data-stu-id="f476d-123">sharedExternallyFileCount</span></span> | <span data-ttu-id="f476d-124">Int64</span><span class="sxs-lookup"><span data-stu-id="f476d-124">Int64</span></span>             |
| <span data-ttu-id="f476d-125">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="f476d-125">assignedProducts</span></span>          | <span data-ttu-id="f476d-126">Colección String</span><span class="sxs-lookup"><span data-stu-id="f476d-126">String collection</span></span> |
| <span data-ttu-id="f476d-127">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="f476d-127">reportPeriod</span></span>              | <span data-ttu-id="f476d-128">String</span><span class="sxs-lookup"><span data-stu-id="f476d-128">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="f476d-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f476d-129">JSON representation</span></span>

<span data-ttu-id="f476d-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f476d-130">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.oneDriveActivityUserDetail"
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
  "assignedProducts": ["String"], 
  "reportPeriod": "String"
}
```
