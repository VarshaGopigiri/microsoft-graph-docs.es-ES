---
title: Crear identityProvider
description: Crear un nuevo identityProvider especificando el nombre para mostrar, identityProvider tipo, identificador de cliente y el secreto de cliente.
ms.openlocfilehash: 8786cbf6676567a0c6aaef5bf497f50cff1ce9a4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087693"
---
# <a name="create-identityprovider"></a><span data-ttu-id="5031e-103">Crear identityProvider</span><span class="sxs-lookup"><span data-stu-id="5031e-103">Create identityProvider</span></span>

> <span data-ttu-id="5031e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5031e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5031e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5031e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5031e-106">Crear un nuevo [identityProvider](../resources/identityprovider.md) especificando el nombre para mostrar, identityProvider tipo, identificador de cliente y el secreto de cliente.</span><span class="sxs-lookup"><span data-stu-id="5031e-106">Create a new [identityProvider](../resources/identityprovider.md) by specifying display name, identityProvider type, client ID, and client secret.</span></span>

## <a name="permissions"></a><span data-ttu-id="5031e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5031e-107">Permissions</span></span>

<span data-ttu-id="5031e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5031e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5031e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5031e-110">Permission type</span></span>      | <span data-ttu-id="5031e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5031e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5031e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5031e-112">Delegated (work or school account)</span></span>|<span data-ttu-id="5031e-113">IdentityProvider.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5031e-113">IdentityProvider.ReadWrite.All</span></span>|
|<span data-ttu-id="5031e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5031e-114">Delegated (personal Microsoft account)</span></span>| <span data-ttu-id="5031e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5031e-115">Not supported.</span></span>|
|<span data-ttu-id="5031e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5031e-116">Application</span></span>|<span data-ttu-id="5031e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5031e-117">Not supported.</span></span>|

<span data-ttu-id="5031e-118">La cuenta de trabajo o escuela debe ser un administrador global del inquilino.</span><span class="sxs-lookup"><span data-stu-id="5031e-118">The work or school account must be a global administrator of the tenant.</span></span>

