---
title: Crear usuario
description: Utilice esta API para crear un nuevo usuario.
author: dkershaw10
localization_priority: Priority
ms.openlocfilehash: 218752a382da4ccb2bdbe240c8c57d03007b0169
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851656"
---
# <a name="create-user"></a><span data-ttu-id="3dfaa-103">Crear usuario</span><span class="sxs-lookup"><span data-stu-id="3dfaa-103">Create User</span></span>

<span data-ttu-id="3dfaa-p101">Use esta API para crear un nuevo usuario. El cuerpo de la solicitud contiene el usuario que se creará. Como mínimo, debe especificar las propiedades necesarias para el usuario. De forma opcional, puede especificar cualquier otra propiedad modificable.</span><span class="sxs-lookup"><span data-stu-id="3dfaa-p101">Use this API to create a new User. The request body contains the user to create. At a minimum, you must specify the required properties for the user. You can optionally specify any other writable properties.</span></span>
## <a name="permissions"></a><span data-ttu-id="3dfaa-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="3dfaa-108">Permissions</span></span>
<span data-ttu-id="3dfaa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3dfaa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3dfaa-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3dfaa-111">Permission type</span></span>      | <span data-ttu-id="3dfaa-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3dfaa-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3dfaa-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3dfaa-113">Delegated (work or school account)</span></span> | <span data-ttu-id="3dfaa-114">User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="3dfaa-114">User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="3dfaa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3dfaa-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3dfaa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3dfaa-116">Not supported.</span></span>    |
|<span data-ttu-id="3dfaa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3dfaa-117">Application</span></span> | <span data-ttu-id="3dfaa-118">User.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3dfaa-118">User.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3dfaa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3dfaa-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users
```
## <a name="request-headers"></a><span data-ttu-id="3dfaa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3dfaa-120">Request headers</span></span>
| <span data-ttu-id="3dfaa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3dfaa-121">Header</span></span>       | <span data-ttu-id="3dfaa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3dfaa-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3dfaa-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="3dfaa-123">Authorization</span></span>  | <span data-ttu-id="3dfaa-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3dfaa-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="3dfaa-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3dfaa-126">Content-Type</span></span>  | <span data-ttu-id="3dfaa-127">application/json</span><span class="sxs-lookup"><span data-stu-id="3dfaa-127">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3dfaa-128">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="3dfaa-128">Request body</span></span>
<span data-ttu-id="3dfaa-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="3dfaa-129">In the request body, supply a JSON representation of [user](../resources/user.md) object.</span></span>

<span data-ttu-id="3dfaa-130">En la tabla siguiente, se muestran las propiedades necesarias al crear un usuario.</span><span class="sxs-lookup"><span data-stu-id="3dfaa-130">The following table shows the properties that are required when you create a user.</span></span>

| <span data-ttu-id="3dfaa-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3dfaa-131">Parameter</span></span> | <span data-ttu-id="3dfaa-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="3dfaa-132">Type</span></span> | <span data-ttu-id="3dfaa-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="3dfaa-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3dfaa-134">accountEnabled</span><span class="sxs-lookup"><span data-stu-id="3dfaa-134">accountEnabled</span></span> |<span data-ttu-id="3dfaa-135">boolean</span><span class="sxs-lookup"><span data-stu-id="3dfaa-135">boolean</span></span> |<span data-ttu-id="3dfaa-136">true si la cuenta está habilitada; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="3dfaa-136">true if the account is enabled; otherwise, false.</span></span>|
|<span data-ttu-id="3dfaa-137">displayName</span><span class="sxs-lookup"><span data-stu-id="3dfaa-137">displayName</span></span> |<span data-ttu-id="3dfaa-138">string</span><span class="sxs-lookup"><span data-stu-id="3dfaa-138">string</span></span> |<span data-ttu-id="3dfaa-139">El nombre para mostrar en la libreta de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="3dfaa-139">The name to display in the address book for the user.</span></span>|
|<span data-ttu-id="3dfaa-140">onPremisesImmutableId</span><span class="sxs-lookup"><span data-stu-id="3dfaa-140">onPremisesImmutableId</span></span> |<span data-ttu-id="3dfaa-141">string</span><span class="sxs-lookup"><span data-stu-id="3dfaa-141">string</span></span> |<span data-ttu-id="3dfaa-142">Solo se debe especificar al crear una nueva cuenta de usuario si usa un dominio federado para la propiedad userPrincipalName (UPN) del usuario.</span><span class="sxs-lookup"><span data-stu-id="3dfaa-142">Only needs to be specified when creating a new user account if you are using a federated domain for the user's userPrincipalName (UPN) property.</span></span>|
|<span data-ttu-id="3dfaa-143">mailNickname</span><span class="sxs-lookup"><span data-stu-id="3dfaa-143">mailNickname</span></span> |<span data-ttu-id="3dfaa-144">string</span><span class="sxs-lookup"><span data-stu-id="3dfaa-144">string</span></span> |<span data-ttu-id="3dfaa-145">El alias de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="3dfaa-145">The mail alias for the user.</span></span>|
|<span data-ttu-id="3dfaa-146">passwordProfile</span><span class="sxs-lookup"><span data-stu-id="3dfaa-146">passwordProfile</span></span>|[<span data-ttu-id="3dfaa-147">PasswordProfile</span><span class="sxs-lookup"><span data-stu-id="3dfaa-147">PasswordProfile</span></span>](../resources/passwordprofile.md) |<span data-ttu-id="3dfaa-148">El perfil de contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="3dfaa-148">The password profile for the user.</span></span>|
|<span data-ttu-id="3dfaa-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3dfaa-149">userPrincipalName</span></span> |<span data-ttu-id="3dfaa-150">string</span><span class="sxs-lookup"><span data-stu-id="3dfaa-150">string</span></span> |<span data-ttu-id="3dfaa-151">El nombre principal de usuario (usuario@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="3dfaa-151">The user principal name (someuser@contoso.com).</span></span>|

## <a name="response"></a><span data-ttu-id="3dfaa-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3dfaa-152">Response</span></span>

<span data-ttu-id="3dfaa-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3dfaa-153">If successful, this method returns `201 Created` response code and [user](../resources/user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3dfaa-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3dfaa-154">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3dfaa-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3dfaa-155">Request</span></span>
<span data-ttu-id="3dfaa-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3dfaa-156">Here is an example of the request.</span></span>
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
<span data-ttu-id="3dfaa-157">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="3dfaa-157">In the request body, supply a JSON representation of [user](../resources/user.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="3dfaa-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3dfaa-158">Response</span></span>
<span data-ttu-id="3dfaa-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3dfaa-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
