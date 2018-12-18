---
title: Crear usuario
description: Utilice esta API para crear un nuevo usuario.
author: dkershaw10
ms.openlocfilehash: d5e85b0538790ce08f2ad36231830ac53cbf6e9d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27342654"
---
# <a name="create-user"></a><span data-ttu-id="a5ba9-103">Crear usuario</span><span class="sxs-lookup"><span data-stu-id="a5ba9-103">Create User</span></span>

<span data-ttu-id="a5ba9-p101">Use esta API para crear un nuevo usuario. El cuerpo de la solicitud contiene el usuario que se creará. Como mínimo, debe especificar las propiedades necesarias para el usuario. De forma opcional, puede especificar cualquier otra propiedad modificable.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-p101">Use this API to create a new User. The request body contains the user to create. At a minimum, you must specify the required properties for the user. You can optionally specify any other writable properties.</span></span>
## <a name="permissions"></a><span data-ttu-id="a5ba9-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="a5ba9-108">Permissions</span></span>
<span data-ttu-id="a5ba9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5ba9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a5ba9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5ba9-111">Permission type</span></span>      | <span data-ttu-id="a5ba9-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5ba9-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a5ba9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5ba9-113">Delegated (work or school account)</span></span> | <span data-ttu-id="a5ba9-114">User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a5ba9-114">User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="a5ba9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5ba9-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a5ba9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-116">Not supported.</span></span>    |
|<span data-ttu-id="a5ba9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5ba9-117">Application</span></span> | <span data-ttu-id="a5ba9-118">User.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a5ba9-118">User.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a5ba9-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5ba9-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users
```
## <a name="request-headers"></a><span data-ttu-id="a5ba9-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5ba9-120">Request headers</span></span>
| <span data-ttu-id="a5ba9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5ba9-121">Header</span></span>       | <span data-ttu-id="a5ba9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a5ba9-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a5ba9-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a5ba9-123">Authorization</span></span>  | <span data-ttu-id="a5ba9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a5ba9-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a5ba9-126">Content-Type</span></span>  | <span data-ttu-id="a5ba9-127">application/json</span><span class="sxs-lookup"><span data-stu-id="a5ba9-127">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a5ba9-128">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5ba9-128">Request body</span></span>
<span data-ttu-id="a5ba9-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="a5ba9-129">In the request body, supply a JSON representation of [user](../resources/user.md) object.</span></span>

<span data-ttu-id="a5ba9-130">En la tabla siguiente, se muestran las propiedades necesarias al crear un usuario.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-130">The following table shows the properties that are required when you create a user.</span></span>

| <span data-ttu-id="a5ba9-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a5ba9-131">Parameter</span></span> | <span data-ttu-id="a5ba9-132">Type</span><span class="sxs-lookup"><span data-stu-id="a5ba9-132">Type</span></span> | <span data-ttu-id="a5ba9-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5ba9-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a5ba9-134">accountEnabled</span><span class="sxs-lookup"><span data-stu-id="a5ba9-134">accountEnabled</span></span> |<span data-ttu-id="a5ba9-135">boolean</span><span class="sxs-lookup"><span data-stu-id="a5ba9-135">boolean</span></span> |<span data-ttu-id="a5ba9-136">true si la cuenta está habilitada; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-136">true if the account is enabled; otherwise, false.</span></span>|
|<span data-ttu-id="a5ba9-137">displayName</span><span class="sxs-lookup"><span data-stu-id="a5ba9-137">displayName</span></span> |<span data-ttu-id="a5ba9-138">string</span><span class="sxs-lookup"><span data-stu-id="a5ba9-138">string</span></span> |<span data-ttu-id="a5ba9-139">El nombre para mostrar en la libreta de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-139">The name to display in the address book for the user.</span></span>|
|<span data-ttu-id="a5ba9-140">onPremisesImmutableId</span><span class="sxs-lookup"><span data-stu-id="a5ba9-140">onPremisesImmutableId</span></span> |<span data-ttu-id="a5ba9-141">string</span><span class="sxs-lookup"><span data-stu-id="a5ba9-141">string</span></span> |<span data-ttu-id="a5ba9-142">Solo se debe especificar al crear una nueva cuenta de usuario si usa un dominio federado para la propiedad userPrincipalName (UPN) del usuario.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-142">Only needs to be specified when creating a new user account if you are using a federated domain for the user's userPrincipalName (UPN) property.</span></span>|
|<span data-ttu-id="a5ba9-143">mailNickname</span><span class="sxs-lookup"><span data-stu-id="a5ba9-143">mailNickname</span></span> |<span data-ttu-id="a5ba9-144">string</span><span class="sxs-lookup"><span data-stu-id="a5ba9-144">string</span></span> |<span data-ttu-id="a5ba9-145">El alias de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-145">The mail alias for the user.</span></span>|
|<span data-ttu-id="a5ba9-146">passwordProfile</span><span class="sxs-lookup"><span data-stu-id="a5ba9-146">passwordProfile</span></span>|[<span data-ttu-id="a5ba9-147">PasswordProfile</span><span class="sxs-lookup"><span data-stu-id="a5ba9-147">PasswordProfile</span></span>](../resources/passwordprofile.md) |<span data-ttu-id="a5ba9-148">El perfil de contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-148">The password profile for the user.</span></span>|
|<span data-ttu-id="a5ba9-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a5ba9-149">userPrincipalName</span></span> |<span data-ttu-id="a5ba9-150">string</span><span class="sxs-lookup"><span data-stu-id="a5ba9-150">string</span></span> |<span data-ttu-id="a5ba9-151">El nombre principal de usuario (usuario@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="a5ba9-151">The user principal name (someuser@contoso.com).</span></span>|

## <a name="response"></a><span data-ttu-id="a5ba9-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5ba9-152">Response</span></span>

<span data-ttu-id="a5ba9-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-153">If successful, this method returns `201 Created` response code and [user](../resources/user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a5ba9-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5ba9-154">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a5ba9-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5ba9-155">Request</span></span>
<span data-ttu-id="a5ba9-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-156">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_user_from_users"
}-->
```http
POST https://graph.microsoft.com/v1.0/users
Content-type: application/json

{
  "accountEnabled": true,
  "displayName": "displayName-value",
  "mailNickname": "mailNickname-value",
  "userPrincipalName": "upn-value@tenant-value.onmicrosoft.com",
  "passwordProfile" : {
    "forceChangePasswordNextSignIn": true,
    "password": "password-value"
  }
}
```
<span data-ttu-id="a5ba9-157">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="a5ba9-157">In the request body, supply a JSON representation of [user](../resources/user.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="a5ba9-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5ba9-158">Response</span></span>
<span data-ttu-id="a5ba9-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a5ba9-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users/$entity",
    "id": "id-value",
    "businessPhones": [],
    "displayName": "displayName-value",
    "givenName": null,
    "jobTitle": null,
    "mail": null,
    "mobilePhone": null,
    "officeLocation": null,
    "preferredLanguage": null,
    "surname": null,
    "userPrincipalName": "upn-value@tenant-value.onmicrosoft.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create User",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
