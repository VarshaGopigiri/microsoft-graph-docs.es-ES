---
title: 'driveItem: vista previa'
description: Esta acción le permite obtener corta duración puede incrustar las direcciones URL de un elemento con el fin de representar una vista previa temporal.
localization_priority: Normal
ms.openlocfilehash: c04a73d514dfb5a92030c4c2016579d469063f9d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850774"
---
# <a name="driveitem-preview"></a><span data-ttu-id="3bcba-103">driveItem: vista previa</span><span class="sxs-lookup"><span data-stu-id="3bcba-103">driveItem: preview</span></span>

<span data-ttu-id="3bcba-104">Esta acción le permite obtener corta duración puede incrustar las direcciones URL de un elemento con el fin de representar una vista previa temporal.</span><span class="sxs-lookup"><span data-stu-id="3bcba-104">This action allows you to obtain short-lived embeddable URLs for an item in order to render a temporary preview.</span></span>

<span data-ttu-id="3bcba-105">Si desea obtener vínculos puede incrustar larga duración, use la API [createLink][] en su lugar.</span><span class="sxs-lookup"><span data-stu-id="3bcba-105">If you want to obtain long-lived embeddable links, use the [createLink][] API instead.</span></span>

> <span data-ttu-id="3bcba-106">**Nota:** Actualmente, la acción de **vista previa** sólo está disponible en SharePoint y OneDrive para la empresa.</span><span class="sxs-lookup"><span data-stu-id="3bcba-106">**Note:** The **preview** action is currently only available on SharePoint and OneDrive for Business.</span></span>

[createLink]: driveitem-createlink.md

## <a name="permissions"></a><span data-ttu-id="3bcba-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="3bcba-108">Permissions</span></span>

<span data-ttu-id="3bcba-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3bcba-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="3bcba-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3bcba-111">Permission type</span></span>                        | <span data-ttu-id="3bcba-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3bcba-112">Permissions (from least to most privileged)</span></span>
|:---------------------------------------|:-------------------------------------------
| <span data-ttu-id="3bcba-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3bcba-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="3bcba-114">Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3bcba-114">Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>
| <span data-ttu-id="3bcba-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3bcba-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3bcba-116">Files.Read, Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3bcba-116">Files.Read, Files.ReadWrite, Files.ReadWrite.All</span></span>
| <span data-ttu-id="3bcba-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3bcba-117">Application</span></span>                            | <span data-ttu-id="3bcba-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3bcba-118">Not supported.</span></span>

