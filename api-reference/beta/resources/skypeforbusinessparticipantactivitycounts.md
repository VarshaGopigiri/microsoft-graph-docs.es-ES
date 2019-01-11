---
title: tipo de recurso skypeForBusinessParticipantActivityCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: de86c49da34c9af48478a912a6ab042a354a7bf5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27808193"
---
# <a name="skypeforbusinessparticipantactivitycounts-resource-type"></a><span data-ttu-id="ee69b-103">tipo de recurso skypeForBusinessParticipantActivityCounts</span><span class="sxs-lookup"><span data-stu-id="ee69b-103">skypeForBusinessParticipantActivityCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="ee69b-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ee69b-104">Properties</span></span>

| <span data-ttu-id="ee69b-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ee69b-105">Property</span></span>          | <span data-ttu-id="ee69b-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee69b-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="ee69b-107">mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="ee69b-107">im</span></span>                | <span data-ttu-id="ee69b-108">Int64</span><span class="sxs-lookup"><span data-stu-id="ee69b-108">Int64</span></span>  |
| <span data-ttu-id="ee69b-109">Recurso</span><span class="sxs-lookup"><span data-stu-id="ee69b-109">audioVideo</span></span>        | <span data-ttu-id="ee69b-110">Int64</span><span class="sxs-lookup"><span data-stu-id="ee69b-110">Int64</span></span>  |
| <span data-ttu-id="ee69b-111">uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ee69b-111">appSharing</span></span>        | <span data-ttu-id="ee69b-112">Int64</span><span class="sxs-lookup"><span data-stu-id="ee69b-112">Int64</span></span>  |
| <span data-ttu-id="ee69b-113">web</span><span class="sxs-lookup"><span data-stu-id="ee69b-113">web</span></span>               | <span data-ttu-id="ee69b-114">Int64</span><span class="sxs-lookup"><span data-stu-id="ee69b-114">Int64</span></span>  |
| <span data-ttu-id="ee69b-115">dialInOut3rdParty</span><span class="sxs-lookup"><span data-stu-id="ee69b-115">dialInOut3rdParty</span></span> | <span data-ttu-id="ee69b-116">Int64</span><span class="sxs-lookup"><span data-stu-id="ee69b-116">Int64</span></span>  |
| <span data-ttu-id="ee69b-117">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="ee69b-117">reportRefreshDate</span></span> | <span data-ttu-id="ee69b-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="ee69b-118">Date</span></span>   |
| <span data-ttu-id="ee69b-119">reportDate</span><span class="sxs-lookup"><span data-stu-id="ee69b-119">reportDate</span></span>        | <span data-ttu-id="ee69b-120">Fecha</span><span class="sxs-lookup"><span data-stu-id="ee69b-120">Date</span></span>   |
| <span data-ttu-id="ee69b-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="ee69b-121">reportPeriod</span></span>      | <span data-ttu-id="ee69b-122">String</span><span class="sxs-lookup"><span data-stu-id="ee69b-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="ee69b-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ee69b-123">JSON representation</span></span>

<span data-ttu-id="ee69b-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ee69b-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessParticipantActivityCounts"
} -->

```json
{
  "im": 1024, 
  "audioVideo": 1024, 
  "appSharing": 1024, 
  "web": 1024, 
  "dialInOut3rdParty": 1024, 
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
