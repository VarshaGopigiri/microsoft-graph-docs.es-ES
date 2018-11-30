---
title: tipo de recurso yammerActivityUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: a1ca33efe8327b1c1e52de25714df9c0bd45ee05
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089134"
---
# <a name="yammeractivityuserdetail-resource-type"></a><span data-ttu-id="97c26-103">tipo de recurso yammerActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="97c26-103">yammerActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="97c26-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97c26-104">Properties</span></span>

| <span data-ttu-id="97c26-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="97c26-105">Property</span></span>          | <span data-ttu-id="97c26-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="97c26-106">Type</span></span>              |
| :---------------- | :---------------- |
| <span data-ttu-id="97c26-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="97c26-107">reportRefreshDate</span></span> | <span data-ttu-id="97c26-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="97c26-108">Date</span></span>              |
| <span data-ttu-id="97c26-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="97c26-109">userPrincipalName</span></span> | <span data-ttu-id="97c26-110">String</span><span class="sxs-lookup"><span data-stu-id="97c26-110">String</span></span>            |
| <span data-ttu-id="97c26-111">displayName</span><span class="sxs-lookup"><span data-stu-id="97c26-111">displayName</span></span>       | <span data-ttu-id="97c26-112">String</span><span class="sxs-lookup"><span data-stu-id="97c26-112">String</span></span>            |
| <span data-ttu-id="97c26-113">userState</span><span class="sxs-lookup"><span data-stu-id="97c26-113">userState</span></span>         | <span data-ttu-id="97c26-114">String</span><span class="sxs-lookup"><span data-stu-id="97c26-114">String</span></span>            |
| <span data-ttu-id="97c26-115">stateChangeDate</span><span class="sxs-lookup"><span data-stu-id="97c26-115">stateChangeDate</span></span>   | <span data-ttu-id="97c26-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="97c26-116">Date</span></span>              |
| <span data-ttu-id="97c26-117">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="97c26-117">lastActivityDate</span></span>  | <span data-ttu-id="97c26-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="97c26-118">Date</span></span>              |
| <span data-ttu-id="97c26-119">postedCount</span><span class="sxs-lookup"><span data-stu-id="97c26-119">postedCount</span></span>       | <span data-ttu-id="97c26-120">Int64</span><span class="sxs-lookup"><span data-stu-id="97c26-120">Int64</span></span>             |
| <span data-ttu-id="97c26-121">readCount</span><span class="sxs-lookup"><span data-stu-id="97c26-121">readCount</span></span>         | <span data-ttu-id="97c26-122">Int64</span><span class="sxs-lookup"><span data-stu-id="97c26-122">Int64</span></span>             |
| <span data-ttu-id="97c26-123">likedCount</span><span class="sxs-lookup"><span data-stu-id="97c26-123">likedCount</span></span>        | <span data-ttu-id="97c26-124">Int64</span><span class="sxs-lookup"><span data-stu-id="97c26-124">Int64</span></span>             |
| <span data-ttu-id="97c26-125">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="97c26-125">assignedProducts</span></span>  | <span data-ttu-id="97c26-126">Colección String</span><span class="sxs-lookup"><span data-stu-id="97c26-126">String collection</span></span> |
| <span data-ttu-id="97c26-127">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="97c26-127">reportPeriod</span></span>      | <span data-ttu-id="97c26-128">String</span><span class="sxs-lookup"><span data-stu-id="97c26-128">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="97c26-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="97c26-129">JSON representation</span></span>

<span data-ttu-id="97c26-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="97c26-130">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yammerActivityUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "displayName": "String", 
  "userState": "String", 
  "stateChangeDate": "Date", 
  "lastActivityDate": "Date", 
  "postedCount": 1024, 
  "readCount": 1024, 
  "likedCount": 1024, 
  "assignedProducts": ["String"], 
  "reportPeriod": "String"
}
```
