---
title: tipo de recurso skypeForBusinessPeerToPeerActivityUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: ad3b409f3abc4cc9e7476825f9dbf5b7c2120d92
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088145"
---
# <a name="skypeforbusinesspeertopeeractivityusercounts-resource-type"></a><span data-ttu-id="7331a-103">tipo de recurso skypeForBusinessPeerToPeerActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="7331a-103">skypeForBusinessPeerToPeerActivityUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="7331a-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7331a-104">Properties</span></span>

| <span data-ttu-id="7331a-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7331a-105">Property</span></span>          | <span data-ttu-id="7331a-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="7331a-106">Type</span></span>   |
| :---------------- | :----- |
| <span data-ttu-id="7331a-107">mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="7331a-107">im</span></span>                | <span data-ttu-id="7331a-108">Int64</span><span class="sxs-lookup"><span data-stu-id="7331a-108">Int64</span></span>  |
| <span data-ttu-id="7331a-109">audio</span><span class="sxs-lookup"><span data-stu-id="7331a-109">audio</span></span>             | <span data-ttu-id="7331a-110">Int64</span><span class="sxs-lookup"><span data-stu-id="7331a-110">Int64</span></span>  |
| <span data-ttu-id="7331a-111">video</span><span class="sxs-lookup"><span data-stu-id="7331a-111">video</span></span>             | <span data-ttu-id="7331a-112">Int64</span><span class="sxs-lookup"><span data-stu-id="7331a-112">Int64</span></span>  |
| <span data-ttu-id="7331a-113">uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="7331a-113">appSharing</span></span>        | <span data-ttu-id="7331a-114">Int64</span><span class="sxs-lookup"><span data-stu-id="7331a-114">Int64</span></span>  |
| <span data-ttu-id="7331a-115">fileTransfer</span><span class="sxs-lookup"><span data-stu-id="7331a-115">fileTransfer</span></span>      | <span data-ttu-id="7331a-116">Int64</span><span class="sxs-lookup"><span data-stu-id="7331a-116">Int64</span></span>  |
| <span data-ttu-id="7331a-117">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="7331a-117">reportRefreshDate</span></span> | <span data-ttu-id="7331a-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="7331a-118">Date</span></span>   |
| <span data-ttu-id="7331a-119">reportDate</span><span class="sxs-lookup"><span data-stu-id="7331a-119">reportDate</span></span>        | <span data-ttu-id="7331a-120">Fecha</span><span class="sxs-lookup"><span data-stu-id="7331a-120">Date</span></span>   |
| <span data-ttu-id="7331a-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="7331a-121">reportPeriod</span></span>      | <span data-ttu-id="7331a-122">String</span><span class="sxs-lookup"><span data-stu-id="7331a-122">String</span></span> |

## <a name="json-representation"></a><span data-ttu-id="7331a-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7331a-123">JSON representation</span></span>

<span data-ttu-id="7331a-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7331a-124">The following is a JSON representation of the resource.</span></span>

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
