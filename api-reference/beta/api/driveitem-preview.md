---
title: 'driveItem: vista previa'
description: Esta acción le permite obtener corta duración puede incrustar las direcciones URL de un elemento con el fin de representar una vista previa temporal.
ms.openlocfilehash: 51432e53d6986e680dda8508ef0069c7713b3a9d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084600"
---
# <a name="driveitem-preview"></a><span data-ttu-id="ed4d4-103">driveItem: vista previa</span><span class="sxs-lookup"><span data-stu-id="ed4d4-103">driveItem: preview</span></span>

> <span data-ttu-id="ed4d4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ed4d4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ed4d4-106">Esta acción le permite obtener corta duración puede incrustar las direcciones URL de un elemento con el fin de representar una vista previa temporal.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-106">This action allows you to obtain short-lived embeddable URLs for an item in order to render a temporary preview.</span></span>

<span data-ttu-id="ed4d4-107">Si desea obtener vínculos puede incrustar larga duración, use la API [createLink][] en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-107">If you want to obtain long-lived embeddable links, use the [createLink][] API instead.</span></span>

> <span data-ttu-id="ed4d4-108">**Nota:** Actualmente, la acción de **vista previa** sólo está disponible en SharePoint y OneDrive para la empresa.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-108">**Note:** The **preview** action is currently only available on SharePoint and OneDrive for Business.</span></span>

[createLink]: driveitem-createlink.md

## <a name="permissions"></a><span data-ttu-id="ed4d4-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="ed4d4-110">Permissions</span></span>

<span data-ttu-id="ed4d4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ed4d4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ed4d4-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ed4d4-113">Permission type</span></span>                        | <span data-ttu-id="ed4d4-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ed4d4-114">Permissions (from least to most privileged)</span></span>
|:---------------------------------------|:-------------------------------------------
| <span data-ttu-id="ed4d4-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ed4d4-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="ed4d4-116">Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed4d4-116">Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>
| <span data-ttu-id="ed4d4-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ed4d4-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ed4d4-118">Files.Read, Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed4d4-118">Files.Read, Files.ReadWrite, Files.ReadWrite.All</span></span>
| <span data-ttu-id="ed4d4-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ed4d4-119">Application</span></span>                            | <span data-ttu-id="ed4d4-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-120">Not supported.</span></span>

