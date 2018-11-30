---
title: tipo de recurso mailboxUsageStorage
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 8cc26c5d3cc30529857ed3273f8ee66c7373327a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084839"
---
# <a name="mailboxusagestorage-resource-type"></a><span data-ttu-id="69e82-103">tipo de recurso mailboxUsageStorage</span><span class="sxs-lookup"><span data-stu-id="69e82-103">mailboxUsageStorage resource type</span></span>

## <a name="properties"></a><span data-ttu-id="69e82-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="69e82-104">Properties</span></span>

| <span data-ttu-id="69e82-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="69e82-105">Property</span></span>           | <span data-ttu-id="69e82-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="69e82-106">Type</span></span>   |
| :----------------- | :----- |
| <span data-ttu-id="69e82-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="69e82-107">reportRefreshDate</span></span>  | <span data-ttu-id="69e82-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="69e82-108">Date</span></span>   |
| <span data-ttu-id="69e82-109">storageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="69e82-109">storageUsedInBytes</span></span> | <span data-ttu-id="69e82-110">Int64</span><span class="sxs-lookup"><span data-stu-id="69e82-110">Int64</span></span>  |
| <span data-ttu-id="69e82-111">reportDate</span><span class="sxs-lookup"><span data-stu-id="69e82-111">reportDate</span></span>         | <span data-ttu-id="69e82-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="69e82-112">Date</span></span>   |
| <span data-ttu-id="69e82-113">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="69e82-113">reportPeriod</span></span>       | <span data-ttu-id="69e82-114">String</span><span class="sxs-lookup"><span data-stu-id="69e82-114">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="69e82-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="69e82-115">JSON representation</span></span>

<span data-ttu-id="69e82-116">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="69e82-116">The following is a JSON representation of the resource.</span></span>

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
