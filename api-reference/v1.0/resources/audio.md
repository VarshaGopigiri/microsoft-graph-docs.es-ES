---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Audio
ms.openlocfilehash: 43b9999ecfb472a82e00a12ca820fdf8548eec64
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="audio-facet"></a><span data-ttu-id="68053-102">Faceta Audio</span><span class="sxs-lookup"><span data-stu-id="68053-102">Audio facet</span></span>

<span data-ttu-id="68053-103">El recurso **Audio** agrupa las propiedades relacionadas con el audio en un elemento en una sola estructura.</span><span class="sxs-lookup"><span data-stu-id="68053-103">The **Audio** resource groups audio-related properties on an item into a single structure.</span></span>

<span data-ttu-id="68053-104">Si un objeto [**DriveItem**](driveitem.md) tiene una faceta **audio** que no sea null, el elemento representa un archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="68053-104">If a [**DriveItem**](driveitem.md) has a non-null **audio** facet, the item represents an audio file. The properties of the Audio resource are populated by extracting metadata from the file.</span></span>
<span data-ttu-id="68053-105">Las propiedades del recurso **Audio** se rellenan al extraer metadatos del archivo.</span><span class="sxs-lookup"><span data-stu-id="68053-105">If a DriveItem has a non-null audio facet, the item represents an audio file. The properties of the **Audio** resource are populated by extracting metadata from the file.</span></span> 

## <a name="json-representation"></a><span data-ttu-id="68053-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="68053-106">JSON representation</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.audio" } -->
```json
{
  "album": "string",
  "albumArtist": "string",
  "artist": "string",
  "bitrate": 128,
  "composers": "string",
  "copyright": "string",
  "disc": 0,
  "discCount": 0,
  "duration": 567,
  "genre": "string",
  "hasDrm": false,
  "isVariableBitrate": false,
  "title": "string",
  "track": 1,
  "trackCount": 16,
  "year": 2014
}
```

## <a name="properties"></a><span data-ttu-id="68053-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68053-107">Properties</span></span>

