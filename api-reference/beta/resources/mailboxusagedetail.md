---
title: tipo de recurso mailboxUsageDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: af49fac7c6286c7e9f9ce1e6d7ffdede225b4072
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084797"
---
# <a name="mailboxusagedetail-resource-type"></a><span data-ttu-id="63422-103">tipo de recurso mailboxUsageDetail</span><span class="sxs-lookup"><span data-stu-id="63422-103">mailboxUsageDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="63422-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63422-104">Properties</span></span>

| <span data-ttu-id="63422-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63422-105">Property</span></span>                        | <span data-ttu-id="63422-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="63422-106">Type</span></span>    |
| :------------------------------ | :------ |
| <span data-ttu-id="63422-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="63422-107">reportRefreshDate</span></span>               | <span data-ttu-id="63422-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="63422-108">Date</span></span>    |
| <span data-ttu-id="63422-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="63422-109">userPrincipalName</span></span>               | <span data-ttu-id="63422-110">String</span><span class="sxs-lookup"><span data-stu-id="63422-110">String</span></span>  |
| <span data-ttu-id="63422-111">displayName</span><span class="sxs-lookup"><span data-stu-id="63422-111">displayName</span></span>                     | <span data-ttu-id="63422-112">String</span><span class="sxs-lookup"><span data-stu-id="63422-112">String</span></span>  |
| <span data-ttu-id="63422-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="63422-113">isDeleted</span></span>                       | <span data-ttu-id="63422-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="63422-114">Boolean</span></span> |
| <span data-ttu-id="63422-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="63422-115">deletedDate</span></span>                     | <span data-ttu-id="63422-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="63422-116">Date</span></span>    |
| <span data-ttu-id="63422-117">createdDate</span><span class="sxs-lookup"><span data-stu-id="63422-117">createdDate</span></span>                     | <span data-ttu-id="63422-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="63422-118">Date</span></span>    |
| <span data-ttu-id="63422-119">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="63422-119">lastActivityDate</span></span>                | <span data-ttu-id="63422-120">Fecha</span><span class="sxs-lookup"><span data-stu-id="63422-120">Date</span></span>    |
| <span data-ttu-id="63422-121">itemCount</span><span class="sxs-lookup"><span data-stu-id="63422-121">itemCount</span></span>                       | <span data-ttu-id="63422-122">Int64</span><span class="sxs-lookup"><span data-stu-id="63422-122">Int64</span></span>   |
| <span data-ttu-id="63422-123">storageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="63422-123">storageUsedInBytes</span></span>              | <span data-ttu-id="63422-124">Int64</span><span class="sxs-lookup"><span data-stu-id="63422-124">Int64</span></span>   |
| <span data-ttu-id="63422-125">issueWarningQuotaInBytes</span><span class="sxs-lookup"><span data-stu-id="63422-125">issueWarningQuotaInBytes</span></span>        | <span data-ttu-id="63422-126">Int64</span><span class="sxs-lookup"><span data-stu-id="63422-126">Int64</span></span>   |
| <span data-ttu-id="63422-127">prohibitSendQuotaInBytes</span><span class="sxs-lookup"><span data-stu-id="63422-127">prohibitSendQuotaInBytes</span></span>        | <span data-ttu-id="63422-128">Int64</span><span class="sxs-lookup"><span data-stu-id="63422-128">Int64</span></span>   |
| <span data-ttu-id="63422-129">prohibitSendReceiveQuotaInBytes</span><span class="sxs-lookup"><span data-stu-id="63422-129">prohibitSendReceiveQuotaInBytes</span></span> | <span data-ttu-id="63422-130">Int64</span><span class="sxs-lookup"><span data-stu-id="63422-130">Int64</span></span>   |
| <span data-ttu-id="63422-131">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="63422-131">reportPeriod</span></span>                    | <span data-ttu-id="63422-132">String</span><span class="sxs-lookup"><span data-stu-id="63422-132">String</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="63422-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="63422-133">JSON representation</span></span>

<span data-ttu-id="63422-134">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="63422-134">The following is a JSON representation of the resource.</span></span>

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
