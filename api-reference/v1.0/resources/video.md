---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: "Vídeo"
ms.openlocfilehash: dd6ece46ce54fe791c0e6b5801287e2abad4fe48
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="video-resource-type"></a><span data-ttu-id="0a8ee-102">Tipo de recurso Video</span><span class="sxs-lookup"><span data-stu-id="0a8ee-102">Video resource type</span></span>

<span data-ttu-id="0a8ee-103">El recurso **Video** agrupa en una sola estructura los elementos de datos relacionados con vídeos.</span><span class="sxs-lookup"><span data-stu-id="0a8ee-103">The **Video** resource groups video-related data items into a single structure.</span></span>

<span data-ttu-id="0a8ee-104">Si un [**DriveItem**](driveitem.md) tiene una faceta **video** no-null, el elemento representa un archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0a8ee-104">If a [**DriveItem**](driveitem.md) has a non-null **video** facet, the item represents a video file. The properties of the Video resource are populated by extracting metadata from the file.</span></span>
<span data-ttu-id="0a8ee-105">Las propiedades del recurso **Video** se rellenan extrayendo metadatos del archivo.</span><span class="sxs-lookup"><span data-stu-id="0a8ee-105">If a DriveItem has a non-null video facet, the item represents a video file. The properties of the **Video** resource are populated by extracting metadata from the file.</span></span>

## <a name="json-representation"></a><span data-ttu-id="0a8ee-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0a8ee-106">JSON representation</span></span>

<span data-ttu-id="0a8ee-107">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0a8ee-107">Here is a JSON representation of the resource</span></span>

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

## <a name="properties"></a><span data-ttu-id="0a8ee-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0a8ee-108">Properties</span></span>

| <span data-ttu-id="0a8ee-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="0a8ee-109">Property name</span></span>             | <span data-ttu-id="0a8ee-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a8ee-110">Type</span></span>   | <span data-ttu-id="0a8ee-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a8ee-111">Description</span></span>
|:--------------------------|:-------|:----------------------------------------
| <span data-ttu-id="0a8ee-112">**audioBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="0a8ee-112">**audioBitsPerSample**</span></span>    | <span data-ttu-id="0a8ee-113">Int32</span><span class="sxs-lookup"><span data-stu-id="0a8ee-113">Int32</span></span>  | <span data-ttu-id="0a8ee-114">Número de bits de audio por muestra.</span><span class="sxs-lookup"><span data-stu-id="0a8ee-114">Number of audio bits per sample.</span></span>
| <span data-ttu-id="0a8ee-115">**audioChannels**</span><span class="sxs-lookup"><span data-stu-id="0a8ee-115">**audioChannels**</span></span>         | <span data-ttu-id="0a8ee-116">Int32</span><span class="sxs-lookup"><span data-stu-id="0a8ee-116">Int32</span></span>  | <span data-ttu-id="0a8ee-117">Número de canales de audio.</span><span class="sxs-lookup"><span data-stu-id="0a8ee-117">Number of audio channels.</span></span>
| <span data-ttu-id="0a8ee-118">**audioFormat**</span><span class="sxs-lookup"><span data-stu-id="0a8ee-118">**audioFormat**</span></span>           | <span data-ttu-id="0a8ee-119">string</span><span class="sxs-lookup"><span data-stu-id="0a8ee-119">string</span></span> | <span data-ttu-id="0a8ee-120">Nombre del formato de audio (AAC, MP3, etc.).</span><span class="sxs-lookup"><span data-stu-id="0a8ee-120">Name of the audio format (AAC, MP3, etc.).</span></span>
| <span data-ttu-id="0a8ee-121">**audioSamplesPerSecond**</span><span class="sxs-lookup"><span data-stu-id="0a8ee-121">**audioSamplesPerSecond**</span></span> | <span data-ttu-id="0a8ee-122">Int32</span><span class="sxs-lookup"><span data-stu-id="0a8ee-122">Int32</span></span>  | <span data-ttu-id="0a8ee-123">Número de muestras de audio por segundo.</span><span class="sxs-lookup"><span data-stu-id="0a8ee-123">Number of audio samples per second.</span></span>
| <span data-ttu-id="0a8ee-124">**bitrate**</span><span class="sxs-lookup"><span data-stu-id="0a8ee-124">**bitrate**</span></span>               | <span data-ttu-id="0a8ee-125">Int32</span><span class="sxs-lookup"><span data-stu-id="0a8ee-125">Int32</span></span>  | <span data-ttu-id="0a8ee-126">Velocidad de bits del vídeo en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="0a8ee-126">Bit rate of the video in bits per second.</span></span>
| <span data-ttu-id="0a8ee-127">**duration**</span><span class="sxs-lookup"><span data-stu-id="0a8ee-127">**duration**</span></span>              | <span data-ttu-id="0a8ee-128">Int64</span><span class="sxs-lookup"><span data-stu-id="0a8ee-128">Int64</span></span>  | <span data-ttu-id="0a8ee-129">Duración del archivo en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="0a8ee-129">Duration of the file in milliseconds.</span></span>
| <span data-ttu-id="0a8ee-130">**fourCC**</span><span class="sxs-lookup"><span data-stu-id="0a8ee-130">**fourCC**</span></span>                | <span data-ttu-id="0a8ee-131">string</span><span class="sxs-lookup"><span data-stu-id="0a8ee-131">string</span></span> | <span data-ttu-id="0a8ee-132">Nombre en "código de cuatro caracteres" del formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0a8ee-132">"Four character code" name of the video format.</span></span>
| <span data-ttu-id="0a8ee-133">**framerate**</span><span class="sxs-lookup"><span data-stu-id="0a8ee-133">**framerate**</span></span>             | <span data-ttu-id="0a8ee-134">double</span><span class="sxs-lookup"><span data-stu-id="0a8ee-134">double</span></span> | <span data-ttu-id="0a8ee-135">Velocidad de fotogramas del vídeo.</span><span class="sxs-lookup"><span data-stu-id="0a8ee-135">Frame rate of the video.</span></span>
| <span data-ttu-id="0a8ee-136">**height**</span><span class="sxs-lookup"><span data-stu-id="0a8ee-136">**height**</span></span>                | <span data-ttu-id="0a8ee-137">Int32</span><span class="sxs-lookup"><span data-stu-id="0a8ee-137">Int32</span></span>  | <span data-ttu-id="0a8ee-138">Alto del vídeo en píxeles.</span><span class="sxs-lookup"><span data-stu-id="0a8ee-138">Height of the video, in pixels.</span></span>
| <span data-ttu-id="0a8ee-139">**width**</span><span class="sxs-lookup"><span data-stu-id="0a8ee-139">**width**</span></span>                 | <span data-ttu-id="0a8ee-140">Int32</span><span class="sxs-lookup"><span data-stu-id="0a8ee-140">Int32</span></span>  | <span data-ttu-id="0a8ee-141">Ancho del vídeo en píxeles.</span><span class="sxs-lookup"><span data-stu-id="0a8ee-141">Width of the video, in pixels.</span></span>

[item-resource]: ../resources/driveitem.md

## <a name="remarks"></a><span data-ttu-id="0a8ee-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a8ee-142">Remarks</span></span>

<span data-ttu-id="0a8ee-143">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="0a8ee-143">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The video facet provides information about the properties of a video file.",
  "keywords": "bitrate,duration,size,video",
  "section": "documentation",
  "tocPath": "Facets/Video"
} -->
