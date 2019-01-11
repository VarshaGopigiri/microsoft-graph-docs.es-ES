---
title: tipo de recurso oneDriveActivityUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 2f498c7c9507c4210f12f76d57f62729f84da578
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820793"
---
# <a name="onedriveactivityuserdetail-resource-type"></a><span data-ttu-id="d3291-103">tipo de recurso oneDriveActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="d3291-103">oneDriveActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="d3291-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d3291-104">Properties</span></span>

| <span data-ttu-id="d3291-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d3291-105">Property</span></span>                  | <span data-ttu-id="d3291-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3291-106">Type</span></span>              |
| :------------------------ | :---------------- |
| <span data-ttu-id="d3291-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="d3291-107">reportRefreshDate</span></span>         | <span data-ttu-id="d3291-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="d3291-108">Date</span></span>              |
| <span data-ttu-id="d3291-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d3291-109">userPrincipalName</span></span>         | <span data-ttu-id="d3291-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="d3291-110">String</span></span>            |
| <span data-ttu-id="d3291-111">isDeleted</span><span class="sxs-lookup"><span data-stu-id="d3291-111">isDeleted</span></span>                 | <span data-ttu-id="d3291-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="d3291-112">Boolean</span></span>           |
| <span data-ttu-id="d3291-113">deletedDate</span><span class="sxs-lookup"><span data-stu-id="d3291-113">deletedDate</span></span>               | <span data-ttu-id="d3291-114">Fecha</span><span class="sxs-lookup"><span data-stu-id="d3291-114">Date</span></span>              |
| <span data-ttu-id="d3291-115">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="d3291-115">lastActivityDate</span></span>          | <span data-ttu-id="d3291-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="d3291-116">Date</span></span>              |
| <span data-ttu-id="d3291-117">viewedOrEditedFileCount</span><span class="sxs-lookup"><span data-stu-id="d3291-117">viewedOrEditedFileCount</span></span>   | <span data-ttu-id="d3291-118">Int64</span><span class="sxs-lookup"><span data-stu-id="d3291-118">Int64</span></span>             |
| <span data-ttu-id="d3291-119">syncedFileCount</span><span class="sxs-lookup"><span data-stu-id="d3291-119">syncedFileCount</span></span>           | <span data-ttu-id="d3291-120">Int64</span><span class="sxs-lookup"><span data-stu-id="d3291-120">Int64</span></span>             |
| <span data-ttu-id="d3291-121">sharedInternallyFileCount</span><span class="sxs-lookup"><span data-stu-id="d3291-121">sharedInternallyFileCount</span></span> | <span data-ttu-id="d3291-122">Int64</span><span class="sxs-lookup"><span data-stu-id="d3291-122">Int64</span></span>             |
| <span data-ttu-id="d3291-123">sharedExternallyFileCount</span><span class="sxs-lookup"><span data-stu-id="d3291-123">sharedExternallyFileCount</span></span> | <span data-ttu-id="d3291-124">Int64</span><span class="sxs-lookup"><span data-stu-id="d3291-124">Int64</span></span>             |
| <span data-ttu-id="d3291-125">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="d3291-125">assignedProducts</span></span>          | <span data-ttu-id="d3291-126">Colección String</span><span class="sxs-lookup"><span data-stu-id="d3291-126">String collection</span></span> |
| <span data-ttu-id="d3291-127">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="d3291-127">reportPeriod</span></span>              | <span data-ttu-id="d3291-128">String</span><span class="sxs-lookup"><span data-stu-id="d3291-128">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="d3291-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d3291-129">JSON representation</span></span>

<span data-ttu-id="d3291-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d3291-130">The following is a JSON representation of the resource.</span></span>

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
