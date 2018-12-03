---
title: tipo de recurso skypeForBusinessOrganizerActivityCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 0729aef6367ebcb0a5edfaa461d80ffd8cb0775c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091164"
---
# <a name="skypeforbusinessorganizeractivitycounts-resource-type"></a><span data-ttu-id="633eb-103">tipo de recurso skypeForBusinessOrganizerActivityCounts</span><span class="sxs-lookup"><span data-stu-id="633eb-103">skypeForBusinessOrganizerActivityCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="633eb-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="633eb-104">Properties</span></span>

| <span data-ttu-id="633eb-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="633eb-105">Property</span></span>           | <span data-ttu-id="633eb-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="633eb-106">Type</span></span>   |
| :----------------- | :----- |
| <span data-ttu-id="633eb-107">mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="633eb-107">im</span></span>                 | <span data-ttu-id="633eb-108">Int64</span><span class="sxs-lookup"><span data-stu-id="633eb-108">Int64</span></span>  |
| <span data-ttu-id="633eb-109">Recurso</span><span class="sxs-lookup"><span data-stu-id="633eb-109">audioVideo</span></span>         | <span data-ttu-id="633eb-110">Int64</span><span class="sxs-lookup"><span data-stu-id="633eb-110">Int64</span></span>  |
| <span data-ttu-id="633eb-111">uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="633eb-111">appSharing</span></span>         | <span data-ttu-id="633eb-112">Int64</span><span class="sxs-lookup"><span data-stu-id="633eb-112">Int64</span></span>  |
| <span data-ttu-id="633eb-113">web</span><span class="sxs-lookup"><span data-stu-id="633eb-113">web</span></span>                | <span data-ttu-id="633eb-114">Int64</span><span class="sxs-lookup"><span data-stu-id="633eb-114">Int64</span></span>  |
| <span data-ttu-id="633eb-115">dialInOut3rdParty</span><span class="sxs-lookup"><span data-stu-id="633eb-115">dialInOut3rdParty</span></span>  | <span data-ttu-id="633eb-116">Int64</span><span class="sxs-lookup"><span data-stu-id="633eb-116">Int64</span></span>  |
| <span data-ttu-id="633eb-117">dialInOutMicrosoft</span><span class="sxs-lookup"><span data-stu-id="633eb-117">dialInOutMicrosoft</span></span> | <span data-ttu-id="633eb-118">Int64</span><span class="sxs-lookup"><span data-stu-id="633eb-118">Int64</span></span>  |
| <span data-ttu-id="633eb-119">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="633eb-119">reportRefreshDate</span></span>  | <span data-ttu-id="633eb-120">Fecha</span><span class="sxs-lookup"><span data-stu-id="633eb-120">Date</span></span>   |
| <span data-ttu-id="633eb-121">reportDate</span><span class="sxs-lookup"><span data-stu-id="633eb-121">reportDate</span></span>         | <span data-ttu-id="633eb-122">Fecha</span><span class="sxs-lookup"><span data-stu-id="633eb-122">Date</span></span>   |
| <span data-ttu-id="633eb-123">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="633eb-123">reportPeriod</span></span>       | <span data-ttu-id="633eb-124">String</span><span class="sxs-lookup"><span data-stu-id="633eb-124">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="633eb-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="633eb-125">JSON representation</span></span>

<span data-ttu-id="633eb-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="633eb-126">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessOrganizerActivityCounts"
} -->

```json
{
  "im": 1024, 
  "audioVideo": 1024, 
  "appSharing": 1024, 
  "web": 1024, 
  "dialInOut3rdParty": 1024, 
  "dialInOutMicrosoft": 1024, 
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```