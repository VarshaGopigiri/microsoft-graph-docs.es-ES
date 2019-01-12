---
title: tipo de recurso yammerActivityUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: d24e21c9525d49b7af5f8c4efaddd606c20c162b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923036"
---
# <a name="yammeractivityuserdetail-resource-type"></a><span data-ttu-id="b058d-103">tipo de recurso yammerActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="b058d-103">yammerActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="b058d-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b058d-104">Properties</span></span>

| <span data-ttu-id="b058d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b058d-105">Property</span></span>          | <span data-ttu-id="b058d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="b058d-106">Type</span></span>              |
| :---------------- | :---------------- |
| <span data-ttu-id="b058d-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="b058d-107">reportRefreshDate</span></span> | <span data-ttu-id="b058d-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="b058d-108">Date</span></span>              |
| <span data-ttu-id="b058d-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b058d-109">userPrincipalName</span></span> | <span data-ttu-id="b058d-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="b058d-110">String</span></span>            |
| <span data-ttu-id="b058d-111">displayName</span><span class="sxs-lookup"><span data-stu-id="b058d-111">displayName</span></span>       | <span data-ttu-id="b058d-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="b058d-112">String</span></span>            |
| <span data-ttu-id="b058d-113">userState</span><span class="sxs-lookup"><span data-stu-id="b058d-113">userState</span></span>         | <span data-ttu-id="b058d-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="b058d-114">String</span></span>            |
| <span data-ttu-id="b058d-115">stateChangeDate</span><span class="sxs-lookup"><span data-stu-id="b058d-115">stateChangeDate</span></span>   | <span data-ttu-id="b058d-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="b058d-116">Date</span></span>              |
| <span data-ttu-id="b058d-117">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="b058d-117">lastActivityDate</span></span>  | <span data-ttu-id="b058d-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="b058d-118">Date</span></span>              |
| <span data-ttu-id="b058d-119">postedCount</span><span class="sxs-lookup"><span data-stu-id="b058d-119">postedCount</span></span>       | <span data-ttu-id="b058d-120">Int64</span><span class="sxs-lookup"><span data-stu-id="b058d-120">Int64</span></span>             |
| <span data-ttu-id="b058d-121">readCount</span><span class="sxs-lookup"><span data-stu-id="b058d-121">readCount</span></span>         | <span data-ttu-id="b058d-122">Int64</span><span class="sxs-lookup"><span data-stu-id="b058d-122">Int64</span></span>             |
| <span data-ttu-id="b058d-123">likedCount</span><span class="sxs-lookup"><span data-stu-id="b058d-123">likedCount</span></span>        | <span data-ttu-id="b058d-124">Int64</span><span class="sxs-lookup"><span data-stu-id="b058d-124">Int64</span></span>             |
| <span data-ttu-id="b058d-125">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="b058d-125">assignedProducts</span></span>  | <span data-ttu-id="b058d-126">Colección String</span><span class="sxs-lookup"><span data-stu-id="b058d-126">String collection</span></span> |
| <span data-ttu-id="b058d-127">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="b058d-127">reportPeriod</span></span>      | <span data-ttu-id="b058d-128">String</span><span class="sxs-lookup"><span data-stu-id="b058d-128">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="b058d-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b058d-129">JSON representation</span></span>

<span data-ttu-id="b058d-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b058d-130">The following is a JSON representation of the resource.</span></span>

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
