---
title: tipo de recurso siteUsageStorage
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 1f656feacdbba3418049bd9f3072270aa04af798
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879929"
---
# <a name="siteusagestorage-resource-type"></a><span data-ttu-id="99ba8-103">tipo de recurso siteUsageStorage</span><span class="sxs-lookup"><span data-stu-id="99ba8-103">siteUsageStorage resource type</span></span>

## <a name="properties"></a><span data-ttu-id="99ba8-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="99ba8-104">Properties</span></span>

| <span data-ttu-id="99ba8-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="99ba8-105">Property</span></span>           | <span data-ttu-id="99ba8-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="99ba8-106">Type</span></span>   |
| :----------------- | :----- |
| <span data-ttu-id="99ba8-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="99ba8-107">reportRefreshDate</span></span>  | <span data-ttu-id="99ba8-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="99ba8-108">Date</span></span>   |
| <span data-ttu-id="99ba8-109">siteType</span><span class="sxs-lookup"><span data-stu-id="99ba8-109">siteType</span></span>           | <span data-ttu-id="99ba8-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="99ba8-110">String</span></span> |
| <span data-ttu-id="99ba8-111">storageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="99ba8-111">storageUsedInBytes</span></span> | <span data-ttu-id="99ba8-112">Int64</span><span class="sxs-lookup"><span data-stu-id="99ba8-112">Int64</span></span>  |
| <span data-ttu-id="99ba8-113">reportDate</span><span class="sxs-lookup"><span data-stu-id="99ba8-113">reportDate</span></span>         | <span data-ttu-id="99ba8-114">Fecha</span><span class="sxs-lookup"><span data-stu-id="99ba8-114">Date</span></span>   |
| <span data-ttu-id="99ba8-115">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="99ba8-115">reportPeriod</span></span>       | <span data-ttu-id="99ba8-116">String</span><span class="sxs-lookup"><span data-stu-id="99ba8-116">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="99ba8-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="99ba8-117">JSON representation</span></span>

<span data-ttu-id="99ba8-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="99ba8-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.siteUsageStorage"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "siteType": "String", 
  "storageUsedInBytes": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
