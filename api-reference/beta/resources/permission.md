---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Permiso
ms.openlocfilehash: 195d4840fdb25339eda3858c0bac2395ee9b1c4a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089972"
---
# <a name="permission-resource-type"></a><span data-ttu-id="cc9f1-102">tipo de recurso de permiso</span><span class="sxs-lookup"><span data-stu-id="cc9f1-102">permission resource type</span></span>

> <span data-ttu-id="cc9f1-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cc9f1-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cc9f1-105">El recurso de **permiso** proporciona información sobre un uso compartido concedido permiso para un recurso [driveItem](driveitem.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9f1-105">The **permission** resource provides information about a sharing permission granted for a [driveItem](driveitem.md) resource.</span></span>

<span data-ttu-id="cc9f1-106">Los permisos de uso compartido tienen varias formas diferentes.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-106">Sharing permissions have a number of different forms.</span></span>
<span data-ttu-id="cc9f1-107">El recurso de **permiso** representa estos formularios diferentes a través de facetas en el recurso.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-107">The **permission** resource represents these different forms through facets on the resource.</span></span>

><span data-ttu-id="cc9f1-108">**Nota:** OneDrive para las bibliotecas de documentos empresariales y de SharePoint no devuelven la propiedad **inheritedFrom** .</span><span class="sxs-lookup"><span data-stu-id="cc9f1-108">**Note:** OneDrive for Business and SharePoint document libraries do not return the **inheritedFrom** property.</span></span>

## <a name="json-representation"></a><span data-ttu-id="cc9f1-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cc9f1-109">JSON representation</span></span>

<span data-ttu-id="cc9f1-110">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-110">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="cc9f1-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc9f1-111">Properties</span></span>

| <span data-ttu-id="cc9f1-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cc9f1-112">Property</span></span>            | <span data-ttu-id="cc9f1-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc9f1-113">Type</span></span>                        | <span data-ttu-id="cc9f1-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc9f1-114">Description</span></span>
|:--------------------|:----------------------------|:-------------------------
| <span data-ttu-id="cc9f1-115">id</span><span class="sxs-lookup"><span data-stu-id="cc9f1-115">id</span></span>                  | <span data-ttu-id="cc9f1-116">String</span><span class="sxs-lookup"><span data-stu-id="cc9f1-116">String</span></span>                      | <span data-ttu-id="cc9f1-p103">El identificador único del permiso entre todos los permisos del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-p103">The unique identifier of the permission among all permissions on the item. Read-only.</span></span>
| <span data-ttu-id="cc9f1-119">grantedTo</span><span class="sxs-lookup"><span data-stu-id="cc9f1-119">grantedTo</span></span>           | <span data-ttu-id="cc9f1-120">[IdentitySet][]</span><span class="sxs-lookup"><span data-stu-id="cc9f1-120">[IdentitySet][]</span></span>             | <span data-ttu-id="cc9f1-p104">Para los permisos de tipo de usuario, los detalles de los usuarios y aplicaciones para este permiso. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-p104">For user type permissions, the details of the users & applications for this permission. Read-only.</span></span>
| <span data-ttu-id="cc9f1-123">grantedToIdentities</span><span class="sxs-lookup"><span data-stu-id="cc9f1-123">grantedToIdentities</span></span> | <span data-ttu-id="cc9f1-124">Colección ([IdentitySet][])</span><span class="sxs-lookup"><span data-stu-id="cc9f1-124">Collection([IdentitySet][])</span></span> | <span data-ttu-id="cc9f1-125">Para los permisos de tipo de vínculo, los detalles de los usuarios a quienes se ha concedido permiso.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-125">For link type permissions, the details of the users to whom permission was granted.</span></span> <span data-ttu-id="cc9f1-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-126">Read-only.</span></span>
| <span data-ttu-id="cc9f1-127">invitation</span><span class="sxs-lookup"><span data-stu-id="cc9f1-127">invitation</span></span>          | <span data-ttu-id="cc9f1-128">[SharingInvitation][]</span><span class="sxs-lookup"><span data-stu-id="cc9f1-128">[SharingInvitation][]</span></span>       | <span data-ttu-id="cc9f1-p106">Detalles de cualquier invitación para uso compartido asociada de este permiso. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-p106">Details of any associated sharing invitation for this permission. Read-only.</span></span>
| <span data-ttu-id="cc9f1-131">inheritedFrom</span><span class="sxs-lookup"><span data-stu-id="cc9f1-131">inheritedFrom</span></span>       | <span data-ttu-id="cc9f1-132">[ItemReference][]</span><span class="sxs-lookup"><span data-stu-id="cc9f1-132">[ItemReference][]</span></span>           | <span data-ttu-id="cc9f1-p107">Proporciona una referencia al antecesor del permiso actual, si se ha heredado de un antecesor. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-p107">Provides a reference to the ancestor of the current permission, if it is inherited from an ancestor. Read-only.</span></span>
| <span data-ttu-id="cc9f1-135">vincular</span><span class="sxs-lookup"><span data-stu-id="cc9f1-135">link</span></span>                | <span data-ttu-id="cc9f1-136">[SharingLink][]</span><span class="sxs-lookup"><span data-stu-id="cc9f1-136">[SharingLink][]</span></span>             | <span data-ttu-id="cc9f1-p108">Proporciona los detalles del vínculo del permiso actual, si es un permiso de tipo de vínculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-p108">Provides the link details of the current permission, if it is a link type permissions. Read-only.</span></span>
| <span data-ttu-id="cc9f1-139">roles</span><span class="sxs-lookup"><span data-stu-id="cc9f1-139">roles</span></span>               | <span data-ttu-id="cc9f1-140">Collection(String)</span><span class="sxs-lookup"><span data-stu-id="cc9f1-140">Collection(String)</span></span>          | <span data-ttu-id="cc9f1-p109">El tipo de permiso, p. ej., `read`. Más adelante encontrará una lista completa de roles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-p109">The type of permission, e.g. `read`. See below for the full list of roles. Read-only.</span></span>
| <span data-ttu-id="cc9f1-144">shareId</span><span class="sxs-lookup"><span data-stu-id="cc9f1-144">shareId</span></span>             | <span data-ttu-id="cc9f1-145">String</span><span class="sxs-lookup"><span data-stu-id="cc9f1-145">String</span></span>                      | <span data-ttu-id="cc9f1-146">Un token único que se puede usar para tener acceso a este elemento compartido a través de la **[API de comparte][]**.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-146">A unique token that can be used to access this shared item via the **[shares API][]**.</span></span> <span data-ttu-id="cc9f1-147">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-147">Read-only.</span></span>
| <span data-ttu-id="cc9f1-148">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="cc9f1-148">expirationDateTime</span></span>  | <span data-ttu-id="cc9f1-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cc9f1-149">DateTimeOffset</span></span>              | <span data-ttu-id="cc9f1-150">Un formato aaaa-MM-ddTHH de DateTimeOffset indica la hora de caducidad del permiso.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-150">A format of yyyy-MM-ddTHH:mm:ssZ of DateTimeOffset indicates the expiration time of the permission.</span></span> <span data-ttu-id="cc9f1-151">DateTime.MinValue indica que hay no se establece expiración de este permiso.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-151">DateTime.MinValue indicates there is no expiration set for this permission.</span></span> <span data-ttu-id="cc9f1-152">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-152">Optional.</span></span>
| <span data-ttu-id="cc9f1-153">hasPassword</span><span class="sxs-lookup"><span data-stu-id="cc9f1-153">hasPassword</span></span>         | <span data-ttu-id="cc9f1-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc9f1-154">Boolean</span></span>                     | <span data-ttu-id="cc9f1-155">Esto indica si se establece la contraseña de este permiso, sólo se muestra en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-155">This indicates whether password is set for this permission, it's only showing in response.</span></span> <span data-ttu-id="cc9f1-156">Opcional y de sólo lectura y para OneDrive Personal sólo.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-156">Optional and Read-only and for OneDrive Personal only.</span></span>

### <a name="roles-enumeration-values"></a><span data-ttu-id="cc9f1-157">Valores de roles (enumeración)</span><span class="sxs-lookup"><span data-stu-id="cc9f1-157">Roles enumeration values</span></span>

| <span data-ttu-id="cc9f1-158">Valor</span><span class="sxs-lookup"><span data-stu-id="cc9f1-158">Value</span></span>        | <span data-ttu-id="cc9f1-159">Detalles</span><span class="sxs-lookup"><span data-stu-id="cc9f1-159">Details</span></span>                                                                        |
|:------------|:-------------------------------------------------------------------------------|
| `read`      | <span data-ttu-id="cc9f1-160">Proporciona la capacidad de leer los metadatos y el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-160">Provides the ability to read the metadata and contents of the item.</span></span>            |
| `write`     | <span data-ttu-id="cc9f1-161">Proporciona la capacidad de leer y modificar los metadatos y el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-161">Provides the ability to read and modify the metadata and contents of the item.</span></span> |
| `sp.owner`  | <span data-ttu-id="cc9f1-162">Para SharePoint y OneDrive para la Empresa, representa el rol de propietario.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-162">For SharePoint and OneDrive for Business this represents the owner role.</span></span>       |
| `sp.member` | <span data-ttu-id="cc9f1-163">Para SharePoint y OneDrive para la Empresa, representa el rol de miembro.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-163">For SharePoint and OneDrive for Business this represents the member role.</span></span>      |

<span data-ttu-id="cc9f1-164">El recurso de permiso usa _facetas_ para proporcionar información sobre el tipo de permiso que representa el recurso.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-164">The permission resource uses _facets_ to provide information about the kind of permission represented by the resource.</span></span>

<span data-ttu-id="cc9f1-165">Para compartir vínculos contienen un token único necesario para obtener acceso al elemento.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-165">Sharing links contain a unique token required to access the item.</span></span>

<span data-ttu-id="cc9f1-166">Los permisos con una faceta [**invitation**][SharingInvitation] representan los permisos agregados al invitar a usuarios o grupos específicos para que tengan acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-166">Permissions with an [**invitation**][SharingInvitation] facet represent permissions added by inviting specific users or groups to have access to the file.</span></span>

## <a name="sharing-links"></a><span data-ttu-id="cc9f1-167">Vínculos para compartir</span><span class="sxs-lookup"><span data-stu-id="cc9f1-167">Sharing links</span></span>

<span data-ttu-id="cc9f1-168">Permisos con un representan de faceta de [**vínculo**][SharingLink] vínculos creados en el elemento de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-168">Permissions with a [**link**][SharingLink] facet represent sharing links created on the item.</span></span>
<span data-ttu-id="cc9f1-169">Estos son los tipos más comunes de permisos.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-169">These are the most common kinds of permissions.</span></span>
<span data-ttu-id="cc9f1-170">Uso compartidos vínculos proporciona una dirección URL única que se puede usar para tener acceso a un archivo o carpeta.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-170">Sharing links provide a unique URL that can be used to access a file or folder.</span></span>
<span data-ttu-id="cc9f1-171">Se puede configurar para conceder acceso en una variedad de formas.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-171">They can be set up to grant access in a variety of ways.</span></span>
<span data-ttu-id="cc9f1-172">Por ejemplo, puede usar la API [createLink][] para crear un vínculo que funciona para cualquier persona que ha iniciado sesión en su organización, o puede crear un vínculo que funciona para cualquier persona, sin necesidad de iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-172">For example, you can use the [createLink][] API to create a link that works for anyone signed into your organization, or you can create a link that works for anyone, without needing to sign in.</span></span>
<span data-ttu-id="cc9f1-173">Puede usar el [Invitar a][] API para crear un vínculo que funciona sólo para usuarios específicos, si están en su compañía o no.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-173">You can use the [invite][] API to create a link that only works for specific people, whether they're in your company or not.</span></span>

<span data-ttu-id="cc9f1-174">Estos son algunos ejemplos de uso compartido de vínculos.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-174">Here are some examples of sharing links.</span></span>

### <a name="view-link"></a><span data-ttu-id="cc9f1-175">Vínculo de la vista</span><span class="sxs-lookup"><span data-stu-id="cc9f1-175">View link</span></span>

<span data-ttu-id="cc9f1-176">Este vínculo de la vista proporciona acceso de solo lectura a todas las personas con el vínculo.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-176">This view link provides read-only access to anyone with the link.</span></span>

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

### <a name="edit-link"></a><span data-ttu-id="cc9f1-177">Vínculo de edición</span><span class="sxs-lookup"><span data-stu-id="cc9f1-177">Edit link</span></span>

<span data-ttu-id="cc9f1-178">Este vínculo Editar proporciona acceso de lectura y escritura a cualquier persona de la organización con el vínculo.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-178">This edit link provides read and write access to anyone in the organization with the link.</span></span>

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

### <a name="specific-people-link"></a><span data-ttu-id="cc9f1-179">Vínculo de personas específicas</span><span class="sxs-lookup"><span data-stu-id="cc9f1-179">Specific people link</span></span>

<span data-ttu-id="cc9f1-180">Este vínculo proporciona acceso de lectura y escritura a las personas específicas en el `grantedToIdentities` colección.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-180">This link provides read and write access to the specific people in the `grantedToIdentities` collection.</span></span>

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

## <a name="sharing-invitations"></a><span data-ttu-id="cc9f1-181">Uso compartido de invitaciones</span><span class="sxs-lookup"><span data-stu-id="cc9f1-181">Sharing invitations</span></span>

<span data-ttu-id="cc9f1-182">Los permisos que se envió el [Invitar a][] API pueden tener información adicional en el aspecto de[SharingInvitation] de [invitación].</span><span class="sxs-lookup"><span data-stu-id="cc9f1-182">Permissions sent by the [invite][] API may have additional information in the [invitation][SharingInvitation] facet.</span></span>
<span data-ttu-id="cc9f1-183">Si se ha enviado una invitación a una dirección de correo electrónico que no coincide con una cuenta conocida, la propiedad **grantedTo** no puede establecerse hasta que se presentan la invitación, que se produce la primera vez que el usuario hace clic en el vínculo e inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="cc9f1-183">If an invitation was sent to an email address that doesn't match a known account, the **grantedTo** property may not be set until the invitation is redeemed, which occurs the first time the user clicks the link and signs in.</span></span>

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

<span data-ttu-id="cc9f1-184">Después de que la invitación de uso compartido se ha canjeado por un usuario, la propiedad **grantedTo** contendrá la información sobre la cuenta que canjea los permisos:</span><span class="sxs-lookup"><span data-stu-id="cc9f1-184">After the sharing invitation has been redeemed by a user, the **grantedTo** property will contain the information about the account that redeemed the permissions:</span></span>

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

## <a name="methods"></a><span data-ttu-id="cc9f1-185">Métodos</span><span class="sxs-lookup"><span data-stu-id="cc9f1-185">Methods</span></span>

| <span data-ttu-id="cc9f1-186">Método</span><span class="sxs-lookup"><span data-stu-id="cc9f1-186">Method</span></span>                                                   | <span data-ttu-id="cc9f1-187">Ruta de acceso a REST</span><span class="sxs-lookup"><span data-stu-id="cc9f1-187">REST Path</span></span>
|:---------------------------------------------------------|:-----------------------
| [<span data-ttu-id="cc9f1-188">Enumerar permisos</span><span class="sxs-lookup"><span data-stu-id="cc9f1-188">List permissions</span></span>](../api/driveitem-list-permissions.md) | `GET /drive/items/{item-id}/permissions`
| [<span data-ttu-id="cc9f1-189">Obtener permiso</span><span class="sxs-lookup"><span data-stu-id="cc9f1-189">Get permission</span></span>](../api/permission-get.md)               | `GET /drive/items/{item-id}/permissions/{id}`
| <span data-ttu-id="cc9f1-190">[Crear vínculo] [createLink]</span><span class="sxs-lookup"><span data-stu-id="cc9f1-190">[Create link][createLink]</span></span>                                | `POST /drive/items/{item-id}/createLink`
| <span data-ttu-id="cc9f1-191">[Invitar a personas] [Invitar a]</span><span class="sxs-lookup"><span data-stu-id="cc9f1-191">[Invite people][invite]</span></span>                                  | `POST /drive/items/{item-id}/invite`
| [<span data-ttu-id="cc9f1-192">Actualizar</span><span class="sxs-lookup"><span data-stu-id="cc9f1-192">Update</span></span>](../api/permission-update.md)                    | `PATCH /drive/items/{item-id}/permissions/{id}`
| [<span data-ttu-id="cc9f1-193">Eliminar</span><span class="sxs-lookup"><span data-stu-id="cc9f1-193">Delete</span></span>](../api/permission-delete.md)                    | `DELETE /drive/items/{item-id}/permissions/{id}`



[createLink]: ../api/driveitem-createlink.md
[IdentitySet]: identityset.md
[invitar a]: ../api/driveitem-invite.md
[invite]: ../api/driveitem-invite.md
[ItemReference]: itemreference.md
[API de recursos compartidos]: ../api/shares-get.md
[shares API]: ../api/shares-get.md
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
