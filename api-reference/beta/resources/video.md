---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Vídeo
ms.openlocfilehash: a9bf228d814526d089fb102444e6952558b07e1c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089943"
---
# <a name="video-resource-type"></a><span data-ttu-id="67202-102">Tipo de recurso Video</span><span class="sxs-lookup"><span data-stu-id="67202-102">Video resource type</span></span>

> <span data-ttu-id="67202-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="67202-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="67202-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="67202-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="67202-105">El recurso **Video** agrupa en una sola estructura los elementos de datos relacionados con vídeos.</span><span class="sxs-lookup"><span data-stu-id="67202-105">The **Video** resource groups video-related data items into a single structure.</span></span>

<span data-ttu-id="67202-p102">Si un [**DriveItem**](driveitem.md) tiene una faceta **video** no-null, el elemento representa un archivo de vídeo. Las propiedades del recurso **Video** se rellenan extrayendo metadatos del archivo.</span><span class="sxs-lookup"><span data-stu-id="67202-p102">If a [**DriveItem**](driveitem.md) has a non-null **video** facet, the item represents a video file. The properties of the **Video** resource are populated by extracting metadata from the file.</span></span>

## <a name="json-representation"></a><span data-ttu-id="67202-108">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="67202-108">JSON representation</span></span>

<span data-ttu-id="67202-109">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="67202-109">Here is a JSON representation of the resource</span></span>

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

## <a name="properties"></a><span data-ttu-id="67202-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67202-110">Properties</span></span>

| <span data-ttu-id="67202-111">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="67202-111">Property name</span></span>             | <span data-ttu-id="67202-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="67202-112">Type</span></span>   | <span data-ttu-id="67202-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="67202-113">Description</span></span>
|:--------------------------|:-------|:----------------------------------------
| <span data-ttu-id="67202-114">**audioBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="67202-114">**audioBitsPerSample**</span></span>    | <span data-ttu-id="67202-115">Int32</span><span class="sxs-lookup"><span data-stu-id="67202-115">Int32</span></span>  | <span data-ttu-id="67202-116">Número de bits de audio por muestra.</span><span class="sxs-lookup"><span data-stu-id="67202-116">Number of audio bits per sample.</span></span>
| <span data-ttu-id="67202-117">**audioChannels**</span><span class="sxs-lookup"><span data-stu-id="67202-117">**audioChannels**</span></span>         | <span data-ttu-id="67202-118">Int32</span><span class="sxs-lookup"><span data-stu-id="67202-118">Int32</span></span>  | <span data-ttu-id="67202-119">Número de canales de audio.</span><span class="sxs-lookup"><span data-stu-id="67202-119">Number of audio channels.</span></span>
| <span data-ttu-id="67202-120">**audioFormat**</span><span class="sxs-lookup"><span data-stu-id="67202-120">**audioFormat**</span></span>           | <span data-ttu-id="67202-121">string</span><span class="sxs-lookup"><span data-stu-id="67202-121">string</span></span> | <span data-ttu-id="67202-122">Nombre del formato de audio (AAC, MP3, etc.).</span><span class="sxs-lookup"><span data-stu-id="67202-122">Name of the audio format (AAC, MP3, etc.).</span></span>
| <span data-ttu-id="67202-123">**audioSamplesPerSecond**</span><span class="sxs-lookup"><span data-stu-id="67202-123">**audioSamplesPerSecond**</span></span> | <span data-ttu-id="67202-124">Int32</span><span class="sxs-lookup"><span data-stu-id="67202-124">Int32</span></span>  | <span data-ttu-id="67202-125">Número de muestras de audio por segundo.</span><span class="sxs-lookup"><span data-stu-id="67202-125">Number of audio samples per second.</span></span>
| <span data-ttu-id="67202-126">**bitrate**</span><span class="sxs-lookup"><span data-stu-id="67202-126">**bitrate**</span></span>               | <span data-ttu-id="67202-127">Int32</span><span class="sxs-lookup"><span data-stu-id="67202-127">Int32</span></span>  | <span data-ttu-id="67202-128">Velocidad de bits del vídeo en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="67202-128">Bit rate of the video in bits per second.</span></span>
| <span data-ttu-id="67202-129">**duration**</span><span class="sxs-lookup"><span data-stu-id="67202-129">**duration**</span></span>              | <span data-ttu-id="67202-130">Int64</span><span class="sxs-lookup"><span data-stu-id="67202-130">Int64</span></span>  | <span data-ttu-id="67202-131">Duración del archivo en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="67202-131">Duration of the file in milliseconds.</span></span>
| <span data-ttu-id="67202-132">**fourCC**</span><span class="sxs-lookup"><span data-stu-id="67202-132">**fourCC**</span></span>                | <span data-ttu-id="67202-133">string</span><span class="sxs-lookup"><span data-stu-id="67202-133">string</span></span> | <span data-ttu-id="67202-134">Nombre en "código de cuatro caracteres" del formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="67202-134">"Four character code" name of the video format.</span></span>
| <span data-ttu-id="67202-135">**framerate**</span><span class="sxs-lookup"><span data-stu-id="67202-135">**framerate**</span></span>             | <span data-ttu-id="67202-136">double</span><span class="sxs-lookup"><span data-stu-id="67202-136">double</span></span> | <span data-ttu-id="67202-137">Velocidad de fotogramas del vídeo.</span><span class="sxs-lookup"><span data-stu-id="67202-137">Frame rate of the video.</span></span>
| <span data-ttu-id="67202-138">**height**</span><span class="sxs-lookup"><span data-stu-id="67202-138">**height**</span></span>                | <span data-ttu-id="67202-139">Int32</span><span class="sxs-lookup"><span data-stu-id="67202-139">Int32</span></span>  | <span data-ttu-id="67202-140">Alto del vídeo en píxeles.</span><span class="sxs-lookup"><span data-stu-id="67202-140">Height of the video, in pixels.</span></span>
| <span data-ttu-id="67202-141">**width**</span><span class="sxs-lookup"><span data-stu-id="67202-141">**width**</span></span>                 | <span data-ttu-id="67202-142">Int32</span><span class="sxs-lookup"><span data-stu-id="67202-142">Int32</span></span>  | <span data-ttu-id="67202-143">Ancho del vídeo en píxeles.</span><span class="sxs-lookup"><span data-stu-id="67202-143">Width of the video, in pixels.</span></span>

[item-resource]: ../resources/driveitem.md

## <a name="remarks"></a><span data-ttu-id="67202-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="67202-144">Remarks</span></span>

<span data-ttu-id="67202-145">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="67202-145">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>





<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The video facet provides information about the properties of a video file.",
  "keywords": "bitrate,duration,size,video",
  "section": "documentation",
  "tocPath": ""
}-->