## <a name="http-request"></a><span data-ttu-id="3bcba-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3bcba-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/preview
POST /groups/{groupId}/drive/items/{itemId}/preview
POST /me/drive/items/{itemId}/preview
POST /sites/{siteId}/drive/items/{itemId}/preview
POST /users/{userId}/drive/items/{itemId}/preview
POST /shares/{shareId}/driveItem/preview
```

## <a name="request-body"></a><span data-ttu-id="3bcba-120">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3bcba-120">Request body</span></span>

<span data-ttu-id="3bcba-121">El cuerpo de la solicitud define las propiedades de la dirección URL puede incrustar está solicitando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3bcba-121">The body of the request defines properties of the embeddable URL your application is requesting.</span></span>
<span data-ttu-id="3bcba-122">La solicitud debe ser un objeto JSON con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="3bcba-122">The request should be a JSON object with the following properties.</span></span>

|   <span data-ttu-id="3bcba-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="3bcba-123">Name</span></span>      |  <span data-ttu-id="3bcba-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="3bcba-124">Type</span></span>         | <span data-ttu-id="3bcba-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bcba-125">Description</span></span>
|:------------|:--------------|:-----------------------------------------------
| <span data-ttu-id="3bcba-126">page</span><span class="sxs-lookup"><span data-stu-id="3bcba-126">page</span></span>        | <span data-ttu-id="3bcba-127">cadena o número</span><span class="sxs-lookup"><span data-stu-id="3bcba-127">string/number</span></span> | <span data-ttu-id="3bcba-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3bcba-128">Optional.</span></span> <span data-ttu-id="3bcba-129">Número de página del documento para iniciar en, si procede.</span><span class="sxs-lookup"><span data-stu-id="3bcba-129">Page number of document to start at, if applicable.</span></span> <span data-ttu-id="3bcba-130">Especificado como cadena para los casos de uso futuro alrededor de tipos de archivo como ZIP.</span><span class="sxs-lookup"><span data-stu-id="3bcba-130">Specified as string for future use cases around file types such as ZIP.</span></span>
| <span data-ttu-id="3bcba-131">zoom</span><span class="sxs-lookup"><span data-stu-id="3bcba-131">zoom</span></span>        | <span data-ttu-id="3bcba-132">number</span><span class="sxs-lookup"><span data-stu-id="3bcba-132">number</span></span>        | <span data-ttu-id="3bcba-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3bcba-133">Optional.</span></span> <span data-ttu-id="3bcba-134">Aumentar nivel para iniciar en, si procede.</span><span class="sxs-lookup"><span data-stu-id="3bcba-134">Zoom level to start at, if applicable.</span></span>

## <a name="response"></a><span data-ttu-id="3bcba-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3bcba-135">Response</span></span>

```json
{
    "getUrl": "https://www.onedrive.com/embed?foo=bar&bar=baz",
    "postParameters": "param1=value&param2=another%20value",
    "postUrl": "https://www.onedrive.com/embed_by_post"
}
```

<span data-ttu-id="3bcba-136">La respuesta será un objeto JSON que contiene las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="3bcba-136">The response will be a JSON object containing the following properties:</span></span>

| <span data-ttu-id="3bcba-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="3bcba-137">Name</span></span>           | <span data-ttu-id="3bcba-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="3bcba-138">Type</span></span>   | <span data-ttu-id="3bcba-139">Description</span><span class="sxs-lookup"><span data-stu-id="3bcba-139">Description</span></span>
|:---------------|:-------|:---------------------------------------------------
| <span data-ttu-id="3bcba-140">getUrl</span><span class="sxs-lookup"><span data-stu-id="3bcba-140">getUrl</span></span>         | <span data-ttu-id="3bcba-141">string</span><span class="sxs-lookup"><span data-stu-id="3bcba-141">string</span></span> | <span data-ttu-id="3bcba-142">Dirección URL adecuada para incrustar mediante HTTP GET (IFRAME, etcetera).</span><span class="sxs-lookup"><span data-stu-id="3bcba-142">URL suitable for embedding using HTTP GET (iframes, etc.)</span></span>
| <span data-ttu-id="3bcba-143">URL para exponer</span><span class="sxs-lookup"><span data-stu-id="3bcba-143">postUrl</span></span>        | <span data-ttu-id="3bcba-144">string</span><span class="sxs-lookup"><span data-stu-id="3bcba-144">string</span></span> | <span data-ttu-id="3bcba-145">Dirección URL adecuada para incrustar el uso de HTTP POST (de envío de formulario, JS, etcetera.)</span><span class="sxs-lookup"><span data-stu-id="3bcba-145">URL suitable for embedding using HTTP POST (form post, JS, etc.)</span></span>
| <span data-ttu-id="3bcba-146">postParameters</span><span class="sxs-lookup"><span data-stu-id="3bcba-146">postParameters</span></span> | <span data-ttu-id="3bcba-147">string</span><span class="sxs-lookup"><span data-stu-id="3bcba-147">string</span></span> | <span data-ttu-id="3bcba-148">Parámetros de entrada para incluir si usa URL para exponer</span><span class="sxs-lookup"><span data-stu-id="3bcba-148">POST parameters to include if using postUrl</span></span>

<span data-ttu-id="3bcba-149">Es posible que se devolverá getUrl, URL para exponer o ambos según el estado actual del embed compatibilidad con las opciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="3bcba-149">Either getUrl, postUrl, or both might be returned depending on the current state of embed support for the specified options.</span></span>

<span data-ttu-id="3bcba-150">postParameters es una cadena con formato como `application/x-www-form-urlencoded`, y si se realiza una entrada a la URL para exponer el tipo de contenido se debe establecer en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="3bcba-150">postParameters is a string formatted as `application/x-www-form-urlencoded`, and if performing a POST to the postUrl the content-type should be set accordingly.</span></span> <span data-ttu-id="3bcba-151">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3bcba-151">For example:</span></span>
```
POST https://www.onedrive.com/embed_by_post
Content-Type: application/x-www-form-urlencoded

param1=value&param2=another%20value
```

### <a name="pagezoom"></a><span data-ttu-id="3bcba-152">Página/zoom</span><span class="sxs-lookup"><span data-stu-id="3bcba-152">Page/zoom</span></span>

<span data-ttu-id="3bcba-153">Las opciones de 'zoom' y 'page' podrían no estar disponibles para todas las aplicaciones de vista previa, pero se aplicará si lo admite la aplicación de vista previa.</span><span class="sxs-lookup"><span data-stu-id="3bcba-153">The 'page' and 'zoom' options may not be available for all preview apps, but will be applied if the preview app supports it.</span></span>
