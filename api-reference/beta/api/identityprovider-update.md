---
title: Actualizar identityProvider
description: Actualizar las propiedades en un identityProvider existente.
localization_priority: Normal
ms.openlocfilehash: ebe49fb562f77004edfa3504130fbf50f4d40003
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832812"
---
# <a name="update-identityprovider"></a><span data-ttu-id="a803d-103">Actualizar identityProvider</span><span class="sxs-lookup"><span data-stu-id="a803d-103">Update identityProvider</span></span>

> <span data-ttu-id="a803d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a803d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a803d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a803d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a803d-106">Actualizar las propiedades en una existente [identityProvider](../resources/identityprovider.md).</span><span class="sxs-lookup"><span data-stu-id="a803d-106">Update properties in an existing [identityProvider](../resources/identityprovider.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="a803d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a803d-107">Permissions</span></span>

<span data-ttu-id="a803d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a803d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a803d-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a803d-110">Permission type</span></span>      | <span data-ttu-id="a803d-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a803d-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a803d-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a803d-112">Delegated (work or school account)</span></span>|<span data-ttu-id="a803d-113">IdentityProvider.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a803d-113">IdentityProvider.ReadWrite.All</span></span>|
|<span data-ttu-id="a803d-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a803d-114">Delegated (personal Microsoft account)</span></span>| <span data-ttu-id="a803d-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a803d-115">Not supported.</span></span>|
|<span data-ttu-id="a803d-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a803d-116">Application</span></span>|<span data-ttu-id="a803d-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a803d-117">Not supported.</span></span>|

<span data-ttu-id="a803d-118">La cuenta de trabajo o escuela debe ser un administrador global del inquilino.</span><span class="sxs-lookup"><span data-stu-id="a803d-118">The work or school account must be a global administrator of the tenant.</span></span>

## <a name="http-request"></a><span data-ttu-id="a803d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a803d-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH /identityProviders/{id}
```

## <a name="request-headers"></a><span data-ttu-id="a803d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a803d-120">Request headers</span></span>

|<span data-ttu-id="a803d-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="a803d-121">Name</span></span>|<span data-ttu-id="a803d-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a803d-122">Description</span></span>|
|:---------------|:----------|
|<span data-ttu-id="a803d-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a803d-123">Authorization</span></span>|<span data-ttu-id="a803d-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a803d-p103">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="a803d-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a803d-126">Content-Type</span></span>|<span data-ttu-id="a803d-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a803d-p104">application/json. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="a803d-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a803d-129">Request body</span></span>

<span data-ttu-id="a803d-130">En el cuerpo de la solicitud, proporcione un objeto JSON con una o varias propiedades que necesitan actualizarse.</span><span class="sxs-lookup"><span data-stu-id="a803d-130">In the request body, provide a JSON object with one or more properties that need to be updated.</span></span>

|<span data-ttu-id="a803d-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a803d-131">Property</span></span>|<span data-ttu-id="a803d-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="a803d-132">Type</span></span>|<span data-ttu-id="a803d-133">Description</span><span class="sxs-lookup"><span data-stu-id="a803d-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a803d-134">clientId</span><span class="sxs-lookup"><span data-stu-id="a803d-134">clientId</span></span>|<span data-ttu-id="a803d-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="a803d-135">String</span></span>|<span data-ttu-id="a803d-136">El identificador de cliente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a803d-136">The client ID for the application.</span></span> <span data-ttu-id="a803d-137">Este es el identificador de cliente que se obtuvieron cuando se registra la aplicación con el proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="a803d-137">This is the client ID obtained when registering the application with the identity provider.</span></span>|
|<span data-ttu-id="a803d-138">clientSecret</span><span class="sxs-lookup"><span data-stu-id="a803d-138">clientSecret</span></span>|<span data-ttu-id="a803d-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="a803d-139">String</span></span>|<span data-ttu-id="a803d-140">El secreto de cliente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a803d-140">The client secret for the application.</span></span> <span data-ttu-id="a803d-141">Este es el secreto de cliente que se obtuvieron cuando se registra la aplicación con el proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="a803d-141">This is the client secret obtained when registering the application with the identity provider.</span></span>|
|<span data-ttu-id="a803d-142">name</span><span class="sxs-lookup"><span data-stu-id="a803d-142">name</span></span>|<span data-ttu-id="a803d-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="a803d-143">String</span></span>|<span data-ttu-id="a803d-144">El nombre para mostrar del proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="a803d-144">The display name of the identity provider.</span></span>|

## <a name="response"></a><span data-ttu-id="a803d-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a803d-145">Response</span></span>

<span data-ttu-id="a803d-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="a803d-146">If successful, this method returns `204 No Content` response code.</span></span> <span data-ttu-id="a803d-147">Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.</span><span class="sxs-lookup"><span data-stu-id="a803d-147">If unsuccessful, a `4xx` error will be returned with specific details.</span></span>

## <a name="example"></a><span data-ttu-id="a803d-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a803d-148">Example</span></span>

<span data-ttu-id="a803d-149">En el ejemplo siguiente se actualiza la definición de la duración del token **identityProvider** y se establece como el valor predeterminado de la organización.</span><span class="sxs-lookup"><span data-stu-id="a803d-149">The following example updates the definition of the token lifetime **identityProvider** and sets it as the organization default.</span></span>

##### <a name="request"></a><span data-ttu-id="a803d-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a803d-150">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_identityprovider"
}-->
```http
PATCH https://graph.microsoft.com/beta/identityProviders/Amazon-OAuth
Content-type: application/json
Content-length: 41

{
    "clientSecret": "1111111111111"
}
```

##### <a name="response"></a><span data-ttu-id="a803d-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a803d-151">Response</span></span>

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
  "description": "Update identityProvider",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
