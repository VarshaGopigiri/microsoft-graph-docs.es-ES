# <a name="specialfolder-resource-type"></a>Tipo de recurso SpecialFolder

El recurso **SpecialFolder** agrupa en una sola estructura los elementos de datos relacionados con carpetas especiales.

Si un objeto **DriveItem** tiene una faceta **specialFolder** que no es null, el elemento representa una carpeta especial (con nombre). Se puede acceder a las carpetas especiales directamente a través de la [colección de carpetas especiales](../api/drive_special.md).

Las carpetas especiales proporcionan alias simples para acceder a carpetas conocidas sin necesidad de buscar la carpeta por su ruta (que requeriría localización) o hacer referencia a la carpeta con un identificador. Si una carpeta especial cambia de nombre o se mueve a otra ubicación de la unidad, esta sintaxis seguirá devolviendo esa carpeta.

Las carpetas especiales se crean de forma automática la primera vez que una aplicación intenta escribir en una, si aún no existe. Si un usuario elimina una, se vuelve a crear al volver a escribir en ella.

**Nota:** Si la aplicación solo ha solicitado el ámbito **Files.Read** y solicita una carpeta especial que no existe, la respuesta será un error `403 Forbidden`.

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.specialFolder"
}-->
```json
{
  "name": "string"
}
```

## <a name="properties"></a>Propiedades

| Propiedad  | Tipo   | Descripción                                                            |
|:----------|:-------|:-----------------------------------------------------------------------|
| name      | string | El identificador único de este elemento en la colección `/drive/special` |

## <a name="special-folders"></a>Carpetas especiales

Estas son las carpetas especiales disponibles en OneDrive Personal y OneDrive para la Empresa.

| Nombre        | Id. de carpeta    | Descripción                                                              |
|:------------|:-------------|:-------------------------------------------------------------------------|
| Raíz de la aplicación    | `approot`    | La carpeta personal de la aplicación. Normalmente en `/Apps/{Application Name}` |
| Álbum de cámara | `cameraroll` | La carpeta de copia de seguridad del álbum de cámara. No está disponible en OneDrive para la Empresa.   |
| Documentos   | `documents`  | La carpeta Documentos.                                                    |
| Música       | `music`      | La carpeta Música. No está disponible en OneDrive para la Empresa.                |
| Fotos      | `photos`     | La carpeta Fotos.                                                       |

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "specialFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
