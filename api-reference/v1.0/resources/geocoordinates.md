---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: GeoCoordinates
localization_priority: Normal
ms.openlocfilehash: 33390fa893e99ffb0d7c44642c42751c66265ec8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885515"
---
# <a name="geocoordinates-resource-type"></a><span data-ttu-id="8ad96-102">Tipo de recurso GeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="8ad96-102">GeoCoordinates resource type</span></span>

<span data-ttu-id="8ad96-p101">El recurso **GeoCoordinates** proporciona las coordenadas geográficas y la elevación de una ubicación en función de metadatos contenidos en el archivo. Si un [**DriveItem**](driveitem.md) tiene una faceta **location** no null, el elemento representa un archivo que tiene asociada una ubicación conocida.</span><span class="sxs-lookup"><span data-stu-id="8ad96-p101">The **GeoCoordinates** resource provides geographic coordinates and elevation of a location based on metadata contained within the file. If a [**DriveItem**](driveitem.md) has a non-null **location** facet, the item represents a file with a known location assocaited with it.</span></span>

## <a name="json-representation"></a><span data-ttu-id="8ad96-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8ad96-105">JSON representation</span></span>

<span data-ttu-id="8ad96-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8ad96-106">Here is a JSON representation of the resource</span></span>

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

## <a name="properties"></a><span data-ttu-id="8ad96-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8ad96-107">Properties</span></span>

| <span data-ttu-id="8ad96-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8ad96-108">Property</span></span>  | <span data-ttu-id="8ad96-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ad96-109">Type</span></span>   | <span data-ttu-id="8ad96-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ad96-110">Description</span></span>
|:----------|:-------|:--------------------------------------------------------
| <span data-ttu-id="8ad96-111">altitude</span><span class="sxs-lookup"><span data-stu-id="8ad96-111">altitude</span></span>  | <span data-ttu-id="8ad96-112">Doble</span><span class="sxs-lookup"><span data-stu-id="8ad96-112">Double</span></span> | <span data-ttu-id="8ad96-p102">Opcional. Altitud (alto) en pies sobre el nivel del mar del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8ad96-p102">Optional. The altitude (height), in feet,  above sea level for the item. Read-only.</span></span>
| <span data-ttu-id="8ad96-116">latitude</span><span class="sxs-lookup"><span data-stu-id="8ad96-116">latitude</span></span>  | <span data-ttu-id="8ad96-117">Doble</span><span class="sxs-lookup"><span data-stu-id="8ad96-117">Double</span></span> | <span data-ttu-id="8ad96-p103">Opcional. Latitud en formato decimal del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8ad96-p103">Optional. The latitude, in decimal, for the item. Read-only.</span></span>
| <span data-ttu-id="8ad96-121">longitude</span><span class="sxs-lookup"><span data-stu-id="8ad96-121">longitude</span></span> | <span data-ttu-id="8ad96-122">Doble</span><span class="sxs-lookup"><span data-stu-id="8ad96-122">Double</span></span> | <span data-ttu-id="8ad96-p104">Opcional. Longitud en formato decimal del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8ad96-p104">Optional. The longitude, in decimal, for the item. Read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ad96-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ad96-126">Remarks</span></span>

<span data-ttu-id="8ad96-127">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="8ad96-127">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The location facet provides geographic location related properties for an item",
  "keywords": "location,geographic,item,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Location"
} -->
