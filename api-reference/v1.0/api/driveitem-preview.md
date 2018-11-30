---
title: 'driveItem: vista previa'
description: Esta acción le permite obtener corta duración puede incrustar las direcciones URL de un elemento con el fin de representar una vista previa temporal.
ms.openlocfilehash: 741e449c972ad372aae30d9921cdb3b7fa1fc40d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031495"
---
# <a name="driveitem-preview"></a><span data-ttu-id="997a9-103">driveItem: vista previa</span><span class="sxs-lookup"><span data-stu-id="997a9-103">driveItem: preview</span></span>

<span data-ttu-id="997a9-104">Esta acción le permite obtener corta duración puede incrustar las direcciones URL de un elemento con el fin de representar una vista previa temporal.</span><span class="sxs-lookup"><span data-stu-id="997a9-104">This action allows you to obtain short-lived embeddable URLs for an item in order to render a temporary preview.</span></span>

<span data-ttu-id="997a9-105">Si desea obtener vínculos puede incrustar larga duración, use la API [createLink][] en su lugar.</span><span class="sxs-lookup"><span data-stu-id="997a9-105">If you want to obtain long-lived embeddable links, use the [createLink][] API instead.</span></span>

> <span data-ttu-id="997a9-106">**Nota:** Actualmente, la acción de **vista previa** sólo está disponible en SharePoint y OneDrive para la empresa.</span><span class="sxs-lookup"><span data-stu-id="997a9-106">**Note:** The **preview** action is currently only available on SharePoint and OneDrive for Business.</span></span>

[createLink]: driveitem-createlink.md

## <a name="permissions"></a><span data-ttu-id="997a9-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="997a9-108">Permissions</span></span>

<span data-ttu-id="997a9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="997a9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="997a9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="997a9-111">Permission type</span></span>                        | <span data-ttu-id="997a9-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="997a9-112">Permissions (from least to most privileged)</span></span>
|:---------------------------------------|:-------------------------------------------
| <span data-ttu-id="997a9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="997a9-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="997a9-114">Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="997a9-114">Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>
| <span data-ttu-id="997a9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="997a9-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="997a9-116">Files.Read, Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="997a9-116">Files.Read, Files.ReadWrite, Files.ReadWrite.All</span></span>
| <span data-ttu-id="997a9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="997a9-117">Application</span></span>                            | <span data-ttu-id="997a9-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="997a9-118">Not supported.</span></span>

