---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Foto
ms.openlocfilehash: 391eafd84ab1abd4670c953720ff7097e060bfd3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031883"
---
# <a name="photo-resource-type"></a><span data-ttu-id="e6942-102">Tipo de recurso Photo</span><span class="sxs-lookup"><span data-stu-id="e6942-102">Photo resource type</span></span>

<span data-ttu-id="e6942-103">El recurso **photo** proporciona propiedades de foto y cámara, por ejemplo, los metadatos EXIF, en un [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="e6942-103">The **photo** resource provides photo and camera properties, for example, EXIF metadata, on a [driveItem](driveitem.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="e6942-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e6942-104">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="e6942-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e6942-105">Properties</span></span>

| <span data-ttu-id="e6942-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e6942-106">Property</span></span>                | <span data-ttu-id="e6942-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6942-107">Type</span></span>           | <span data-ttu-id="e6942-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6942-108">Description</span></span>
|:------------------------|:---------------|:----------------------------------
| <span data-ttu-id="e6942-109">**takenDateTime**</span><span class="sxs-lookup"><span data-stu-id="e6942-109">**takenDateTime**</span></span>       | <span data-ttu-id="e6942-110">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e6942-110">DateTimeOffset</span></span> | <span data-ttu-id="e6942-p101">Representa la fecha y hora en que se tomó la foto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6942-p101">Represents the date and time the photo was taken. Read-only.</span></span>
| <span data-ttu-id="e6942-113">**cameraMake**</span><span class="sxs-lookup"><span data-stu-id="e6942-113">**cameraMake**</span></span>          | <span data-ttu-id="e6942-114">String</span><span class="sxs-lookup"><span data-stu-id="e6942-114">String</span></span>         | <span data-ttu-id="e6942-p102">Fabricante de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6942-p102">Camera manufacturer. Read-only.</span></span>
| <span data-ttu-id="e6942-117">**cameraModel**</span><span class="sxs-lookup"><span data-stu-id="e6942-117">**cameraModel**</span></span>         | <span data-ttu-id="e6942-118">String</span><span class="sxs-lookup"><span data-stu-id="e6942-118">String</span></span>         | <span data-ttu-id="e6942-p103">Modelo de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6942-p103">Camera model. Read-only.</span></span>
| <span data-ttu-id="e6942-121">**fNumber**</span><span class="sxs-lookup"><span data-stu-id="e6942-121">**fNumber**</span></span>             | <span data-ttu-id="e6942-122">Doble</span><span class="sxs-lookup"><span data-stu-id="e6942-122">Double</span></span>         | <span data-ttu-id="e6942-p104">Valor punto F de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6942-p104">The F-stop value from the camera. Read-only.</span></span>
| <span data-ttu-id="e6942-125">**exposureDenominator**</span><span class="sxs-lookup"><span data-stu-id="e6942-125">**exposureDenominator**</span></span> | <span data-ttu-id="e6942-126">Double</span><span class="sxs-lookup"><span data-stu-id="e6942-126">Double</span></span>         | <span data-ttu-id="e6942-p105">Denominador de la fracción de tiempo de exposición de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6942-p105">The denominator for the exposure time fraction from the camera. Read-only.</span></span>
| <span data-ttu-id="e6942-129">**exposureNumerator**</span><span class="sxs-lookup"><span data-stu-id="e6942-129">**exposureNumerator**</span></span>   | <span data-ttu-id="e6942-130">Double</span><span class="sxs-lookup"><span data-stu-id="e6942-130">Double</span></span>         | <span data-ttu-id="e6942-p106">Numerador de la fracción de tiempo de exposición de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6942-p106">The numerator for the exposure time fraction from the camera. Read-only.</span></span>
| <span data-ttu-id="e6942-133">**focalLength**</span><span class="sxs-lookup"><span data-stu-id="e6942-133">**focalLength**</span></span>         | <span data-ttu-id="e6942-134">Doble</span><span class="sxs-lookup"><span data-stu-id="e6942-134">Double</span></span>         | <span data-ttu-id="e6942-p107">Distancia focal de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6942-p107">The focal length from the camera. Read-only.</span></span>
| <span data-ttu-id="e6942-137">**iso**</span><span class="sxs-lookup"><span data-stu-id="e6942-137">**iso**</span></span>                 | <span data-ttu-id="e6942-138">Int32</span><span class="sxs-lookup"><span data-stu-id="e6942-138">Int32</span></span>          | <span data-ttu-id="e6942-p108">El valor ISO de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6942-p108">The ISO value from the camera. Read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6942-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6942-141">Remarks</span></span>

<span data-ttu-id="e6942-142">OneDrive para la Empresa y SharePoint solo devuelven la propiedad **takenDateTime**.</span><span class="sxs-lookup"><span data-stu-id="e6942-142">OneDrive for Business and SharePoint only return the **takenDateTime** property.</span></span>

<span data-ttu-id="e6942-143">Para obtener más información sobre las facetas de un DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="e6942-143">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>
<!-- {
  "type": "#page.annotation",
  "description": "The photo facet provides details about the camera and settings on the camera for photos.",
  "keywords": "camera make,camera model, exposure, f-stop, iso",
  "section": "documentation",
  "tocPath": "Facets/Photo"
} -->