## <a name="http-request"></a><span data-ttu-id="ed4d4-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ed4d4-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/preview
POST /groups/{groupId}/drive/items/{itemId}/preview
POST /me/drive/items/{itemId}/preview
POST /sites/{siteId}/drive/items/{itemId}/preview
POST /users/{userId}/drive/items/{itemId}/preview
POST /shares/{shareId}/driveItem/preview
```

## <a name="request-body"></a><span data-ttu-id="ed4d4-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ed4d4-122">Request body</span></span>

<span data-ttu-id="ed4d4-123">El cuerpo de la solicitud define las propiedades de la dirección URL puede incrustar está solicitando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-123">The body of the request defines properties of the embeddable URL your application is requesting.</span></span>
<span data-ttu-id="ed4d4-124">La solicitud debe ser un objeto JSON con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-124">The request should be a JSON object with the following properties.</span></span>

|   <span data-ttu-id="ed4d4-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="ed4d4-125">Name</span></span>      |  <span data-ttu-id="ed4d4-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed4d4-126">Type</span></span>         | <span data-ttu-id="ed4d4-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed4d4-127">Description</span></span>
|:------------|:--------------|:-----------------------------------------------
| <span data-ttu-id="ed4d4-128">Visor de</span><span class="sxs-lookup"><span data-stu-id="ed4d4-128">viewer</span></span>      | <span data-ttu-id="ed4d4-129">string</span><span class="sxs-lookup"><span data-stu-id="ed4d4-129">string</span></span>        | <span data-ttu-id="ed4d4-130">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-130">Optional.</span></span> <span data-ttu-id="ed4d4-131">Aplicación de vista previa para que utilice.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-131">Preview app to use.</span></span> <span data-ttu-id="ed4d4-132">`onedrive` o `office`.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-132">`onedrive` or `office`.</span></span> <span data-ttu-id="ed4d4-133">Si es null, se seleccionará automáticamente un visor adecuado.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-133">If null, a suitable viewer will be chosen automatically.</span></span>
| <span data-ttu-id="ed4d4-134">sin cromo</span><span class="sxs-lookup"><span data-stu-id="ed4d4-134">chromeless</span></span>  | <span data-ttu-id="ed4d4-135">boolean</span><span class="sxs-lookup"><span data-stu-id="ed4d4-135">boolean</span></span>       | <span data-ttu-id="ed4d4-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-136">Optional.</span></span> <span data-ttu-id="ed4d4-137">Si `true` (valor predeterminado), la vista incrustada no incluirá todos los controles.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-137">If `true` (default), the embedded view will not include any controls.</span></span>
| <span data-ttu-id="ed4d4-138">allowEdit</span><span class="sxs-lookup"><span data-stu-id="ed4d4-138">allowEdit</span></span>   | <span data-ttu-id="ed4d4-139">boolean</span><span class="sxs-lookup"><span data-stu-id="ed4d4-139">boolean</span></span>       | <span data-ttu-id="ed4d4-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-140">Optional.</span></span> <span data-ttu-id="ed4d4-141">Si `true`, se puede editar el archivo desde la interfaz de usuario incrustado.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-141">If `true`, the file can be edited from the embedded UI.</span></span>
| <span data-ttu-id="ed4d4-142">page</span><span class="sxs-lookup"><span data-stu-id="ed4d4-142">page</span></span>        | <span data-ttu-id="ed4d4-143">cadena o número</span><span class="sxs-lookup"><span data-stu-id="ed4d4-143">string/number</span></span> | <span data-ttu-id="ed4d4-144">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-144">Optional.</span></span> <span data-ttu-id="ed4d4-145">Número de página del documento para iniciar en, si procede.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-145">Page number of document to start at, if applicable.</span></span> <span data-ttu-id="ed4d4-146">Especificado como cadena para los casos de uso futuro alrededor de tipos de archivo como ZIP.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-146">Specified as string for future use cases around file types such as ZIP.</span></span>
| <span data-ttu-id="ed4d4-147">zoom</span><span class="sxs-lookup"><span data-stu-id="ed4d4-147">zoom</span></span>        | <span data-ttu-id="ed4d4-148">n?mero</span><span class="sxs-lookup"><span data-stu-id="ed4d4-148">number</span></span>        | <span data-ttu-id="ed4d4-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-149">Optional.</span></span> <span data-ttu-id="ed4d4-150">Aumentar nivel para iniciar en, si procede.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-150">Zoom level to start at, if applicable.</span></span>

## <a name="response"></a><span data-ttu-id="ed4d4-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed4d4-151">Response</span></span>

```json
{
    "getUrl": "https://www.onedrive.com/embed?foo=bar&bar=baz",
    "postParameters": "param1=value&param2=another%20value",
    "postUrl": "https://www.onedrive.com/embed_by_post"
}
```

<span data-ttu-id="ed4d4-152">La respuesta será un objeto JSON que contiene las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="ed4d4-152">The response will be a JSON object containing the following properties:</span></span>

| <span data-ttu-id="ed4d4-153">Nombre</span><span class="sxs-lookup"><span data-stu-id="ed4d4-153">Name</span></span>           | <span data-ttu-id="ed4d4-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed4d4-154">Type</span></span>   | <span data-ttu-id="ed4d4-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed4d4-155">Description</span></span>
|:---------------|:-------|:---------------------------------------------------
| <span data-ttu-id="ed4d4-156">getUrl</span><span class="sxs-lookup"><span data-stu-id="ed4d4-156">getUrl</span></span>         | <span data-ttu-id="ed4d4-157">string</span><span class="sxs-lookup"><span data-stu-id="ed4d4-157">string</span></span> | <span data-ttu-id="ed4d4-158">Dirección URL adecuada para incrustar mediante HTTP GET (IFRAME, etcetera).</span><span class="sxs-lookup"><span data-stu-id="ed4d4-158">URL suitable for embedding using HTTP GET (iframes, etc.)</span></span>
| <span data-ttu-id="ed4d4-159">URL para exponer</span><span class="sxs-lookup"><span data-stu-id="ed4d4-159">postUrl</span></span>        | <span data-ttu-id="ed4d4-160">string</span><span class="sxs-lookup"><span data-stu-id="ed4d4-160">string</span></span> | <span data-ttu-id="ed4d4-161">Dirección URL adecuada para incrustar el uso de HTTP POST (de envío de formulario, JS, etcetera.)</span><span class="sxs-lookup"><span data-stu-id="ed4d4-161">URL suitable for embedding using HTTP POST (form post, JS, etc.)</span></span>
| <span data-ttu-id="ed4d4-162">postParameters</span><span class="sxs-lookup"><span data-stu-id="ed4d4-162">postParameters</span></span> | <span data-ttu-id="ed4d4-163">string</span><span class="sxs-lookup"><span data-stu-id="ed4d4-163">string</span></span> | <span data-ttu-id="ed4d4-164">Parámetros de entrada para incluir si usa URL para exponer</span><span class="sxs-lookup"><span data-stu-id="ed4d4-164">POST parameters to include if using postUrl</span></span>

<span data-ttu-id="ed4d4-165">Es posible que se devolverá getUrl, URL para exponer o ambos según el estado actual del embed compatibilidad con las opciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-165">Either getUrl, postUrl, or both might be returned depending on the current state of embed support for the specified options.</span></span>

<span data-ttu-id="ed4d4-166">postParameters es una cadena con formato como `application/x-www-form-urlencoded`, y si se realiza una entrada a la URL para exponer el tipo de contenido se debe establecer en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-166">postParameters is a string formatted as `application/x-www-form-urlencoded`, and if performing a POST to the postUrl the content-type should be set accordingly.</span></span> <span data-ttu-id="ed4d4-167">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ed4d4-167">For example:</span></span>
```
POST https://www.onedrive.com/embed_by_post
Content-Type: application/x-www-form-urlencoded

