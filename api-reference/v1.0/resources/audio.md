---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Audio
ms.openlocfilehash: e68b70565f0eccd7847fba2b8085661071a75ae7
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23266236"
---
# <a name="audio-facet"></a>Faceta Audio

El recurso **Audio** agrupa las propiedades relacionadas con el audio en un elemento en una sola estructura.

Si un objeto [**DriveItem**](driveitem.md) tiene una faceta **audio** que no sea null, el elemento representa un archivo de audio. Las propiedades del recurso **Audio** se rellenan al extraer metadatos del archivo. 

## <a name="json-representation"></a>Representación JSON

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

## <a name="properties"></a>Propiedades

| Nombre de propiedad         | Tipo    | Descripción                                                          |
|:----------------------|:--------|:---------------------------------------------------------------------|
| **album**             | cadena  | El título del álbum de este archivo de audio.                          |
| **albumArtist**       | cadena  | El artista que se nombra en el álbum del archivo de audio.                    |
| **artist**            | cadena  | El intérprete del archivo de audio.                            |
| **bitrate**           | Int64   | Velocidad de bits expresada en kbps.                                           |
| **composers**         | cadena  | El nombre del compositor del archivo de audio.                          |
| **copyright**         | cadena  | Información de copyright del archivo de audio.                            |
| **disc**              | Int16   | El número del disco del que procede este archivo de audio.                    |
| **discCount**         | Int16   | El número total de discos de este álbum.                             |
| **duration**          | Int64   | Duración del archivo de audio, expresada en milisegundos                |
| **genre**             | cadena  | El género de este archivo de audio.                                        |
| **hasDrm**            | booleano | Indica si el archivo está protegido con administración de derechos digitales.   |
| **isVariableBitrate** | booleano | Indica si el archivo está codificado con una velocidad de bits variable.            |
| **title**             | cadena  | El título del archivo de audio.                                         |
| **track**             | Int32   | El número de la pista en el disco original de este archivo de audio.    |
| **trackCount**        | Int32   | El número total de pistas en el disco original de este archivo de audio. |
| **year**              | Int32   | El año en que se ha grabado el archivo de audio.                                |

[item-resource]: ../resources/driveitem.md

## <a name="remarks"></a>Comentarios

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "The audio facet provides information about music or audio metadata.",
  "keywords": "music,audio,metadata,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Audio"
} -->
