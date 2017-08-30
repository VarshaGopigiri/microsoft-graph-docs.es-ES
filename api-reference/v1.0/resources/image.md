# <a name="image-resource-type"></a>Tipo de recurso Image

El recurso **Image** agrupa en una sola estructura las propiedades relacionadas con la imagen. Si un [**DriveItem**](driveitem.md) tiene una faceta de **image** no null, el elemento representa una imagen de mapa de bits.

**Nota**: Si el servicio no puede determinar el ancho y el alto de la imagen, puede que el recurso **image** esté vacío.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@odata.type": "microsoft.graph.image"
}-->

```json
{
  "height": 1024,
  "width": 1024
}
```

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo  | Descripción                                |
|:-----------|:------|:-------------------------------------------|
| **height** | Int32 | Opcional. Ancho o alto de la imagen en píxeles. Solo lectura. |
| **width**  | Int32 | Opcional. Ancho de la imagen en píxeles. Solo lectura.  |

## <a name="remarks"></a>Observaciones

En OneDrive para la Empresa, este recurso se devuelve en los elementos que se esperan que sean imágenes en función de la extensión de archivo. Este recurso no devuelve propiedades en OneDrive para la Empresa.

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "image resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
