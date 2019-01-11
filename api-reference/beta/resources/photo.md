---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Foto
localization_priority: Normal
ms.openlocfilehash: ed891f917ba8018aac349976df0455adfd269fdb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27869387"
---
# <a name="photo-resource-type"></a><span data-ttu-id="05c44-102">Tipo de recurso Photo</span><span class="sxs-lookup"><span data-stu-id="05c44-102">Photo resource type</span></span>

> <span data-ttu-id="05c44-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="05c44-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="05c44-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="05c44-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="05c44-105">El recurso **photo** proporciona propiedades de foto y cámara, por ejemplo, los metadatos EXIF, en un [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="05c44-105">The **photo** resource provides photo and camera properties, for example, EXIF metadata, on a [driveItem](driveitem.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="05c44-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="05c44-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.photo"
}-->
```json
{
  "cameraMake": "string",
  "cameraModel": "string",
  "exposureDenominator": 1000.0,
  "exposureNumerator": 1.0,
  "fNumber": 1.8,
  "focalLength": 22.5,
  "iso": 100,
  "takenDateTime": "String (timestamp)"
}
```

## <a name="properties"></a><span data-ttu-id="05c44-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="05c44-107">Properties</span></span>

| <span data-ttu-id="05c44-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="05c44-108">Property</span></span>                | <span data-ttu-id="05c44-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="05c44-109">Type</span></span>           | <span data-ttu-id="05c44-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="05c44-110">Description</span></span>
|:------------------------|:---------------|:----------------------------------
| <span data-ttu-id="05c44-111">**takenDateTime**</span><span class="sxs-lookup"><span data-stu-id="05c44-111">**takenDateTime**</span></span>       | <span data-ttu-id="05c44-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="05c44-112">DateTimeOffset</span></span> | <span data-ttu-id="05c44-p102">Representa la fecha y hora en que se tomó la foto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="05c44-p102">Represents the date and time the photo was taken. Read-only.</span></span>
| <span data-ttu-id="05c44-115">**cameraMake**</span><span class="sxs-lookup"><span data-stu-id="05c44-115">**cameraMake**</span></span>          | <span data-ttu-id="05c44-116">String</span><span class="sxs-lookup"><span data-stu-id="05c44-116">String</span></span>         | <span data-ttu-id="05c44-p103">Fabricante de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="05c44-p103">Camera manufacturer. Read-only.</span></span>
| <span data-ttu-id="05c44-119">**cameraModel**</span><span class="sxs-lookup"><span data-stu-id="05c44-119">**cameraModel**</span></span>         | <span data-ttu-id="05c44-120">String</span><span class="sxs-lookup"><span data-stu-id="05c44-120">String</span></span>         | <span data-ttu-id="05c44-p104">Modelo de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="05c44-p104">Camera model. Read-only.</span></span>
| <span data-ttu-id="05c44-123">**fNumber**</span><span class="sxs-lookup"><span data-stu-id="05c44-123">**fNumber**</span></span>             | <span data-ttu-id="05c44-124">Doble</span><span class="sxs-lookup"><span data-stu-id="05c44-124">Double</span></span>         | <span data-ttu-id="05c44-p105">Valor punto F de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="05c44-p105">The F-stop value from the camera. Read-only.</span></span>
| <span data-ttu-id="05c44-127">**exposureDenominator**</span><span class="sxs-lookup"><span data-stu-id="05c44-127">**exposureDenominator**</span></span> | <span data-ttu-id="05c44-128">Double</span><span class="sxs-lookup"><span data-stu-id="05c44-128">Double</span></span>         | <span data-ttu-id="05c44-p106">Denominador de la fracción de tiempo de exposición de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="05c44-p106">The denominator for the exposure time fraction from the camera. Read-only.</span></span>
| <span data-ttu-id="05c44-131">**exposureNumerator**</span><span class="sxs-lookup"><span data-stu-id="05c44-131">**exposureNumerator**</span></span>   | <span data-ttu-id="05c44-132">Double</span><span class="sxs-lookup"><span data-stu-id="05c44-132">Double</span></span>         | <span data-ttu-id="05c44-p107">Numerador de la fracción de tiempo de exposición de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="05c44-p107">The numerator for the exposure time fraction from the camera. Read-only.</span></span>
| <span data-ttu-id="05c44-135">**focalLength**</span><span class="sxs-lookup"><span data-stu-id="05c44-135">**focalLength**</span></span>         | <span data-ttu-id="05c44-136">Doble</span><span class="sxs-lookup"><span data-stu-id="05c44-136">Double</span></span>         | <span data-ttu-id="05c44-p108">Distancia focal de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="05c44-p108">The focal length from the camera. Read-only.</span></span>
| <span data-ttu-id="05c44-139">**iso**</span><span class="sxs-lookup"><span data-stu-id="05c44-139">**iso**</span></span>                 | <span data-ttu-id="05c44-140">Int64</span><span class="sxs-lookup"><span data-stu-id="05c44-140">Int64</span></span>          | <span data-ttu-id="05c44-p109">El valor ISO de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="05c44-p109">The ISO value from the camera. Read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="05c44-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05c44-143">Remarks</span></span>
<span data-ttu-id="05c44-144">OneDrive para la Empresa y SharePoint solo devuelven la propiedad **takenDateTime**.</span><span class="sxs-lookup"><span data-stu-id="05c44-144">OneDrive for Business and SharePoint only return the **takenDateTime** property.</span></span>

<span data-ttu-id="05c44-145">Para obtener más información sobre las facetas de un DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="05c44-145">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>
<!-- {
  "type": "#page.annotation",
  "description": "The photo facet provides details about the camera and settings on the camera for photos.",
  "keywords": "camera make,camera model, exposure, f-stop, iso",
  "section": "documentation",
  "tocPath": "Facets/Photo"
} -->
