---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: GeoCoordinates
ms.openlocfilehash: 0a4af14f08b94f0ba64f33838322fb0210bcda15
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031621"
---
# <a name="geocoordinates-resource-type"></a><span data-ttu-id="9f10b-102">Tipo de recurso GeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="9f10b-102">GeoCoordinates resource type</span></span>

<span data-ttu-id="9f10b-p101">El recurso **GeoCoordinates** proporciona las coordenadas geográficas y la elevación de una ubicación en función de metadatos contenidos en el archivo. Si un [**DriveItem**](driveitem.md) tiene una faceta **location** no null, el elemento representa un archivo que tiene asociada una ubicación conocida.</span><span class="sxs-lookup"><span data-stu-id="9f10b-p101">The **GeoCoordinates** resource provides geographic coordinates and elevation of a location based on metadata contained within the file. If a [**DriveItem**](driveitem.md) has a non-null **location** facet, the item represents a file with a known location assocaited with it.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9f10b-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9f10b-105">JSON representation</span></span>

<span data-ttu-id="9f10b-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9f10b-106">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.geoCoordinates"
}-->

```json
{
  "altitude": 1024.13,
  "latitude": 26.13246,
  "longitude": 24.34616
}
```

## <a name="properties"></a><span data-ttu-id="9f10b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f10b-107">Properties</span></span>

| <span data-ttu-id="9f10b-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f10b-108">Property</span></span>  | <span data-ttu-id="9f10b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f10b-109">Type</span></span>   | <span data-ttu-id="9f10b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f10b-110">Description</span></span>
|:----------|:-------|:--------------------------------------------------------
| <span data-ttu-id="9f10b-111">altitude</span><span class="sxs-lookup"><span data-stu-id="9f10b-111">altitude</span></span>  | <span data-ttu-id="9f10b-112">Doble</span><span class="sxs-lookup"><span data-stu-id="9f10b-112">Double</span></span> | <span data-ttu-id="9f10b-p102">Opcional. Altitud (alto) en pies sobre el nivel del mar del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9f10b-p102">Optional. The altitude (height), in feet,  above sea level for the item. Read-only.</span></span>
| <span data-ttu-id="9f10b-116">latitude</span><span class="sxs-lookup"><span data-stu-id="9f10b-116">latitude</span></span>  | <span data-ttu-id="9f10b-117">Doble</span><span class="sxs-lookup"><span data-stu-id="9f10b-117">Double</span></span> | <span data-ttu-id="9f10b-p103">Opcional. Latitud en formato decimal del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9f10b-p103">Optional. The latitude, in decimal, for the item. Read-only.</span></span>
| <span data-ttu-id="9f10b-121">longitude</span><span class="sxs-lookup"><span data-stu-id="9f10b-121">longitude</span></span> | <span data-ttu-id="9f10b-122">Doble</span><span class="sxs-lookup"><span data-stu-id="9f10b-122">Double</span></span> | <span data-ttu-id="9f10b-p104">Opcional. Longitud en formato decimal del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9f10b-p104">Optional. The longitude, in decimal, for the item. Read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f10b-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f10b-126">Remarks</span></span>

<span data-ttu-id="9f10b-127">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="9f10b-127">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The location facet provides geographic location related properties for an item",
  "keywords": "location,geographic,item,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Location"
} -->
