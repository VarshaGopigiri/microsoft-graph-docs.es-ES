---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: GeoCoordinates
ms.openlocfilehash: f9110591ee1e3350979aa2c7785cdebb2d4a584c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086571"
---
# <a name="geocoordinates-resource-type"></a><span data-ttu-id="109aa-102">Tipo de recurso GeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="109aa-102">GeoCoordinates resource type</span></span>

> <span data-ttu-id="109aa-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="109aa-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="109aa-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="109aa-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="109aa-p102">El recurso **GeoCoordinates** proporciona las coordenadas geográficas y la elevación de una ubicación en función de metadatos contenidos en el archivo. Si un [**DriveItem**](driveitem.md) tiene una faceta **location** no null, el elemento representa un archivo que tiene asociada una ubicación conocida.</span><span class="sxs-lookup"><span data-stu-id="109aa-p102">The **GeoCoordinates** resource provides geographic coordinates and elevation of a location based on metadata contained within the file. If a [**DriveItem**](driveitem.md) has a non-null **location** facet, the item represents a file with a known location assocaited with it.</span></span>

## <a name="json-representation"></a><span data-ttu-id="109aa-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="109aa-107">JSON representation</span></span>

<span data-ttu-id="109aa-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="109aa-108">Here is a JSON representation of the resource</span></span>

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

## <a name="properties"></a><span data-ttu-id="109aa-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="109aa-109">Properties</span></span>

| <span data-ttu-id="109aa-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="109aa-110">Property</span></span>  | <span data-ttu-id="109aa-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="109aa-111">Type</span></span>   | <span data-ttu-id="109aa-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="109aa-112">Description</span></span>
|:----------|:-------|:--------------------------------------------------------
| <span data-ttu-id="109aa-113">altitude</span><span class="sxs-lookup"><span data-stu-id="109aa-113">altitude</span></span>  | <span data-ttu-id="109aa-114">Doble</span><span class="sxs-lookup"><span data-stu-id="109aa-114">Double</span></span> | <span data-ttu-id="109aa-p103">Opcional. Altitud (alto) en pies sobre el nivel del mar del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="109aa-p103">Optional. The altitude (height), in feet,  above sea level for the item. Read-only.</span></span>
| <span data-ttu-id="109aa-118">latitude</span><span class="sxs-lookup"><span data-stu-id="109aa-118">latitude</span></span>  | <span data-ttu-id="109aa-119">Doble</span><span class="sxs-lookup"><span data-stu-id="109aa-119">Double</span></span> | <span data-ttu-id="109aa-p104">Opcional. Latitud en formato decimal del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="109aa-p104">Optional. The latitude, in decimal, for the item. Read-only.</span></span>
| <span data-ttu-id="109aa-123">longitude</span><span class="sxs-lookup"><span data-stu-id="109aa-123">longitude</span></span> | <span data-ttu-id="109aa-124">Doble</span><span class="sxs-lookup"><span data-stu-id="109aa-124">Double</span></span> | <span data-ttu-id="109aa-p105">Opcional. Longitud en formato decimal del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="109aa-p105">Optional. The longitude, in decimal, for the item. Read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="109aa-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="109aa-128">Remarks</span></span>

<span data-ttu-id="109aa-129">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="109aa-129">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The location facet provides geographic location related properties for an item",
  "keywords": "location,geographic,item,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Location"
} -->
