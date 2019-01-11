---
title: tipo de recurso mailboxUsageQuotaStatusMailboxCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: b87bb1ce91626f9151d294e2243bba72ba72346b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27835227"
---
# <a name="mailboxusagequotastatusmailboxcounts-resource-type"></a><span data-ttu-id="e0fe6-103">tipo de recurso mailboxUsageQuotaStatusMailboxCounts</span><span class="sxs-lookup"><span data-stu-id="e0fe6-103">mailboxUsageQuotaStatusMailboxCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="e0fe6-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e0fe6-104">Properties</span></span>

| <span data-ttu-id="e0fe6-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e0fe6-105">Property</span></span>              | <span data-ttu-id="e0fe6-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0fe6-106">Type</span></span>   |
| :-------------------- | :----- |
| <span data-ttu-id="e0fe6-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="e0fe6-107">reportRefreshDate</span></span>     | <span data-ttu-id="e0fe6-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="e0fe6-108">Date</span></span>   |
| <span data-ttu-id="e0fe6-109">underLimit</span><span class="sxs-lookup"><span data-stu-id="e0fe6-109">underLimit</span></span>            | <span data-ttu-id="e0fe6-110">Int64</span><span class="sxs-lookup"><span data-stu-id="e0fe6-110">Int64</span></span>  |
| <span data-ttu-id="e0fe6-111">warningIssued</span><span class="sxs-lookup"><span data-stu-id="e0fe6-111">warningIssued</span></span>         | <span data-ttu-id="e0fe6-112">Int64</span><span class="sxs-lookup"><span data-stu-id="e0fe6-112">Int64</span></span>  |
| <span data-ttu-id="e0fe6-113">sendProhibited</span><span class="sxs-lookup"><span data-stu-id="e0fe6-113">sendProhibited</span></span>        | <span data-ttu-id="e0fe6-114">Int64</span><span class="sxs-lookup"><span data-stu-id="e0fe6-114">Int64</span></span>  |
| <span data-ttu-id="e0fe6-115">sendReceiveProhibited</span><span class="sxs-lookup"><span data-stu-id="e0fe6-115">sendReceiveProhibited</span></span> | <span data-ttu-id="e0fe6-116">Int64</span><span class="sxs-lookup"><span data-stu-id="e0fe6-116">Int64</span></span>  |
| <span data-ttu-id="e0fe6-117">indeterminado</span><span class="sxs-lookup"><span data-stu-id="e0fe6-117">indeterminate</span></span>         | <span data-ttu-id="e0fe6-118">Int64</span><span class="sxs-lookup"><span data-stu-id="e0fe6-118">Int64</span></span>  |
| <span data-ttu-id="e0fe6-119">reportDate</span><span class="sxs-lookup"><span data-stu-id="e0fe6-119">reportDate</span></span>            | <span data-ttu-id="e0fe6-120">Fecha</span><span class="sxs-lookup"><span data-stu-id="e0fe6-120">Date</span></span>   |
| <span data-ttu-id="e0fe6-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="e0fe6-121">reportPeriod</span></span>          | <span data-ttu-id="e0fe6-122">String</span><span class="sxs-lookup"><span data-stu-id="e0fe6-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="e0fe6-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e0fe6-123">JSON representation</span></span>

<span data-ttu-id="e0fe6-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e0fe6-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mailboxUsageQuotaStatusMailboxCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "underLimit": 1024, 
  "warningIssued": 1024, 
  "sendProhibited": 1024, 
  "sendReceiveProhibited": 1024, 
  "indeterminate": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
