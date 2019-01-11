---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Permiso
localization_priority: Priority
ms.openlocfilehash: 988a4d6dcd1b04b34c5d2d03aca404b0a570922f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834170"
---
# <a name="permission-resource-type"></a><span data-ttu-id="530eb-102">Tipo de recurso Permission</span><span class="sxs-lookup"><span data-stu-id="530eb-102">Permission resource type</span></span>

<span data-ttu-id="530eb-103">El recurso **Permission** proporciona información sobre un permiso de uso compartido concedido para un recurso [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="530eb-103">The **Permission** resource provides information about a sharing permission granted for a [DriveItem](driveitem.md) resource.</span></span>

<span data-ttu-id="530eb-104">Los permisos de uso compartido tienen varias formas diferentes.</span><span class="sxs-lookup"><span data-stu-id="530eb-104">Sharing permissions have a number of different forms.</span></span>
<span data-ttu-id="530eb-105">El recurso **Permission** representa estas formas diferentes a través de facetas en el recurso.</span><span class="sxs-lookup"><span data-stu-id="530eb-105">The **Permission** resource represents these different forms through facets on the resource.</span></span>

## <a name="json-representation"></a><span data-ttu-id="530eb-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="530eb-106">JSON representation</span></span>

<span data-ttu-id="530eb-107">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="530eb-107">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "link",
    "grantedTo",
    "invitation",
    "inheritedFrom",
    "shareId"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
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

## <a name="properties"></a><span data-ttu-id="530eb-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="530eb-108">Properties</span></span>

| <span data-ttu-id="530eb-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="530eb-109">Property</span></span>      | <span data-ttu-id="530eb-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="530eb-110">Type</span></span>                                      | <span data-ttu-id="530eb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="530eb-111">Description</span></span>
|:--------------|:------------------------------------------|:-----------------
| <span data-ttu-id="530eb-112">id</span><span class="sxs-lookup"><span data-stu-id="530eb-112">id</span></span>            | <span data-ttu-id="530eb-113">String</span><span class="sxs-lookup"><span data-stu-id="530eb-113">String</span></span>                                    | <span data-ttu-id="530eb-p102">El identificador único del permiso entre todos los permisos del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="530eb-p102">The unique identifier of the permission among all permissions on the item. Read-only.</span></span>
| <span data-ttu-id="530eb-116">grantedTo</span><span class="sxs-lookup"><span data-stu-id="530eb-116">grantedTo</span></span>     | [<span data-ttu-id="530eb-117">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="530eb-117">IdentitySet</span></span>](identityset.md)             | <span data-ttu-id="530eb-p103">Para los permisos de tipo de usuario, los detalles de los usuarios y aplicaciones para este permiso. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="530eb-p103">For user type permissions, the details of the users & applications for this permission. Read-only.</span></span>
| <span data-ttu-id="530eb-120">invitation</span><span class="sxs-lookup"><span data-stu-id="530eb-120">invitation</span></span>    | <span data-ttu-id="530eb-121">[SharingInvitation][]</span><span class="sxs-lookup"><span data-stu-id="530eb-121">[SharingInvitation][]</span></span>                     | <span data-ttu-id="530eb-p104">Detalles de cualquier invitación para uso compartido asociada de este permiso. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="530eb-p104">Details of any associated sharing invitation for this permission. Read-only.</span></span>
| <span data-ttu-id="530eb-124">inheritedFrom</span><span class="sxs-lookup"><span data-stu-id="530eb-124">inheritedFrom</span></span> | [<span data-ttu-id="530eb-125">ItemReference</span><span class="sxs-lookup"><span data-stu-id="530eb-125">ItemReference</span></span>](itemreference.md)         | <span data-ttu-id="530eb-p105">Proporciona una referencia al antecesor del permiso actual, si se ha heredado de un antecesor. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="530eb-p105">Provides a reference to the ancestor of the current permission, if it is inherited from an ancestor. Read-only.</span></span>
| <span data-ttu-id="530eb-128">vincular</span><span class="sxs-lookup"><span data-stu-id="530eb-128">link</span></span>          | <span data-ttu-id="530eb-129">[SharingLink][]</span><span class="sxs-lookup"><span data-stu-id="530eb-129">[SharingLink][]</span></span>                           | <span data-ttu-id="530eb-p106">Proporciona los detalles del vínculo del permiso actual, si es un permiso de tipo de vínculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="530eb-p106">Provides the link details of the current permission, if it is a link type permissions. Read-only.</span></span>
| <span data-ttu-id="530eb-132">roles</span><span class="sxs-lookup"><span data-stu-id="530eb-132">roles</span></span>         | <span data-ttu-id="530eb-133">Colección de String.</span><span class="sxs-lookup"><span data-stu-id="530eb-133">Collection of String</span></span>                      | <span data-ttu-id="530eb-p107">El tipo de permiso, p. ej., `read`. Más adelante encontrará una lista completa de roles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="530eb-p107">The type of permission, e.g. `read`. See below for the full list of roles. Read-only.</span></span>
| <span data-ttu-id="530eb-137">shareId</span><span class="sxs-lookup"><span data-stu-id="530eb-137">shareId</span></span>       | <span data-ttu-id="530eb-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="530eb-138">String</span></span>                                    | <span data-ttu-id="530eb-p108">Token único que se puede utilizar para tener acceso a este elemento compartido a través de la [API **shares**](../api/shares-get.md). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="530eb-p108">A unique token that can be used to access this shared item via the [**shares** API](../api/shares-get.md). Read-only.</span></span>

<span data-ttu-id="530eb-141">El recurso de permiso usa _facetas_ para proporcionar información sobre el tipo de permiso que representa el recurso.</span><span class="sxs-lookup"><span data-stu-id="530eb-141">The permission resource uses _facets_ to provide information about the kind of permission represented by the resource.</span></span>

<span data-ttu-id="530eb-p109">Los permisos con una faceta [**link**][SharingLink] representan vínculos para compartir creados en el elemento. Los vínculos para compartir contienen un token único que proporciona acceso al elemento a cualquier usuario con el vínculo.</span><span class="sxs-lookup"><span data-stu-id="530eb-p109">Permissions with a [**link**][SharingLink] facet represent sharing links created on the item. Sharing links contain a unique token that provides access to the item for anyone with the link.</span></span>

<span data-ttu-id="530eb-144">Los permisos con una faceta [**invitation**][SharingInvitation] representan los permisos agregados al invitar a usuarios o grupos específicos para que tengan acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="530eb-144">Permissions with an [**invitation**][SharingInvitation] facet represent permissions added by inviting specific users or groups to have access to the file.</span></span>

[SharingInvitation]: sharinginvitation.md
[SharingLink]: sharinglink.md

## <a name="roles-enumeration"></a><span data-ttu-id="530eb-147">Enumeración de roles</span><span class="sxs-lookup"><span data-stu-id="530eb-147">Roles enumeration</span></span>

| <span data-ttu-id="530eb-148">Rol</span><span class="sxs-lookup"><span data-stu-id="530eb-148">Role</span></span>        | <span data-ttu-id="530eb-149">Detalles</span><span class="sxs-lookup"><span data-stu-id="530eb-149">Details</span></span>                                                                        |
|:------------|:-------------------------------------------------------------------------------|
| `read`      | <span data-ttu-id="530eb-150">Proporciona la capacidad de leer los metadatos y el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="530eb-150">Provides the ability to read the metadata and contents of the item.</span></span>            |
| `write`     | <span data-ttu-id="530eb-151">Proporciona la capacidad de leer y modificar los metadatos y el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="530eb-151">Provides the ability to read and modify the metadata and contents of the item.</span></span> |
| `sp.owner`  | <span data-ttu-id="530eb-152">Para SharePoint y OneDrive para la Empresa, representa el rol de propietario.</span><span class="sxs-lookup"><span data-stu-id="530eb-152">For SharePoint and OneDrive for Business this represents the owner role.</span></span>       |
| `sp.member` | <span data-ttu-id="530eb-153">Para SharePoint y OneDrive para la Empresa, representa el rol de miembro.</span><span class="sxs-lookup"><span data-stu-id="530eb-153">For SharePoint and OneDrive for Business this represents the member role.</span></span>      |

## <a name="sharing-links"></a><span data-ttu-id="530eb-154">Vínculos para compartir</span><span class="sxs-lookup"><span data-stu-id="530eb-154">Sharing links</span></span>
<span data-ttu-id="530eb-155">El tipo de permisos más común son los vínculos para compartir.</span><span class="sxs-lookup"><span data-stu-id="530eb-155">The most common type of permissions are sharing links.</span></span>
<span data-ttu-id="530eb-156">Los vínculos para compartir proporcionan una dirección URL única que incluye el recurso que se va a compartir y un token de autenticación que proporciona acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="530eb-156">Sharing links provide a unique URL that includes both the resource being shared and an authentication token that provides access to the resource.</span></span> <span data-ttu-id="530eb-157">Los usuarios no necesitan iniciar sesión para tener acceso al contenido compartido con un vínculo para compartir.</span><span class="sxs-lookup"><span data-stu-id="530eb-157">Users don't need to sign-in to access the content shared with a sharing link.</span></span> <span data-ttu-id="530eb-158">Los usuarios pueden compartir un vínculo que proporcione acceso de solo lectura al contenido o acceso de escritura al contenido.</span><span class="sxs-lookup"><span data-stu-id="530eb-158">Users can share a link that gives read-only access to the content or writable access to the content.</span></span>

### <a name="view-link"></a><span data-ttu-id="530eb-159">Vínculo de visualización</span><span class="sxs-lookup"><span data-stu-id="530eb-159">View Link</span></span>
<span data-ttu-id="530eb-160">Un vínculo de visualización proporciona acceso de solo lectura a un elemento.</span><span class="sxs-lookup"><span data-stu-id="530eb-160">A view link provides read-only access to an item.</span></span>

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

### <a name="edit-link"></a><span data-ttu-id="530eb-161">Vínculo de edición</span><span class="sxs-lookup"><span data-stu-id="530eb-161">Edit link</span></span>
<span data-ttu-id="530eb-162">Un vínculo de edición proporciona acceso de lectura y escritura a un elemento.</span><span class="sxs-lookup"><span data-stu-id="530eb-162">An edit link provides read and write access to an item.</span></span>

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

### <a name="sharing-invitation"></a><span data-ttu-id="530eb-163">Invitación para uso compartido</span><span class="sxs-lookup"><span data-stu-id="530eb-163">Sharing Invitation</span></span>
<span data-ttu-id="530eb-164">Además de crear vínculos para compartir, un usuario puede ser invitado por una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="530eb-164">In addition to creating sharing links, a user can be invited by e-mail address.</span></span>
<span data-ttu-id="530eb-165">En este escenario, el permiso crea una invitación que se envía al correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="530eb-165">In this scenario the permission creates an invitation that is sent to the user's email.</span></span>

#### <a name="invitation-to-an-email-address"></a><span data-ttu-id="530eb-166">Invitación a una dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="530eb-166">Invitation to an email address</span></span>
<span data-ttu-id="530eb-167">Si el permiso se ha enviado mediante una dirección de correo electrónico a un destinatario que no tiene una cuenta coincidente, la propiedad **grantedTo** puede no establecerse hasta que la invitación se canjee, lo que se produce la primera vez que un usuario hace clic en el vínculo e inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="530eb-167">If the permission was sent via an email address to a recipient who does not have a matching account, the **grantedTo** property may not be set until the invitation is redeemed, which occurs the first time a user clicks the link and signs in.</span></span>

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

<span data-ttu-id="530eb-168">Después de que la invitación de uso compartido se ha canjeado por un usuario, la propiedad **grantedTo** contendrá la información sobre la cuenta que canjea los permisos:</span><span class="sxs-lookup"><span data-stu-id="530eb-168">After the sharing invitation has been redeemed by a user, the **grantedTo** property will contain the information about the account that redeemed the permissions:</span></span>

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

## <a name="methods"></a><span data-ttu-id="530eb-169">Métodos</span><span class="sxs-lookup"><span data-stu-id="530eb-169">Methods</span></span>

| <span data-ttu-id="530eb-170">Método</span><span class="sxs-lookup"><span data-stu-id="530eb-170">Method</span></span>                                                   | <span data-ttu-id="530eb-171">Ruta de acceso a REST</span><span class="sxs-lookup"><span data-stu-id="530eb-171">REST Path</span></span>
|:---------------------------------------------------------|:-----------------------
| [<span data-ttu-id="530eb-172">Enumerar permisos</span><span class="sxs-lookup"><span data-stu-id="530eb-172">List permissions</span></span>](../api/driveitem-list-permissions.md) | `GET /drive/items/{item-id}/permissions`
| [<span data-ttu-id="530eb-173">Obtener permiso</span><span class="sxs-lookup"><span data-stu-id="530eb-173">Get permission</span></span>](../api/permission-get.md)               | `GET /drive/items/{item-id}/permissions/{id}`
| [<span data-ttu-id="530eb-174">Agregar</span><span class="sxs-lookup"><span data-stu-id="530eb-174">Add</span></span>](../api/driveitem-invite.md)                        | `POST /drive/items/{item-id}/invite`
| [<span data-ttu-id="530eb-175">Actualizar</span><span class="sxs-lookup"><span data-stu-id="530eb-175">Update</span></span>](../api/permission-update.md)                    | `PATCH /drive/items/{item-id}/permissions/{id}`
| [<span data-ttu-id="530eb-176">Eliminar</span><span class="sxs-lookup"><span data-stu-id="530eb-176">Delete</span></span>](../api/permission-delete.md)                    | `DELETE /drive/items/{item-id}/permissions/{id}`


## <a name="remarks"></a><span data-ttu-id="530eb-177">Comentarios</span><span class="sxs-lookup"><span data-stu-id="530eb-177">Remarks</span></span>

<span data-ttu-id="530eb-178">Las bibliotecas de documentos de OneDrive para la Empresa y SharePoint no devuelven la propiedad **inheritedFrom**.</span><span class="sxs-lookup"><span data-stu-id="530eb-178">OneDrive for Business and SharePoint document libraries do not return the **inheritedFrom** property.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The permission object provides information about permissions and roles and sharing information.",
  "keywords": "sharing,permissions,read,write,acl",
  "section": "documentation",
  "tocPath": "Resources/Permission"
} -->
