---
title: tipo de recurso siteActivitySummary
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 2eb5bdb89924338d1d352ea80bd516b8fb948250
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817769"
---
# <a name="siteactivitysummary-resource-type"></a><span data-ttu-id="c25ed-103">tipo de recurso siteActivitySummary</span><span class="sxs-lookup"><span data-stu-id="c25ed-103">siteActivitySummary resource type</span></span>

## <a name="properties"></a><span data-ttu-id="c25ed-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c25ed-104">Properties</span></span>

| <span data-ttu-id="c25ed-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c25ed-105">Property</span></span>          | <span data-ttu-id="c25ed-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="c25ed-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="c25ed-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="c25ed-107">reportRefreshDate</span></span> | <span data-ttu-id="c25ed-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="c25ed-108">Date</span></span>   |
| <span data-ttu-id="c25ed-109">viewedOrEdited</span><span class="sxs-lookup"><span data-stu-id="c25ed-109">viewedOrEdited</span></span>    | <span data-ttu-id="c25ed-110">Int64</span><span class="sxs-lookup"><span data-stu-id="c25ed-110">Int64</span></span>  |
| <span data-ttu-id="c25ed-111">sincronizado</span><span class="sxs-lookup"><span data-stu-id="c25ed-111">synced</span></span>            | <span data-ttu-id="c25ed-112">Int64</span><span class="sxs-lookup"><span data-stu-id="c25ed-112">Int64</span></span>  |
| <span data-ttu-id="c25ed-113">sharedInternally</span><span class="sxs-lookup"><span data-stu-id="c25ed-113">sharedInternally</span></span>  | <span data-ttu-id="c25ed-114">Int64</span><span class="sxs-lookup"><span data-stu-id="c25ed-114">Int64</span></span>  |
| <span data-ttu-id="c25ed-115">sharedExternally</span><span class="sxs-lookup"><span data-stu-id="c25ed-115">sharedExternally</span></span>  | <span data-ttu-id="c25ed-116">Int64</span><span class="sxs-lookup"><span data-stu-id="c25ed-116">Int64</span></span>  |
| <span data-ttu-id="c25ed-117">reportDate</span><span class="sxs-lookup"><span data-stu-id="c25ed-117">reportDate</span></span>        | <span data-ttu-id="c25ed-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="c25ed-118">Date</span></span>   |
| <span data-ttu-id="c25ed-119">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="c25ed-119">reportPeriod</span></span>      | <span data-ttu-id="c25ed-120">String</span><span class="sxs-lookup"><span data-stu-id="c25ed-120">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="c25ed-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c25ed-121">JSON representation</span></span>

<span data-ttu-id="c25ed-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="c25ed-122">The following is a JSON representation of the resource.</span></span>

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
