---
title: tipo de recurso yammerGroupsActivityDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 79ce924fff5d1ce9ca861c3d48589a0ecad149dc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939171"
---
# <a name="yammergroupsactivitydetail-resource-type"></a><span data-ttu-id="da4f0-103">tipo de recurso yammerGroupsActivityDetail</span><span class="sxs-lookup"><span data-stu-id="da4f0-103">yammerGroupsActivityDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="da4f0-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="da4f0-104">Properties</span></span>

| <span data-ttu-id="da4f0-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="da4f0-105">Property</span></span>           | <span data-ttu-id="da4f0-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="da4f0-106">Type</span></span>    |
| :----------------- | :------ |
| <span data-ttu-id="da4f0-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="da4f0-107">reportRefreshDate</span></span>  | <span data-ttu-id="da4f0-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="da4f0-108">Date</span></span>    |
| <span data-ttu-id="da4f0-109">groupDisplayName</span><span class="sxs-lookup"><span data-stu-id="da4f0-109">groupDisplayName</span></span>   | <span data-ttu-id="da4f0-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="da4f0-110">String</span></span>  |
| <span data-ttu-id="da4f0-111">isDeleted</span><span class="sxs-lookup"><span data-stu-id="da4f0-111">isDeleted</span></span>          | <span data-ttu-id="da4f0-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="da4f0-112">Boolean</span></span> |
| <span data-ttu-id="da4f0-113">ownerPrincipalName</span><span class="sxs-lookup"><span data-stu-id="da4f0-113">ownerPrincipalName</span></span> | <span data-ttu-id="da4f0-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="da4f0-114">String</span></span>  |
| <span data-ttu-id="da4f0-115">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="da4f0-115">lastActivityDate</span></span>   | <span data-ttu-id="da4f0-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="da4f0-116">Date</span></span>    |
| <span data-ttu-id="da4f0-117">groupType</span><span class="sxs-lookup"><span data-stu-id="da4f0-117">groupType</span></span>          | <span data-ttu-id="da4f0-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="da4f0-118">String</span></span>  |
| <span data-ttu-id="da4f0-119">office365Connected</span><span class="sxs-lookup"><span data-stu-id="da4f0-119">office365Connected</span></span> | <span data-ttu-id="da4f0-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="da4f0-120">Boolean</span></span> |
| <span data-ttu-id="da4f0-121">memberCount</span><span class="sxs-lookup"><span data-stu-id="da4f0-121">memberCount</span></span>        | <span data-ttu-id="da4f0-122">Int64</span><span class="sxs-lookup"><span data-stu-id="da4f0-122">Int64</span></span>   |
| <span data-ttu-id="da4f0-123">postedCount</span><span class="sxs-lookup"><span data-stu-id="da4f0-123">postedCount</span></span>        | <span data-ttu-id="da4f0-124">Int64</span><span class="sxs-lookup"><span data-stu-id="da4f0-124">Int64</span></span>   |
| <span data-ttu-id="da4f0-125">readCount</span><span class="sxs-lookup"><span data-stu-id="da4f0-125">readCount</span></span>          | <span data-ttu-id="da4f0-126">Int64</span><span class="sxs-lookup"><span data-stu-id="da4f0-126">Int64</span></span>   |
| <span data-ttu-id="da4f0-127">likedCount</span><span class="sxs-lookup"><span data-stu-id="da4f0-127">likedCount</span></span>         | <span data-ttu-id="da4f0-128">Int64</span><span class="sxs-lookup"><span data-stu-id="da4f0-128">Int64</span></span>   |
| <span data-ttu-id="da4f0-129">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="da4f0-129">reportPeriod</span></span>       | <span data-ttu-id="da4f0-130">String</span><span class="sxs-lookup"><span data-stu-id="da4f0-130">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="da4f0-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="da4f0-131">JSON representation</span></span>

<span data-ttu-id="da4f0-132">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="da4f0-132">The following is a JSON representation of the resource.</span></span>

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
