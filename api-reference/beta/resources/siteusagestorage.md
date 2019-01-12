---
title: tipo de recurso siteUsageStorage
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: c136b776e0c96a8bc63a1c82ae2ad17f059026cc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928104"
---
# <a name="siteusagestorage-resource-type"></a><span data-ttu-id="85c3c-103">tipo de recurso siteUsageStorage</span><span class="sxs-lookup"><span data-stu-id="85c3c-103">siteUsageStorage resource type</span></span>

## <a name="properties"></a><span data-ttu-id="85c3c-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85c3c-104">Properties</span></span>

| <span data-ttu-id="85c3c-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="85c3c-105">Property</span></span>           | <span data-ttu-id="85c3c-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="85c3c-106">Type</span></span>   |
| :----------------- | :----- |
| <span data-ttu-id="85c3c-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="85c3c-107">reportRefreshDate</span></span>  | <span data-ttu-id="85c3c-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="85c3c-108">Date</span></span>   |
| <span data-ttu-id="85c3c-109">siteType</span><span class="sxs-lookup"><span data-stu-id="85c3c-109">siteType</span></span>           | <span data-ttu-id="85c3c-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="85c3c-110">String</span></span> |
| <span data-ttu-id="85c3c-111">storageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="85c3c-111">storageUsedInBytes</span></span> | <span data-ttu-id="85c3c-112">Int64</span><span class="sxs-lookup"><span data-stu-id="85c3c-112">Int64</span></span>  |
| <span data-ttu-id="85c3c-113">reportDate</span><span class="sxs-lookup"><span data-stu-id="85c3c-113">reportDate</span></span>         | <span data-ttu-id="85c3c-114">Fecha</span><span class="sxs-lookup"><span data-stu-id="85c3c-114">Date</span></span>   |
| <span data-ttu-id="85c3c-115">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="85c3c-115">reportPeriod</span></span>       | <span data-ttu-id="85c3c-116">String</span><span class="sxs-lookup"><span data-stu-id="85c3c-116">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="85c3c-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="85c3c-117">JSON representation</span></span>

<span data-ttu-id="85c3c-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="85c3c-118">The following is a JSON representation of the resource.</span></span>

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
