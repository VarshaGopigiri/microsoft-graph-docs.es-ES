---
title: tipo de recurso yammerGroupsActivityDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 9a4bb00aecb2ae1d14b68a5388e0dedc7c41b1cb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084112"
---
# <a name="yammergroupsactivitydetail-resource-type"></a><span data-ttu-id="73cf5-103">tipo de recurso yammerGroupsActivityDetail</span><span class="sxs-lookup"><span data-stu-id="73cf5-103">yammerGroupsActivityDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="73cf5-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73cf5-104">Properties</span></span>

| <span data-ttu-id="73cf5-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="73cf5-105">Property</span></span>           | <span data-ttu-id="73cf5-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="73cf5-106">Type</span></span>    |
| :----------------- | :------ |
| <span data-ttu-id="73cf5-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="73cf5-107">reportRefreshDate</span></span>  | <span data-ttu-id="73cf5-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="73cf5-108">Date</span></span>    |
| <span data-ttu-id="73cf5-109">groupDisplayName</span><span class="sxs-lookup"><span data-stu-id="73cf5-109">groupDisplayName</span></span>   | <span data-ttu-id="73cf5-110">String</span><span class="sxs-lookup"><span data-stu-id="73cf5-110">String</span></span>  |
| <span data-ttu-id="73cf5-111">isDeleted</span><span class="sxs-lookup"><span data-stu-id="73cf5-111">isDeleted</span></span>          | <span data-ttu-id="73cf5-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="73cf5-112">Boolean</span></span> |
| <span data-ttu-id="73cf5-113">ownerPrincipalName</span><span class="sxs-lookup"><span data-stu-id="73cf5-113">ownerPrincipalName</span></span> | <span data-ttu-id="73cf5-114">String</span><span class="sxs-lookup"><span data-stu-id="73cf5-114">String</span></span>  |
| <span data-ttu-id="73cf5-115">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="73cf5-115">lastActivityDate</span></span>   | <span data-ttu-id="73cf5-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="73cf5-116">Date</span></span>    |
| <span data-ttu-id="73cf5-117">groupType</span><span class="sxs-lookup"><span data-stu-id="73cf5-117">groupType</span></span>          | <span data-ttu-id="73cf5-118">String</span><span class="sxs-lookup"><span data-stu-id="73cf5-118">String</span></span>  |
| <span data-ttu-id="73cf5-119">office365Connected</span><span class="sxs-lookup"><span data-stu-id="73cf5-119">office365Connected</span></span> | <span data-ttu-id="73cf5-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="73cf5-120">Boolean</span></span> |
| <span data-ttu-id="73cf5-121">memberCount</span><span class="sxs-lookup"><span data-stu-id="73cf5-121">memberCount</span></span>        | <span data-ttu-id="73cf5-122">Int64</span><span class="sxs-lookup"><span data-stu-id="73cf5-122">Int64</span></span>   |
| <span data-ttu-id="73cf5-123">postedCount</span><span class="sxs-lookup"><span data-stu-id="73cf5-123">postedCount</span></span>        | <span data-ttu-id="73cf5-124">Int64</span><span class="sxs-lookup"><span data-stu-id="73cf5-124">Int64</span></span>   |
| <span data-ttu-id="73cf5-125">readCount</span><span class="sxs-lookup"><span data-stu-id="73cf5-125">readCount</span></span>          | <span data-ttu-id="73cf5-126">Int64</span><span class="sxs-lookup"><span data-stu-id="73cf5-126">Int64</span></span>   |
| <span data-ttu-id="73cf5-127">likedCount</span><span class="sxs-lookup"><span data-stu-id="73cf5-127">likedCount</span></span>         | <span data-ttu-id="73cf5-128">Int64</span><span class="sxs-lookup"><span data-stu-id="73cf5-128">Int64</span></span>   |
| <span data-ttu-id="73cf5-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="73cf5-129">reportPeriod</span></span>       | <span data-ttu-id="73cf5-130">String</span><span class="sxs-lookup"><span data-stu-id="73cf5-130">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="73cf5-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="73cf5-131">JSON representation</span></span>

<span data-ttu-id="73cf5-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="73cf5-132">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yammerGroupsActivityDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "groupDisplayName": "String", 
  "isDeleted": true, 
  "ownerPrincipalName": "String", 
  "lastActivityDate": "Date", 
  "groupType": "String", 
  "office365Connected": true, 
  "memberCount": 1024, 
  "postedCount": 1024, 
  "readCount": 1024, 
  "likedCount": 1024, 
  "reportPeriod": "String"
}
```
