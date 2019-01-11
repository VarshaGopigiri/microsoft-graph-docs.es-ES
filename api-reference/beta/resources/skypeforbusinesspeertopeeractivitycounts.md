---
title: tipo de recurso skypeForBusinessPeerToPeerActivityCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 4baf218ed9398a8f208c4d1d44a28579773dea6f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874476"
---
# <a name="skypeforbusinesspeertopeeractivitycounts-resource-type"></a><span data-ttu-id="cefd3-103">tipo de recurso skypeForBusinessPeerToPeerActivityCounts</span><span class="sxs-lookup"><span data-stu-id="cefd3-103">skypeForBusinessPeerToPeerActivityCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="cefd3-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cefd3-104">Properties</span></span>

| <span data-ttu-id="cefd3-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cefd3-105">Property</span></span>          | <span data-ttu-id="cefd3-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="cefd3-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="cefd3-107">mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="cefd3-107">im</span></span>                | <span data-ttu-id="cefd3-108">Int64</span><span class="sxs-lookup"><span data-stu-id="cefd3-108">Int64</span></span>  |
| <span data-ttu-id="cefd3-109">audio</span><span class="sxs-lookup"><span data-stu-id="cefd3-109">audio</span></span>             | <span data-ttu-id="cefd3-110">Int64</span><span class="sxs-lookup"><span data-stu-id="cefd3-110">Int64</span></span>  |
| <span data-ttu-id="cefd3-111">video</span><span class="sxs-lookup"><span data-stu-id="cefd3-111">video</span></span>             | <span data-ttu-id="cefd3-112">Int64</span><span class="sxs-lookup"><span data-stu-id="cefd3-112">Int64</span></span>  |
| <span data-ttu-id="cefd3-113">uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="cefd3-113">appSharing</span></span>        | <span data-ttu-id="cefd3-114">Int64</span><span class="sxs-lookup"><span data-stu-id="cefd3-114">Int64</span></span>  |
| <span data-ttu-id="cefd3-115">fileTransfer</span><span class="sxs-lookup"><span data-stu-id="cefd3-115">fileTransfer</span></span>      | <span data-ttu-id="cefd3-116">Int64</span><span class="sxs-lookup"><span data-stu-id="cefd3-116">Int64</span></span>  |
| <span data-ttu-id="cefd3-117">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="cefd3-117">reportRefreshDate</span></span> | <span data-ttu-id="cefd3-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="cefd3-118">Date</span></span>   |
| <span data-ttu-id="cefd3-119">reportDate</span><span class="sxs-lookup"><span data-stu-id="cefd3-119">reportDate</span></span>        | <span data-ttu-id="cefd3-120">Fecha</span><span class="sxs-lookup"><span data-stu-id="cefd3-120">Date</span></span>   |
| <span data-ttu-id="cefd3-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="cefd3-121">reportPeriod</span></span>      | <span data-ttu-id="cefd3-122">String</span><span class="sxs-lookup"><span data-stu-id="cefd3-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="cefd3-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cefd3-123">JSON representation</span></span>

<span data-ttu-id="cefd3-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="cefd3-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessPeerToPeerActivityCounts"
} -->

```json
{
  "im": 1024, 
  "audio": 1024, 
  "video": 1024, 
  "appSharing": 1024, 
  "fileTransfer": 1024, 
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