## <a name="http-request"></a><span data-ttu-id="997a9-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="997a9-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/preview
POST /groups/{groupId}/drive/items/{itemId}/preview
POST /me/drive/items/{itemId}/preview
POST /sites/{siteId}/drive/items/{itemId}/preview
POST /users/{userId}/drive/items/{itemId}/preview
POST /shares/{shareId}/driveItem/preview
```

## <a name="request-body"></a><span data-ttu-id="997a9-120">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="997a9-120">Request body</span></span>

<span data-ttu-id="997a9-121">El cuerpo de la solicitud define las propiedades de la dirección URL puede incrustar está solicitando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="997a9-121">The body of the request defines properties of the embeddable URL your application is requesting.</span></span>
<span data-ttu-id="997a9-122">La solicitud debe ser un objeto JSON con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="997a9-122">The request should be a JSON object with the following properties.</span></span>

|   <span data-ttu-id="997a9-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="997a9-123">Name</span></span>      |  <span data-ttu-id="997a9-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="997a9-124">Type</span></span>         | <span data-ttu-id="997a9-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="997a9-125">Description</span></span>
|:------------|:--------------|:-----------------------------------------------
| <span data-ttu-id="997a9-126">page</span><span class="sxs-lookup"><span data-stu-id="997a9-126">page</span></span>        | <span data-ttu-id="997a9-127">cadena o número</span><span class="sxs-lookup"><span data-stu-id="997a9-127">string/number</span></span> | <span data-ttu-id="997a9-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="997a9-128">Optional.</span></span> <span data-ttu-id="997a9-129">Número de página del documento para iniciar en, si procede.</span><span class="sxs-lookup"><span data-stu-id="997a9-129">Page number of document to start at, if applicable.</span></span> <span data-ttu-id="997a9-130">Especificado como cadena para los casos de uso futuro alrededor de tipos de archivo como ZIP.</span><span class="sxs-lookup"><span data-stu-id="997a9-130">Specified as string for future use cases around file types such as ZIP.</span></span>
| <span data-ttu-id="997a9-131">zoom</span><span class="sxs-lookup"><span data-stu-id="997a9-131">zoom</span></span>        | <span data-ttu-id="997a9-132">n?mero</span><span class="sxs-lookup"><span data-stu-id="997a9-132">number</span></span>        | <span data-ttu-id="997a9-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="997a9-133">Optional.</span></span> <span data-ttu-id="997a9-134">Aumentar nivel para iniciar en, si procede.</span><span class="sxs-lookup"><span data-stu-id="997a9-134">Zoom level to start at, if applicable.</span></span>

## <a name="response"></a><span data-ttu-id="997a9-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="997a9-135">Response</span></span>

```json
{
    "getUrl": "https://www.onedrive.com/embed?foo=bar&bar=baz",
    "postParameters": "param1=value&param2=another%20value",
    "postUrl": "https://www.onedrive.com/embed_by_post"
}
```

<span data-ttu-id="997a9-136">La respuesta será un objeto JSON que contiene las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="997a9-136">The response will be a JSON object containing the following properties:</span></span>

| <span data-ttu-id="997a9-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="997a9-137">Name</span></span>           | <span data-ttu-id="997a9-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="997a9-138">Type</span></span>   | <span data-ttu-id="997a9-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="997a9-139">Description</span></span>
|:---------------|:-------|:---------------------------------------------------
| <span data-ttu-id="997a9-140">getUrl</span><span class="sxs-lookup"><span data-stu-id="997a9-140">getUrl</span></span>         | <span data-ttu-id="997a9-141">string</span><span class="sxs-lookup"><span data-stu-id="997a9-141">string</span></span> | <span data-ttu-id="997a9-142">Dirección URL adecuada para incrustar mediante HTTP GET (IFRAME, etcetera).</span><span class="sxs-lookup"><span data-stu-id="997a9-142">URL suitable for embedding using HTTP GET (iframes, etc.)</span></span>
| <span data-ttu-id="997a9-143">URL para exponer</span><span class="sxs-lookup"><span data-stu-id="997a9-143">postUrl</span></span>        | <span data-ttu-id="997a9-144">string</span><span class="sxs-lookup"><span data-stu-id="997a9-144">string</span></span> | <span data-ttu-id="997a9-145">Dirección URL adecuada para incrustar el uso de HTTP POST (de envío de formulario, JS, etcetera.)</span><span class="sxs-lookup"><span data-stu-id="997a9-145">URL suitable for embedding using HTTP POST (form post, JS, etc.)</span></span>
| <span data-ttu-id="997a9-146">postParameters</span><span class="sxs-lookup"><span data-stu-id="997a9-146">postParameters</span></span> | <span data-ttu-id="997a9-147">string</span><span class="sxs-lookup"><span data-stu-id="997a9-147">string</span></span> | <span data-ttu-id="997a9-148">Parámetros de entrada para incluir si usa URL para exponer</span><span class="sxs-lookup"><span data-stu-id="997a9-148">POST parameters to include if using postUrl</span></span>

<span data-ttu-id="997a9-149">Es posible que se devolverá getUrl, URL para exponer o ambos según el estado actual del embed compatibilidad con las opciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="997a9-149">Either getUrl, postUrl, or both might be returned depending on the current state of embed support for the specified options.</span></span>

<span data-ttu-id="997a9-150">postParameters es una cadena con formato como `application/x-www-form-urlencoded`, y si se realiza una entrada a la URL para exponer el tipo de contenido se debe establecer en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="997a9-150">postParameters is a string formatted as `application/x-www-form-urlencoded`, and if performing a POST to the postUrl the content-type should be set accordingly.</span></span> <span data-ttu-id="997a9-151">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="997a9-151">For example:</span></span>
```
POST https://www.onedrive.com/embed_by_post
Content-Type: application/x-www-form-urlencoded

param1=value&param2=another%20value
```

### <a name="pagezoom"></a><span data-ttu-id="997a9-152">Página/zoom</span><span class="sxs-lookup"><span data-stu-id="997a9-152">Page/zoom</span></span>

<span data-ttu-id="997a9-153">Las opciones de 'zoom' y 'page' podrían no estar disponibles para todas las aplicaciones de vista previa, pero se aplicará si lo admite la aplicación de vista previa.</span><span class="sxs-lookup"><span data-stu-id="997a9-153">The 'page' and 'zoom' options may not be available for all preview apps, but will be applied if the preview app supports it.</span></span>
