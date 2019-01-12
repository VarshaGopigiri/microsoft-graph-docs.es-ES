---
title: tipo de recurso siteActivitySummary
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: a49b8e47ca2a6efcc5c5c87702fdea0122b208e1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957140"
---
# <a name="siteactivitysummary-resource-type"></a><span data-ttu-id="a0b09-103">tipo de recurso siteActivitySummary</span><span class="sxs-lookup"><span data-stu-id="a0b09-103">siteActivitySummary resource type</span></span>

## <a name="properties"></a><span data-ttu-id="a0b09-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0b09-104">Properties</span></span>

| <span data-ttu-id="a0b09-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a0b09-105">Property</span></span>          | <span data-ttu-id="a0b09-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0b09-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="a0b09-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="a0b09-107">reportRefreshDate</span></span> | <span data-ttu-id="a0b09-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="a0b09-108">Date</span></span>   |
| <span data-ttu-id="a0b09-109">viewedOrEdited</span><span class="sxs-lookup"><span data-stu-id="a0b09-109">viewedOrEdited</span></span>    | <span data-ttu-id="a0b09-110">Int64</span><span class="sxs-lookup"><span data-stu-id="a0b09-110">Int64</span></span>  |
| <span data-ttu-id="a0b09-111">sincronizado</span><span class="sxs-lookup"><span data-stu-id="a0b09-111">synced</span></span>            | <span data-ttu-id="a0b09-112">Int64</span><span class="sxs-lookup"><span data-stu-id="a0b09-112">Int64</span></span>  |
| <span data-ttu-id="a0b09-113">sharedInternally</span><span class="sxs-lookup"><span data-stu-id="a0b09-113">sharedInternally</span></span>  | <span data-ttu-id="a0b09-114">Int64</span><span class="sxs-lookup"><span data-stu-id="a0b09-114">Int64</span></span>  |
| <span data-ttu-id="a0b09-115">sharedExternally</span><span class="sxs-lookup"><span data-stu-id="a0b09-115">sharedExternally</span></span>  | <span data-ttu-id="a0b09-116">Int64</span><span class="sxs-lookup"><span data-stu-id="a0b09-116">Int64</span></span>  |
| <span data-ttu-id="a0b09-117">reportDate</span><span class="sxs-lookup"><span data-stu-id="a0b09-117">reportDate</span></span>        | <span data-ttu-id="a0b09-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="a0b09-118">Date</span></span>   |
| <span data-ttu-id="a0b09-119">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="a0b09-119">reportPeriod</span></span>      | <span data-ttu-id="a0b09-120">String</span><span class="sxs-lookup"><span data-stu-id="a0b09-120">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="a0b09-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a0b09-121">JSON representation</span></span>

<span data-ttu-id="a0b09-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a0b09-122">The following is a JSON representation of the resource.</span></span>

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
