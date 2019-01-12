---
title: Forzar la eliminación de dominio
description: Elimina un dominio mediante una operación asincrónica de larga duración.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: bbf56fdd2f623a918b43298626bd08269ad922ef
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918430"
---
# <a name="force-domain-deletion"></a><span data-ttu-id="cc85a-103">Forzar la eliminación de dominio</span><span class="sxs-lookup"><span data-stu-id="cc85a-103">Force domain deletion</span></span>

<span data-ttu-id="cc85a-104">Elimina un dominio mediante una operación asincrónica de larga duración.</span><span class="sxs-lookup"><span data-stu-id="cc85a-104">Deletes a domain using an asynchronous long-running operation.</span></span>

<span data-ttu-id="cc85a-105">Como parte de esta operación, se realizan las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="cc85a-105">The following actions are performed as part of this operation:</span></span>

* <span data-ttu-id="cc85a-106">Actualizaciones de la `userPrincipalName`, `mail`, y `proxyAddresses` propiedades de `users` con referencias al dominio eliminado que se va a usar el dominio onmicrosoft.com inicial.</span><span class="sxs-lookup"><span data-stu-id="cc85a-106">Updates the `userPrincipalName`, `mail`, and `proxyAddresses` properties of `users` with references to the deleted domain to use the initial onmicrosoft.com domain.</span></span>

* <span data-ttu-id="cc85a-107">Actualizaciones de la `mail` (propiedad) de `groups` con referencias al dominio eliminado que se va a usar el dominio onmicrosoft.com inicial.</span><span class="sxs-lookup"><span data-stu-id="cc85a-107">Updates the `mail` property of `groups` with references to the deleted domain to use the initial onmicrosoft.com domain.</span></span>

* <span data-ttu-id="cc85a-108">Actualizaciones de la `identifierUris` (propiedad) de `applications` con referencias al dominio eliminado que se va a usar el dominio onmicrosoft.com inicial.</span><span class="sxs-lookup"><span data-stu-id="cc85a-108">Updates the `identifierUris` property of `applications` with references to the deleted domain to use the initial onmicrosoft.com domain.</span></span>

* <span data-ttu-id="cc85a-109">Si el número de objetos que se puede cambiar el nombre es mayor que 1000, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="cc85a-109">If the number of objects to be renamed is greater than 1000, an error is returned.</span></span>

* <span data-ttu-id="cc85a-110">Si uno de los `applications` se cambia el nombre es una aplicación de varios inquilino, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="cc85a-110">If one of the `applications` to be renamed is a multi-tenant app, an error is returned.</span></span>

<span data-ttu-id="cc85a-111">Una vez completada la eliminación del dominio, las operaciones de API para el dominio eliminado devolverá un código de estado de error 404 de HTTP.</span><span class="sxs-lookup"><span data-stu-id="cc85a-111">After the domain deletion completes, API operations for the deleted domain will return a HTTP 404 status code.</span></span> <span data-ttu-id="cc85a-112">Para comprobar la eliminación de un dominio, puede realizar una operación [get de dominio](domain-get.md) .</span><span class="sxs-lookup"><span data-stu-id="cc85a-112">To verify deletion of a domain, you can perform a [get domain](domain-get.md) operation.</span></span>

## <a name="permissions"></a><span data-ttu-id="cc85a-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="cc85a-113">Permissions</span></span>

<span data-ttu-id="cc85a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cc85a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cc85a-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cc85a-116">Permission type</span></span>      | <span data-ttu-id="cc85a-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cc85a-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cc85a-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cc85a-118">Delegated (work or school account)</span></span> | <span data-ttu-id="cc85a-119">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cc85a-119">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="cc85a-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cc85a-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cc85a-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc85a-121">Not supported.</span></span>    |
|<span data-ttu-id="cc85a-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cc85a-122">Application</span></span> | <span data-ttu-id="cc85a-123">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cc85a-123">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cc85a-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cc85a-124">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /domains/{id}/forceDelete
```

> <span data-ttu-id="cc85a-125">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="cc85a-125">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="cc85a-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cc85a-126">Request headers</span></span>

| <span data-ttu-id="cc85a-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="cc85a-127">Name</span></span> | <span data-ttu-id="cc85a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc85a-128">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="cc85a-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="cc85a-129">Authorization</span></span>  | <span data-ttu-id="cc85a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc85a-p103">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="cc85a-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="cc85a-132">Content-Type</span></span>  | <span data-ttu-id="cc85a-133">application/json</span><span class="sxs-lookup"><span data-stu-id="cc85a-133">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="cc85a-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cc85a-134">Request body</span></span>

<span data-ttu-id="cc85a-135">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="cc85a-135">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="cc85a-136">Parámetro</span><span class="sxs-lookup"><span data-stu-id="cc85a-136">Parameter</span></span> | <span data-ttu-id="cc85a-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc85a-137">Type</span></span> | <span data-ttu-id="cc85a-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc85a-138">Description</span></span> |
|:---------------|:--------|:----------|
|`disableUserAccounts`|`Boolean`| <span data-ttu-id="cc85a-139">Opción para deshabilitar las cuentas de usuario que han cambiado de nombre.</span><span class="sxs-lookup"><span data-stu-id="cc85a-139">Option to disable user accounts which are renamed.</span></span> <span data-ttu-id="cc85a-140">Si una cuenta de usuario está deshabilitada, el usuario no podrá iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="cc85a-140">If a user account is disabled, the user will not be allowed to sign in.</span></span> <span data-ttu-id="cc85a-141">Si establece en **true** la `users` actualizados tal como parte de esta operación se deshabilitará.</span><span class="sxs-lookup"><span data-stu-id="cc85a-141">If set to **true** the `users` updated as part of this operation will be disabled.</span></span>  <span data-ttu-id="cc85a-142">Valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="cc85a-142">Default value is **true**.</span></span> |

## <a name="response-body"></a><span data-ttu-id="cc85a-143">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="cc85a-143">Response body</span></span>

<span data-ttu-id="cc85a-144">Si tiene éxito, este método devuelve `HTTP/1.1 204 OK` código de estado.</span><span class="sxs-lookup"><span data-stu-id="cc85a-144">If successful, this method returns `HTTP/1.1 204 OK` status code.</span></span>

## <a name="example"></a><span data-ttu-id="cc85a-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc85a-145">Example</span></span>

### <a name="request"></a><span data-ttu-id="cc85a-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cc85a-146">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "domain_forcedelete"
}-->

```http
POST https://graph.microsoft.com/beta/domains/{id}/forceDelete
Content-type: application/json
Content-length: 33

{
  "disableUserAccounts": true
}
```

### <a name="response"></a><span data-ttu-id="cc85a-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc85a-147">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->

```http
HTTP/1.1 204 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domain: forcedelete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
