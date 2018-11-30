---
title: tipo de recurso mailboxUsageQuotaStatusMailboxCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: ac6c597cad9d28f985da97d6f55a5726ebbf491e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086042"
---
# <a name="mailboxusagequotastatusmailboxcounts-resource-type"></a><span data-ttu-id="610e4-103">tipo de recurso mailboxUsageQuotaStatusMailboxCounts</span><span class="sxs-lookup"><span data-stu-id="610e4-103">mailboxUsageQuotaStatusMailboxCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="610e4-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="610e4-104">Properties</span></span>

| <span data-ttu-id="610e4-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="610e4-105">Property</span></span>              | <span data-ttu-id="610e4-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="610e4-106">Type</span></span>   |
| :-------------------- | :----- |
| <span data-ttu-id="610e4-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="610e4-107">reportRefreshDate</span></span>     | <span data-ttu-id="610e4-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="610e4-108">Date</span></span>   |
| <span data-ttu-id="610e4-109">underLimit</span><span class="sxs-lookup"><span data-stu-id="610e4-109">underLimit</span></span>            | <span data-ttu-id="610e4-110">Int64</span><span class="sxs-lookup"><span data-stu-id="610e4-110">Int64</span></span>  |
| <span data-ttu-id="610e4-111">warningIssued</span><span class="sxs-lookup"><span data-stu-id="610e4-111">warningIssued</span></span>         | <span data-ttu-id="610e4-112">Int64</span><span class="sxs-lookup"><span data-stu-id="610e4-112">Int64</span></span>  |
| <span data-ttu-id="610e4-113">sendProhibited</span><span class="sxs-lookup"><span data-stu-id="610e4-113">sendProhibited</span></span>        | <span data-ttu-id="610e4-114">Int64</span><span class="sxs-lookup"><span data-stu-id="610e4-114">Int64</span></span>  |
| <span data-ttu-id="610e4-115">sendReceiveProhibited</span><span class="sxs-lookup"><span data-stu-id="610e4-115">sendReceiveProhibited</span></span> | <span data-ttu-id="610e4-116">Int64</span><span class="sxs-lookup"><span data-stu-id="610e4-116">Int64</span></span>  |
| <span data-ttu-id="610e4-117">indeterminado</span><span class="sxs-lookup"><span data-stu-id="610e4-117">indeterminate</span></span>         | <span data-ttu-id="610e4-118">Int64</span><span class="sxs-lookup"><span data-stu-id="610e4-118">Int64</span></span>  |
| <span data-ttu-id="610e4-119">reportDate</span><span class="sxs-lookup"><span data-stu-id="610e4-119">reportDate</span></span>            | <span data-ttu-id="610e4-120">Fecha</span><span class="sxs-lookup"><span data-stu-id="610e4-120">Date</span></span>   |
| <span data-ttu-id="610e4-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="610e4-121">reportPeriod</span></span>          | <span data-ttu-id="610e4-122">String</span><span class="sxs-lookup"><span data-stu-id="610e4-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="610e4-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="610e4-123">JSON representation</span></span>

<span data-ttu-id="610e4-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="610e4-124">The following is a JSON representation of the resource.</span></span>

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
