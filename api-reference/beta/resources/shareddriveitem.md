# <a name="shareddriveitem-resource-type"></a>Tipo de recurso SharedDriveItem

El recurso **sharedDriveItem** se devuelve al usar la API [Shares](../api/shares_get.md) para obtener acceso a un objeto [driveItem](driveitem.md) compartido.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **sharedDriveItem**.

El recurso **sharedDriveItem** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.

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

    /* relationships*/
    "items": [ { "@odata.type": "microsoft.graph.driveItem" }],
    "root": { "@odata.type": "microsoft.graph.driveItem" },
    "driveItem": { "@odata.type": "microsoft.graph.driveItem" },
    "site": { "@odata.type": "microsoft.graph.site" }
}
```

## <a name="properties"></a>Propiedades

| Propiedad | Tipo                          | Descripción                                                      |
| :------- | :---------------------------- | :--------------------------------------------------------------- |
| id       | String                        | El identificador único del recurso compartido al que se accede.              |
| name     | String                        | El nombre para mostrar del elemento compartido.                             |
| owner    | [IdentitySet](identityset.md) | Información sobre el propietario del elemento compartido al que se hace referencia. |

## <a name="relationships"></a>Relaciones

| Relación | Tipo                                  | Descripción                                                                                                                                                                                                |
| :----------- | :------------------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| elementos        | Collection([DriveItem](driveitem.md)) | Una colección de recursos **driveItem** compartidos. Esta colección no se puede enumerar, pero se puede acceder a los elementos mediante su identificador único.                                                                        |
| root         | [DriveItem](driveitem.md)             | El objeto **driveItem** compartido de nivel superior. Si se comparte un único archivo, este elemento es el archivo. Si se comparte una carpeta, este elemento será la carpeta. Puede usar las facetas del elemento para determinar qué caso se aplica. |
| driveItem    | [driveItem](driveitem.md)             | Un objeto **driveItem** para el recurso que se ha compartido.  Es idéntico a la propiedad **root**.                                                                                                             |
| site         | [site](site.md)                       | Un recurso **site** que contiene el elemento que se ha compartido.                                                                                                                                                |

## <a name="methods"></a>Métodos

| Método                                  | Ruta de acceso a REST                |
| :-------------------------------------- | :----------------------- |
| [Obtener el elemento compartido](../api/shares_get.md) | `GET /shares/{share-id}` |

## <a name="remarks"></a>Observaciones

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