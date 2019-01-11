---
title: 'dominio: forceDelete'
description: Elimina un dominio mediante una operación asincrónica.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: e90b960bc2e2ff63068b1d91029371044075be27
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838062"
---
# <a name="domain-forcedelete"></a><span data-ttu-id="2142f-103">dominio: forceDelete</span><span class="sxs-lookup"><span data-stu-id="2142f-103">domain: forceDelete</span></span>

> <span data-ttu-id="2142f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2142f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2142f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2142f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2142f-106">Elimina un dominio mediante una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="2142f-106">Deletes a domain using an asynchronous operation.</span></span>

<span data-ttu-id="2142f-107">Como parte de esta operación, se realizan las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="2142f-107">The following actions are performed as part of this operation:</span></span>

* <span data-ttu-id="2142f-108">Cambia el nombre el UPN, EmailAddress y ProxyAddress de usuarios con referencias al dominio eliminado.</span><span class="sxs-lookup"><span data-stu-id="2142f-108">Renames the UPN, EmailAddress, and ProxyAddress of users with references to the deleted domain.</span></span>

* <span data-ttu-id="2142f-109">Cambia el nombre de la EmailAddress de grupos con referencias al dominio eliminado.</span><span class="sxs-lookup"><span data-stu-id="2142f-109">Renames the EmailAddress of groups with references to the deleted domain.</span></span>

* <span data-ttu-id="2142f-110">Cambia el nombre de la identifierUris de aplicaciones con referencias al dominio eliminado.</span><span class="sxs-lookup"><span data-stu-id="2142f-110">Renames the identifierUris of applications with references to the deleted domain.</span></span>

* <span data-ttu-id="2142f-111">Si el número de objetos que se puede cambiar el nombre es mayor que 1000, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="2142f-111">If the number of objects to be renamed is greater than 1000, an error is returned.</span></span>

* <span data-ttu-id="2142f-112">Si una de las aplicaciones se cambia el nombre es una aplicación de varios inquilino, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="2142f-112">If one of the applications to be renamed is a multi-tenant app, an error is returned.</span></span>

<span data-ttu-id="2142f-113">Una vez completada la eliminación del dominio, las operaciones de API para el dominio eliminado devolverá un código de respuesta HTTP 404.</span><span class="sxs-lookup"><span data-stu-id="2142f-113">After the domain deletion completes, API operations for the deleted domain will return a 404 HTTP response code.</span></span> <span data-ttu-id="2142f-114">Para comprobar la eliminación de un dominio, puede realizar una operación [obtener el dominio](domain-get.md).</span><span class="sxs-lookup"><span data-stu-id="2142f-114">To verify deletion of a domain, you can perform a [get domain](domain-get.md).</span></span> <span data-ttu-id="2142f-115">Si el dominio se eliminó correctamente, se devolverá un código de respuesta 404 de HTTP en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2142f-115">If the domain was successfully deleted, a 404 HTTP response code will be returned in the response.</span></span>

## <a name="permissions"></a><span data-ttu-id="2142f-116">Permisos</span><span class="sxs-lookup"><span data-stu-id="2142f-116">Permissions</span></span>

<span data-ttu-id="2142f-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2142f-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="2142f-119">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2142f-119">Permission type</span></span>      | <span data-ttu-id="2142f-120">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2142f-120">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2142f-121">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2142f-121">Delegated (work or school account)</span></span> | <span data-ttu-id="2142f-122">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="2142f-122">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="2142f-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2142f-123">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2142f-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2142f-124">Not supported.</span></span>    |
|<span data-ttu-id="2142f-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2142f-125">Application</span></span> | <span data-ttu-id="2142f-126">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2142f-126">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2142f-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2142f-127">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /domains/{id}/forceDelete
```

> <span data-ttu-id="2142f-128">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="2142f-128">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2142f-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2142f-129">Request headers</span></span>

| <span data-ttu-id="2142f-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="2142f-130">Name</span></span>       | <span data-ttu-id="2142f-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="2142f-131">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2142f-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="2142f-132">Authorization</span></span>  | <span data-ttu-id="2142f-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2142f-p104">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="2142f-135">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2142f-135">Content-Type</span></span>  | <span data-ttu-id="2142f-136">application/json</span><span class="sxs-lookup"><span data-stu-id="2142f-136">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="2142f-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2142f-137">Request body</span></span>

<span data-ttu-id="2142f-138">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="2142f-138">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="2142f-139">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2142f-139">Parameter</span></span>    | <span data-ttu-id="2142f-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="2142f-140">Type</span></span>   |<span data-ttu-id="2142f-141">Description</span><span class="sxs-lookup"><span data-stu-id="2142f-141">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2142f-142">disableUserAccounts</span><span class="sxs-lookup"><span data-stu-id="2142f-142">disableUserAccounts</span></span>|<span data-ttu-id="2142f-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="2142f-143">Boolean</span></span>| <span data-ttu-id="2142f-144">Opción para deshabilitar las cuentas de usuario cuyo nombre ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="2142f-144">Option to disable renamed user accounts.</span></span> <span data-ttu-id="2142f-145">Si una cuenta de usuario está deshabilitada, el usuario no podrá iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="2142f-145">If a user account is disabled, the user will not be allowed to sign in.</span></span><br><span data-ttu-id="2142f-146">*Es true* (valor predeterminado) - usuario cambió como parte de una operación de cuentas están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="2142f-146">*True* (default) - User accounts renamed as part of this operation are disabled.</span></span><br><span data-ttu-id="2142f-147">*False* : las cuentas de usuario para cambiar el nombre como parte de esta operación no estén deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="2142f-147">*False* - User accounts renamed as part of this operation are not disabled.</span></span> |

## <a name="response"></a><span data-ttu-id="2142f-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2142f-148">Response</span></span>

<span data-ttu-id="2142f-149">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="2142f-149">If successful, this method returns `200 OK` response code.</span></span> 

## <a name="example"></a><span data-ttu-id="2142f-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2142f-150">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2142f-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2142f-151">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "domain_forcedelete"
}-->
```http
POST https://graph.microsoft.com/beta/domains/contoso.com/forceDelete
Content-type: application/json
Content-length: 33

{
  "disableUserAccounts": true
}
```

##### <a name="response"></a><span data-ttu-id="2142f-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2142f-152">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->

```http
HTTP/1.1 200 OK
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
