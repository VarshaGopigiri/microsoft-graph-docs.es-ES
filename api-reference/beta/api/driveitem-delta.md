---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Sincronizar el contenido de una unidad
ms.openlocfilehash: 4ccaec230d5801f563f81e6a30584db9f7ed5714
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084625"
---
# <a name="track-changes-for-a-drive"></a><span data-ttu-id="43b6c-102">Control de cambios de una unidad</span><span class="sxs-lookup"><span data-stu-id="43b6c-102">Track changes for a Drive</span></span>

> <span data-ttu-id="43b6c-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="43b6c-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="43b6c-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="43b6c-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="43b6c-105">Este método permite que su aplicación realice el control de cambios de una unidad y de sus elementos secundarios con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="43b6c-105">This method allows your app to track changes to a drive and its children over time.</span></span>

<span data-ttu-id="43b6c-p102">La aplicación comienza llamando a `delta` sin ningún parámetro. El servicio comienza enumerando la jerarquía de la unidad, devuelve páginas de elementos y también `@odata.nextLink` o `@odata.deltaLink`, tal y como se describe a continuación. La aplicación debe continuar la llamada con `@odata.nextLink` hasta que ya no se devuelva `@odata.nextLink` o hasta que la respuesta contenga un conjunto de cambios vacío.</span><span class="sxs-lookup"><span data-stu-id="43b6c-p102">Your app begins by calling `delta` without any parameters. The service starts enumerating the drive's hierarchy, returning pages of items and either an `@odata.nextLink` or an `@odata.deltaLink`, as described below. Your app should continue calling with the `@odata.nextLink` until you no longer see an `@odata.nextLink` returned, or you see a response with an empty set of changes.</span></span>

<span data-ttu-id="43b6c-p103">Una vez que termine de recibir todos los cambios, puede aplicarlos a su estado local. Para comprobar si hay cambios en el futuro, llame a `delta` con el `@odata.deltaLink` de la respuesta anterior.</span><span class="sxs-lookup"><span data-stu-id="43b6c-p103">After you have finished receiving all the changes, you may apply them to your local state. To check for changes in the future, call `delta` again with the `@odata.deltaLink` from the previous response.</span></span>

<span data-ttu-id="43b6c-p104">Los elementos eliminados se devuelven con la [`deleted`faceta](../resources/deleted.md). Los elementos con este conjunto de propiedades deben ser eliminados de su estado local.</span><span class="sxs-lookup"><span data-stu-id="43b6c-p104">Deleted items are returned with the [`deleted` facet](../resources/deleted.md). Items with this property set should be removed from your local state.</span></span> 

<span data-ttu-id="43b6c-113">**Nota:** Solo debe eliminar una carpeta de forma local si está vacía después de sincronizar todos los cambios.</span><span class="sxs-lookup"><span data-stu-id="43b6c-113">**Note:** you should only delete a folder locally if it is empty after syncing all the changes.</span></span>

## <a name="permissions"></a><span data-ttu-id="43b6c-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="43b6c-114">Permissions</span></span>

