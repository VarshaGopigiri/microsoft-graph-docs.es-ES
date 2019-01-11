---
title: tipo de recurso mailboxUsageStorage
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: dcabfab0e8a64f2d74442f7d7464708501a59b95
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840744"
---
# <a name="mailboxusagestorage-resource-type"></a><span data-ttu-id="a2981-103">tipo de recurso mailboxUsageStorage</span><span class="sxs-lookup"><span data-stu-id="a2981-103">mailboxUsageStorage resource type</span></span>

## <a name="properties"></a><span data-ttu-id="a2981-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a2981-104">Properties</span></span>

| <span data-ttu-id="a2981-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2981-105">Property</span></span>           | <span data-ttu-id="a2981-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2981-106">Type</span></span>   |
| :----------------- | :----- |
| <span data-ttu-id="a2981-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="a2981-107">reportRefreshDate</span></span>  | <span data-ttu-id="a2981-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="a2981-108">Date</span></span>   |
| <span data-ttu-id="a2981-109">storageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="a2981-109">storageUsedInBytes</span></span> | <span data-ttu-id="a2981-110">Int64</span><span class="sxs-lookup"><span data-stu-id="a2981-110">Int64</span></span>  |
| <span data-ttu-id="a2981-111">reportDate</span><span class="sxs-lookup"><span data-stu-id="a2981-111">reportDate</span></span>         | <span data-ttu-id="a2981-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="a2981-112">Date</span></span>   |
| <span data-ttu-id="a2981-113">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="a2981-113">reportPeriod</span></span>       | <span data-ttu-id="a2981-114">String</span><span class="sxs-lookup"><span data-stu-id="a2981-114">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="a2981-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a2981-115">JSON representation</span></span>

<span data-ttu-id="a2981-116">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a2981-116">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mailboxUsageStorage"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "storageUsedInBytes": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
