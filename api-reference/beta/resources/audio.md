---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Audio
ms.openlocfilehash: 1472bffec12ed5626a65ea71b971dc5bc2b77aa9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085079"
---
# <a name="audio-facet"></a><span data-ttu-id="f743c-102">Faceta Audio</span><span class="sxs-lookup"><span data-stu-id="f743c-102">Audio facet</span></span>

> <span data-ttu-id="f743c-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f743c-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f743c-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f743c-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f743c-105">El recurso **Audio** agrupa las propiedades relacionadas con el audio en un elemento en una sola estructura.</span><span class="sxs-lookup"><span data-stu-id="f743c-105">The **Audio** resource groups audio-related properties on an item into a single structure.</span></span>

<span data-ttu-id="f743c-p102">Si un objeto [**DriveItem**](driveitem.md) tiene una faceta **audio** que no sea null, el elemento representa un archivo de audio. Las propiedades del recurso **Audio** se rellenan al extraer metadatos del archivo.</span><span class="sxs-lookup"><span data-stu-id="f743c-p102">If a [**DriveItem**](driveitem.md) has a non-null **audio** facet, the item represents an audio file. The properties of the **Audio** resource are populated by extracting metadata from the file.</span></span> 

## <a name="json-representation"></a><span data-ttu-id="f743c-108">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f743c-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="f743c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f743c-109">Properties</span></span>

