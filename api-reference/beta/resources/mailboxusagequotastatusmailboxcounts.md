---
title: tipo de recurso mailboxUsageQuotaStatusMailboxCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 45e4754fef0dd3a2f7a669e3b3b96692d117c8f0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921237"
---
# <a name="mailboxusagequotastatusmailboxcounts-resource-type"></a><span data-ttu-id="41ff1-103">tipo de recurso mailboxUsageQuotaStatusMailboxCounts</span><span class="sxs-lookup"><span data-stu-id="41ff1-103">mailboxUsageQuotaStatusMailboxCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="41ff1-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41ff1-104">Properties</span></span>

| <span data-ttu-id="41ff1-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="41ff1-105">Property</span></span>              | <span data-ttu-id="41ff1-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="41ff1-106">Type</span></span>   |
| :-------------------- | :----- |
| <span data-ttu-id="41ff1-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="41ff1-107">reportRefreshDate</span></span>     | <span data-ttu-id="41ff1-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="41ff1-108">Date</span></span>   |
| <span data-ttu-id="41ff1-109">underLimit</span><span class="sxs-lookup"><span data-stu-id="41ff1-109">underLimit</span></span>            | <span data-ttu-id="41ff1-110">Int64</span><span class="sxs-lookup"><span data-stu-id="41ff1-110">Int64</span></span>  |
| <span data-ttu-id="41ff1-111">warningIssued</span><span class="sxs-lookup"><span data-stu-id="41ff1-111">warningIssued</span></span>         | <span data-ttu-id="41ff1-112">Int64</span><span class="sxs-lookup"><span data-stu-id="41ff1-112">Int64</span></span>  |
| <span data-ttu-id="41ff1-113">sendProhibited</span><span class="sxs-lookup"><span data-stu-id="41ff1-113">sendProhibited</span></span>        | <span data-ttu-id="41ff1-114">Int64</span><span class="sxs-lookup"><span data-stu-id="41ff1-114">Int64</span></span>  |
| <span data-ttu-id="41ff1-115">sendReceiveProhibited</span><span class="sxs-lookup"><span data-stu-id="41ff1-115">sendReceiveProhibited</span></span> | <span data-ttu-id="41ff1-116">Int64</span><span class="sxs-lookup"><span data-stu-id="41ff1-116">Int64</span></span>  |
| <span data-ttu-id="41ff1-117">indeterminado</span><span class="sxs-lookup"><span data-stu-id="41ff1-117">indeterminate</span></span>         | <span data-ttu-id="41ff1-118">Int64</span><span class="sxs-lookup"><span data-stu-id="41ff1-118">Int64</span></span>  |
| <span data-ttu-id="41ff1-119">reportDate</span><span class="sxs-lookup"><span data-stu-id="41ff1-119">reportDate</span></span>            | <span data-ttu-id="41ff1-120">Fecha</span><span class="sxs-lookup"><span data-stu-id="41ff1-120">Date</span></span>   |
| <span data-ttu-id="41ff1-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="41ff1-121">reportPeriod</span></span>          | <span data-ttu-id="41ff1-122">String</span><span class="sxs-lookup"><span data-stu-id="41ff1-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="41ff1-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="41ff1-123">JSON representation</span></span>

<span data-ttu-id="41ff1-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="41ff1-124">The following is a JSON representation of the resource.</span></span>

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
