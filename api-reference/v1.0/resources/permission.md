---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Permiso
ms.openlocfilehash: 9f73684d51ab4cee047219e142f72edf778cb171
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="permission-resource-type"></a>Tipo de recurso Permission

El recurso **Permission** proporciona información sobre un permiso de uso compartido concedido para un recurso [DriveItem](driveitem.md).

Los permisos de uso compartido tienen varias formas diferentes.
El recurso **Permission** representa estas formas diferentes a través de facetas en el recurso.

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

| Propiedad      | Tipo                                      | Descripción
|:--------------|:------------------------------------------|:-----------------
| id            | String                                    | El identificador único del permiso entre todos los permisos del elemento. Solo lectura.
| grantedTo     | [IdentitySet](identityset.md)             | Para los permisos de tipo de usuario, los detalles de los usuarios y aplicaciones para este permiso. Solo lectura.
| invitation    | [SharingInvitation][]                     | Detalles de cualquier invitación para uso compartido asociada de este permiso. Solo lectura.
| inheritedFrom | [ItemReference](itemreference.md)         | Proporciona una referencia al antecesor del permiso actual, si se ha heredado de un antecesor. Solo lectura.
| link          | [SharingLink][]                           | Proporciona los detalles del vínculo del permiso actual, si es un permiso de tipo de vínculo. Solo lectura.
| role          | Colección de String.                      | El tipo de permiso, p. ej., `read`. Más adelante encontrará una lista completa de roles. Solo lectura.
| shareId       | Cadena                                    | Token único que se puede utilizar para tener acceso a este elemento compartido a través de la [API **shares**](../api/shares_get.md). Solo lectura.

El recurso de permiso usa _facetas_ para proporcionar información sobre el tipo de permiso que representa el recurso.

Los permisos con una faceta [**link**][SharingLink] representan vínculos para compartir creados en el elemento. Los vínculos para compartir contienen un token único que proporciona acceso al elemento a cualquier usuario con el vínculo.

Los permisos con una faceta [**invitation**][SharingInvitation] representan los permisos agregados al invitar a usuarios o grupos específicos para que tengan acceso al archivo.

[SharingInvitation]: sharinginvitation.md
[SharingLink]: sharinglink.md

## <a name="roles-enumeration"></a>Enumeración de roles

| Rol        | Detalles                                                                        |
|:------------|:-------------------------------------------------------------------------------|
| `read`      | Proporciona la capacidad de leer los metadatos y el contenido del elemento.            |
| `write`     | Proporciona la capacidad de leer y modificar los metadatos y el contenido del elemento. |
| `sp.owner`  | Para SharePoint y OneDrive para la Empresa, representa el rol de propietario.       |
| `sp.member` | Para SharePoint y OneDrive para la Empresa, representa el rol de miembro.      |

## <a name="sharing-links"></a>Vínculos para compartir
El tipo de permisos más común son los vínculos para compartir.
Los vínculos para compartir proporcionan una dirección URL única que incluye el recurso que se va a compartir y un token de autenticación que proporciona acceso al recurso. Los usuarios no necesitan iniciar sesión para tener acceso al contenido compartido con un vínculo para compartir. Los usuarios pueden compartir un vínculo que proporcione acceso de solo lectura al contenido o acceso de escritura al contenido.

### <a name="view-link"></a>Vínculo de visualización
Un vínculo de visualización proporciona acceso de solo lectura a un elemento.

<!-- {"blockType": "example", "@odata.type": "microsoft.graph.permission", "name": "permission-view-link" } -->
```json
{
  "id": "1",
  "roles": ["read"],
  "link": {
    "type": "view",
    "webUrl": "https://onedrive.live.com/redir?resid=5D33DD65C6932946!70859&authkey=!AL7N1QAfSWcjNU8&ithint=folder%2cgif",
    "application": { "id": "1234", "displayName": "Sample Application" }
  },
  "shareId": "!LKj1lkdlals90j1nlkascl"
}
```

### <a name="edit-link"></a>Vínculo de edición
Un vínculo de edición proporciona acceso de lectura y escritura a un elemento.

<!-- {"blockType": "example", "@odata.type": "microsoft.graph.permission", "name": "permission-edit-link" } -->
```json
{
  "id": "2",
  "roles": ["write"],
  "link": {
    "type": "edit",
    "webUrl": "https://onedrive.live.com/redir?resid=5D33DD65C6932946!70859&authkey=!AL7N1QAfSWcjNU8&ithint=folder%2cgif",
    "application": { "id": "1234", "displayName": "Sample Application" }
  },
  "shareId": "!LKj1lkdlals90j1nlkascl"
}
```

### <a name="sharing-invitation"></a>Invitación para uso compartido
Además de crear vínculos para compartir, un usuario puede ser invitado por una dirección de correo electrónico.
En este escenario, el permiso crea una invitación que se envía al correo electrónico del usuario.

#### <a name="invitation-to-an-email-address"></a>Invitación a una dirección de correo electrónico
Si el permiso se ha enviado mediante una dirección de correo electrónico a un destinatario que no tiene una cuenta coincidente, la propiedad **grantedTo** puede no establecerse hasta que la invitación se canjee, lo que se produce la primera vez que un usuario hace clic en el vínculo e inicia sesión.

<!-- {"blockType": "example", "@odata.type": "microsoft.graph.permission", "name": "permission-invite-email" } -->
```json
{
  "id": "1",
  "roles": ["write"],
  "invitation": {
    "email": "jd@gmail.com",
    "signInRequired": true
  },
  "shareId": "FWxc1lasfdbEAGM5fI7B67aB5ZMPDMmQ11U"
}
```

Después de que la invitación de uso compartido se ha canjeado por un usuario, la propiedad **grantedTo** contendrá la información sobre la cuenta que canjea los permisos:

<!-- {"blockType": "example", "@odata.type": "microsoft.graph.permission", "name": "permission-invite-redeemed" } -->
```json
{
  "id": "1",
  "roles": ["write"],
  "grantedTo": {
    "user": {
      "id": "5D33DD65C6932946",
      "displayName": "John Doe"
    }
  },
  "invitation": {
    "email": "jd@outlook.com",
    "signInRequired": true
  },
  "shareId": "FWxc1lasfdbEAGM5fI7B67aB5ZMPDMmQ11U"
}
```

## <a name="methods"></a>Métodos

| Método                                                   | Ruta de acceso a REST
|:---------------------------------------------------------|:-----------------------
| [Enumerar permisos](../api/driveitem_list_permissions.md) | `GET /drive/items/{item-id}/permissions`
| [Obtener permiso](../api/permission_get.md)               | `GET /drive/items/{item-id}/permissions/{id}`
| [Agregar](../api/driveitem_invite.md)                        | `POST /drive/items/{item-id}/invite`
| [Actualizar](../api/permission_update.md)                    | `PATCH /drive/items/{item-id}/permissions/{id}`
| [Eliminar](../api/permission_delete.md)                    | `DELETE /drive/items/{item-id}/permissions/{id}`


## <a name="remarks"></a>Comentarios

Las bibliotecas de documentos de OneDrive para la Empresa y SharePoint no devuelven la propiedad **inheritedFrom**.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The permission object provides information about permissions and roles and sharing information.",
  "keywords": "sharing,permissions,read,write,acl",
  "section": "documentation",
  "tocPath": "Resources/Permission"
} -->