## <a name="http-request"></a><span data-ttu-id="5031e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5031e-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /identityProviders
```

## <a name="request-headers"></a><span data-ttu-id="5031e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5031e-120">Request headers</span></span>

|<span data-ttu-id="5031e-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="5031e-121">Name</span></span>|<span data-ttu-id="5031e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5031e-122">Description</span></span>|
|:---------------|:----------|
|<span data-ttu-id="5031e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="5031e-123">Authorization</span></span>|<span data-ttu-id="5031e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5031e-p103">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="5031e-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5031e-126">Content-Type</span></span>|<span data-ttu-id="5031e-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5031e-p104">application/json. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="5031e-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5031e-129">Request body</span></span>

<span data-ttu-id="5031e-130">En el cuerpo de la solicitud, proporcionan una representación JSON del objeto [identityProvider](../resources/identityprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="5031e-130">In the request body, provide a JSON representation of [identityProvider](../resources/identityprovider.md) object.</span></span> <span data-ttu-id="5031e-131">Todas las propiedades enumeradas en la siguiente tabla son necesarias.</span><span class="sxs-lookup"><span data-stu-id="5031e-131">All the properties listed in the following table are required.</span></span>

|<span data-ttu-id="5031e-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5031e-132">Property</span></span>|<span data-ttu-id="5031e-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="5031e-133">Type</span></span>|<span data-ttu-id="5031e-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="5031e-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5031e-135">clientId</span><span class="sxs-lookup"><span data-stu-id="5031e-135">clientId</span></span>|<span data-ttu-id="5031e-136">String</span><span class="sxs-lookup"><span data-stu-id="5031e-136">String</span></span>|<span data-ttu-id="5031e-137">El identificador de cliente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5031e-137">The client ID for the application.</span></span> <span data-ttu-id="5031e-138">Este es el identificador de cliente que se obtuvieron cuando se registra la aplicación con el proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="5031e-138">This is the client ID obtained when registering the application with the identity provider.</span></span>|
|<span data-ttu-id="5031e-139">clientSecret</span><span class="sxs-lookup"><span data-stu-id="5031e-139">clientSecret</span></span>|<span data-ttu-id="5031e-140">String</span><span class="sxs-lookup"><span data-stu-id="5031e-140">String</span></span>|<span data-ttu-id="5031e-141">El secreto de cliente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5031e-141">The client secret for the application.</span></span> <span data-ttu-id="5031e-142">Este es el secreto de cliente que se obtuvieron cuando se registra la aplicación con el proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="5031e-142">This is the client secret obtained when registering the application with the identity provider.</span></span>|
|<span data-ttu-id="5031e-143">name</span><span class="sxs-lookup"><span data-stu-id="5031e-143">name</span></span>|<span data-ttu-id="5031e-144">String</span><span class="sxs-lookup"><span data-stu-id="5031e-144">String</span></span>|<span data-ttu-id="5031e-145">El nombre para mostrar del proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="5031e-145">The display name of the identity provider.</span></span>|
|<span data-ttu-id="5031e-146">type</span><span class="sxs-lookup"><span data-stu-id="5031e-146">type</span></span>|<span data-ttu-id="5031e-147">String</span><span class="sxs-lookup"><span data-stu-id="5031e-147">String</span></span>|<span data-ttu-id="5031e-148">El tipo de proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="5031e-148">The identity provider type.</span></span> <span data-ttu-id="5031e-149">Debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5031e-149">It must be one of the following values:</span></span> <ul><li/><span data-ttu-id="5031e-150">Microsoft</span><span class="sxs-lookup"><span data-stu-id="5031e-150">Microsoft</span></span><li/><span data-ttu-id="5031e-151">Google</span><span class="sxs-lookup"><span data-stu-id="5031e-151">Google</span></span><li/><span data-ttu-id="5031e-152">Amazon</span><span class="sxs-lookup"><span data-stu-id="5031e-152">Amazon</span></span><li/><span data-ttu-id="5031e-153">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="5031e-153">LinkedIn</span></span><li/><span data-ttu-id="5031e-154">Facebook</span><span class="sxs-lookup"><span data-stu-id="5031e-154">Facebook</span></span></ul>|

## <a name="response"></a><span data-ttu-id="5031e-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5031e-155">Response</span></span>

<span data-ttu-id="5031e-156">Si tiene éxito, este método devuelve `201 Created` objeto de código y [identityProvider](../resources/identityprovider.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5031e-156">If successful, this method returns `201 Created` response code and [identityProvider](../resources/identityprovider.md) object in the response body.</span></span> <span data-ttu-id="5031e-157">Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.</span><span class="sxs-lookup"><span data-stu-id="5031e-157">If unsuccessful, a `4xx` error will be returned with specific details.</span></span>

## <a name="example"></a><span data-ttu-id="5031e-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5031e-158">Example</span></span>

<span data-ttu-id="5031e-159">En el ejemplo siguiente se crea un **identityProvider**.</span><span class="sxs-lookup"><span data-stu-id="5031e-159">The following example creates an **identityProvider**.</span></span>

##### <a name="request"></a><span data-ttu-id="5031e-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5031e-160">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_identityprovider_from_identityproviders"
}-->
```http
POST https://graph.microsoft.com/beta/identityProviders
Content-type: application/json

{
    "name": "Login with Amazon",
    "type": "Amazon",
    "clientId": "56433757-cadd-4135-8431-2c9e3fd68ae8",
    "clientSecret": "000000000000"
}
```

##### <a name="response"></a><span data-ttu-id="5031e-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5031e-161">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.IdentityProvider"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "id": "Amazon-OAUTH",
    "name": "Login with Amazon",
    "type": "Amazon",
    "clientId": "56433757-cadd-4135-8431-2c9e3fd68ae8",
    "clientSecret": "*****"
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create identityProvider",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