<span data-ttu-id="43b6c-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="43b6c-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="43b6c-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="43b6c-117">Permission type</span></span>      | <span data-ttu-id="43b6c-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="43b6c-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="43b6c-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="43b6c-119">Delegated (work or school account)</span></span> | <span data-ttu-id="43b6c-120">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="43b6c-120">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="43b6c-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="43b6c-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="43b6c-122">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="43b6c-122">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="43b6c-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="43b6c-123">Application</span></span> | <span data-ttu-id="43b6c-124">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="43b6c-124">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="43b6c-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="43b6c-125">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/root/delta
GET /groups/{groupId}/drive/root/delta
GET /me/drive/root/delta
GET /sites/{siteId}/drive/root/delta
GET /users/{userId}/drive/root/delta
```

## <a name="function-parameters"></a><span data-ttu-id="43b6c-126">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="43b6c-126">Function parameters</span></span>

| <span data-ttu-id="43b6c-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="43b6c-127">Name</span></span>   | <span data-ttu-id="43b6c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="43b6c-128">Value</span></span>  | <span data-ttu-id="43b6c-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="43b6c-129">Description</span></span>                                                                                                                          |
|:-------|:-------|:-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43b6c-130">token</span><span class="sxs-lookup"><span data-stu-id="43b6c-130">token</span></span>  | <span data-ttu-id="43b6c-131">string</span><span class="sxs-lookup"><span data-stu-id="43b6c-131">string</span></span> | <span data-ttu-id="43b6c-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="43b6c-132">Optional.</span></span> <span data-ttu-id="43b6c-133">Si no se especifica, enumera el estado actual de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="43b6c-133">If unspecified, enumerates the hierarchy's current state.</span></span> <span data-ttu-id="43b6c-134">Si `latest`, devuelve vacío respuesta con un símbolo (token) delta más reciente.</span><span class="sxs-lookup"><span data-stu-id="43b6c-134">If `latest`, returns empty response with latest delta token.</span></span> <span data-ttu-id="43b6c-135">Si un token de delta anterior, devuelve el nuevo estado desde ese token.</span><span class="sxs-lookup"><span data-stu-id="43b6c-135">If a previous delta token, returns new state since that token.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="43b6c-136">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="43b6c-136">Optional query parameters</span></span>

<span data-ttu-id="43b6c-137">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$select`, `$expand` y `$top` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43b6c-137">This method supports the `$select`, `$expand`, and `$top` [OData query parameters](/graph/query-parameters) to customize the response.</span></span>

## <a name="response"></a><span data-ttu-id="43b6c-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43b6c-138">Response</span></span>

<span data-ttu-id="43b6c-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de recursos [DriveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43b6c-139">If successful, this method returns a `200 OK` response code and a collection of [DriveItem](../resources/driveitem.md) resources in the response body.</span></span>

<span data-ttu-id="43b6c-140">Además de la colección de DriveItems, la respuesta también incluirá una de las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="43b6c-140">In addition to the collection of DriveItems, the response will also include one of the following properties:</span></span>

| <span data-ttu-id="43b6c-141">Nombre</span><span class="sxs-lookup"><span data-stu-id="43b6c-141">Name</span></span>                 | <span data-ttu-id="43b6c-142">Valor</span><span class="sxs-lookup"><span data-stu-id="43b6c-142">Value</span></span>  | <span data-ttu-id="43b6c-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="43b6c-143">Description</span></span>                                                                                                                                      |
|:---------------------|:-------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43b6c-144">**@odata.nextLink**</span><span class="sxs-lookup"><span data-stu-id="43b6c-144">**@odata.nextLink**</span></span>  | <span data-ttu-id="43b6c-145">url</span><span class="sxs-lookup"><span data-stu-id="43b6c-145">url</span></span>    | <span data-ttu-id="43b6c-146">Una dirección URL que recupera la siguiente página de cambios disponible, si hay cambios adicionales en el conjunto actual.</span><span class="sxs-lookup"><span data-stu-id="43b6c-146">A URL to retrieve the next available page of changes, if there are additional changes in the current set.</span></span>                                        |
| <span data-ttu-id="43b6c-147">**@odata.deltaLink**</span><span class="sxs-lookup"><span data-stu-id="43b6c-147">**@odata.deltaLink**</span></span> | <span data-ttu-id="43b6c-148">url</span><span class="sxs-lookup"><span data-stu-id="43b6c-148">url</span></span>    | <span data-ttu-id="43b6c-p107">Una dirección URL que se devuelve en lugar de **@odata.nextLink** cuando se han devuelto todos los cambios actuales. Se utiliza para leer el siguiente conjunto de cambios en el futuro.</span><span class="sxs-lookup"><span data-stu-id="43b6c-p107">A URL returned instead of **@odata.nextLink** after all current changes have been returned. Used to read the next set of changes in the future.</span></span>  |

## <a name="example-initial-request"></a><span data-ttu-id="43b6c-151">Ejemplo (solicitud inicial)</span><span class="sxs-lookup"><span data-stu-id="43b6c-151">Example (Initial Request)</span></span>

<span data-ttu-id="43b6c-152">Aquí tiene un ejemplo de cómo llamar a esta API para establecer su estado local.</span><span class="sxs-lookup"><span data-stu-id="43b6c-152">Here is an example of how to call this API to establish your local state.</span></span>

