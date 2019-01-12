---
title: Tipo de recurso outlookGeoCoordinates
description: Coordenadas geográficas, elevación y su grado de precisión para una ubicación geográfica.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: f51f5eeb663a1d1ce55bee083639d244905b2c37
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973121"
---
# <a name="outlookgeocoordinates-resource-type"></a><span data-ttu-id="04ebe-103">Tipo de recurso outlookGeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="04ebe-103">outlookGeoCoordinates resource type</span></span>

> <span data-ttu-id="04ebe-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="04ebe-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="04ebe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="04ebe-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="04ebe-106">Coordenadas geográficas, elevación y su grado de precisión para una ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="04ebe-106">The geographic coordinates, elevation, and their degree of accuracy for a physical location.</span></span>

## <a name="json-representation"></a><span data-ttu-id="04ebe-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="04ebe-107">JSON representation</span></span>

<span data-ttu-id="04ebe-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="04ebe-108">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="04ebe-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="04ebe-109">Properties</span></span>
| <span data-ttu-id="04ebe-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04ebe-110">Property</span></span>     | <span data-ttu-id="04ebe-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="04ebe-111">Type</span></span>   |<span data-ttu-id="04ebe-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="04ebe-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="04ebe-113">accuracy</span><span class="sxs-lookup"><span data-stu-id="04ebe-113">accuracy</span></span>|<span data-ttu-id="04ebe-114">double</span><span class="sxs-lookup"><span data-stu-id="04ebe-114">double</span></span>|<span data-ttu-id="04ebe-115">Exactitud de la latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="04ebe-115">The accuracy of the latitude and longitude.</span></span> <span data-ttu-id="04ebe-116">Por ejemplo, la precisión puede medirse en metros, como que la latitud y longitud tienen una precisión de 50 metros.</span><span class="sxs-lookup"><span data-stu-id="04ebe-116">As an example, the accuracy can be measured in meters, such as the latitude and longitude are accurate to within 50 meters.</span></span>|
|<span data-ttu-id="04ebe-117">altitude</span><span class="sxs-lookup"><span data-stu-id="04ebe-117">altitude</span></span>|<span data-ttu-id="04ebe-118">double</span><span class="sxs-lookup"><span data-stu-id="04ebe-118">double</span></span>|<span data-ttu-id="04ebe-119">Altitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="04ebe-119">The altitude of the location.</span></span>|
|<span data-ttu-id="04ebe-120">altitudeAccuracy</span><span class="sxs-lookup"><span data-stu-id="04ebe-120">altitudeAccuracy</span></span>|<span data-ttu-id="04ebe-121">double</span><span class="sxs-lookup"><span data-stu-id="04ebe-121">double</span></span>|<span data-ttu-id="04ebe-122">Exactitud de la altitud.</span><span class="sxs-lookup"><span data-stu-id="04ebe-122">The accuracy of the altitude.</span></span>|
|<span data-ttu-id="04ebe-123">latitude</span><span class="sxs-lookup"><span data-stu-id="04ebe-123">latitude</span></span>|<span data-ttu-id="04ebe-124">double</span><span class="sxs-lookup"><span data-stu-id="04ebe-124">double</span></span>|<span data-ttu-id="04ebe-125">Latitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="04ebe-125">The latitude of the location.</span></span>|
|<span data-ttu-id="04ebe-126">longitude</span><span class="sxs-lookup"><span data-stu-id="04ebe-126">longitude</span></span>|<span data-ttu-id="04ebe-127">double</span><span class="sxs-lookup"><span data-stu-id="04ebe-127">double</span></span>|<span data-ttu-id="04ebe-128">Longitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="04ebe-128">The longitude of the location.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookGeoCoordinates resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
