---
title: tipo de recurso skypeForBusinessPeerToPeerActivityCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: cdc8ec2a63c4a03ac8b77bedba06c6addfba4584
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086470"
---
# <a name="skypeforbusinesspeertopeeractivitycounts-resource-type"></a><span data-ttu-id="60153-103">tipo de recurso skypeForBusinessPeerToPeerActivityCounts</span><span class="sxs-lookup"><span data-stu-id="60153-103">skypeForBusinessPeerToPeerActivityCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="60153-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60153-104">Properties</span></span>

| <span data-ttu-id="60153-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60153-105">Property</span></span>          | <span data-ttu-id="60153-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="60153-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="60153-107">mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="60153-107">im</span></span>                | <span data-ttu-id="60153-108">Int64</span><span class="sxs-lookup"><span data-stu-id="60153-108">Int64</span></span>  |
| <span data-ttu-id="60153-109">audio</span><span class="sxs-lookup"><span data-stu-id="60153-109">audio</span></span>             | <span data-ttu-id="60153-110">Int64</span><span class="sxs-lookup"><span data-stu-id="60153-110">Int64</span></span>  |
| <span data-ttu-id="60153-111">video</span><span class="sxs-lookup"><span data-stu-id="60153-111">video</span></span>             | <span data-ttu-id="60153-112">Int64</span><span class="sxs-lookup"><span data-stu-id="60153-112">Int64</span></span>  |
| <span data-ttu-id="60153-113">uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="60153-113">appSharing</span></span>        | <span data-ttu-id="60153-114">Int64</span><span class="sxs-lookup"><span data-stu-id="60153-114">Int64</span></span>  |
| <span data-ttu-id="60153-115">fileTransfer</span><span class="sxs-lookup"><span data-stu-id="60153-115">fileTransfer</span></span>      | <span data-ttu-id="60153-116">Int64</span><span class="sxs-lookup"><span data-stu-id="60153-116">Int64</span></span>  |
| <span data-ttu-id="60153-117">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="60153-117">reportRefreshDate</span></span> | <span data-ttu-id="60153-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="60153-118">Date</span></span>   |
| <span data-ttu-id="60153-119">reportDate</span><span class="sxs-lookup"><span data-stu-id="60153-119">reportDate</span></span>        | <span data-ttu-id="60153-120">Fecha</span><span class="sxs-lookup"><span data-stu-id="60153-120">Date</span></span>   |
| <span data-ttu-id="60153-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="60153-121">reportPeriod</span></span>      | <span data-ttu-id="60153-122">String</span><span class="sxs-lookup"><span data-stu-id="60153-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="60153-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="60153-123">JSON representation</span></span>

<span data-ttu-id="60153-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="60153-124">The following is a JSON representation of the resource.</span></span>

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