### <a name="request"></a><span data-ttu-id="43b6c-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="43b6c-153">Request</span></span>

<span data-ttu-id="43b6c-154">Aquí tiene un ejemplo de la solicitud inicial.</span><span class="sxs-lookup"><span data-stu-id="43b6c-154">Here is an example of the initial request.</span></span>

<!-- { "blockType": "request", "name": "get_item_delta_first" } -->

```http
GET https://graph.microsoft.com/v1.0/me/drive/root/delta
```

### <a name="response"></a><span data-ttu-id="43b6c-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43b6c-155">Response</span></span>

<span data-ttu-id="43b6c-156">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43b6c-156">Here is an example of the response.</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItem)", "truncated": true, "scope": "file.read" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "0123456789abc",
            "name": "folder2",
            "folder": { }
        },
        {
            "id": "123010204abac",
            "name": "file.txt",
            "file": { }
        },
        {
            "id": "2353010204ddgg",
            "name": "file5.txt",
            "deleted": { }
        }
    ],
    "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/drive/delta(token=1230919asd190410jlka)"
}
```

<span data-ttu-id="43b6c-p108">Esta respuesta incluye la primera página de cambios y la propiedad **@odata.nextLink** indica que hay más elementos disponibles en el conjunto actual de elementos. Su aplicación debe continuar solicitando el valor de dirección URL **@odata.nextLink** hasta que se recuperen todas las páginas de elementos.</span><span class="sxs-lookup"><span data-stu-id="43b6c-p108">This response includes the first page of changes, and the **@odata.nextLink** property indicates that there are more items available in the current set of items. Your app should continue to request the URL value of **@odata.nextLink** until all pages of items have been retrieved.</span></span>

## <a name="example-last-page-in-a-set"></a><span data-ttu-id="43b6c-159">Ejemplo (última página de un conjunto)</span><span class="sxs-lookup"><span data-stu-id="43b6c-159">Example (Last page in a set)</span></span>

<span data-ttu-id="43b6c-160">Aquí tiene un ejemplo de cómo llamar a esta API para actualizar su estado local.</span><span class="sxs-lookup"><span data-stu-id="43b6c-160">Here is an example of how to call this API to update your local state.</span></span>

### <a name="request"></a><span data-ttu-id="43b6c-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="43b6c-161">Request</span></span>

<span data-ttu-id="43b6c-162">Aquí tiene un ejemplo después de la solicitud inicial.</span><span class="sxs-lookup"><span data-stu-id="43b6c-162">Here is an example request after the initial request.</span></span>

<!-- { "blockType": "request", "name": "get_item_delta_last" }-->

```http
GET https://graph.microsoft.com/v1.0/me/drive/root/delta(token='1230919asd190410jlka')
```

### <a name="response"></a><span data-ttu-id="43b6c-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43b6c-163">Response</span></span>

<span data-ttu-id="43b6c-164">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43b6c-164">Here is an example of the response.</span></span>

<!-- { "blockType": "response", "truncated": true, "@odata.type": "Collection(microsoft.graph.driveItem)", "scope": "file.read" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "0123456789abc",
            "name": "folder2",
            "folder": { },
            "deleted": { }
        },
        {
            "id": "123010204abac",
            "name": "file.txt",
            "file": { }
        }
    ],
    "@odata.deltaLink": "https://graph.microsoft.com/v1.0/me/drive/root/delta?(token='1230919asd190410jlka')"
}
```

<span data-ttu-id="43b6c-165">Esta respuesta indica que el elemento llamado `folder2` se ha eliminado y el elemento `file.txt` se ha agregado o se ha modificado entre la solicitud inicial y esta solicitud para actualizar el estado local.</span><span class="sxs-lookup"><span data-stu-id="43b6c-165">This response indicates that the item named `folder2` was deleted and the item `file.txt` was either added or modified between the initial request and this request to update the local state.</span></span>

<span data-ttu-id="43b6c-166">La última página de elementos incluirá la propiedad **@odata.deltaLink**, que proporciona la dirección URL que puede utilizarse posteriormente para recuperar los cambios desde el conjunto actual de elementos.</span><span class="sxs-lookup"><span data-stu-id="43b6c-166">The final page of items will include the **@odata.deltaLink** property, which provides the URL that can be used later to retrieve changes since the current set of items.</span></span>

