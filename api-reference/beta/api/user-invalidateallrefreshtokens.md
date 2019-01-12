---
title: 'usuario: invalidateAllRefreshTokens'
description: Invalida todos los tokens de actualización del usuario otorgan a las aplicaciones (así como las cookies de sesión en el Explorador de un usuario), al restablecer la propiedad de usuario **refreshTokensValidFromDateTime** a la fecha y hora actual. Normalmente, esta operación se realiza (por el usuario o un administrador) si el usuario tiene un dispositivo perdido o robado.  Esta operación podría impedir el acceso a los datos de la organización tener acceso a través de aplicaciones en el dispositivo sin que el usuario que se requiere en primer lugar para iniciar sesión de nuevo. De hecho, esta operación forzará que el usuario para iniciar sesión de nuevo para todas las aplicaciones que han aceptado anteriormente, independientemente del dispositivo.
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 740829e4ebd3b64308e514ab1c7633db7f35e7d7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950182"
---
# <a name="user-invalidateallrefreshtokens"></a><span data-ttu-id="31fef-106">usuario: invalidateAllRefreshTokens</span><span class="sxs-lookup"><span data-stu-id="31fef-106">user: invalidateAllRefreshTokens</span></span>

> <span data-ttu-id="31fef-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="31fef-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="31fef-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="31fef-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="31fef-109">Invalida todos los tokens de actualización del usuario otorgan a las aplicaciones (así como las cookies de sesión en el Explorador de un usuario), al restablecer la propiedad de usuario **refreshTokensValidFromDateTime** a la fecha y hora actual.</span><span class="sxs-lookup"><span data-stu-id="31fef-109">Invalidates all of the user's refresh tokens issued to applications (as well as session cookies in a user's browser), by resetting the **refreshTokensValidFromDateTime** user property to the current date-time.</span></span> <span data-ttu-id="31fef-110">Normalmente, esta operación se realiza (por el usuario o un administrador) si el usuario tiene un dispositivo perdido o robado.</span><span class="sxs-lookup"><span data-stu-id="31fef-110">Typically, this operation is performed (by the user or an administrator) if the user has a lost or stolen device.</span></span>  <span data-ttu-id="31fef-111">Esta operación podría impedir el acceso a los datos de la organización tener acceso a través de aplicaciones en el dispositivo sin que el usuario que se requiere en primer lugar para iniciar sesión de nuevo.</span><span class="sxs-lookup"><span data-stu-id="31fef-111">This operation would prevent access to any of the organization's data accessed through applications on the device without the user first being required to sign in again.</span></span> <span data-ttu-id="31fef-112">De hecho, esta operación forzará que el usuario para iniciar sesión de nuevo para todas las aplicaciones que han aceptado anteriormente, independientemente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31fef-112">In fact, this operation would force the user to sign in again for all applications that they have previously consented to, independent of device.</span></span>

<span data-ttu-id="31fef-113">Para los desarrolladores, si la aplicación intenta canjee un token de acceso delegado para este usuario mediante el uso de un token de actualización invalidada, la aplicación obtendrá un error.</span><span class="sxs-lookup"><span data-stu-id="31fef-113">For developers, if the application attempts to redeem a delegated access token for this user by using an invalidated refresh token, the application will get an error.</span></span> <span data-ttu-id="31fef-114">En este caso, necesitará adquirir un nuevo token de actualización mediante la realización de una solicitud al extremo de autorizar, lo que obliga al usuario que inicie sesión en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31fef-114">If this happens, the application will need to acquire a new refresh token by making a request to the authorize endpoint, which will force the user to sign in.</span></span>

## <a name="permissions"></a><span data-ttu-id="31fef-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="31fef-115">Permissions</span></span>
<span data-ttu-id="31fef-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="31fef-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

+ <span data-ttu-id="31fef-118">De la aplicación para permitir que el firmado de usuario para invalidar las aplicaciones ha dado su consentimiento a: User.ReadWrite, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="31fef-118">For an application to allow the signed in user to invalidate applications they've consented to: User.ReadWrite, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>
+ <span data-ttu-id="31fef-119">Para que una aplicación permitir que un administrador invalidar las aplicaciones de un usuario ha aceptado: Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="31fef-119">For an application to allow an administrator to invalidate applications a user has consented to: Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>

## <a name="http-request"></a><span data-ttu-id="31fef-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="31fef-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/invalidateAllRefreshTokens
POST /users/{id | userPrincipalName}/invalidateAllRefreshTokens
```
## <a name="request-headers"></a><span data-ttu-id="31fef-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="31fef-121">Request headers</span></span>
| <span data-ttu-id="31fef-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31fef-122">Header</span></span>       | <span data-ttu-id="31fef-123">Valor</span><span class="sxs-lookup"><span data-stu-id="31fef-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="31fef-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="31fef-124">Authorization</span></span>  | <span data-ttu-id="31fef-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="31fef-p106">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="31fef-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="31fef-127">Request body</span></span>
<span data-ttu-id="31fef-128">Esta operación no tiene ningún contenido de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31fef-128">This operation has no request content.</span></span>

## <a name="response"></a><span data-ttu-id="31fef-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31fef-129">Response</span></span>

<span data-ttu-id="31fef-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="31fef-130">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="31fef-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="31fef-131">Example</span></span>
<span data-ttu-id="31fef-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="31fef-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="31fef-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="31fef-133">Request</span></span>
<span data-ttu-id="31fef-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31fef-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_invalidateallrefreshtokens"
}-->
```http
POST https://graph.microsoft.com/beta/me/invalidateAllRefreshTokens
```

##### <a name="response"></a><span data-ttu-id="31fef-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31fef-135">Response</span></span>
<span data-ttu-id="31fef-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="31fef-136">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: invalidateAllRefreshTokens",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