| <span data-ttu-id="f743c-110">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="f743c-110">Property name</span></span>         | <span data-ttu-id="f743c-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="f743c-111">Type</span></span>    | <span data-ttu-id="f743c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f743c-112">Description</span></span>                                                          |
|:----------------------|:--------|:---------------------------------------------------------------------|
| <span data-ttu-id="f743c-113">**album**</span><span class="sxs-lookup"><span data-stu-id="f743c-113">**album**</span></span>             | <span data-ttu-id="f743c-114">string</span><span class="sxs-lookup"><span data-stu-id="f743c-114">string</span></span>  | <span data-ttu-id="f743c-115">El título del álbum de este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f743c-115">The title of the album for this audio file.</span></span>                          |
| <span data-ttu-id="f743c-116">**albumArtist**</span><span class="sxs-lookup"><span data-stu-id="f743c-116">**albumArtist**</span></span>       | <span data-ttu-id="f743c-117">string</span><span class="sxs-lookup"><span data-stu-id="f743c-117">string</span></span>  | <span data-ttu-id="f743c-118">El artista que se nombra en el álbum del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f743c-118">The artist named on the album for the audio file.</span></span>                    |
| <span data-ttu-id="f743c-119">**artist**</span><span class="sxs-lookup"><span data-stu-id="f743c-119">**artist**</span></span>            | <span data-ttu-id="f743c-120">string</span><span class="sxs-lookup"><span data-stu-id="f743c-120">string</span></span>  | <span data-ttu-id="f743c-121">El intérprete del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f743c-121">The performing artist for the audio file.</span></span>                            |
| <span data-ttu-id="f743c-122">**bitrate**</span><span class="sxs-lookup"><span data-stu-id="f743c-122">**bitrate**</span></span>           | <span data-ttu-id="f743c-123">Int32</span><span class="sxs-lookup"><span data-stu-id="f743c-123">Int32</span></span>   | <span data-ttu-id="f743c-124">Velocidad de bits expresada en kbps.</span><span class="sxs-lookup"><span data-stu-id="f743c-124">Bitrate expressed in kbps.</span></span>                                           |
| <span data-ttu-id="f743c-125">**composers**</span><span class="sxs-lookup"><span data-stu-id="f743c-125">**composers**</span></span>         | <span data-ttu-id="f743c-126">string</span><span class="sxs-lookup"><span data-stu-id="f743c-126">string</span></span>  | <span data-ttu-id="f743c-127">El nombre del compositor del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f743c-127">The name of the composer of the audio file.</span></span>                          |
| <span data-ttu-id="f743c-128">**copyright**</span><span class="sxs-lookup"><span data-stu-id="f743c-128">**copyright**</span></span>         | <span data-ttu-id="f743c-129">string</span><span class="sxs-lookup"><span data-stu-id="f743c-129">string</span></span>  | <span data-ttu-id="f743c-130">Información de copyright del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f743c-130">Copyright information for the audio file.</span></span>                            |
| <span data-ttu-id="f743c-131">**disc**</span><span class="sxs-lookup"><span data-stu-id="f743c-131">**disc**</span></span>              | <span data-ttu-id="f743c-132">Int32</span><span class="sxs-lookup"><span data-stu-id="f743c-132">Int32</span></span>   | <span data-ttu-id="f743c-133">El número del disco del que procede este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f743c-133">The number of the disc this audio file came from.</span></span>                    |
| <span data-ttu-id="f743c-134">**discCount**</span><span class="sxs-lookup"><span data-stu-id="f743c-134">**discCount**</span></span>         | <span data-ttu-id="f743c-135">Int32</span><span class="sxs-lookup"><span data-stu-id="f743c-135">Int32</span></span>   | <span data-ttu-id="f743c-136">El número total de discos de este álbum.</span><span class="sxs-lookup"><span data-stu-id="f743c-136">The total number of discs in this album.</span></span>                             |
| <span data-ttu-id="f743c-137">**duration**</span><span class="sxs-lookup"><span data-stu-id="f743c-137">**duration**</span></span>          | <span data-ttu-id="f743c-138">Int64</span><span class="sxs-lookup"><span data-stu-id="f743c-138">Int64</span></span>   | <span data-ttu-id="f743c-139">Duración del archivo de audio, expresada en milisegundos</span><span class="sxs-lookup"><span data-stu-id="f743c-139">Duration of the audio file, expressed in milliseconds</span></span>                |
| <span data-ttu-id="f743c-140">**genre**</span><span class="sxs-lookup"><span data-stu-id="f743c-140">**genre**</span></span>             | <span data-ttu-id="f743c-141">string</span><span class="sxs-lookup"><span data-stu-id="f743c-141">string</span></span>  | <span data-ttu-id="f743c-142">El género de este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f743c-142">The genre of this audio file.</span></span>                                        |
| <span data-ttu-id="f743c-143">**hasDrm**</span><span class="sxs-lookup"><span data-stu-id="f743c-143">**hasDrm**</span></span>            | <span data-ttu-id="f743c-144">boolean</span><span class="sxs-lookup"><span data-stu-id="f743c-144">boolean</span></span> | <span data-ttu-id="f743c-145">Indica si el archivo está protegido con administración de derechos digitales.</span><span class="sxs-lookup"><span data-stu-id="f743c-145">Indicates if the file is protected with digital rights management.</span></span>   |
| <span data-ttu-id="f743c-146">**isVariableBitrate**</span><span class="sxs-lookup"><span data-stu-id="f743c-146">**isVariableBitrate**</span></span> | <span data-ttu-id="f743c-147">boolean</span><span class="sxs-lookup"><span data-stu-id="f743c-147">boolean</span></span> | <span data-ttu-id="f743c-148">Indica si el archivo está codificado con una velocidad de bits variable.</span><span class="sxs-lookup"><span data-stu-id="f743c-148">Indicates if the file is encoded with a variable bitrate.</span></span>            |
| <span data-ttu-id="f743c-149">**title**</span><span class="sxs-lookup"><span data-stu-id="f743c-149">**title**</span></span>             | <span data-ttu-id="f743c-150">string</span><span class="sxs-lookup"><span data-stu-id="f743c-150">string</span></span>  | <span data-ttu-id="f743c-151">El título del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f743c-151">The title of the audio file.</span></span>                                         |
| <span data-ttu-id="f743c-152">**track**</span><span class="sxs-lookup"><span data-stu-id="f743c-152">**track**</span></span>             | <span data-ttu-id="f743c-153">Int32</span><span class="sxs-lookup"><span data-stu-id="f743c-153">Int32</span></span>   | <span data-ttu-id="f743c-154">El número de la pista en el disco original de este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f743c-154">The number of the track on the original disc for this audio file.</span></span>    |
| <span data-ttu-id="f743c-155">**trackCount**</span><span class="sxs-lookup"><span data-stu-id="f743c-155">**trackCount**</span></span>        | <span data-ttu-id="f743c-156">Int32</span><span class="sxs-lookup"><span data-stu-id="f743c-156">Int32</span></span>   | <span data-ttu-id="f743c-157">El número total de pistas en el disco original de este archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f743c-157">The total number of tracks on the original disc for this audio file.</span></span> |
| <span data-ttu-id="f743c-158">**year**</span><span class="sxs-lookup"><span data-stu-id="f743c-158">**year**</span></span>              | <span data-ttu-id="f743c-159">Int32</span><span class="sxs-lookup"><span data-stu-id="f743c-159">Int32</span></span>   | <span data-ttu-id="f743c-160">El año en que se ha grabado el archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f743c-160">The year the audio file was recorded.</span></span>                                |

[item-resource]: ../resources/driveitem.md

## <a name="remarks"></a><span data-ttu-id="f743c-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f743c-161">Remarks</span></span>

<span data-ttu-id="f743c-162">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="f743c-162">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The audio facet provides information about music or audio metadata.",
  "keywords": "music,audio,metadata,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Audio"
} -->
