---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Permiso
localization_priority: Normal
ms.openlocfilehash: 34798437f1bf27c68c390b0f04618985de5cecf3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843319"
---
# <a name="permission-resource-type"></a>tipo de recurso de permiso

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso de **permiso** proporciona información sobre un uso compartido concedido permiso para un recurso [driveItem](driveitem.md) .

Los permisos de uso compartido tienen varias formas diferentes.
El recurso de **permiso** representa estos formularios diferentes a través de facetas en el recurso.

>**Nota:** OneDrive para las bibliotecas de documentos empresariales y de SharePoint no devuelven la propiedad **inheritedFrom** .

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "link",
    "grantedTo",
    "grantedToIdentities",
    "invitation",
    "inheritedFrom",
    "shareId",
    "expirationDateTime",
    "hasPassword"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.permission"
}-->

```json
{
  "id": "string (identifier)",
  "grantedTo": {"@odata.type": "microsoft.graph.identitySet"},
  "grantedToIdentities": [{"@odata.type": "microsoft.graph.identitySet"}],
  "inheritedFrom": {"@odata.type": "microsoft.graph.itemReference"},
  "invitation": {"@odata.type": "microsoft.graph.sharingInvitation"},
  "link": {"@odata.type": "microsoft.graph.sharingLink"},
  "roles": ["string"],
  "shareId": "string",
  "expirationDateTime": "string (timestamp)",
  "hasPassword": "boolean"
}
```

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo                        | Descripción
|:--------------------|:----------------------------|:-------------------------
| id                  | String                      | El identificador único del permiso entre todos los permisos del elemento. Solo lectura.
| grantedTo           | [IdentitySet][]             | Para los permisos de tipo de usuario, los detalles de los usuarios y aplicaciones para este permiso. Solo lectura.
| grantedToIdentities | Colección ([IdentitySet][]) | Para los permisos de tipo de vínculo, los detalles de los usuarios a quienes se ha concedido permiso. Solo lectura.
| invitation          | [SharingInvitation][]       | Detalles de cualquier invitación para uso compartido asociada de este permiso. Solo lectura.
| inheritedFrom       | [ItemReference][]           | Proporciona una referencia al antecesor del permiso actual, si se ha heredado de un antecesor. Solo lectura.
| vincular                | [SharingLink][]             | Proporciona los detalles del vínculo del permiso actual, si es un permiso de tipo de vínculo. Solo lectura.
| roles               | Collection(String)          | El tipo de permiso, p. ej., `read`. Más adelante encontrará una lista completa de roles. Solo lectura.
| shareId             | Cadena                      | Un token único que se puede usar para tener acceso a este elemento compartido a través de la **[API de comparte][]**. Solo lectura.
| expirationDateTime  | DateTimeOffset              | Un formato aaaa-MM-ddTHH de DateTimeOffset indica la hora de caducidad del permiso. DateTime.MinValue indica que hay no se establece expiración de este permiso. Opcional.
| hasPassword         | Booleano                     | Esto indica si se establece la contraseña de este permiso, sólo se muestra en la respuesta. Opcional y de sólo lectura y para OneDrive Personal sólo.

### <a name="roles-enumeration-values"></a>Valores de roles (enumeración)

| Valor        | Detalles                                                                        |
|:------------|:-------------------------------------------------------------------------------|
| `read`      | Proporciona la capacidad de leer los metadatos y el contenido del elemento.            |
| `write`     | Proporciona la capacidad de leer y modificar los metadatos y el contenido del elemento. |
| `sp.owner`  | Para SharePoint y OneDrive para la Empresa, representa el rol de propietario.       |
| `sp.member` | Para SharePoint y OneDrive para la Empresa, representa el rol de miembro.      |

El recurso de permiso usa _facetas_ para proporcionar información sobre el tipo de permiso que representa el recurso.

Para compartir vínculos contienen un token único necesario para obtener acceso al elemento.

Los permisos con una faceta [**invitation**][SharingInvitation] representan los permisos agregados al invitar a usuarios o grupos específicos para que tengan acceso al archivo.

## <a name="sharing-links"></a>Vínculos para compartir

Permisos con un representan de faceta de [**vínculo**][SharingLink] vínculos creados en el elemento de uso compartido.
Estos son los tipos más comunes de permisos.
Uso compartidos vínculos proporciona una dirección URL única que se puede usar para tener acceso a un archivo o carpeta.
Se puede configurar para conceder acceso en una variedad de formas.
Por ejemplo, puede usar la API [createLink][] para crear un vínculo que funciona para cualquier persona que ha iniciado sesión en su organización, o puede crear un vínculo que funciona para cualquier persona, sin necesidad de iniciar sesión.
Puede usar el [Invitar a][] API para crear un vínculo que funciona sólo para usuarios específicos, si están en su compañía o no.

Estos son algunos ejemplos de uso compartido de vínculos.

### <a name="view-link"></a>Vínculo de la vista

Este vínculo de la vista proporciona acceso de solo lectura a todas las personas con el vínculo.

