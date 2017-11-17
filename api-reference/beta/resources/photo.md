# <a name="photo-resource-type"></a>Tipo de recurso Photo

El recurso **photo** proporciona propiedades de foto y cámara, por ejemplo, los metadatos EXIF, en un [driveItem](driveitem.md).

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.photo"
}-->
```json
{
  "cameraMake": "string",
  "cameraModel": "string",
  "exposureDenominator": 1024,
  "exposureNumerator": 1024,
  "fNumber": 1024,
  "focalLength": 1024,
  "iso": 1024,
  "takenDateTime": "String (timestamp)"
}
```

## <a name="properties"></a>Propiedades
| Propiedad                | Tipo                      | Descripción                                                     |
|:------------------------|:--------------------------|:----------------------------------------------------------------|
| **takenDateTime**       | DateTimeOffset            | Representa la fecha y hora en que se tomó la foto. Solo lectura.               |
| **cameraMake**          | String                    | Fabricante de la cámara. Solo lectura.                                            |
| **cameraModel**         | String                    | Modelo de la cámara. Solo lectura.                                                   |
| **fNumber**             | Doble                    | Valor punto F de la cámara. Solo lectura.                               |
| **exposureDenominator** | Int32                     | Denominador de la fracción de tiempo de exposición de la cámara. Solo lectura. |
| **exposureNumerator**   | Int32                     | Numerador de la fracción de tiempo de exposición de la cámara. Solo lectura.   |
| **focalLength**         | Doble                    | Distancia focal de la cámara. Solo lectura.                               |
| **iso**                 | Int32                     | Valor ISO de la cámara. Solo lectura.                                  |


## <a name="remarks"></a>Comentarios
OneDrive para la Empresa y SharePoint solo devuelven la propiedad **takenDateTime**.

Para obtener más información sobre las facetas de un DriveItem, consulte [DriveItem](driveitem.md).

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "photo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
