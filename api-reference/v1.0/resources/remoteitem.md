# <a name="remoteitem-resource-type"></a>Tipo de recurso RemoteItem

El recurso **RemoteItem** indica que un objeto [DriveItem](driveitem.md) hace referencia a un elemento que existe en otra unidad. Este recurso proporciona los identificadores únicos de la unidad de origen y del elemento de destino.

Los objetos [**DriveItem**](driveitem.md) con una faceta **remoteItem** que no sea null son recursos que se comparten, agregan al OneDrive del usuario o que están en elementos devueltos de colecciones heterogéneas de elementos (como los resultados de la búsqueda). 

**Nota:** A diferencia de las carpetas de la misma unidad, puede que a un objeto DriveItem que se mueva a un elemento remoto se le cambie el valor `id`.
## <a name="json-representation"></a>Representación JSON

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.remoteItem", optionalProperties: ["name", "fileSystemInfo", "file", "folder"] } -->
```json
{
  "id": "string",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "timestamp",
  "file": { "@odata.type": "microsoft.graph.file" },
  "fileSystemInfo": { "@odata.type": "microsoft.graph.fileSystemInfo" },
  "folder": { "@odata.type": "microsoft.graph.folder" },
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "timestamp",
  "name": "string",
  "package": { "@odata.type": "microsoft.graph.package" },
  "parentReference": { "@odata.type": "microsoft.graph.itemReference" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "size": 1024,
  "specialFolder": { "@odata.type": "microsoft.graph.specialFolder" },
  "webDavUrl": "url",
  "webUrl": "url"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad        | Tipo                                          | Descripción                                                              |
|:---------------------|:----------------------------------------------|:-------------------------------------------------------------------------|
| createdBy            | [IdentitySet](identityset.md)                 | Identidad del usuario, el dispositivo y la aplicación que ha creado el elemento. Solo lectura.   |
| createdDateTime      | Timestamp                                     | Fecha y hora de creación del elemento. Solo lectura. |
| archivo                 | [File](file.md)                               | Indica que el elemento remoto es un archivo. Solo lectura.                     |
| fileSystemInfo       | [FileSystemInfo](filesysteminfo.md)           | Información sobre el elemento remoto del sistema de archivos local. Solo lectura. |
| folder               | [Folder](folder.md)                           | Indica que el elemento remoto es una carpeta. Solo lectura.                   |
| id                   | String                                        | Identificador único del elemento remoto en su unidad. Solo lectura.           |
| lastModifiedBy       | [IdentitySet](identityset.md)                 | Identidad del usuario, el dispositivo y la aplicación que ha modificado por última vez el elemento. Solo lectura. |
| lastModifiedDateTime | Timestamp                                     | Fecha y hora de la última modificación del elemento. Solo lectura.  | 
| name                 | String                                        | Opcional. Nombre de archivo del elemento remoto. Solo lectura.                        |
| paquete              | [Package](package.md)                         | Si está presente, indica que este elemento es un paquete en lugar de una carpeta o archivo. Los paquetes se tratan como archivos en algunos contextos y como carpetas en otros. Solo lectura. |
| parentReference      | [ItemReference](itemreference.md)             | Propiedades del elemento primario del elemento remoto. Solo lectura.                  |
| sharepointIds        | [SharepointIds](sharepointids.md)             | Proporciona interoperabilidad entre elementos de OneDrive para la Empresa y SharePoint con el conjunto completo de identificadores de elementos. Solo lectura.  |
| size                 | Int64                                         | Tamaño del elemento remoto. Solo lectura.                                      |
| specialFolder        | [SpecialFolder](specialfolder.md)             | Si el elemento actual también está disponible como una carpeta especial, se devuelve esta faceta. Solo lectura. |
| webDavUrl            | Url                                           | Dirección URL compatible con DAV del elemento.  |
| webUrl               | Url                                           | Dirección URL que muestra el recurso en el explorador. Solo lectura. | 

## <a name="remarks"></a>Observaciones 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).


<!-- {
  "type": "#page.annotation",
  "description": "remoteItem resource type provides a link to an item in another drive.",
  "keywords": "remoteitem symlink remote drive shared with me add to onedrive",
  "section": "documentation"
} -->