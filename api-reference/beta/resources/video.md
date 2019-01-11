---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Vídeo
localization_priority: Normal
ms.openlocfilehash: 3883dd494304409b76d10781039424267ada85f0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866636"
---
# <a name="video-resource-type"></a>Tipo de recurso Video

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **Video** agrupa en una sola estructura los elementos de datos relacionados con vídeos.

Si un [**DriveItem**](driveitem.md) tiene una faceta **video** no-null, el elemento representa un archivo de vídeo. Las propiedades del recurso **Video** se rellenan extrayendo metadatos del archivo.

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





<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The video facet provides information about the properties of a video file.",
  "keywords": "bitrate,duration,size,video",
  "section": "documentation",
  "tocPath": ""
}-->