<!-- {"blockType": "example", "@odata.type": "microsoft.graph.permission", "name": "permission-view-link" } -->

```json
{
  "id": "1",
  "roles": ["read"],
  "link": {
    "scope": "anonymous",
    "type": "view",
    "webUrl": "https://onedrive.live.com/redir?resid=5D33DD65C6932946!70859&authkey=!AL7N1QAfSWcjNU8&ithint=folder%2cgif",
    "application": { "id": "1234", "displayName": "Sample Application" }
  },
  "shareId": "!LKj1lkdlals90j1nlkascl",
  "expirationDateTime": "0001-01-01T00:00:00Z"
}
```

### <a name="edit-link"></a>Vínculo de edición

Este vínculo Editar proporciona acceso de lectura y escritura a cualquier persona de la organización con el vínculo.

<!-- {"blockType": "example", "@odata.type": "microsoft.graph.permission", "name": "permission-edit-link" } -->

```json
{
  "id": "2ceefb3g32hh",
  "roles": ["write"],
  "link": {
    "scope": "organization",
    "type": "edit",
    "webUrl": "https://contoso.sharepoint.com/:w:/t/design/fj277ghautbb422707565gnvg23",
    "application": { "id": "1234", "displayName": "Sample Application" }
  },
  "shareId": "!LKj1lkdlals90j1nlkascl",
  "expirationDateTime": "0001-01-01T00:00:00Z"
}
```

### <a name="specific-people-link"></a>Vínculo de personas específicas

Este vínculo proporciona acceso de lectura y escritura a las personas específicas en el `grantedToIdentities` colección.

<!-- {"blockType": "example", "@odata.type": "microsoft.graph.permission", "name": "permission-people-link" } -->

```json
{
  "id": "3",
  "grantedToIdentities": [
    {
       "user": {
        "id": "35fij1974gb8832",
        "displayName": "Misty Suarez"
      }
    },
    {
       "user": {
        "id": "9397721fh4hgh73",
        "displayName": "Judith Clemons"
      }
    }
  ],
  "roles": ["write"],
  "link": {
    "webUrl": "https://contoso.sharepoint.com/:w:/t/design/a577ghg9hgh737613bmbjf839026561fmzhsr85ng9f3hjck2t5s",
    "application": { "id": "1234", "displayName": "Sample Application" }
  },
  "shareId": "!LKj1lkdlals90j1nlkascl",
  "expirationDateTime": "0001-01-01T00:00:00Z"
}
```

## <a name="sharing-invitations"></a>Uso compartido de invitaciones

Los permisos que se envió el [Invitar a][] API pueden tener información adicional en el aspecto de[SharingInvitation] de [invitación].
Si se ha enviado una invitación a una dirección de correo electrónico que no coincide con una cuenta conocida, la propiedad **grantedTo** no puede establecerse hasta que se presentan la invitación, que se produce la primera vez que el usuario hace clic en el vínculo e inicia sesión.

<!-- {"blockType": "example", "@odata.type": "microsoft.graph.permission", "name": "permission-invite-email" } -->

```json
{
  "id": "1",
  "roles": ["write"],
  "invitation": {
    "email": "jd@fabrikam.com",
    "signInRequired": true
  },
  "shareId": "FWxc1lasfdbEAGM5fI7B67aB5ZMPDMmQ11U",
  "expirationDateTime": "0001-01-01T00:00:00Z"
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
    "email": "jd@fabrikam.com",
    "signInRequired": true
  },
  "shareId": "FWxc1lasfdbEAGM5fI7B67aB5ZMPDMmQ11U",
  "expirationDateTime": "0001-01-01T00:00:00Z"
}
```

## <a name="methods"></a>Métodos

| Método                                                   | Ruta de acceso a REST
|:---------------------------------------------------------|:-----------------------
| [Enumerar permisos](../api/driveitem-list-permissions.md) | `GET /drive/items/{item-id}/permissions`
| [Obtener permiso](../api/permission-get.md)               | `GET /drive/items/{item-id}/permissions/{id}`
| [Crear vínculo] [createLink]                                | `POST /drive/items/{item-id}/createLink`
| [Invitar a personas] [Invitar a]                                  | `POST /drive/items/{item-id}/invite`
| [Actualizar](../api/permission-update.md)                    | `PATCH /drive/items/{item-id}/permissions/{id}`
| [Eliminar](../api/permission-delete.md)                    | `DELETE /drive/items/{item-id}/permissions/{id}`



[createLink]: ../api/driveitem-createlink.md
[IdentitySet]: identityset.md
[invitar a]: ../api/driveitem-invite.md
[ItemReference]: itemreference.md
[API de recursos compartidos]: ../api/shares-get.md
[SharingInvitation]: sharinginvitation.md
[SharingLink]: sharinglink.md

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The permission object provides information about permissions and roles and sharing information.",
  "keywords": "sharing,permissions,read,write,acl",
  "section": "documentation",
  "tocPath": "Resources/Permission"
} -->
