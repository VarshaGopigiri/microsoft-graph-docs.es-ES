---
title: tipo de recurso yammerActivityUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: d7869869466dc785b92db23f8b574eb2e77dd786
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816404"
---
# <a name="yammeractivityuserdetail-resource-type"></a><span data-ttu-id="2e7be-103">tipo de recurso yammerActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="2e7be-103">yammerActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="2e7be-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2e7be-104">Properties</span></span>

| <span data-ttu-id="2e7be-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2e7be-105">Property</span></span>          | <span data-ttu-id="2e7be-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="2e7be-106">Type</span></span>              |
| :---------------- | :---------------- |
| <span data-ttu-id="2e7be-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="2e7be-107">reportRefreshDate</span></span> | <span data-ttu-id="2e7be-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="2e7be-108">Date</span></span>              |
| <span data-ttu-id="2e7be-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2e7be-109">userPrincipalName</span></span> | <span data-ttu-id="2e7be-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="2e7be-110">String</span></span>            |
| <span data-ttu-id="2e7be-111">displayName</span><span class="sxs-lookup"><span data-stu-id="2e7be-111">displayName</span></span>       | <span data-ttu-id="2e7be-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="2e7be-112">String</span></span>            |
| <span data-ttu-id="2e7be-113">userState</span><span class="sxs-lookup"><span data-stu-id="2e7be-113">userState</span></span>         | <span data-ttu-id="2e7be-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="2e7be-114">String</span></span>            |
| <span data-ttu-id="2e7be-115">stateChangeDate</span><span class="sxs-lookup"><span data-stu-id="2e7be-115">stateChangeDate</span></span>   | <span data-ttu-id="2e7be-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="2e7be-116">Date</span></span>              |
| <span data-ttu-id="2e7be-117">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="2e7be-117">lastActivityDate</span></span>  | <span data-ttu-id="2e7be-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="2e7be-118">Date</span></span>              |
| <span data-ttu-id="2e7be-119">postedCount</span><span class="sxs-lookup"><span data-stu-id="2e7be-119">postedCount</span></span>       | <span data-ttu-id="2e7be-120">Int64</span><span class="sxs-lookup"><span data-stu-id="2e7be-120">Int64</span></span>             |
| <span data-ttu-id="2e7be-121">readCount</span><span class="sxs-lookup"><span data-stu-id="2e7be-121">readCount</span></span>         | <span data-ttu-id="2e7be-122">Int64</span><span class="sxs-lookup"><span data-stu-id="2e7be-122">Int64</span></span>             |
| <span data-ttu-id="2e7be-123">likedCount</span><span class="sxs-lookup"><span data-stu-id="2e7be-123">likedCount</span></span>        | <span data-ttu-id="2e7be-124">Int64</span><span class="sxs-lookup"><span data-stu-id="2e7be-124">Int64</span></span>             |
| <span data-ttu-id="2e7be-125">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="2e7be-125">assignedProducts</span></span>  | <span data-ttu-id="2e7be-126">Colección String</span><span class="sxs-lookup"><span data-stu-id="2e7be-126">String collection</span></span> |
| <span data-ttu-id="2e7be-127">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="2e7be-127">reportPeriod</span></span>      | <span data-ttu-id="2e7be-128">String</span><span class="sxs-lookup"><span data-stu-id="2e7be-128">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="2e7be-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2e7be-129">JSON representation</span></span>

<span data-ttu-id="2e7be-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="2e7be-130">The following is a JSON representation of the resource.</span></span>

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
