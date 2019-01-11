---
title: tipo de recurso emailActivitySummary
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 82fbdc2621b9c8746ed3028fe44414edeb7e56db
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871347"
---
# <a name="emailactivitysummary-resource-type"></a><span data-ttu-id="b26e0-103">tipo de recurso emailActivitySummary</span><span class="sxs-lookup"><span data-stu-id="b26e0-103">emailActivitySummary resource type</span></span>

## <a name="properties"></a><span data-ttu-id="b26e0-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b26e0-104">Properties</span></span>

| <span data-ttu-id="b26e0-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b26e0-105">Property</span></span>          | <span data-ttu-id="b26e0-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="b26e0-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="b26e0-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="b26e0-107">reportRefreshDate</span></span> | <span data-ttu-id="b26e0-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="b26e0-108">Date</span></span>   |
| <span data-ttu-id="b26e0-109">enviar</span><span class="sxs-lookup"><span data-stu-id="b26e0-109">send</span></span>              | <span data-ttu-id="b26e0-110">Int64</span><span class="sxs-lookup"><span data-stu-id="b26e0-110">Int64</span></span>  |
| <span data-ttu-id="b26e0-111">recibir</span><span class="sxs-lookup"><span data-stu-id="b26e0-111">receive</span></span>           | <span data-ttu-id="b26e0-112">Int64</span><span class="sxs-lookup"><span data-stu-id="b26e0-112">Int64</span></span>  |
| <span data-ttu-id="b26e0-113">lectura</span><span class="sxs-lookup"><span data-stu-id="b26e0-113">read</span></span>              | <span data-ttu-id="b26e0-114">Int64</span><span class="sxs-lookup"><span data-stu-id="b26e0-114">Int64</span></span>  |
| <span data-ttu-id="b26e0-115">reportDate</span><span class="sxs-lookup"><span data-stu-id="b26e0-115">reportDate</span></span>        | <span data-ttu-id="b26e0-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="b26e0-116">Date</span></span>   |
| <span data-ttu-id="b26e0-117">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="b26e0-117">reportPeriod</span></span>      | <span data-ttu-id="b26e0-118">String</span><span class="sxs-lookup"><span data-stu-id="b26e0-118">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="b26e0-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b26e0-119">JSON representation</span></span>

<span data-ttu-id="b26e0-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b26e0-120">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.emailActivitySummary"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "send": 1024, 
  "receive": 1024, 
  "read": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
