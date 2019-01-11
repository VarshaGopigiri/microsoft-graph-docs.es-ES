---
title: tipo de recurso mailboxUsageDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 25cb41e38138a677bfc6636b035003bb8fc5858c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818014"
---
# <a name="mailboxusagedetail-resource-type"></a><span data-ttu-id="51532-103">tipo de recurso mailboxUsageDetail</span><span class="sxs-lookup"><span data-stu-id="51532-103">mailboxUsageDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="51532-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51532-104">Properties</span></span>

| <span data-ttu-id="51532-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51532-105">Property</span></span>                        | <span data-ttu-id="51532-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="51532-106">Type</span></span>    |
| :------------------------------ | :------ |
| <span data-ttu-id="51532-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="51532-107">reportRefreshDate</span></span>               | <span data-ttu-id="51532-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="51532-108">Date</span></span>    |
| <span data-ttu-id="51532-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="51532-109">userPrincipalName</span></span>               | <span data-ttu-id="51532-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="51532-110">String</span></span>  |
| <span data-ttu-id="51532-111">displayName</span><span class="sxs-lookup"><span data-stu-id="51532-111">displayName</span></span>                     | <span data-ttu-id="51532-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="51532-112">String</span></span>  |
| <span data-ttu-id="51532-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="51532-113">isDeleted</span></span>                       | <span data-ttu-id="51532-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="51532-114">Boolean</span></span> |
| <span data-ttu-id="51532-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="51532-115">deletedDate</span></span>                     | <span data-ttu-id="51532-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="51532-116">Date</span></span>    |
| <span data-ttu-id="51532-117">createdDate</span><span class="sxs-lookup"><span data-stu-id="51532-117">createdDate</span></span>                     | <span data-ttu-id="51532-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="51532-118">Date</span></span>    |
| <span data-ttu-id="51532-119">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="51532-119">lastActivityDate</span></span>                | <span data-ttu-id="51532-120">Fecha</span><span class="sxs-lookup"><span data-stu-id="51532-120">Date</span></span>    |
| <span data-ttu-id="51532-121">itemCount</span><span class="sxs-lookup"><span data-stu-id="51532-121">itemCount</span></span>                       | <span data-ttu-id="51532-122">Int64</span><span class="sxs-lookup"><span data-stu-id="51532-122">Int64</span></span>   |
| <span data-ttu-id="51532-123">storageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="51532-123">storageUsedInBytes</span></span>              | <span data-ttu-id="51532-124">Int64</span><span class="sxs-lookup"><span data-stu-id="51532-124">Int64</span></span>   |
| <span data-ttu-id="51532-125">issueWarningQuotaInBytes</span><span class="sxs-lookup"><span data-stu-id="51532-125">issueWarningQuotaInBytes</span></span>        | <span data-ttu-id="51532-126">Int64</span><span class="sxs-lookup"><span data-stu-id="51532-126">Int64</span></span>   |
| <span data-ttu-id="51532-127">prohibitSendQuotaInBytes</span><span class="sxs-lookup"><span data-stu-id="51532-127">prohibitSendQuotaInBytes</span></span>        | <span data-ttu-id="51532-128">Int64</span><span class="sxs-lookup"><span data-stu-id="51532-128">Int64</span></span>   |
| <span data-ttu-id="51532-129">prohibitSendReceiveQuotaInBytes</span><span class="sxs-lookup"><span data-stu-id="51532-129">prohibitSendReceiveQuotaInBytes</span></span> | <span data-ttu-id="51532-130">Int64</span><span class="sxs-lookup"><span data-stu-id="51532-130">Int64</span></span>   |
| <span data-ttu-id="51532-131">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="51532-131">reportPeriod</span></span>                    | <span data-ttu-id="51532-132">String</span><span class="sxs-lookup"><span data-stu-id="51532-132">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="51532-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="51532-133">JSON representation</span></span>

<span data-ttu-id="51532-134">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="51532-134">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mailboxUsageDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "displayName": "String", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "createdDate": "Date", 
  "lastActivityDate": "Date", 
  "itemCount": 1024, 
  "storageUsedInBytes": 1024, 
  "issueWarningQuotaInBytes": 1024, 
  "prohibitSendQuotaInBytes": 1024, 
  "prohibitSendReceiveQuotaInBytes": 1024, 
  "reportPeriod": "String"
}
```
