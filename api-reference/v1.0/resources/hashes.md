# <a name="hashes-resource-type"></a>Tipo de recurso Hashes

El recurso **Hashes** agrupa hashes disponibles en una sola estructura de un elemento.

**Nota:** No todos los servicios proporcionan un valor para todas las propiedades de hash enumeradas.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "sha1Hash", "crc32Hash", "quickXorHash" ],
  "@odata.type": "microsoft.graph.hashes"
}-->

```json
{
  "crc32Hash": "string",
  "sha1Hash": "string",
  "quickXorHash": "string"
}
```


## <a name="properties"></a>Propiedades

| Propiedad         | Tipo   | Descripción                                                       |
|:-----------------|:-------|:------------------------------------------------------------------|
| **sha1Hash**     | String | Hash SHA1 para el contenido del archivo (si está disponible). Solo lectura. |
| **crc32Hash**    | String | El valor CRC32 del archivo (si está disponible). Solo lectura.            |
| **quickXorHash** | String | Un hash de propietario del archivo que se puede usar para determinar si ha cambiado el contenido del archivo (si está disponible). Solo lectura. | 

**Nota:** En algunos casos, puede que no estén disponibles los valores hash. Si este es el caso, los valores hash de un elemento se actualizarán después de que se descargue el elemento.


## <a name="remarks"></a>Comentarios

En OneDrive para la Empresa, **sha1Hash** y **crc32Hash** no están disponibles. En OneDrive Personal, **quickXorHash** no está disponible.

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "hashes resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
