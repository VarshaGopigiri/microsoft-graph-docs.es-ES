---
title: Crear usuario
description: Utilice esta API para crear un nuevo usuario.
ms.openlocfilehash: 17df752fb3767e82b72e46857e9ce6a2a8769db7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084237"
---
# <a name="create-user"></a><span data-ttu-id="187a0-103">Crear usuario</span><span class="sxs-lookup"><span data-stu-id="187a0-103">Create user</span></span>

> <span data-ttu-id="187a0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="187a0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="187a0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="187a0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="187a0-106">Utilice esta API para crear un nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="187a0-106">Use this API to create a new user.</span></span>
<span data-ttu-id="187a0-107">El cuerpo de la solicitud contiene al usuario que cree.</span><span class="sxs-lookup"><span data-stu-id="187a0-107">The request body contains the user to create.</span></span> <span data-ttu-id="187a0-108">Como mínimo, debe especificar las propiedades necesarias para el usuario.</span><span class="sxs-lookup"><span data-stu-id="187a0-108">At a minimum, you must specify the required properties for the user.</span></span> <span data-ttu-id="187a0-109">Opcionalmente, puede especificar las propiedades de escritura.</span><span class="sxs-lookup"><span data-stu-id="187a0-109">You can optionally specify any other writable properties.</span></span>
## <a name="permissions"></a><span data-ttu-id="187a0-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="187a0-110">Permissions</span></span>
<span data-ttu-id="187a0-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="187a0-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="187a0-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="187a0-113">Permission type</span></span>      | <span data-ttu-id="187a0-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="187a0-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="187a0-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="187a0-115">Delegated (work or school account)</span></span> | <span data-ttu-id="187a0-116">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="187a0-116">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="187a0-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="187a0-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="187a0-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="187a0-118">Not supported.</span></span>    |
|<span data-ttu-id="187a0-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="187a0-119">Application</span></span> | <span data-ttu-id="187a0-120">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="187a0-120">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="187a0-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="187a0-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users
```
## <a name="request-headers"></a><span data-ttu-id="187a0-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="187a0-122">Request headers</span></span>
| <span data-ttu-id="187a0-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="187a0-123">Header</span></span>       | <span data-ttu-id="187a0-124">Valor</span><span class="sxs-lookup"><span data-stu-id="187a0-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="187a0-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="187a0-125">Authorization</span></span>  | <span data-ttu-id="187a0-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="187a0-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="187a0-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="187a0-128">Content-Type</span></span>  | <span data-ttu-id="187a0-129">application/json</span><span class="sxs-lookup"><span data-stu-id="187a0-129">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="187a0-130">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="187a0-130">Request body</span></span>
<span data-ttu-id="187a0-131">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="187a0-131">In the request body, supply a JSON representation of [user](../resources/user.md) object.</span></span>

<span data-ttu-id="187a0-132">En la tabla siguiente, se muestran las propiedades necesarias al crear un usuario.</span><span class="sxs-lookup"><span data-stu-id="187a0-132">The following table shows the properties that are required when you create a user.</span></span>

| <span data-ttu-id="187a0-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="187a0-133">Parameter</span></span> | <span data-ttu-id="187a0-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="187a0-134">Type</span></span> | <span data-ttu-id="187a0-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="187a0-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="187a0-136">accountEnabled</span><span class="sxs-lookup"><span data-stu-id="187a0-136">accountEnabled</span></span> |<span data-ttu-id="187a0-137">boolean</span><span class="sxs-lookup"><span data-stu-id="187a0-137">boolean</span></span> |<span data-ttu-id="187a0-138">true si la cuenta está habilitada; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="187a0-138">true if the account is enabled; otherwise, false.</span></span>|
|<span data-ttu-id="187a0-139">displayName</span><span class="sxs-lookup"><span data-stu-id="187a0-139">displayName</span></span> |<span data-ttu-id="187a0-140">string</span><span class="sxs-lookup"><span data-stu-id="187a0-140">string</span></span> |<span data-ttu-id="187a0-141">El nombre para mostrar en la libreta de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="187a0-141">The name to display in the address book for the user.</span></span>|
|<span data-ttu-id="187a0-142">onPremisesImmutableId</span><span class="sxs-lookup"><span data-stu-id="187a0-142">onPremisesImmutableId</span></span> |<span data-ttu-id="187a0-143">string</span><span class="sxs-lookup"><span data-stu-id="187a0-143">string</span></span> |<span data-ttu-id="187a0-144">Solo se debe especificar al crear una nueva cuenta de usuario si usa un dominio federado para la propiedad userPrincipalName (UPN) del usuario.</span><span class="sxs-lookup"><span data-stu-id="187a0-144">Only needs to be specified when creating a new user account if you are using a federated domain for the user's userPrincipalName (UPN) property.</span></span>|
|<span data-ttu-id="187a0-145">mailNickname</span><span class="sxs-lookup"><span data-stu-id="187a0-145">mailNickname</span></span> |<span data-ttu-id="187a0-146">string</span><span class="sxs-lookup"><span data-stu-id="187a0-146">string</span></span> |<span data-ttu-id="187a0-147">El alias de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="187a0-147">The mail alias for the user.</span></span>|
|<span data-ttu-id="187a0-148">passwordProfile</span><span class="sxs-lookup"><span data-stu-id="187a0-148">passwordProfile</span></span>|[<span data-ttu-id="187a0-149">PasswordProfile</span><span class="sxs-lookup"><span data-stu-id="187a0-149">PasswordProfile</span></span>](../resources/passwordprofile.md) |<span data-ttu-id="187a0-150">El perfil de contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="187a0-150">The password profile for the user.</span></span>|
|<span data-ttu-id="187a0-151">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="187a0-151">userPrincipalName</span></span> |<span data-ttu-id="187a0-152">string</span><span class="sxs-lookup"><span data-stu-id="187a0-152">string</span></span> |<span data-ttu-id="187a0-153">El nombre principal de usuario (usuario@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="187a0-153">The user principal name (someuser@contoso.com).</span></span>|

<span data-ttu-id="187a0-154">Puesto que el recurso de **usuario** admite [extensiones](/graph/extensibility-overview), puede usar el `POST` operación y agregar propiedades personalizadas con sus propios datos a la instancia de usuario al crearla.</span><span class="sxs-lookup"><span data-stu-id="187a0-154">Since the **user** resource supports [extensions](/graph/extensibility-overview), you can use the `POST` operation and add custom properties with your own data to the user instance while creating it.</span></span>

## <a name="response"></a><span data-ttu-id="187a0-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="187a0-155">Response</span></span>

<span data-ttu-id="187a0-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="187a0-156">If successful, this method returns `201 Created` response code and [user](../resources/user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="187a0-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="187a0-157">Example</span></span>
##### <a name="request"></a><span data-ttu-id="187a0-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="187a0-158">Request</span></span>
<span data-ttu-id="187a0-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="187a0-159">Here is an example of the request.</span></span>
<!-- {  
  "blockType": "request",   
  "name": "create_user_from_users_2"    
}-->

```http
POST https://graph.microsoft.com/beta/users
Content-type: application/json

{
  "accountEnabled": true,
  "displayName": "displayName-value",
  "mailNickname": "mailNickname-value",
  "userPrincipalName": "upn-value@tenant-value@onmicrosoft.com",
  "passwordProfile" : {
    "forceChangePasswordNextSignIn": true,
    "password": "password-value"
  }
}
```
<span data-ttu-id="187a0-160">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="187a0-160">In the request body, supply a JSON representation of [user](../resources/user.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="187a0-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="187a0-161">Response</span></span>
<span data-ttu-id="187a0-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="187a0-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#users/$entity",
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

## <a name="see-also"></a><span data-ttu-id="187a0-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="187a0-165">See also</span></span>

- [<span data-ttu-id="187a0-166">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="187a0-166">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="187a0-167">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="187a0-167">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="187a0-168">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="187a0-168">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create User",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->