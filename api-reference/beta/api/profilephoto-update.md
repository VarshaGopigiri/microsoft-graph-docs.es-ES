---
title: Update profilephoto
description: Actualizar la foto para cualquier usuario en el inquilino incluido el firmado de usuario, o el grupo especificado o el contacto. Desde allí
ms.openlocfilehash: 801ccd58e57cb02c1805f927dc22c9fd593cbae5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087868"
---
# <a name="update-profilephoto"></a><span data-ttu-id="3b23c-104">Update profilephoto</span><span class="sxs-lookup"><span data-stu-id="3b23c-104">Update profilephoto</span></span>

> <span data-ttu-id="3b23c-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3b23c-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3b23c-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3b23c-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3b23c-107">Actualizar la foto para cualquier usuario en el inquilino incluido el firmado de usuario, o el grupo especificado o el contacto.</span><span class="sxs-lookup"><span data-stu-id="3b23c-107">Update the photo for any user in the tenant including the signed-in user, or the specified group or contact.</span></span> <span data-ttu-id="3b23c-108">Puesto que actualmente no hay un límite de 4MB en el tamaño total de cada solicitud REST, esto limita el tamaño de la foto que puede agregar a menos de 4MB.</span><span class="sxs-lookup"><span data-stu-id="3b23c-108">Since there is currently a limit of 4MB on the total size of each REST request, this limits the size of the photo you can add to under 4MB.</span></span>

<span data-ttu-id="3b23c-109">Utilice solo PUT para esta operación en la versión beta.</span><span class="sxs-lookup"><span data-stu-id="3b23c-109">Use only PUT for this operation in the beta version.</span></span>

> <span data-ttu-id="3b23c-110">**Nota** La operación de foto de actualización de beta es compatible con sólo el usuario trabajo o escuela buzones y no personal.</span><span class="sxs-lookup"><span data-stu-id="3b23c-110">**Note** The update photo operation in beta supports only the user's work or school mailboxes and not personal mailboxes.</span></span>

## <a name="permissions"></a><span data-ttu-id="3b23c-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="3b23c-111">Permissions</span></span>
<span data-ttu-id="3b23c-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3b23c-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3b23c-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3b23c-114">Permission type</span></span>      | <span data-ttu-id="3b23c-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3b23c-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3b23c-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3b23c-116">Delegated (work or school account)</span></span>     | <span data-ttu-id="3b23c-117">Fotos de perfiles de la ha iniciado sesión del **usuario**:</span><span class="sxs-lookup"><span data-stu-id="3b23c-117">Profile photo of the signed-in **user**:</span></span><br/><span data-ttu-id="3b23c-118">User.ReadWrite, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3b23c-118">User.ReadWrite, User.ReadWrite.All</span></span><br /><br /><span data-ttu-id="3b23c-119">Para el recurso de **grupo**:</span><span class="sxs-lookup"><span data-stu-id="3b23c-119">For **group** resource:</span></span><br /><span data-ttu-id="3b23c-120">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3b23c-120">Group.ReadWrite.All</span></span><br /><br /><span data-ttu-id="3b23c-121">Para el recurso de **contacto**:</span><span class="sxs-lookup"><span data-stu-id="3b23c-121">For **contact** resource:</span></span><br /><span data-ttu-id="3b23c-122">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3b23c-122">Contacts.ReadWrite</span></span> |
|<span data-ttu-id="3b23c-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3b23c-123">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3b23c-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b23c-124">Not supported.</span></span> |
|<span data-ttu-id="3b23c-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3b23c-125">Application</span></span>                            | <span data-ttu-id="3b23c-126">Tipo de recurso del **usuario**:</span><span class="sxs-lookup"><span data-stu-id="3b23c-126">For **user** resource:</span></span><br/><span data-ttu-id="3b23c-127">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3b23c-127">User.ReadWrite.All</span></span><br /><br /><span data-ttu-id="3b23c-128">Para el recurso de **grupo**:</span><span class="sxs-lookup"><span data-stu-id="3b23c-128">For **group** resource:</span></span><br /><span data-ttu-id="3b23c-129">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3b23c-129">Group.ReadWrite.All</span></span><br /><br /><span data-ttu-id="3b23c-130">Para el recurso de **contacto**:</span><span class="sxs-lookup"><span data-stu-id="3b23c-130">For **contact** resource:</span></span><br /><span data-ttu-id="3b23c-131">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3b23c-131">Contacts.ReadWrite</span></span> |

> <span data-ttu-id="3b23c-p105">**Nota** Para actualizar la foto de un usuario de la organización, la aplicación debe tener el permiso de aplicación User.ReadWrite.All y llamar a esta API bajo su propia identidad, no en nombre de un usuario. Para obtener más información, consulte cómo [obtener acceso sin un usuario que ha iniciado sesión](/graph/auth-v2-service).</span><span class="sxs-lookup"><span data-stu-id="3b23c-p105">**Note** To update the photo of any user in the organization, your app must have the User.ReadWrite.All application permission and call this API under its own identity, not on behalf of a user. To learn more, see [get access without a signed-in user](/graph/auth-v2-service).</span></span>

## <a name="http-request"></a><span data-ttu-id="3b23c-134">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3b23c-134">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /me/photo/$value
PUT /users/{id | userPrincipalName}/photo/$value
PUT /groups/{id}/photo/$value
PUT /me/contacts/{id}/photo/$value
PUT /users/{id | userPrincipalName}/contacts/{id}/photo/$value
PUT /me/contactfolders/{contactFolderId}/contacts/{id}/photo/$value
PUT /users/{id | userPrincipalName}/contactfolders/{contactFolderId}/contacts/{id}/photo/$value
```
## <a name="request-headers"></a><span data-ttu-id="3b23c-135">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3b23c-135">Request headers</span></span>
| <span data-ttu-id="3b23c-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b23c-136">Header</span></span>       | <span data-ttu-id="3b23c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="3b23c-137">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3b23c-138">Authorization</span><span class="sxs-lookup"><span data-stu-id="3b23c-138">Authorization</span></span>  | <span data-ttu-id="3b23c-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3b23c-p106">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="3b23c-141">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3b23c-141">Content-Type</span></span>  | <span data-ttu-id="3b23c-p107">image/jpeg. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3b23c-p107">image/jpeg. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3b23c-144">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3b23c-144">Request body</span></span>
<span data-ttu-id="3b23c-145">En el cuerpo de la solicitud, incluya los datos binarios de la foto.</span><span class="sxs-lookup"><span data-stu-id="3b23c-145">In the request body, include the binary data of the photo in the request body.</span></span>

## <a name="response"></a><span data-ttu-id="3b23c-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b23c-146">Response</span></span>

<span data-ttu-id="3b23c-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="3b23c-147">If successful, this method returns a `200 OK` response code.</span></span>
## <a name="example"></a><span data-ttu-id="3b23c-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3b23c-148">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3b23c-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3b23c-149">Request</span></span>
<span data-ttu-id="3b23c-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b23c-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_profilephoto"
}-->
```http
PUT https://graph.microsoft.com/beta/me/photo/$value
Content-type: image/jpeg

Binary data for the image

```
##### <a name="response"></a><span data-ttu-id="3b23c-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b23c-151">Response</span></span>
<span data-ttu-id="3b23c-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3b23c-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.profilePhoto"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update profilephoto",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
