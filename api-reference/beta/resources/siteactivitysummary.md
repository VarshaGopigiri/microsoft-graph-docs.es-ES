---
title: tipo de recurso siteActivitySummary
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 354b329f592964249590b2f551d66681f45de485
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086880"
---
# <a name="siteactivitysummary-resource-type"></a><span data-ttu-id="d477d-103">tipo de recurso siteActivitySummary</span><span class="sxs-lookup"><span data-stu-id="d477d-103">siteActivitySummary resource type</span></span>

## <a name="properties"></a><span data-ttu-id="d477d-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d477d-104">Properties</span></span>

| <span data-ttu-id="d477d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d477d-105">Property</span></span>          | <span data-ttu-id="d477d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="d477d-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="d477d-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="d477d-107">reportRefreshDate</span></span> | <span data-ttu-id="d477d-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="d477d-108">Date</span></span>   |
| <span data-ttu-id="d477d-109">viewedOrEdited</span><span class="sxs-lookup"><span data-stu-id="d477d-109">viewedOrEdited</span></span>    | <span data-ttu-id="d477d-110">Int64</span><span class="sxs-lookup"><span data-stu-id="d477d-110">Int64</span></span>  |
| <span data-ttu-id="d477d-111">sincronizado</span><span class="sxs-lookup"><span data-stu-id="d477d-111">synced</span></span>            | <span data-ttu-id="d477d-112">Int64</span><span class="sxs-lookup"><span data-stu-id="d477d-112">Int64</span></span>  |
| <span data-ttu-id="d477d-113">sharedInternally</span><span class="sxs-lookup"><span data-stu-id="d477d-113">sharedInternally</span></span>  | <span data-ttu-id="d477d-114">Int64</span><span class="sxs-lookup"><span data-stu-id="d477d-114">Int64</span></span>  |
| <span data-ttu-id="d477d-115">sharedExternally</span><span class="sxs-lookup"><span data-stu-id="d477d-115">sharedExternally</span></span>  | <span data-ttu-id="d477d-116">Int64</span><span class="sxs-lookup"><span data-stu-id="d477d-116">Int64</span></span>  |
| <span data-ttu-id="d477d-117">reportDate</span><span class="sxs-lookup"><span data-stu-id="d477d-117">reportDate</span></span>        | <span data-ttu-id="d477d-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="d477d-118">Date</span></span>   |
| <span data-ttu-id="d477d-119">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="d477d-119">reportPeriod</span></span>      | <span data-ttu-id="d477d-120">String</span><span class="sxs-lookup"><span data-stu-id="d477d-120">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="d477d-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d477d-121">JSON representation</span></span>

<span data-ttu-id="d477d-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d477d-122">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.siteActivitySummary"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "viewedOrEdited": 1024, 
  "synced": 1024, 
  "sharedInternally": 1024, 
  "sharedExternally": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
