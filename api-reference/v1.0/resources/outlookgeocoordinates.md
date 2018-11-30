---
title: Tipo de recurso outlookGeoCoordinates
description: Coordenadas geográficas, elevación y su grado de precisión para una ubicación geográfica.
ms.openlocfilehash: 232c40bde9484c74500370a321f0f465150061d9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031036"
---
# <a name="outlookgeocoordinates-resource-type"></a><span data-ttu-id="531f0-103">Tipo de recurso outlookGeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="531f0-103">outlookGeoCoordinates resource type</span></span>

<span data-ttu-id="531f0-104">Coordenadas geográficas, elevación y su grado de precisión para una ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="531f0-104">The geographic coordinates, elevation, and their degree of accuracy for a physical location.</span></span>

## <a name="json-representation"></a><span data-ttu-id="531f0-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="531f0-105">JSON representation</span></span>

<span data-ttu-id="531f0-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="531f0-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.outlookGeoCoordinates"
}-->

```json
{
  "accuracy": 1024.13,
  "altitude": 1024.13,
  "altitudeAccuracy": 1024.13,
  "latitude": 1024.13,
  "longitude": 1024.13
}

```
## <a name="properties"></a><span data-ttu-id="531f0-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="531f0-107">Properties</span></span>
| <span data-ttu-id="531f0-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="531f0-108">Property</span></span>     | <span data-ttu-id="531f0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="531f0-109">Type</span></span>   |<span data-ttu-id="531f0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="531f0-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="531f0-111">accuracy</span><span class="sxs-lookup"><span data-stu-id="531f0-111">accuracy</span></span>|<span data-ttu-id="531f0-112">double</span><span class="sxs-lookup"><span data-stu-id="531f0-112">double</span></span>|<span data-ttu-id="531f0-113">Exactitud de la latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="531f0-113">The accuracy of the latitude and longitude.</span></span> <span data-ttu-id="531f0-114">Por ejemplo, la precisión puede medirse en metros, como que la latitud y longitud tienen una precisión de 50 metros.</span><span class="sxs-lookup"><span data-stu-id="531f0-114">As an example, the accuracy can be measured in meters, such as the latitude and longitude are accurate to within 50 meters.</span></span>|
|<span data-ttu-id="531f0-115">altitude</span><span class="sxs-lookup"><span data-stu-id="531f0-115">altitude</span></span>|<span data-ttu-id="531f0-116">double</span><span class="sxs-lookup"><span data-stu-id="531f0-116">double</span></span>|<span data-ttu-id="531f0-117">Altitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="531f0-117">The altitude of the location.</span></span>|
|<span data-ttu-id="531f0-118">altitudeAccuracy</span><span class="sxs-lookup"><span data-stu-id="531f0-118">altitudeAccuracy</span></span>|<span data-ttu-id="531f0-119">double</span><span class="sxs-lookup"><span data-stu-id="531f0-119">double</span></span>|<span data-ttu-id="531f0-120">Exactitud de la altitud.</span><span class="sxs-lookup"><span data-stu-id="531f0-120">The accuracy of the altitude.</span></span>|
|<span data-ttu-id="531f0-121">latitude</span><span class="sxs-lookup"><span data-stu-id="531f0-121">latitude</span></span>|<span data-ttu-id="531f0-122">double</span><span class="sxs-lookup"><span data-stu-id="531f0-122">double</span></span>|<span data-ttu-id="531f0-123">Latitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="531f0-123">The latitude of the location.</span></span>|
|<span data-ttu-id="531f0-124">longitude</span><span class="sxs-lookup"><span data-stu-id="531f0-124">longitude</span></span>|<span data-ttu-id="531f0-125">double</span><span class="sxs-lookup"><span data-stu-id="531f0-125">double</span></span>|<span data-ttu-id="531f0-126">Longitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="531f0-126">The longitude of the location.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookGeoCoordinates resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->