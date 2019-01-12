---
title: tipo de recurso emailAppUsageVersionsUserCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 371352c42e870f45224999b7a618d1bb694ea512
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965288"
---
# <a name="emailappusageversionsusercounts-resource-type"></a><span data-ttu-id="1cc44-103">tipo de recurso emailAppUsageVersionsUserCounts</span><span class="sxs-lookup"><span data-stu-id="1cc44-103">emailAppUsageVersionsUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="1cc44-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1cc44-104">Properties</span></span>

| <span data-ttu-id="1cc44-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1cc44-105">Property</span></span>          | <span data-ttu-id="1cc44-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="1cc44-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="1cc44-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="1cc44-107">reportRefreshDate</span></span> | <span data-ttu-id="1cc44-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="1cc44-108">Date</span></span>   |
| <span data-ttu-id="1cc44-109">outlook2016</span><span class="sxs-lookup"><span data-stu-id="1cc44-109">outlook2016</span></span>       | <span data-ttu-id="1cc44-110">Int64</span><span class="sxs-lookup"><span data-stu-id="1cc44-110">Int64</span></span>  |
| <span data-ttu-id="1cc44-111">outlook2013</span><span class="sxs-lookup"><span data-stu-id="1cc44-111">outlook2013</span></span>       | <span data-ttu-id="1cc44-112">Int64</span><span class="sxs-lookup"><span data-stu-id="1cc44-112">Int64</span></span>  |
| <span data-ttu-id="1cc44-113">outlook2010</span><span class="sxs-lookup"><span data-stu-id="1cc44-113">outlook2010</span></span>       | <span data-ttu-id="1cc44-114">Int64</span><span class="sxs-lookup"><span data-stu-id="1cc44-114">Int64</span></span>  |
| <span data-ttu-id="1cc44-115">Outlook2007</span><span class="sxs-lookup"><span data-stu-id="1cc44-115">outlook2007</span></span>       | <span data-ttu-id="1cc44-116">Int64</span><span class="sxs-lookup"><span data-stu-id="1cc44-116">Int64</span></span>  |
| <span data-ttu-id="1cc44-117">indeterminado</span><span class="sxs-lookup"><span data-stu-id="1cc44-117">undetermined</span></span>      | <span data-ttu-id="1cc44-118">Int64</span><span class="sxs-lookup"><span data-stu-id="1cc44-118">Int64</span></span>  |
| <span data-ttu-id="1cc44-119">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="1cc44-119">reportPeriod</span></span>      | <span data-ttu-id="1cc44-120">String</span><span class="sxs-lookup"><span data-stu-id="1cc44-120">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="1cc44-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1cc44-121">JSON representation</span></span>

<span data-ttu-id="1cc44-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1cc44-122">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.emailAppUsageVersionsUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "outlook2016": 1024, 
  "outlook2013": 1024, 
  "outlook2010": 1024, 
  "outlook2007": 1024, 
  "undetermined": 1024, 
  "reportPeriod": "String"
}
```
