---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Audio
localization_priority: Normal
ms.openlocfilehash: ead665ee4977a563ebb6b24636b627d72a2428dc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871592"
---
# <a name="audio-facet"></a><span data-ttu-id="57802-102">Faceta Audio</span><span class="sxs-lookup"><span data-stu-id="57802-102">Audio facet</span></span>

> <span data-ttu-id="57802-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="57802-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="57802-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="57802-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="57802-105">El recurso **Audio** agrupa las propiedades relacionadas con el audio en un elemento en una sola estructura.</span><span class="sxs-lookup"><span data-stu-id="57802-105">The **Audio** resource groups audio-related properties on an item into a single structure.</span></span>

<span data-ttu-id="57802-p102">Si un objeto [**DriveItem**](driveitem.md) tiene una faceta **audio** que no sea null, el elemento representa un archivo de audio. Las propiedades del recurso **Audio** se rellenan al extraer metadatos del archivo.</span><span class="sxs-lookup"><span data-stu-id="57802-p102">If a [**DriveItem**](driveitem.md) has a non-null **audio** facet, the item represents an audio file. The properties of the **Audio** resource are populated by extracting metadata from the file.</span></span> 

## <a name="json-representation"></a><span data-ttu-id="57802-108">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="57802-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="57802-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="57802-109">Properties</span></span>

