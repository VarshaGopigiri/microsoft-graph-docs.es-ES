---
title: tipo de recurso emailAppUsageVersionsUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 7b4a59a1e15ddf41f0e4204efc4d3e0c6549e587
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088541"
---
# <a name="emailappusageversionsusercounts-resource-type"></a><span data-ttu-id="0f897-103">tipo de recurso emailAppUsageVersionsUserCounts</span><span class="sxs-lookup"><span data-stu-id="0f897-103">emailAppUsageVersionsUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="0f897-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0f897-104">Properties</span></span>

| <span data-ttu-id="0f897-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0f897-105">Property</span></span>          | <span data-ttu-id="0f897-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="0f897-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="0f897-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="0f897-107">reportRefreshDate</span></span> | <span data-ttu-id="0f897-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="0f897-108">Date</span></span>   |
| <span data-ttu-id="0f897-109">outlook2016</span><span class="sxs-lookup"><span data-stu-id="0f897-109">outlook2016</span></span>       | <span data-ttu-id="0f897-110">Int64</span><span class="sxs-lookup"><span data-stu-id="0f897-110">Int64</span></span>  |
| <span data-ttu-id="0f897-111">outlook2013</span><span class="sxs-lookup"><span data-stu-id="0f897-111">outlook2013</span></span>       | <span data-ttu-id="0f897-112">Int64</span><span class="sxs-lookup"><span data-stu-id="0f897-112">Int64</span></span>  |
| <span data-ttu-id="0f897-113">outlook2010</span><span class="sxs-lookup"><span data-stu-id="0f897-113">outlook2010</span></span>       | <span data-ttu-id="0f897-114">Int64</span><span class="sxs-lookup"><span data-stu-id="0f897-114">Int64</span></span>  |
| <span data-ttu-id="0f897-115">Outlook2007</span><span class="sxs-lookup"><span data-stu-id="0f897-115">outlook2007</span></span>       | <span data-ttu-id="0f897-116">Int64</span><span class="sxs-lookup"><span data-stu-id="0f897-116">Int64</span></span>  |
| <span data-ttu-id="0f897-117">indeterminado</span><span class="sxs-lookup"><span data-stu-id="0f897-117">undetermined</span></span>      | <span data-ttu-id="0f897-118">Int64</span><span class="sxs-lookup"><span data-stu-id="0f897-118">Int64</span></span>  |
| <span data-ttu-id="0f897-119">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="0f897-119">reportPeriod</span></span>      | <span data-ttu-id="0f897-120">String</span><span class="sxs-lookup"><span data-stu-id="0f897-120">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="0f897-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0f897-121">JSON representation</span></span>

<span data-ttu-id="0f897-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0f897-122">The following is a JSON representation of the resource.</span></span>

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
