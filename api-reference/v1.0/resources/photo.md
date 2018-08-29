---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Foto
ms.openlocfilehash: 391eafd84ab1abd4670c953720ff7097e060bfd3
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267069"
---
# <a name="photo-resource-type"></a><span data-ttu-id="3325d-102">Tipo de recurso Photo</span><span class="sxs-lookup"><span data-stu-id="3325d-102">Photo resource type</span></span>

<span data-ttu-id="3325d-103">El recurso **photo** proporciona propiedades de foto y cámara, por ejemplo, los metadatos EXIF, en un [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="3325d-103">The **photo** resource provides photo and camera properties, for example, EXIF metadata, on a [driveItem](driveitem.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="3325d-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3325d-104">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="3325d-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3325d-105">Properties</span></span>

| <span data-ttu-id="3325d-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3325d-106">Property</span></span>                | <span data-ttu-id="3325d-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="3325d-107">Type</span></span>           | <span data-ttu-id="3325d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3325d-108">Description</span></span>
|:------------------------|:---------------|:----------------------------------
| <span data-ttu-id="3325d-109">**takenDateTime**</span><span class="sxs-lookup"><span data-stu-id="3325d-109">**takenDateTime**</span></span>       | <span data-ttu-id="3325d-110">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3325d-110">DateTimeOffset</span></span> | <span data-ttu-id="3325d-p101">Representa la fecha y hora en que se tomó la foto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3325d-p101">Represents the date and time the photo was taken. Read-only.</span></span>
| <span data-ttu-id="3325d-113">**cameraMake**</span><span class="sxs-lookup"><span data-stu-id="3325d-113">**cameraMake**</span></span>          | <span data-ttu-id="3325d-114">String</span><span class="sxs-lookup"><span data-stu-id="3325d-114">String</span></span>         | <span data-ttu-id="3325d-p102">Fabricante de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3325d-p102">Camera manufacturer. Read-only.</span></span>
| <span data-ttu-id="3325d-117">**cameraModel**</span><span class="sxs-lookup"><span data-stu-id="3325d-117">**cameraModel**</span></span>         | <span data-ttu-id="3325d-118">String</span><span class="sxs-lookup"><span data-stu-id="3325d-118">String</span></span>         | <span data-ttu-id="3325d-p103">Modelo de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3325d-p103">Camera model. Read-only.</span></span>
| <span data-ttu-id="3325d-121">**fNumber**</span><span class="sxs-lookup"><span data-stu-id="3325d-121">**fNumber**</span></span>             | <span data-ttu-id="3325d-122">Doble</span><span class="sxs-lookup"><span data-stu-id="3325d-122">Double</span></span>         | <span data-ttu-id="3325d-p104">Valor punto F de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3325d-p104">The F-stop value from the camera. Read-only.</span></span>
| <span data-ttu-id="3325d-125">**exposureDenominator**</span><span class="sxs-lookup"><span data-stu-id="3325d-125">**exposureDenominator**</span></span> | <span data-ttu-id="3325d-126">Double</span><span class="sxs-lookup"><span data-stu-id="3325d-126">Double</span></span>         | <span data-ttu-id="3325d-p105">Denominador de la fracción de tiempo de exposición de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3325d-p105">The denominator for the exposure time fraction from the camera. Read-only.</span></span>
| <span data-ttu-id="3325d-129">**exposureNumerator**</span><span class="sxs-lookup"><span data-stu-id="3325d-129">**exposureNumerator**</span></span>   | <span data-ttu-id="3325d-130">Double</span><span class="sxs-lookup"><span data-stu-id="3325d-130">Double</span></span>         | <span data-ttu-id="3325d-p106">Numerador de la fracción de tiempo de exposición de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3325d-p106">The numerator for the exposure time fraction from the camera. Read-only.</span></span>
| <span data-ttu-id="3325d-133">**focalLength**</span><span class="sxs-lookup"><span data-stu-id="3325d-133">**focalLength**</span></span>         | <span data-ttu-id="3325d-134">Doble</span><span class="sxs-lookup"><span data-stu-id="3325d-134">Double</span></span>         | <span data-ttu-id="3325d-p107">Distancia focal de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3325d-p107">The focal length from the camera. Read-only.</span></span>
| <span data-ttu-id="3325d-137">**iso**</span><span class="sxs-lookup"><span data-stu-id="3325d-137">**iso**</span></span>                 | <span data-ttu-id="3325d-138">Int32</span><span class="sxs-lookup"><span data-stu-id="3325d-138">Int32</span></span>          | <span data-ttu-id="3325d-p108">Valor ISO de la cámara. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3325d-p108">The ISO value from the camera. Read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="3325d-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3325d-141">Remarks</span></span>

<span data-ttu-id="3325d-142">OneDrive para la Empresa y SharePoint solo devuelven la propiedad **takenDateTime**.</span><span class="sxs-lookup"><span data-stu-id="3325d-142">OneDrive for Business and SharePoint only return the **takenDateTime** property.</span></span>

<span data-ttu-id="3325d-143">Para obtener más información sobre las facetas de un DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="3325d-143">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>
<!-- {
  "type": "#page.annotation",
  "description": "The photo facet provides details about the camera and settings on the camera for photos.",
  "keywords": "camera make,camera model, exposure, f-stop, iso",
  "section": "documentation",
  "tocPath": "Facets/Photo"
} -->
