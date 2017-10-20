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
# <a name="video-resource-type"></a>Tipo de recurso Video

El recurso **Video** agrupa en una sola estructura los elementos de datos relacionados con vídeos.

Si un [**DriveItem**](driveitem.md) tiene una faceta **video** no-null, el elemento representa un archivo de vídeo.
Las propiedades del recurso **Video** se rellenan extrayendo metadatos del archivo.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

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

## <a name="properties"></a>Propiedades

| Nombre de la propiedad             | Tipo   | Descripción
|:--------------------------|:-------|:----------------------------------------
| **audioBitsPerSample**    | Int32  | Número de bits de audio por muestra.
| **audioChannels**         | Int32  | Número de canales de audio.
| **audioFormat**           | string | Nombre del formato de audio (AAC, MP3, etc.).
| **audioSamplesPerSecond** | Int32  | Número de muestras de audio por segundo.
| **bitrate**               | Int32  | Velocidad de bits del vídeo en bits por segundo.
| **duration**              | Int64  | Duración del archivo en milisegundos.
| **fourCC**                | string | Nombre en "código de cuatro caracteres" del formato de vídeo.
| **framerate**             | double | Velocidad de fotogramas del vídeo.
| **height**                | Int32  | Alto del vídeo en píxeles.
| **width**                 | Int32  | Ancho del vídeo en píxeles.

[item-resource]: ../resources/driveitem.md

## <a name="remarks"></a>Comentarios

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "The video facet provides information about the properties of a video file.",
  "keywords": "bitrate,duration,size,video",
  "section": "documentation",
  "tocPath": "Facets/Video"
} -->
