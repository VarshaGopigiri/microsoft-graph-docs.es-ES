---
title: tipo de recurso mailboxUsageStorage
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 44b97c7b18264e01c86b34bfd8265246f80ab031
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917870"
---
# <a name="mailboxusagestorage-resource-type"></a><span data-ttu-id="27708-103">tipo de recurso mailboxUsageStorage</span><span class="sxs-lookup"><span data-stu-id="27708-103">mailboxUsageStorage resource type</span></span>

## <a name="properties"></a><span data-ttu-id="27708-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27708-104">Properties</span></span>

| <span data-ttu-id="27708-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27708-105">Property</span></span>           | <span data-ttu-id="27708-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="27708-106">Type</span></span>   |
| :----------------- | :----- |
| <span data-ttu-id="27708-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="27708-107">reportRefreshDate</span></span>  | <span data-ttu-id="27708-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="27708-108">Date</span></span>   |
| <span data-ttu-id="27708-109">storageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="27708-109">storageUsedInBytes</span></span> | <span data-ttu-id="27708-110">Int64</span><span class="sxs-lookup"><span data-stu-id="27708-110">Int64</span></span>  |
| <span data-ttu-id="27708-111">reportDate</span><span class="sxs-lookup"><span data-stu-id="27708-111">reportDate</span></span>         | <span data-ttu-id="27708-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="27708-112">Date</span></span>   |
| <span data-ttu-id="27708-113">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="27708-113">reportPeriod</span></span>       | <span data-ttu-id="27708-114">String</span><span class="sxs-lookup"><span data-stu-id="27708-114">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="27708-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="27708-115">JSON representation</span></span>

<span data-ttu-id="27708-116">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="27708-116">The following is a JSON representation of the resource.</span></span>

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