| <span data-ttu-id="57802-110">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="57802-110">Property name</span></span>         | <span data-ttu-id="57802-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="57802-111">Type</span></span>    | <span data-ttu-id="57802-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="57802-112">Description</span></span>                                                          |
|:----------------------|:--------|:---------------------------------------------------------------------|
| <span data-ttu-id="57802-113">**album**</span><span class="sxs-lookup"><span data-stu-id="57802-113">**album**</span></span>             | <span data-ttu-id="57802-114">string</span><span class="sxs-lookup"><span data-stu-id="57802-114">string</span></span>  | <span data-ttu-id="57802-115">El título del álbum de este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="57802-115">The title of the album for this audio file.</span></span>                          |
| <span data-ttu-id="57802-116">**albumArtist**</span><span class="sxs-lookup"><span data-stu-id="57802-116">**albumArtist**</span></span>       | <span data-ttu-id="57802-117">string</span><span class="sxs-lookup"><span data-stu-id="57802-117">string</span></span>  | <span data-ttu-id="57802-118">El artista que se nombra en el álbum del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="57802-118">The artist named on the album for the audio file.</span></span>                    |
| <span data-ttu-id="57802-119">**artist**</span><span class="sxs-lookup"><span data-stu-id="57802-119">**artist**</span></span>            | <span data-ttu-id="57802-120">string</span><span class="sxs-lookup"><span data-stu-id="57802-120">string</span></span>  | <span data-ttu-id="57802-121">El intérprete del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="57802-121">The performing artist for the audio file.</span></span>                            |
| <span data-ttu-id="57802-122">**bitrate**</span><span class="sxs-lookup"><span data-stu-id="57802-122">**bitrate**</span></span>           | <span data-ttu-id="57802-123">Int32</span><span class="sxs-lookup"><span data-stu-id="57802-123">Int32</span></span>   | <span data-ttu-id="57802-124">Velocidad de bits expresada en kbps.</span><span class="sxs-lookup"><span data-stu-id="57802-124">Bitrate expressed in kbps.</span></span>                                           |
| <span data-ttu-id="57802-125">**composers**</span><span class="sxs-lookup"><span data-stu-id="57802-125">**composers**</span></span>         | <span data-ttu-id="57802-126">string</span><span class="sxs-lookup"><span data-stu-id="57802-126">string</span></span>  | <span data-ttu-id="57802-127">El nombre del compositor del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="57802-127">The name of the composer of the audio file.</span></span>                          |
| <span data-ttu-id="57802-128">**copyright**</span><span class="sxs-lookup"><span data-stu-id="57802-128">**copyright**</span></span>         | <span data-ttu-id="57802-129">string</span><span class="sxs-lookup"><span data-stu-id="57802-129">string</span></span>  | <span data-ttu-id="57802-130">Información de copyright del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="57802-130">Copyright information for the audio file.</span></span>                            |
| <span data-ttu-id="57802-131">**disc**</span><span class="sxs-lookup"><span data-stu-id="57802-131">**disc**</span></span>              | <span data-ttu-id="57802-132">Int32</span><span class="sxs-lookup"><span data-stu-id="57802-132">Int32</span></span>   | <span data-ttu-id="57802-133">El número del disco del que procede este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="57802-133">The number of the disc this audio file came from.</span></span>                    |
| <span data-ttu-id="57802-134">**discCount**</span><span class="sxs-lookup"><span data-stu-id="57802-134">**discCount**</span></span>         | <span data-ttu-id="57802-135">Int32</span><span class="sxs-lookup"><span data-stu-id="57802-135">Int32</span></span>   | <span data-ttu-id="57802-136">El número total de discos de este álbum.</span><span class="sxs-lookup"><span data-stu-id="57802-136">The total number of discs in this album.</span></span>                             |
| <span data-ttu-id="57802-137">**duration**</span><span class="sxs-lookup"><span data-stu-id="57802-137">**duration**</span></span>          | <span data-ttu-id="57802-138">Int64</span><span class="sxs-lookup"><span data-stu-id="57802-138">Int64</span></span>   | <span data-ttu-id="57802-139">Duración del archivo de audio, expresada en milisegundos</span><span class="sxs-lookup"><span data-stu-id="57802-139">Duration of the audio file, expressed in milliseconds</span></span>                |
| <span data-ttu-id="57802-140">**genre**</span><span class="sxs-lookup"><span data-stu-id="57802-140">**genre**</span></span>             | <span data-ttu-id="57802-141">string</span><span class="sxs-lookup"><span data-stu-id="57802-141">string</span></span>  | <span data-ttu-id="57802-142">El género de este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="57802-142">The genre of this audio file.</span></span>                                        |
| <span data-ttu-id="57802-143">**hasDrm**</span><span class="sxs-lookup"><span data-stu-id="57802-143">**hasDrm**</span></span>            | <span data-ttu-id="57802-144">boolean</span><span class="sxs-lookup"><span data-stu-id="57802-144">boolean</span></span> | <span data-ttu-id="57802-145">Indica si el archivo está protegido con administración de derechos digitales.</span><span class="sxs-lookup"><span data-stu-id="57802-145">Indicates if the file is protected with digital rights management.</span></span>   |
| <span data-ttu-id="57802-146">**isVariableBitrate**</span><span class="sxs-lookup"><span data-stu-id="57802-146">**isVariableBitrate**</span></span> | <span data-ttu-id="57802-147">boolean</span><span class="sxs-lookup"><span data-stu-id="57802-147">boolean</span></span> | <span data-ttu-id="57802-148">Indica si el archivo está codificado con una velocidad de bits variable.</span><span class="sxs-lookup"><span data-stu-id="57802-148">Indicates if the file is encoded with a variable bitrate.</span></span>            |
| <span data-ttu-id="57802-149">**title**</span><span class="sxs-lookup"><span data-stu-id="57802-149">**title**</span></span>             | <span data-ttu-id="57802-150">string</span><span class="sxs-lookup"><span data-stu-id="57802-150">string</span></span>  | <span data-ttu-id="57802-151">El título del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="57802-151">The title of the audio file.</span></span>                                         |
| <span data-ttu-id="57802-152">**track**</span><span class="sxs-lookup"><span data-stu-id="57802-152">**track**</span></span>             | <span data-ttu-id="57802-153">Int32</span><span class="sxs-lookup"><span data-stu-id="57802-153">Int32</span></span>   | <span data-ttu-id="57802-154">El número de la pista en el disco original de este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="57802-154">The number of the track on the original disc for this audio file.</span></span>    |
| <span data-ttu-id="57802-155">**trackCount**</span><span class="sxs-lookup"><span data-stu-id="57802-155">**trackCount**</span></span>        | <span data-ttu-id="57802-156">Int32</span><span class="sxs-lookup"><span data-stu-id="57802-156">Int32</span></span>   | <span data-ttu-id="57802-157">El número total de pistas en el disco original de este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="57802-157">The total number of tracks on the original disc for this audio file.</span></span> |
| <span data-ttu-id="57802-158">**year**</span><span class="sxs-lookup"><span data-stu-id="57802-158">**year**</span></span>              | <span data-ttu-id="57802-159">Int32</span><span class="sxs-lookup"><span data-stu-id="57802-159">Int32</span></span>   | <span data-ttu-id="57802-160">El año en que se ha grabado el archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="57802-160">The year the audio file was recorded.</span></span>                                |

[item-resource]: ../resources/driveitem.md

## <a name="remarks"></a><span data-ttu-id="57802-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57802-161">Remarks</span></span>

<span data-ttu-id="57802-162">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="57802-162">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The audio facet provides information about music or audio metadata.",
  "keywords": "music,audio,metadata,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Audio"
} -->
