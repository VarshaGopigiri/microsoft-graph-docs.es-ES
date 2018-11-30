---
title: tipo de recurso oneDriveActivityUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 679ec9b8452d388fe311e67d88bcfffd6fe73d93
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085856"
---
# <a name="onedriveactivityuserdetail-resource-type"></a><span data-ttu-id="adb15-103">tipo de recurso oneDriveActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="adb15-103">oneDriveActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="adb15-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="adb15-104">Properties</span></span>

| <span data-ttu-id="adb15-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="adb15-105">Property</span></span>                  | <span data-ttu-id="adb15-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="adb15-106">Type</span></span>              |
| :------------------------ | :---------------- |
| <span data-ttu-id="adb15-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="adb15-107">reportRefreshDate</span></span>         | <span data-ttu-id="adb15-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="adb15-108">Date</span></span>              |
| <span data-ttu-id="adb15-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="adb15-109">userPrincipalName</span></span>         | <span data-ttu-id="adb15-110">String</span><span class="sxs-lookup"><span data-stu-id="adb15-110">String</span></span>            |
| <span data-ttu-id="adb15-111">isDeleted</span><span class="sxs-lookup"><span data-stu-id="adb15-111">isDeleted</span></span>                 | <span data-ttu-id="adb15-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="adb15-112">Boolean</span></span>           |
| <span data-ttu-id="adb15-113">deletedDate</span><span class="sxs-lookup"><span data-stu-id="adb15-113">deletedDate</span></span>               | <span data-ttu-id="adb15-114">Fecha</span><span class="sxs-lookup"><span data-stu-id="adb15-114">Date</span></span>              |
| <span data-ttu-id="adb15-115">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="adb15-115">lastActivityDate</span></span>          | <span data-ttu-id="adb15-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="adb15-116">Date</span></span>              |
| <span data-ttu-id="adb15-117">viewedOrEditedFileCount</span><span class="sxs-lookup"><span data-stu-id="adb15-117">viewedOrEditedFileCount</span></span>   | <span data-ttu-id="adb15-118">Int64</span><span class="sxs-lookup"><span data-stu-id="adb15-118">Int64</span></span>             |
| <span data-ttu-id="adb15-119">syncedFileCount</span><span class="sxs-lookup"><span data-stu-id="adb15-119">syncedFileCount</span></span>           | <span data-ttu-id="adb15-120">Int64</span><span class="sxs-lookup"><span data-stu-id="adb15-120">Int64</span></span>             |
| <span data-ttu-id="adb15-121">sharedInternallyFileCount</span><span class="sxs-lookup"><span data-stu-id="adb15-121">sharedInternallyFileCount</span></span> | <span data-ttu-id="adb15-122">Int64</span><span class="sxs-lookup"><span data-stu-id="adb15-122">Int64</span></span>             |
| <span data-ttu-id="adb15-123">sharedExternallyFileCount</span><span class="sxs-lookup"><span data-stu-id="adb15-123">sharedExternallyFileCount</span></span> | <span data-ttu-id="adb15-124">Int64</span><span class="sxs-lookup"><span data-stu-id="adb15-124">Int64</span></span>             |
| <span data-ttu-id="adb15-125">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="adb15-125">assignedProducts</span></span>          | <span data-ttu-id="adb15-126">Colección String</span><span class="sxs-lookup"><span data-stu-id="adb15-126">String collection</span></span> |
| <span data-ttu-id="adb15-127">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="adb15-127">reportPeriod</span></span>              | <span data-ttu-id="adb15-128">String</span><span class="sxs-lookup"><span data-stu-id="adb15-128">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="adb15-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="adb15-129">JSON representation</span></span>

<span data-ttu-id="adb15-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="adb15-130">The following is a JSON representation of the resource.</span></span>

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