| <span data-ttu-id="68053-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="68053-108">Property name</span></span>         | <span data-ttu-id="68053-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="68053-109">Type</span></span>    | <span data-ttu-id="68053-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="68053-110">Description</span></span>                                                          |
|:----------------------|:--------|:---------------------------------------------------------------------|
| <span data-ttu-id="68053-111">**album**</span><span class="sxs-lookup"><span data-stu-id="68053-111">**album**</span></span>             | <span data-ttu-id="68053-112">string</span><span class="sxs-lookup"><span data-stu-id="68053-112">string</span></span>  | <span data-ttu-id="68053-113">El título del álbum de este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="68053-113">The title of the album for this audio file.</span></span>                          |
| <span data-ttu-id="68053-114">**albumArtist**</span><span class="sxs-lookup"><span data-stu-id="68053-114">**albumArtist**</span></span>       | <span data-ttu-id="68053-115">string</span><span class="sxs-lookup"><span data-stu-id="68053-115">string</span></span>  | <span data-ttu-id="68053-116">El artista que se nombra en el álbum del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="68053-116">The artist named on the album for the audio file.</span></span>                    |
| <span data-ttu-id="68053-117">**artist**</span><span class="sxs-lookup"><span data-stu-id="68053-117">**artist**</span></span>            | <span data-ttu-id="68053-118">string</span><span class="sxs-lookup"><span data-stu-id="68053-118">string</span></span>  | <span data-ttu-id="68053-119">El intérprete del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="68053-119">The performing artist for the audio file.</span></span>                            |
| <span data-ttu-id="68053-120">**bitrate**</span><span class="sxs-lookup"><span data-stu-id="68053-120">**bitrate**</span></span>           | <span data-ttu-id="68053-121">Int32</span><span class="sxs-lookup"><span data-stu-id="68053-121">Int32</span></span>   | <span data-ttu-id="68053-122">Velocidad de bits expresada en kbps.</span><span class="sxs-lookup"><span data-stu-id="68053-122">Bitrate expressed in kbps.</span></span>                                           |
| <span data-ttu-id="68053-123">**composers**</span><span class="sxs-lookup"><span data-stu-id="68053-123">**composers**</span></span>         | <span data-ttu-id="68053-124">string</span><span class="sxs-lookup"><span data-stu-id="68053-124">string</span></span>  | <span data-ttu-id="68053-125">El nombre del compositor del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="68053-125">The name of the composer of the audio file.</span></span>                          |
| <span data-ttu-id="68053-126">**copyright**</span><span class="sxs-lookup"><span data-stu-id="68053-126">**copyright**</span></span>         | <span data-ttu-id="68053-127">string</span><span class="sxs-lookup"><span data-stu-id="68053-127">string</span></span>  | <span data-ttu-id="68053-128">Información de copyright del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="68053-128">Copyright information for the audio file.</span></span>                            |
| <span data-ttu-id="68053-129">**disc**</span><span class="sxs-lookup"><span data-stu-id="68053-129">**disc**</span></span>              | <span data-ttu-id="68053-130">Int32</span><span class="sxs-lookup"><span data-stu-id="68053-130">Int32</span></span>   | <span data-ttu-id="68053-131">El número del disco del que procede este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="68053-131">The number of the disc this audio file came from.</span></span>                    |
| <span data-ttu-id="68053-132">**discCount**</span><span class="sxs-lookup"><span data-stu-id="68053-132">**discCount**</span></span>         | <span data-ttu-id="68053-133">Int32</span><span class="sxs-lookup"><span data-stu-id="68053-133">Int32</span></span>   | <span data-ttu-id="68053-134">El número total de discos de este álbum.</span><span class="sxs-lookup"><span data-stu-id="68053-134">The total number of discs in this album.</span></span>                             |
| <span data-ttu-id="68053-135">**duration**</span><span class="sxs-lookup"><span data-stu-id="68053-135">**duration**</span></span>          | <span data-ttu-id="68053-136">Int64</span><span class="sxs-lookup"><span data-stu-id="68053-136">Int64</span></span>   | <span data-ttu-id="68053-137">Duración del archivo de audio, expresada en milisegundos</span><span class="sxs-lookup"><span data-stu-id="68053-137">Duration of the audio file, expressed in milliseconds</span></span>                |
| <span data-ttu-id="68053-138">**genre**</span><span class="sxs-lookup"><span data-stu-id="68053-138">**genre**</span></span>             | <span data-ttu-id="68053-139">string</span><span class="sxs-lookup"><span data-stu-id="68053-139">string</span></span>  | <span data-ttu-id="68053-140">El género de este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="68053-140">The genre of this audio file.</span></span>                                        |
| <span data-ttu-id="68053-141">**hasDrm**</span><span class="sxs-lookup"><span data-stu-id="68053-141">**hasDrm**</span></span>            | <span data-ttu-id="68053-142">boolean</span><span class="sxs-lookup"><span data-stu-id="68053-142">boolean</span></span> | <span data-ttu-id="68053-143">Indica si el archivo está protegido con administración de derechos digitales.</span><span class="sxs-lookup"><span data-stu-id="68053-143">Indicates if the file is protected with digital rights management.</span></span>   |
| <span data-ttu-id="68053-144">**isVariableBitrate**</span><span class="sxs-lookup"><span data-stu-id="68053-144">**isVariableBitrate**</span></span> | <span data-ttu-id="68053-145">boolean</span><span class="sxs-lookup"><span data-stu-id="68053-145">boolean</span></span> | <span data-ttu-id="68053-146">Indica si el archivo está codificado con una velocidad de bits variable.</span><span class="sxs-lookup"><span data-stu-id="68053-146">Indicates if the file is encoded with a variable bitrate.</span></span>            |
| <span data-ttu-id="68053-147">**title**</span><span class="sxs-lookup"><span data-stu-id="68053-147">**title**</span></span>             | <span data-ttu-id="68053-148">string</span><span class="sxs-lookup"><span data-stu-id="68053-148">string</span></span>  | <span data-ttu-id="68053-149">El título del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="68053-149">The title of the audio file.</span></span>                                         |
| <span data-ttu-id="68053-150">**track**</span><span class="sxs-lookup"><span data-stu-id="68053-150">**track**</span></span>             | <span data-ttu-id="68053-151">Int32</span><span class="sxs-lookup"><span data-stu-id="68053-151">Int32</span></span>   | <span data-ttu-id="68053-152">El número de la pista en el disco original de este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="68053-152">The number of the track on the original disc for this audio file.</span></span>    |
| <span data-ttu-id="68053-153">**trackCount**</span><span class="sxs-lookup"><span data-stu-id="68053-153">**trackCount**</span></span>        | <span data-ttu-id="68053-154">Int32</span><span class="sxs-lookup"><span data-stu-id="68053-154">Int32</span></span>   | <span data-ttu-id="68053-155">El número total de pistas en el disco original de este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="68053-155">The total number of tracks on the original disc for this audio file.</span></span> |
| <span data-ttu-id="68053-156">**year**</span><span class="sxs-lookup"><span data-stu-id="68053-156">**year**</span></span>              | <span data-ttu-id="68053-157">Int32</span><span class="sxs-lookup"><span data-stu-id="68053-157">Int32</span></span>   | <span data-ttu-id="68053-158">El año en que se ha grabado el archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="68053-158">The year the audio file was recorded.</span></span>                                |

[item-resource]: ../resources/driveitem.md

## <a name="remarks"></a><span data-ttu-id="68053-159">Comentarios</span><span class="sxs-lookup"><span data-stu-id="68053-159">Remarks</span></span>

<span data-ttu-id="68053-160">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="68053-160">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The audio facet provides information about music or audio metadata.",
  "keywords": "music,audio,metadata,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Audio"
} -->
