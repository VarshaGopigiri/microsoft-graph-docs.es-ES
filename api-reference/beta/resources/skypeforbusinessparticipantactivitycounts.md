---
title: tipo de recurso skypeForBusinessParticipantActivityCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 1e61526b281a87370835e8f6558ab3f0cb5707a4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086878"
---
# <a name="skypeforbusinessparticipantactivitycounts-resource-type"></a><span data-ttu-id="95b93-103">tipo de recurso skypeForBusinessParticipantActivityCounts</span><span class="sxs-lookup"><span data-stu-id="95b93-103">skypeForBusinessParticipantActivityCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="95b93-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95b93-104">Properties</span></span>

| <span data-ttu-id="95b93-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="95b93-105">Property</span></span>          | <span data-ttu-id="95b93-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="95b93-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="95b93-107">mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="95b93-107">im</span></span>                | <span data-ttu-id="95b93-108">Int64</span><span class="sxs-lookup"><span data-stu-id="95b93-108">Int64</span></span>  |
| <span data-ttu-id="95b93-109">Recurso</span><span class="sxs-lookup"><span data-stu-id="95b93-109">audioVideo</span></span>        | <span data-ttu-id="95b93-110">Int64</span><span class="sxs-lookup"><span data-stu-id="95b93-110">Int64</span></span>  |
| <span data-ttu-id="95b93-111">uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="95b93-111">appSharing</span></span>        | <span data-ttu-id="95b93-112">Int64</span><span class="sxs-lookup"><span data-stu-id="95b93-112">Int64</span></span>  |
| <span data-ttu-id="95b93-113">web</span><span class="sxs-lookup"><span data-stu-id="95b93-113">web</span></span>               | <span data-ttu-id="95b93-114">Int64</span><span class="sxs-lookup"><span data-stu-id="95b93-114">Int64</span></span>  |
| <span data-ttu-id="95b93-115">dialInOut3rdParty</span><span class="sxs-lookup"><span data-stu-id="95b93-115">dialInOut3rdParty</span></span> | <span data-ttu-id="95b93-116">Int64</span><span class="sxs-lookup"><span data-stu-id="95b93-116">Int64</span></span>  |
| <span data-ttu-id="95b93-117">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="95b93-117">reportRefreshDate</span></span> | <span data-ttu-id="95b93-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="95b93-118">Date</span></span>   |
| <span data-ttu-id="95b93-119">reportDate</span><span class="sxs-lookup"><span data-stu-id="95b93-119">reportDate</span></span>        | <span data-ttu-id="95b93-120">Fecha</span><span class="sxs-lookup"><span data-stu-id="95b93-120">Date</span></span>   |
| <span data-ttu-id="95b93-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="95b93-121">reportPeriod</span></span>      | <span data-ttu-id="95b93-122">String</span><span class="sxs-lookup"><span data-stu-id="95b93-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="95b93-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="95b93-123">JSON representation</span></span>

<span data-ttu-id="95b93-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="95b93-124">The following is a JSON representation of the resource.</span></span>

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
