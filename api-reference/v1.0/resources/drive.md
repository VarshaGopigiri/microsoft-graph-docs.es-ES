# <a name="drive-resource-type"></a>Tipo de recurso Drive

El recurso de unidad es el objeto de nivel superior que representa el OneDrive de un usuario o una biblioteca de documentos de SharePoint.

Los usuarios de OneDrive siempre tendrán al menos una unidad disponible, la unidad predeterminada. Es posible que los usuarios sin licencia de OneDrive no tengan una unidad predeterminada disponible.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "items", "root", "special" ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.drive"
}-->
```json
{
  "id": "string (identifier)",
  "driveType": "string",
  "owner": {"@odata.type": "microsoft.graph.identitySet"},
  "quota": {"@odata.type": "microsoft.graph.quota"},
  "root": {"@odata.type": "microsoft.graph.driveItem" },
  "items": [ {"@odata.type": "microsoft.graph.driveItem" }],
  "special": [ {"@odata.type": "microsoft.graph.driveItem" }]
}
```

## <a name="properties"></a>Propiedades

| Propiedad  | Tipo                          | Descripción                                                                                          |
|:----------|:------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| id        | String                        | El identificador único de la unidad. Solo lectura.                                                                                                           |
| driveType | String                        | Describe el tipo de unidad que representa este recurso. Las unidades personales de OneDrive devolverán `personal`. OneDrive para la Empresa devolverá `business`. Las bibliotecas de documentos de SharePoint devolverán `documentLibrary`. Solo lectura. |
| owner     | [identitySet](identityset.md) | Opcional. La cuenta de usuario propietaria de la unidad.                                                                                                                    |
| cuota     | [quota](quota.md)             | Opcional. Información sobre la cuota de espacio de almacenamiento de la unidad.                                                                                                       |

## <a name="relationships"></a>Relaciones

| Relación | Tipo |Descripción |
|:--------|:---------------------------|:-------------------------------------------------------------------------|
| items   | Colección [driveitem](driveitem.md) | Todos los elementos contenidos en la unidad. Solo lectura. Admite valores NULL.                   |
| root    | [driveitem](driveitem.md)            | La carpeta raíz de la unidad. Solo lectura.                                 |
| special | Colección [driveitem](driveitem.md) | Colección de carpetas comunes disponibles en OneDrive. Solo lectura. Admite valores NULL. |


## <a name="methods"></a>Métodos

Los métodos siguientes están disponibles para los recursos de la unidad.

| Método                                                    | Ruta de acceso a REST                            | 
|:----------------------------------------------------------|:-------------------------------------|
| [Obtener unidad predeterminado del usuario](../api/drive_get.md)           | `GET /me/drive`                      |
| [Obtener unidad de otro usuario](../api/drive_get.md)           | `GET /users/{user-id}/drive`         |
| [Obtener la carpeta raíz de una unidad](../api/item_get.md)         | `GET /drives/{drive-id}/root`        |
| [Enumerar elementos en una unidad](../api/item_list_children.md)     | `GET /me/drive/root/children`        |
| [Enumerar cambios en una unidad](../api/item_delta.md)           | `GET /me/drive/root/delta`           |
| [Buscar elementos en una unidad](../api/item_search.md)          | `GET /me/drive/search(q='text')`     |




<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "drive resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Drive"
}-->