<span data-ttu-id="43b6c-p109">En algunos casos, puede que el servicio no pueda proporcionar una lista de cambios de un token determinado (por ejemplo, si un cliente intenta reutilizar un token anterior después de haber estado desconectado durante mucho tiempo o si ha cambiado el estado del servidor y se requiere un nuevo token). En estos casos, el servicio devolverá un error `HTTP 410 Gone` con una respuesta de error que contiene uno de los códigos de error siguientes y un encabezado `Location` con un nuevo nextLink que comienza una nueva enumeración delta desde cero. Cuando finalice la enumeración completa, compare los elementos devueltos con su estado local y siga estas instrucciones.</span><span class="sxs-lookup"><span data-stu-id="43b6c-p109">There may be cases when the service can't provide a list of changes for a given token (for example, if a client tries to reuse an old token after being disconnected for a long time, or if server state has changed and a new token is required). In these cases the service will return an `HTTP 410 Gone` error with an error response containing one of the error codes below, and a `Location` header containing a new nextLink that starts a fresh delta enumeration from scratch. After finishing the full enumeration, compare the returned items with your local state and follow these instructions.</span></span>

| <span data-ttu-id="43b6c-170">Tipo de error</span><span class="sxs-lookup"><span data-stu-id="43b6c-170">Error Type</span></span>                       | <span data-ttu-id="43b6c-171">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="43b6c-171">Instructions</span></span>                                                                                                                                                                                                                    |
|:---------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resyncChangesApplyDifferences`  | <span data-ttu-id="43b6c-p110">Reemplace cualquier elemento local con la versión del servidor (incluyendo eliminaciones) si está seguro de que el servicio estaba actualizado con sus cambios locales cuando lo sincronizó por última vez. Cargue cualquier cambio local que no conozca el servidor.</span><span class="sxs-lookup"><span data-stu-id="43b6c-p110">Replace any local items with the server's version (including deletes) if you're sure that the service was up to date with your local changes when you last sync'd. Upload any local changes that the server doesn't know about.</span></span> |
| `resyncChangesUploadDifferences` | <span data-ttu-id="43b6c-174">Cargue cualquier elemento local que el servicio no devolvió y cargue cualquier archivo que difiera de la versión del servidor (mantenga ambas copias si no está seguro de cuál está más actualizada).</span><span class="sxs-lookup"><span data-stu-id="43b6c-174">Upload any local items that the service did not return, and upload any files that differ from the server's version (keeping both copies if you're not sure which one is more up-to-date).</span></span>                                       |

## <a name="retrieving-the-current-deltalink"></a><span data-ttu-id="43b6c-175">Recuperar el valor deltaLink actual</span><span class="sxs-lookup"><span data-stu-id="43b6c-175">Retrieving the current deltaLink</span></span>

<span data-ttu-id="43b6c-176">En algunos casos, puede ser útil solicitar el valor deltaLink actual sin enumerar primero todos los elementos que ya hay en la unidad.</span><span class="sxs-lookup"><span data-stu-id="43b6c-176">In some scenarios, it may be useful to request the current deltaLink value without first enumerating all of the items in the drive already.</span></span>

<span data-ttu-id="43b6c-177">Esto puede ser útil si su aplicación solo quiere conocer los cambios y no necesita saber si hay elementos existentes.</span><span class="sxs-lookup"><span data-stu-id="43b6c-177">This can be useful if your app only wants to know about changes, and doesn't need to know about existing items.</span></span>
<span data-ttu-id="43b6c-178">Para recuperar el último valor deltaLink, llame a `delta` con un parámetro de cadena de consulta `?token=latest`.</span><span class="sxs-lookup"><span data-stu-id="43b6c-178">To retrieve the latest deltaLink, call `delta` with a query string parameter `?token=latest`.</span></span>

<span data-ttu-id="43b6c-179">\*\*Nota: Si está intentando mantener una representación local completa de los elementos de una carpeta o una unidad, debe usar `delta` para la enumeración inicial. Otros enfoques, como la paginación mediante la colección `children` de una carpeta, no se garantizan para devolver cada elemento único si se produce una escritura durante la enumeración. Usar `delta` es la única manera de garantizar que ha leído todos los datos que necesita en \*\*.</span><span class="sxs-lookup"><span data-stu-id="43b6c-179">**Note: If you are trying to maintain a full local representation of the items in a folder or a drive, you must use `delta` for the initial enumeration. Other approaches, such as paging through the `children` collection of a folder, are not guaranteed to return every single item if any writes take place during the enumeration. Using `delta` is the only way to guarantee that you've read all of the data you need to.**</span></span>

### <a name="request"></a><span data-ttu-id="43b6c-180">Solicitud</span><span class="sxs-lookup"><span data-stu-id="43b6c-180">Request</span></span>

<!-- { "blockType": "request", "name": "get-delta-latest", "scope": "files.read", "target": "action" } -->

```http
GET /me/drive/root/delta?token=latest
```

### <a name="response"></a><span data-ttu-id="43b6c-181">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43b6c-181">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItem)" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [ ],
    "@odata.deltaLink": "https://graph.microsoft.com/v1.0/me/drive/root/delta?token=1230919asd190410jlka"
}
```

