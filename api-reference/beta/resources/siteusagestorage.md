---
title: tipo de recurso siteUsageStorage
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 1fdfa6cb2690d6dbacf5e534792061b6e64025d8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084388"
---
# <a name="siteusagestorage-resource-type"></a><span data-ttu-id="77494-103">tipo de recurso siteUsageStorage</span><span class="sxs-lookup"><span data-stu-id="77494-103">siteUsageStorage resource type</span></span>

## <a name="properties"></a><span data-ttu-id="77494-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="77494-104">Properties</span></span>

| <span data-ttu-id="77494-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="77494-105">Property</span></span>           | <span data-ttu-id="77494-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="77494-106">Type</span></span>   |
| :----------------- | :----- |
| <span data-ttu-id="77494-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="77494-107">reportRefreshDate</span></span>  | <span data-ttu-id="77494-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="77494-108">Date</span></span>   |
| <span data-ttu-id="77494-109">siteType</span><span class="sxs-lookup"><span data-stu-id="77494-109">siteType</span></span>           | <span data-ttu-id="77494-110">String</span><span class="sxs-lookup"><span data-stu-id="77494-110">String</span></span> |
| <span data-ttu-id="77494-111">storageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="77494-111">storageUsedInBytes</span></span> | <span data-ttu-id="77494-112">Int64</span><span class="sxs-lookup"><span data-stu-id="77494-112">Int64</span></span>  |
| <span data-ttu-id="77494-113">reportDate</span><span class="sxs-lookup"><span data-stu-id="77494-113">reportDate</span></span>         | <span data-ttu-id="77494-114">Fecha</span><span class="sxs-lookup"><span data-stu-id="77494-114">Date</span></span>   |
| <span data-ttu-id="77494-115">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="77494-115">reportPeriod</span></span>       | <span data-ttu-id="77494-116">String</span><span class="sxs-lookup"><span data-stu-id="77494-116">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="77494-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="77494-117">JSON representation</span></span>

<span data-ttu-id="77494-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="77494-118">The following is a JSON representation of the resource.</span></span>

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
