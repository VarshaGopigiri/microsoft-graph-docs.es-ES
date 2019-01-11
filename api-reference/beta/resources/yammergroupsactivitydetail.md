---
title: tipo de recurso yammerGroupsActivityDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 9e4ac61f2af69b4229c2e9c3df7c653428cc2033
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832035"
---
# <a name="yammergroupsactivitydetail-resource-type"></a><span data-ttu-id="167ba-103">tipo de recurso yammerGroupsActivityDetail</span><span class="sxs-lookup"><span data-stu-id="167ba-103">yammerGroupsActivityDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="167ba-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="167ba-104">Properties</span></span>

| <span data-ttu-id="167ba-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="167ba-105">Property</span></span>           | <span data-ttu-id="167ba-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="167ba-106">Type</span></span>    |
| :----------------- | :------ |
| <span data-ttu-id="167ba-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="167ba-107">reportRefreshDate</span></span>  | <span data-ttu-id="167ba-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="167ba-108">Date</span></span>    |
| <span data-ttu-id="167ba-109">groupDisplayName</span><span class="sxs-lookup"><span data-stu-id="167ba-109">groupDisplayName</span></span>   | <span data-ttu-id="167ba-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="167ba-110">String</span></span>  |
| <span data-ttu-id="167ba-111">isDeleted</span><span class="sxs-lookup"><span data-stu-id="167ba-111">isDeleted</span></span>          | <span data-ttu-id="167ba-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="167ba-112">Boolean</span></span> |
| <span data-ttu-id="167ba-113">ownerPrincipalName</span><span class="sxs-lookup"><span data-stu-id="167ba-113">ownerPrincipalName</span></span> | <span data-ttu-id="167ba-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="167ba-114">String</span></span>  |
| <span data-ttu-id="167ba-115">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="167ba-115">lastActivityDate</span></span>   | <span data-ttu-id="167ba-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="167ba-116">Date</span></span>    |
| <span data-ttu-id="167ba-117">groupType</span><span class="sxs-lookup"><span data-stu-id="167ba-117">groupType</span></span>          | <span data-ttu-id="167ba-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="167ba-118">String</span></span>  |
| <span data-ttu-id="167ba-119">office365Connected</span><span class="sxs-lookup"><span data-stu-id="167ba-119">office365Connected</span></span> | <span data-ttu-id="167ba-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="167ba-120">Boolean</span></span> |
| <span data-ttu-id="167ba-121">memberCount</span><span class="sxs-lookup"><span data-stu-id="167ba-121">memberCount</span></span>        | <span data-ttu-id="167ba-122">Int64</span><span class="sxs-lookup"><span data-stu-id="167ba-122">Int64</span></span>   |
| <span data-ttu-id="167ba-123">postedCount</span><span class="sxs-lookup"><span data-stu-id="167ba-123">postedCount</span></span>        | <span data-ttu-id="167ba-124">Int64</span><span class="sxs-lookup"><span data-stu-id="167ba-124">Int64</span></span>   |
| <span data-ttu-id="167ba-125">readCount</span><span class="sxs-lookup"><span data-stu-id="167ba-125">readCount</span></span>          | <span data-ttu-id="167ba-126">Int64</span><span class="sxs-lookup"><span data-stu-id="167ba-126">Int64</span></span>   |
| <span data-ttu-id="167ba-127">likedCount</span><span class="sxs-lookup"><span data-stu-id="167ba-127">likedCount</span></span>         | <span data-ttu-id="167ba-128">Int64</span><span class="sxs-lookup"><span data-stu-id="167ba-128">Int64</span></span>   |
| <span data-ttu-id="167ba-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="167ba-129">reportPeriod</span></span>       | <span data-ttu-id="167ba-130">String</span><span class="sxs-lookup"><span data-stu-id="167ba-130">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="167ba-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="167ba-131">JSON representation</span></span>

<span data-ttu-id="167ba-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="167ba-132">The following is a JSON representation of the resource.</span></span>

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