## <a name="remarks"></a><span data-ttu-id="43b6c-182">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43b6c-182">Remarks</span></span>

* <span data-ttu-id="43b6c-p112">La fuente delta muestra el estado más reciente de cada elemento, no cada cambio. Si se ha cambiado el nombre de un elemento dos veces, solo aparecerá una vez con el nombre más reciente.</span><span class="sxs-lookup"><span data-stu-id="43b6c-p112">The delta feed shows the latest state for each item, not each change. If an item were renamed twice, it would only show up once, with its latest name.</span></span>
* <span data-ttu-id="43b6c-p113">El mismo elemento puede aparecer más de una vez en una fuente delta por diversas razones. Debe utilizar la última repetición que vea.</span><span class="sxs-lookup"><span data-stu-id="43b6c-p113">The same item may appear more than once in a delta feed, for various reasons. You should use the last occurrence you see.</span></span>
* <span data-ttu-id="43b6c-p114">La propiedad `parentReference` de los elementos no incluirá un valor de **ruta de acceso**. Esto ocurre porque el cambio de nombre de una carpeta no devuelve los descendientes de la carpeta desde **delta**. **Cuando utilice delta, debe hacer siempre un seguimiento de los elementos mediante id**.</span><span class="sxs-lookup"><span data-stu-id="43b6c-p114">The `parentReference` property on items will not include a value for **path**. This occurs because renaming a folder does not result in any descendants of the folder being returned from **delta**. **When using delta you should always track items by id**.</span></span>
* <span data-ttu-id="43b6c-190">En OneDrive para la Empresa y SharePoint, solo se admite `delta` en la carpeta `root`, no en otras carpetas de una unidad.</span><span class="sxs-lookup"><span data-stu-id="43b6c-190">In OneDrive for Business and SharePoint, `delta` is only supported on the `root` folder, not on other folders within a drive.</span></span>

* <span data-ttu-id="43b6c-191">Delta no devolverá las siguientes propiedades de DriveItem:</span><span class="sxs-lookup"><span data-stu-id="43b6c-191">Delta will not return the following DriveItem properties:</span></span>

* <span data-ttu-id="43b6c-192">**cTag**</span><span class="sxs-lookup"><span data-stu-id="43b6c-192">**cTag**</span></span>
* <span data-ttu-id="43b6c-193">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="43b6c-193">**lastModifiedBy**</span></span>
* <span data-ttu-id="43b6c-194">**size**</span><span class="sxs-lookup"><span data-stu-id="43b6c-194">**size**</span></span>

## <a name="error-responses"></a><span data-ttu-id="43b6c-195">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="43b6c-195">Error responses</span></span>

<span data-ttu-id="43b6c-196">Además de los errores de resincronización que se han mostrado anteriormente, vea [Respuestas de error][error-response] para obtener información sobre cómo se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="43b6c-196">In addition to the resync errors detailed above, see [Error Responses][error-response] for details about how errors are returned.</span></span>

[error-response]: /graph/errors
[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Sync changes from the service to your client state.",
  "keywords": "sync,delta,changes,$delta",
  "section": "documentation",
  "tocPath": "Items/Sync changes"
} -->
