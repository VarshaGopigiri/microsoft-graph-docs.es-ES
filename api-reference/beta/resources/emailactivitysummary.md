---
title: tipo de recurso emailActivitySummary
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 039592a33cd004b9a5dc7800c0dbd4ece91bd48c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088552"
---
# <a name="emailactivitysummary-resource-type"></a><span data-ttu-id="3641e-103">tipo de recurso emailActivitySummary</span><span class="sxs-lookup"><span data-stu-id="3641e-103">emailActivitySummary resource type</span></span>

## <a name="properties"></a><span data-ttu-id="3641e-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3641e-104">Properties</span></span>

| <span data-ttu-id="3641e-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3641e-105">Property</span></span>          | <span data-ttu-id="3641e-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="3641e-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="3641e-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="3641e-107">reportRefreshDate</span></span> | <span data-ttu-id="3641e-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="3641e-108">Date</span></span>   |
| <span data-ttu-id="3641e-109">enviar</span><span class="sxs-lookup"><span data-stu-id="3641e-109">send</span></span>              | <span data-ttu-id="3641e-110">Int64</span><span class="sxs-lookup"><span data-stu-id="3641e-110">Int64</span></span>  |
| <span data-ttu-id="3641e-111">recibir</span><span class="sxs-lookup"><span data-stu-id="3641e-111">receive</span></span>           | <span data-ttu-id="3641e-112">Int64</span><span class="sxs-lookup"><span data-stu-id="3641e-112">Int64</span></span>  |
| <span data-ttu-id="3641e-113">lectura</span><span class="sxs-lookup"><span data-stu-id="3641e-113">read</span></span>              | <span data-ttu-id="3641e-114">Int64</span><span class="sxs-lookup"><span data-stu-id="3641e-114">Int64</span></span>  |
| <span data-ttu-id="3641e-115">reportDate</span><span class="sxs-lookup"><span data-stu-id="3641e-115">reportDate</span></span>        | <span data-ttu-id="3641e-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="3641e-116">Date</span></span>   |
| <span data-ttu-id="3641e-117">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="3641e-117">reportPeriod</span></span>      | <span data-ttu-id="3641e-118">String</span><span class="sxs-lookup"><span data-stu-id="3641e-118">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="3641e-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3641e-119">JSON representation</span></span>

<span data-ttu-id="3641e-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3641e-120">The following is a JSON representation of the resource.</span></span>

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