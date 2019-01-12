---
title: Tipo de recurso outlookGeoCoordinates
description: Coordenadas geográficas, elevación y su grado de precisión para una ubicación geográfica.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 59b5055118cd4a213d59fdcb4921544e3b84608e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976495"
---
# <a name="outlookgeocoordinates-resource-type"></a><span data-ttu-id="125c6-103">Tipo de recurso outlookGeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="125c6-103">outlookGeoCoordinates resource type</span></span>

<span data-ttu-id="125c6-104">Coordenadas geográficas, elevación y su grado de precisión para una ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="125c6-104">The geographic coordinates, elevation, and their degree of accuracy for a physical location.</span></span>

## <a name="json-representation"></a><span data-ttu-id="125c6-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="125c6-105">JSON representation</span></span>

<span data-ttu-id="125c6-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="125c6-106">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="125c6-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="125c6-107">Properties</span></span>
| <span data-ttu-id="125c6-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="125c6-108">Property</span></span>     | <span data-ttu-id="125c6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="125c6-109">Type</span></span>   |<span data-ttu-id="125c6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="125c6-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="125c6-111">accuracy</span><span class="sxs-lookup"><span data-stu-id="125c6-111">accuracy</span></span>|<span data-ttu-id="125c6-112">double</span><span class="sxs-lookup"><span data-stu-id="125c6-112">double</span></span>|<span data-ttu-id="125c6-113">Exactitud de la latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="125c6-113">The accuracy of the latitude and longitude.</span></span> <span data-ttu-id="125c6-114">Por ejemplo, la precisión puede medirse en metros, como que la latitud y longitud tienen una precisión de 50 metros.</span><span class="sxs-lookup"><span data-stu-id="125c6-114">As an example, the accuracy can be measured in meters, such as the latitude and longitude are accurate to within 50 meters.</span></span>|
|<span data-ttu-id="125c6-115">altitude</span><span class="sxs-lookup"><span data-stu-id="125c6-115">altitude</span></span>|<span data-ttu-id="125c6-116">double</span><span class="sxs-lookup"><span data-stu-id="125c6-116">double</span></span>|<span data-ttu-id="125c6-117">Altitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="125c6-117">The altitude of the location.</span></span>|
|<span data-ttu-id="125c6-118">altitudeAccuracy</span><span class="sxs-lookup"><span data-stu-id="125c6-118">altitudeAccuracy</span></span>|<span data-ttu-id="125c6-119">double</span><span class="sxs-lookup"><span data-stu-id="125c6-119">double</span></span>|<span data-ttu-id="125c6-120">Exactitud de la altitud.</span><span class="sxs-lookup"><span data-stu-id="125c6-120">The accuracy of the altitude.</span></span>|
|<span data-ttu-id="125c6-121">latitude</span><span class="sxs-lookup"><span data-stu-id="125c6-121">latitude</span></span>|<span data-ttu-id="125c6-122">double</span><span class="sxs-lookup"><span data-stu-id="125c6-122">double</span></span>|<span data-ttu-id="125c6-123">Latitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="125c6-123">The latitude of the location.</span></span>|
|<span data-ttu-id="125c6-124">longitude</span><span class="sxs-lookup"><span data-stu-id="125c6-124">longitude</span></span>|<span data-ttu-id="125c6-125">double</span><span class="sxs-lookup"><span data-stu-id="125c6-125">double</span></span>|<span data-ttu-id="125c6-126">Longitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="125c6-126">The longitude of the location.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookGeoCoordinates resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
