---
title: Tipo de recurso outlookGeoCoordinates
description: Coordenadas geográficas, elevación y su grado de precisión para una ubicación geográfica.
ms.openlocfilehash: 9de60c218f6fc54ed2be12b2987126195e5eb140
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085311"
---
# <a name="outlookgeocoordinates-resource-type"></a><span data-ttu-id="dbccb-103">Tipo de recurso outlookGeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="dbccb-103">outlookGeoCoordinates resource type</span></span>

> <span data-ttu-id="dbccb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dbccb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dbccb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dbccb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dbccb-106">Coordenadas geográficas, elevación y su grado de precisión para una ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="dbccb-106">The geographic coordinates, elevation, and their degree of accuracy for a physical location.</span></span>

## <a name="json-representation"></a><span data-ttu-id="dbccb-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dbccb-107">JSON representation</span></span>

<span data-ttu-id="dbccb-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="dbccb-108">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="dbccb-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbccb-109">Properties</span></span>
| <span data-ttu-id="dbccb-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dbccb-110">Property</span></span>     | <span data-ttu-id="dbccb-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="dbccb-111">Type</span></span>   |<span data-ttu-id="dbccb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbccb-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dbccb-113">accuracy</span><span class="sxs-lookup"><span data-stu-id="dbccb-113">accuracy</span></span>|<span data-ttu-id="dbccb-114">double</span><span class="sxs-lookup"><span data-stu-id="dbccb-114">double</span></span>|<span data-ttu-id="dbccb-115">Exactitud de la latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="dbccb-115">The accuracy of the latitude and longitude.</span></span> <span data-ttu-id="dbccb-116">Por ejemplo, la precisión puede medirse en metros, como que la latitud y longitud tienen una precisión de 50 metros.</span><span class="sxs-lookup"><span data-stu-id="dbccb-116">As an example, the accuracy can be measured in meters, such as the latitude and longitude are accurate to within 50 meters.</span></span>|
|<span data-ttu-id="dbccb-117">altitude</span><span class="sxs-lookup"><span data-stu-id="dbccb-117">altitude</span></span>|<span data-ttu-id="dbccb-118">double</span><span class="sxs-lookup"><span data-stu-id="dbccb-118">double</span></span>|<span data-ttu-id="dbccb-119">Altitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="dbccb-119">The altitude of the location.</span></span>|
|<span data-ttu-id="dbccb-120">altitudeAccuracy</span><span class="sxs-lookup"><span data-stu-id="dbccb-120">altitudeAccuracy</span></span>|<span data-ttu-id="dbccb-121">double</span><span class="sxs-lookup"><span data-stu-id="dbccb-121">double</span></span>|<span data-ttu-id="dbccb-122">Exactitud de la altitud.</span><span class="sxs-lookup"><span data-stu-id="dbccb-122">The accuracy of the altitude.</span></span>|
|<span data-ttu-id="dbccb-123">latitude</span><span class="sxs-lookup"><span data-stu-id="dbccb-123">latitude</span></span>|<span data-ttu-id="dbccb-124">double</span><span class="sxs-lookup"><span data-stu-id="dbccb-124">double</span></span>|<span data-ttu-id="dbccb-125">Latitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="dbccb-125">The latitude of the location.</span></span>|
|<span data-ttu-id="dbccb-126">longitude</span><span class="sxs-lookup"><span data-stu-id="dbccb-126">longitude</span></span>|<span data-ttu-id="dbccb-127">double</span><span class="sxs-lookup"><span data-stu-id="dbccb-127">double</span></span>|<span data-ttu-id="dbccb-128">Longitud de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="dbccb-128">The longitude of the location.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookGeoCoordinates resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->