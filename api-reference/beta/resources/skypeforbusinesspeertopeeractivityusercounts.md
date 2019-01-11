---
title: tipo de recurso skypeForBusinessPeerToPeerActivityUserCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 619e581fcdd25dda10be7210aefe5db8e4dcd8b7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828640"
---
# <a name="skypeforbusinesspeertopeeractivityusercounts-resource-type"></a><span data-ttu-id="4779f-103">tipo de recurso skypeForBusinessPeerToPeerActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="4779f-103">skypeForBusinessPeerToPeerActivityUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="4779f-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4779f-104">Properties</span></span>

| <span data-ttu-id="4779f-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4779f-105">Property</span></span>          | <span data-ttu-id="4779f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4779f-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="4779f-107">mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="4779f-107">im</span></span>                | <span data-ttu-id="4779f-108">Int64</span><span class="sxs-lookup"><span data-stu-id="4779f-108">Int64</span></span>  |
| <span data-ttu-id="4779f-109">audio</span><span class="sxs-lookup"><span data-stu-id="4779f-109">audio</span></span>             | <span data-ttu-id="4779f-110">Int64</span><span class="sxs-lookup"><span data-stu-id="4779f-110">Int64</span></span>  |
| <span data-ttu-id="4779f-111">video</span><span class="sxs-lookup"><span data-stu-id="4779f-111">video</span></span>             | <span data-ttu-id="4779f-112">Int64</span><span class="sxs-lookup"><span data-stu-id="4779f-112">Int64</span></span>  |
| <span data-ttu-id="4779f-113">uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4779f-113">appSharing</span></span>        | <span data-ttu-id="4779f-114">Int64</span><span class="sxs-lookup"><span data-stu-id="4779f-114">Int64</span></span>  |
| <span data-ttu-id="4779f-115">fileTransfer</span><span class="sxs-lookup"><span data-stu-id="4779f-115">fileTransfer</span></span>      | <span data-ttu-id="4779f-116">Int64</span><span class="sxs-lookup"><span data-stu-id="4779f-116">Int64</span></span>  |
| <span data-ttu-id="4779f-117">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="4779f-117">reportRefreshDate</span></span> | <span data-ttu-id="4779f-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="4779f-118">Date</span></span>   |
| <span data-ttu-id="4779f-119">reportDate</span><span class="sxs-lookup"><span data-stu-id="4779f-119">reportDate</span></span>        | <span data-ttu-id="4779f-120">Fecha</span><span class="sxs-lookup"><span data-stu-id="4779f-120">Date</span></span>   |
| <span data-ttu-id="4779f-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="4779f-121">reportPeriod</span></span>      | <span data-ttu-id="4779f-122">String</span><span class="sxs-lookup"><span data-stu-id="4779f-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="4779f-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4779f-123">JSON representation</span></span>

<span data-ttu-id="4779f-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4779f-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessPeerToPeerActivityUserCounts"
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
