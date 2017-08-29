# <a name="geocoordinates-resource-type"></a>Tipo de recurso GeoCoordinates

El recurso **GeoCoordinates** proporciona las coordenadas geográficas y la elevación de una ubicación en función de metadatos contenidos en el archivo. Si un [**DriveItem**](driveitem.md) tiene una faceta **location** no null, el elemento representa un archivo que tiene asociada una ubicación conocida.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.geoCoordinates"
}-->

```json
{
  "altitude": 1024.13,
  "latitude": 26.13246,
  "longitude": 24.34616
}
```

## <a name="properties"></a>Propiedades

| Propiedad  | Tipo   | Descripción                                                    |
|:----------|:-------|:---------------------------------------------------------------|
| altitude  | Doble | Opcional. Altitud (alto) en pies sobre el nivel del mar del elemento. Solo lectura. |
| latitude  | Doble | Opcional. Latitud en formato decimal del elemento. Solo lectura.   |
| longitude | Doble | Opcional. Longitud en formato decimal del elemento. Solo lectura.  |

## <a name="remarks"></a>Observaciones

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "geoCoordinates resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
