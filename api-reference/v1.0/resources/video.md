---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Vídeo
ms.openlocfilehash: cb9e28c1b26aa60fe7d854796df8bff34ca8e5df
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030177"
---
# <a name="video-resource-type"></a><span data-ttu-id="cc981-102">Tipo de recurso Video</span><span class="sxs-lookup"><span data-stu-id="cc981-102">Video resource type</span></span>

<span data-ttu-id="cc981-103">El recurso **Video** agrupa en una sola estructura los elementos de datos relacionados con vídeos.</span><span class="sxs-lookup"><span data-stu-id="cc981-103">The **Video** resource groups video-related data items into a single structure.</span></span>

<span data-ttu-id="cc981-p101">Si un [**DriveItem**](driveitem.md) tiene una faceta **video** no-null, el elemento representa un archivo de vídeo. Las propiedades del recurso **Video** se rellenan extrayendo metadatos del archivo.</span><span class="sxs-lookup"><span data-stu-id="cc981-p101">If a [**DriveItem**](driveitem.md) has a non-null **video** facet, the item represents a video file. The properties of the **Video** resource are populated by extracting metadata from the file.</span></span>

## <a name="json-representation"></a><span data-ttu-id="cc981-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cc981-106">JSON representation</span></span>

<span data-ttu-id="cc981-107">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="cc981-107">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.video"
}-->

```json
{
  "audioBitsPerSample": 16,
  "audioChannels": 1,
  "audioFormat": "AAC",
  "audioSamplesPerSecond": 44100,
  "bitrate": 39101896,
  "duration": 8053,
  "fourCC": "H264",
  "frameRate": 239.877,
  "height": 1280,
  "width": 720
}
```

## <a name="properties"></a><span data-ttu-id="cc981-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc981-108">Properties</span></span>

| <span data-ttu-id="cc981-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="cc981-109">Property name</span></span>             | <span data-ttu-id="cc981-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc981-110">Type</span></span>   | <span data-ttu-id="cc981-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc981-111">Description</span></span>
|:--------------------------|:-------|:----------------------------------------
| <span data-ttu-id="cc981-112">**audioBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="cc981-112">**audioBitsPerSample**</span></span>    | <span data-ttu-id="cc981-113">Int32</span><span class="sxs-lookup"><span data-stu-id="cc981-113">Int32</span></span>  | <span data-ttu-id="cc981-114">Número de bits de audio por muestra.</span><span class="sxs-lookup"><span data-stu-id="cc981-114">Number of audio bits per sample.</span></span>
| <span data-ttu-id="cc981-115">**audioChannels**</span><span class="sxs-lookup"><span data-stu-id="cc981-115">**audioChannels**</span></span>         | <span data-ttu-id="cc981-116">Int32</span><span class="sxs-lookup"><span data-stu-id="cc981-116">Int32</span></span>  | <span data-ttu-id="cc981-117">Número de canales de audio.</span><span class="sxs-lookup"><span data-stu-id="cc981-117">Number of audio channels.</span></span>
| <span data-ttu-id="cc981-118">**audioFormat**</span><span class="sxs-lookup"><span data-stu-id="cc981-118">**audioFormat**</span></span>           | <span data-ttu-id="cc981-119">string</span><span class="sxs-lookup"><span data-stu-id="cc981-119">string</span></span> | <span data-ttu-id="cc981-120">Nombre del formato de audio (AAC, MP3, etc.).</span><span class="sxs-lookup"><span data-stu-id="cc981-120">Name of the audio format (AAC, MP3, etc.).</span></span>
| <span data-ttu-id="cc981-121">**audioSamplesPerSecond**</span><span class="sxs-lookup"><span data-stu-id="cc981-121">**audioSamplesPerSecond**</span></span> | <span data-ttu-id="cc981-122">Int32</span><span class="sxs-lookup"><span data-stu-id="cc981-122">Int32</span></span>  | <span data-ttu-id="cc981-123">Número de muestras de audio por segundo.</span><span class="sxs-lookup"><span data-stu-id="cc981-123">Number of audio samples per second.</span></span>
| <span data-ttu-id="cc981-124">**bitrate**</span><span class="sxs-lookup"><span data-stu-id="cc981-124">**bitrate**</span></span>               | <span data-ttu-id="cc981-125">Int32</span><span class="sxs-lookup"><span data-stu-id="cc981-125">Int32</span></span>  | <span data-ttu-id="cc981-126">Velocidad de bits del vídeo en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="cc981-126">Bit rate of the video in bits per second.</span></span>
| <span data-ttu-id="cc981-127">**duration**</span><span class="sxs-lookup"><span data-stu-id="cc981-127">**duration**</span></span>              | <span data-ttu-id="cc981-128">Int64</span><span class="sxs-lookup"><span data-stu-id="cc981-128">Int64</span></span>  | <span data-ttu-id="cc981-129">Duración del archivo en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="cc981-129">Duration of the file in milliseconds.</span></span>
| <span data-ttu-id="cc981-130">**fourCC**</span><span class="sxs-lookup"><span data-stu-id="cc981-130">**fourCC**</span></span>                | <span data-ttu-id="cc981-131">string</span><span class="sxs-lookup"><span data-stu-id="cc981-131">string</span></span> | <span data-ttu-id="cc981-132">Nombre en "código de cuatro caracteres" del formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cc981-132">"Four character code" name of the video format.</span></span>
| <span data-ttu-id="cc981-133">**velocidad de fotogramas**</span><span class="sxs-lookup"><span data-stu-id="cc981-133">**frameRate**</span></span>             | <span data-ttu-id="cc981-134">double</span><span class="sxs-lookup"><span data-stu-id="cc981-134">double</span></span> | <span data-ttu-id="cc981-135">Velocidad de fotogramas del vídeo.</span><span class="sxs-lookup"><span data-stu-id="cc981-135">Frame rate of the video.</span></span>
| <span data-ttu-id="cc981-136">**height**</span><span class="sxs-lookup"><span data-stu-id="cc981-136">**height**</span></span>                | <span data-ttu-id="cc981-137">Int32</span><span class="sxs-lookup"><span data-stu-id="cc981-137">Int32</span></span>  | <span data-ttu-id="cc981-138">Alto del vídeo en píxeles.</span><span class="sxs-lookup"><span data-stu-id="cc981-138">Height of the video, in pixels.</span></span>
| <span data-ttu-id="cc981-139">**width**</span><span class="sxs-lookup"><span data-stu-id="cc981-139">**width**</span></span>                 | <span data-ttu-id="cc981-140">Int32</span><span class="sxs-lookup"><span data-stu-id="cc981-140">Int32</span></span>  | <span data-ttu-id="cc981-141">Ancho del vídeo en píxeles.</span><span class="sxs-lookup"><span data-stu-id="cc981-141">Width of the video, in pixels.</span></span>

[item-resource]: ../resources/driveitem.md

## <a name="remarks"></a><span data-ttu-id="cc981-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc981-142">Remarks</span></span>

<span data-ttu-id="cc981-143">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="cc981-143">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The video facet provides information about the properties of a video file.",
  "keywords": "bitrate,duration,size,video",
  "section": "documentation",
  "tocPath": "Facets/Video"
} -->
