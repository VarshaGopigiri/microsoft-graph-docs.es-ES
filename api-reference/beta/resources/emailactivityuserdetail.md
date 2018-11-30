---
title: tipo de recurso emailActivityUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 4f74b4af41c44e41b07bae1a8421011bc5188efc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083139"
---
# <a name="emailactivityuserdetail-resource-type"></a><span data-ttu-id="dc5d0-103">tipo de recurso emailActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="dc5d0-103">emailActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="dc5d0-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc5d0-104">Properties</span></span>

| <span data-ttu-id="dc5d0-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dc5d0-105">Property</span></span>          | <span data-ttu-id="dc5d0-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc5d0-106">Type</span></span>              |
| :---------------- | :---------------- |
| <span data-ttu-id="dc5d0-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="dc5d0-107">reportRefreshDate</span></span> | <span data-ttu-id="dc5d0-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="dc5d0-108">Date</span></span>              |
| <span data-ttu-id="dc5d0-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="dc5d0-109">userPrincipalName</span></span> | <span data-ttu-id="dc5d0-110">String</span><span class="sxs-lookup"><span data-stu-id="dc5d0-110">String</span></span>            |
| <span data-ttu-id="dc5d0-111">displayName</span><span class="sxs-lookup"><span data-stu-id="dc5d0-111">displayName</span></span>       | <span data-ttu-id="dc5d0-112">String</span><span class="sxs-lookup"><span data-stu-id="dc5d0-112">String</span></span>            |
| <span data-ttu-id="dc5d0-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="dc5d0-113">isDeleted</span></span>         | <span data-ttu-id="dc5d0-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="dc5d0-114">Boolean</span></span>           |
| <span data-ttu-id="dc5d0-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="dc5d0-115">deletedDate</span></span>       | <span data-ttu-id="dc5d0-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="dc5d0-116">Date</span></span>              |
| <span data-ttu-id="dc5d0-117">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="dc5d0-117">lastActivityDate</span></span>  | <span data-ttu-id="dc5d0-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="dc5d0-118">Date</span></span>              |
| <span data-ttu-id="dc5d0-119">sendCount</span><span class="sxs-lookup"><span data-stu-id="dc5d0-119">sendCount</span></span>         | <span data-ttu-id="dc5d0-120">Int64</span><span class="sxs-lookup"><span data-stu-id="dc5d0-120">Int64</span></span>             |
| <span data-ttu-id="dc5d0-121">receiveCount</span><span class="sxs-lookup"><span data-stu-id="dc5d0-121">receiveCount</span></span>      | <span data-ttu-id="dc5d0-122">Int64</span><span class="sxs-lookup"><span data-stu-id="dc5d0-122">Int64</span></span>             |
| <span data-ttu-id="dc5d0-123">readCount</span><span class="sxs-lookup"><span data-stu-id="dc5d0-123">readCount</span></span>         | <span data-ttu-id="dc5d0-124">Int64</span><span class="sxs-lookup"><span data-stu-id="dc5d0-124">Int64</span></span>             |
| <span data-ttu-id="dc5d0-125">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="dc5d0-125">assignedProducts</span></span>  | <span data-ttu-id="dc5d0-126">Colección String</span><span class="sxs-lookup"><span data-stu-id="dc5d0-126">String collection</span></span> |
| <span data-ttu-id="dc5d0-127">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="dc5d0-127">reportPeriod</span></span>      | <span data-ttu-id="dc5d0-128">String</span><span class="sxs-lookup"><span data-stu-id="dc5d0-128">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="dc5d0-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dc5d0-129">JSON representation</span></span>

<span data-ttu-id="dc5d0-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="dc5d0-130">The following is a JSON representation of the resource.</span></span>

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
