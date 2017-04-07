# <a name="permission-resource-type"></a>Tipo de recurso Permission

El recurso **Permission** proporciona información sobre un permiso concedido para un recurso [DriveItem](driveitem.md).

Los permisos tienen varias formas diferentes. El recurso **Permission** representa estas formas diferentes a través de facetas en el recurso.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "link", "grantedTo", "invitation", "inheritedFrom", "shareId" ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.permission"
}-->
```json
{
  "id": "string (identifier)",
  "grantedTo": {"@odata.type": "microsoft.graph.identitySet"},
  "inheritedFrom": {"@odata.type": "microsoft.graph.itemReference"},
  "invitation": {"@odata.type": "microsoft.graph.sharingInvitation"},
  "link": {"@odata.type": "microsoft.graph.sharingLink"},
  "roles": ["string"],
  "shareId": "string"
}
```

## <a name="properties"></a>Propiedades

| Propiedad      | Tipo                                      | Descripción                                                                                                                           |
|:--------------|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| id            | String                                    | El identificador único del permiso entre todos los permisos del elemento. Solo lectura.                                                 |
| grantedTo     | [IdentitySet](identityset.md)             | Para los permisos de tipo de usuario, los detalles de los usuarios y aplicaciones para este permiso. Solo lectura.                                    |
| invitation    | [SharingInvitation](sharinginvitation.md) | Detalles de cualquier invitación para uso compartido asociada de este permiso. Solo lectura.                                                          |
| inheritedFrom | [ItemReference](itemreference.md)         | Proporciona una referencia al antecesor del permiso actual, si se ha heredado de un antecesor. Solo lectura.                       |
| vincular          | [SharingLink](sharinglink.md)             | Proporciona los detalles del vínculo del permiso actual, si es un permiso de tipo de vínculo. Solo lectura.                                     |
| role          | Colección de String.                      | El tipo de permiso, p. ej., `read`. Más adelante encontrará una lista completa de roles. Solo lectura.                                                 |
| shareId       | String                                    | Un token único para este permiso. Solo lectura. |

El recurso [Permission](../resources/permission.md) usa _facetas_ para proporcionar información sobre el tipo de permiso que representa el recurso.

Los permisos con una faceta [**link**](sharinglink.md) representan vínculos para compartir creados en el elemento. Los vínculos para compartir contienen un token único que proporciona acceso al elemento a cualquier usuario con el vínculo.

Los permisos con una faceta [**invitation**](sharinginvitation.md) representan los permisos agregados al invitar a usuarios o grupos específicos para que tengan acceso al archivo.

## <a name="roles-enumeration"></a>Enumeración de roles

| Rol  | Detalles                                                                        |
|:------|:-------------------------------------------------------------------------------|
| `read`  | Proporciona la capacidad de leer los metadatos y el contenido del elemento.            |
| `write` | Proporciona la capacidad de leer y modificar los metadatos y el contenido del elemento. |

## <a name="methods"></a>Métodos

| Método                                              | Ruta de acceso a REST                            |
|:----------------------------------------------------|:---------------------------------------|
| [Enumerar permisos](../api/item_list_permissions.md) | `GET /drive/items/{item-id}/permissions`  |
| [Obtener permiso](../api/permission_get.md)          | `GET /drive/items/{item-id}/permissions/{id}` |
| [Agregar](../api/item_invite.md)                        | `POST /drive/items/{item-id}/invite` |
| [Actualizar](../api/permission_update.md)               | `PATH /drive/items/{item-id}/permissions/{id}` |
| [Eliminar](../api/permission_delete.md)               | `DELETE /drive/items/{item-id}/permissions/{id}` |


## <a name="remarks"></a>Comentarios

Las bibliotecas de documentos de OneDrive para la Empresa y SharePoint no devuelven la propiedad **inheritedFrom**.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "permission resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
