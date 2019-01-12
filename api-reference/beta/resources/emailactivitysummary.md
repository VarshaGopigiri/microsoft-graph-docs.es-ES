---
title: tipo de recurso emailActivitySummary
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 84958874af09b31aafed694c1a62d080a5c798ce
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990092"
---
# <a name="emailactivitysummary-resource-type"></a><span data-ttu-id="a5126-103">tipo de recurso emailActivitySummary</span><span class="sxs-lookup"><span data-stu-id="a5126-103">emailActivitySummary resource type</span></span>

## <a name="properties"></a><span data-ttu-id="a5126-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a5126-104">Properties</span></span>

| <span data-ttu-id="a5126-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a5126-105">Property</span></span>          | <span data-ttu-id="a5126-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5126-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="a5126-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="a5126-107">reportRefreshDate</span></span> | <span data-ttu-id="a5126-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="a5126-108">Date</span></span>   |
| <span data-ttu-id="a5126-109">enviar</span><span class="sxs-lookup"><span data-stu-id="a5126-109">send</span></span>              | <span data-ttu-id="a5126-110">Int64</span><span class="sxs-lookup"><span data-stu-id="a5126-110">Int64</span></span>  |
| <span data-ttu-id="a5126-111">recibir</span><span class="sxs-lookup"><span data-stu-id="a5126-111">receive</span></span>           | <span data-ttu-id="a5126-112">Int64</span><span class="sxs-lookup"><span data-stu-id="a5126-112">Int64</span></span>  |
| <span data-ttu-id="a5126-113">lectura</span><span class="sxs-lookup"><span data-stu-id="a5126-113">read</span></span>              | <span data-ttu-id="a5126-114">Int64</span><span class="sxs-lookup"><span data-stu-id="a5126-114">Int64</span></span>  |
| <span data-ttu-id="a5126-115">reportDate</span><span class="sxs-lookup"><span data-stu-id="a5126-115">reportDate</span></span>        | <span data-ttu-id="a5126-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="a5126-116">Date</span></span>   |
| <span data-ttu-id="a5126-117">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="a5126-117">reportPeriod</span></span>      | <span data-ttu-id="a5126-118">String</span><span class="sxs-lookup"><span data-stu-id="a5126-118">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="a5126-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a5126-119">JSON representation</span></span>

<span data-ttu-id="a5126-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a5126-120">The following is a JSON representation of the resource.</span></span>

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