param1=value&param2=another%20value
```

### <a name="viewers"></a><span data-ttu-id="ed4d4-168">Visores</span><span class="sxs-lookup"><span data-stu-id="ed4d4-168">Viewers</span></span>

<span data-ttu-id="ed4d4-169">Se permiten los siguientes valores para el parámetro **Visor** .</span><span class="sxs-lookup"><span data-stu-id="ed4d4-169">The following values are allowed for the **viewer** parameter.</span></span>

| <span data-ttu-id="ed4d4-170">Valor del tipo</span><span class="sxs-lookup"><span data-stu-id="ed4d4-170">Type value</span></span> | <span data-ttu-id="ed4d4-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed4d4-171">Description</span></span>
|:-----------|:----------------------------------------------------------------
| <span data-ttu-id="ed4d4-172">(null)</span><span class="sxs-lookup"><span data-stu-id="ed4d4-172">(null)</span></span>     | <span data-ttu-id="ed4d4-173">Elige una aplicación adecuada para representar el archivo.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-173">Chooses an appropriate app for rendering the file.</span></span> <span data-ttu-id="ed4d4-174">En la mayoría de los casos esto va a usar el `onedrive` controlador de vista previa, pero pueden variar según el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-174">In most cases this will use the `onedrive` previewer, but may vary by file type.</span></span>
| `onedrive` | <span data-ttu-id="ed4d4-175">Use la aplicación de vista previa de OneDrive para representar el archivo.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-175">Use the OneDrive previewer app to render the file.</span></span>
| `office`   | <span data-ttu-id="ed4d4-176">Use el WAC (Office online) para representar el archivo.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-176">Use the WAC (Office online) to render the file.</span></span> <span data-ttu-id="ed4d4-177">Sólo es válido para documentos de Office.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-177">Only valid for Office documents.</span></span>

### <a name="chrome-vs-chromeless"></a><span data-ttu-id="ed4d4-178">Cromo vs sin cromo</span><span class="sxs-lookup"><span data-stu-id="ed4d4-178">Chrome vs chromeless</span></span>

<span data-ttu-id="ed4d4-179">Si `chromeless` es true, la vista previa será una representación reconstrucción del archivo.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-179">If `chromeless` is true, the preview will be a bare rendering of the file.</span></span>
<span data-ttu-id="ed4d4-180">De lo contrario, puede haber otros barras de herramientas o botones que se muestran para interactuar con la vista de documento.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-180">Otherwise, there may be additional toolbars/buttons displayed for interacting with the document/view.</span></span>

### <a name="viewedit"></a><span data-ttu-id="ed4d4-181">Ver o modificar</span><span class="sxs-lookup"><span data-stu-id="ed4d4-181">View/edit</span></span>

<span data-ttu-id="ed4d4-182">Si `allowEdit` es true, el documento se puede modificar mediante la interacción del usuario con la vista previa incrustada.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-182">If `allowEdit` is true, the document can be modified by user interaction with the embedded preview.</span></span>
<span data-ttu-id="ed4d4-183">Esta función no esté disponible para todas las aplicaciones de la vista previa o tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-183">This capability may not be available for all preview apps or file types.</span></span>

### <a name="pagezoom"></a><span data-ttu-id="ed4d4-184">Página/zoom</span><span class="sxs-lookup"><span data-stu-id="ed4d4-184">Page/zoom</span></span>

<span data-ttu-id="ed4d4-185">El `page` y `zoom` opciones podrían no estar disponibles para todas las aplicaciones de vista previa, pero se aplicará si lo admite la aplicación de vista previa.</span><span class="sxs-lookup"><span data-stu-id="ed4d4-185">The `page` and `zoom` options might not be available for all preview apps, but will be applied if the preview app supports it.</span></span>
