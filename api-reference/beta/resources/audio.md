# <a name="audio-resource-type"></a>Tipo de recurso de audio

El recurso **Audio** agrupa las propiedades relacionadas con el audio en un elemento en una sola estructura.

Si un objeto [**DriveItem**](driveitem.md) tiene una faceta **audio** que no sea null, el elemento representa un archivo de audio. Las propiedades del recurso **Audio** se rellenan al extraer metadatos del archivo. 

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@odata.type": "microsoft.graph.audio"
}-->
```json
{
  "album": "string",
  "albumArtist": "string",
  "artist": "string",
  "bitrate": 1024,
  "composers": "string",
  "copyright": "string",
  "disc": 1024,
  "discCount": 1024,
  "duration": 1024,
  "genre": "string",
  "hasDrm": true,
  "isVariableBitrate": true,
  "title": "string",
  "track": 1024,
  "trackCount": 1024,
  "year": 1024
}
```

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo    | Descripción                                                          |
|:------------------|:--------|:---------------------------------------------------------------------|
| album             | string  | El título del álbum de este archivo de audio.                          |
| albumArtist       | string  | El artista que se nombra en el álbum del archivo de audio.                    |
| artist            | string  | El intérprete del archivo de audio.                            |
| bitrate           | string  | Velocidad de bits expresada en kbps.                                           |
| composers         | string  | El nombre del compositor del archivo de audio.                          |
| copyright         | string  | Información de copyright del archivo de audio.                            |
| disc              | number  | El número del disco del que procede este archivo de audio.                    |
| discCount         | number  | El número total de discos de este álbum.                             |
| duration          | number  | Duración del archivo de audio, expresada en milisegundos                |
| genre             | string  | El género de este archivo de audio.                                        |
| hasDrm            | boolean | Indica si el archivo está protegido con administración de derechos digitales.   |
| isVariableBitrate | boolean | Indica si el archivo está codificado con una velocidad de bits variable.            |
| title             | string  | El título del archivo de audio.                                         |
| track             | number  | El número de la pista en el disco original de este archivo de audio.    |
| trackCount        | number  | El número total de pistas en el disco original de este archivo de audio. |
| year              | number  | El año en que se ha grabado el archivo de audio.                                |

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "audio resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->