# <a name="shareddriveitem-resource-type"></a>Tipo de recurso de SharedDriveItem

El recurso **SharedDriveItem** se devuelve al usar la API [Shares](../api/shares_get.md) para acceder a un objeto [DriveItem](driveitem.md) compartido. Este recurso es similar a un recurso [Drive](drive.md), pero el ámbito solo se aplica a los objetos DriveItem a los que se puede acceder al compartir el vínculo o shareId.

### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.sharedDriveItem"
}-->
```json
{
    "id": "string",
    "name": "string",
    "owner": { "@odata.type": "microsoft.graph.identitySet" },
    "items": [ { "@odata.type": "microsoft.graph.driveItem" }],
    "root": { "@odata.type": "microsoft.graph.driveItem" }
}
```

### <a name="properties"></a>Propiedades

| Propiedad  | Tipo                                  | Descripción                                                          |
|:----------|:--------------------------------------|:---------------------------------------------------------------------|
| id        | String                                | El identificador único del recurso compartido al que se accede.                  |
| name      | String                                | El nombre para mostrar del elemento compartido.                                 |
| owner     | [IdentitySet](identityset.md)         | Información sobre el propietario del elemento compartido al que se hace referencia.     |
| items     | Collection([DriveItem](driveitem.md)) | Una colección de recursos DriveItem compartidos. Esta colección no se puede enumerar, pero se puede acceder a los elementos mediante su identificador único. |
| root      | [DriveItem](driveitem.md)             | El objeto DriveItem compartido de nivel superior. Si se comparte un único archivo, este elemento es el archivo. Si se comparte una carpeta, este elemento será la carpeta. Puede usar las facetas del elemento para determinar qué caso se aplica. |

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sharepointIds resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->