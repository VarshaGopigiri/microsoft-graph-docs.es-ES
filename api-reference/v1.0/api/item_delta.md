# <a name="track-changes-for-a-drive"></a><span data-ttu-id="163c7-101">Control de cambios de una unidad</span><span class="sxs-lookup"><span data-stu-id="163c7-101">Track changes for a Drive</span></span>

<span data-ttu-id="163c7-102">Este método permite que su aplicación realice el control de cambios de una unidad y de sus elementos secundarios con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="163c7-102">This method allows your app to track changes to a drive and its children over time.</span></span>

<span data-ttu-id="163c7-p101">La aplicación comienza llamando a `delta` sin ningún parámetro. El servicio comienza enumerando la jerarquía de la unidad, devuelve páginas de elementos y también `@odata.nextLink` o `@odata.deltaLink`, tal y como se describe a continuación. La aplicación debe continuar la llamada con `@odata.nextLink` hasta que ya no se devuelva `@odata.nextLink` o hasta que la respuesta contenga un conjunto de cambios vacío.</span><span class="sxs-lookup"><span data-stu-id="163c7-p101">Your app begins by calling `delta` without any parameters. The service starts enumerating the drive's hierarchy, returning pages of items and either an `@odata.nextLink` or an `@odata.deltaLink`, as described below. Your app should continue calling with the `@odata.nextLink` until you no longer see an `@odata.nextLink` returned, or you see a response with an empty set of changes.</span></span>

<span data-ttu-id="163c7-p102">Una vez que termine de recibir todos los cambios, puede aplicarlos a su estado local. Para comprobar si hay cambios en el futuro, llame a `delta` con el `@odata.deltaLink` de la respuesta anterior.</span><span class="sxs-lookup"><span data-stu-id="163c7-p102">After you have finished receiving all the changes, you may apply them to your local state. To check for changes in the future, call `delta` again with the `@odata.deltaLink` from the previous response.</span></span>

<span data-ttu-id="163c7-p103">Los elementos eliminados se devuelven con la [faceta `deleted`](../resources/deleted.md). Los elementos con este conjunto de propiedades deben ser eliminados de su estado local.</span><span class="sxs-lookup"><span data-stu-id="163c7-p103">Deleted items are returned with the [`deleted` facet](../resources/deleted.md). Items with this property set should be removed from your local state.</span></span> 

<span data-ttu-id="163c7-110">**Nota:** Solo debe eliminar una carpeta de forma local si está vacía después de sincronizar todos los cambios.</span><span class="sxs-lookup"><span data-stu-id="163c7-110">Note: you should only delete a folder locally if it is empty after syncing all the changes.</span></span>

## <a name="permissions"></a><span data-ttu-id="163c7-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="163c7-111">Permissions</span></span>
<span data-ttu-id="163c7-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="163c7-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="163c7-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="163c7-114">Permission type</span></span>      | <span data-ttu-id="163c7-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="163c7-115">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="163c7-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="163c7-116">Delegated (work or school account)</span></span> | <span data-ttu-id="163c7-117">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="163c7-117">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    | 
|<span data-ttu-id="163c7-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="163c7-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="163c7-119">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="163c7-119">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    | 
|<span data-ttu-id="163c7-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="163c7-120">Application</span></span> | <span data-ttu-id="163c7-121">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="163c7-121">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="163c7-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="163c7-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root/delta
GET /drives/{drive-id}/root/delta
GET /groups/{group-id}/drive/root/delta
```

## <a name="optional-query-parameters"></a><span data-ttu-id="163c7-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="163c7-123">Optional query parameters</span></span>
<span data-ttu-id="163c7-124">Este método admite los [parámetros de consulta OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) `$select`, `$expand` y `$top` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="163c7-124">This method supports `$select`, `$expand`, and `$top` [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to customize the response.</span></span>

## <a name="request-body"></a><span data-ttu-id="163c7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="163c7-125">Request body</span></span>
<span data-ttu-id="163c7-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="163c7-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="163c7-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="163c7-127">Response</span></span>

<span data-ttu-id="163c7-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de recursos [DriveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="163c7-128">If successful, this method returns a `200 OK` response code and a collection of [DriveItem](../resources/driveitem.md) resources in the response body.</span></span>

<span data-ttu-id="163c7-129">Además de la colección de DriveItems, la respuesta también incluirá una de las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="163c7-129">In addition to the collection of DriveItems, the response will also include one of the following properties:</span></span>

| <span data-ttu-id="163c7-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="163c7-130">Name</span></span>                 | <span data-ttu-id="163c7-131">Valor</span><span class="sxs-lookup"><span data-stu-id="163c7-131">Value</span></span>  | <span data-ttu-id="163c7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="163c7-132">Description</span></span>                                                                                                                                      |
|:---------------------|:-------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="163c7-133">**@odata.nextLink**</span><span class="sxs-lookup"><span data-stu-id="163c7-133">**@odata.nextLink**</span></span>  | <span data-ttu-id="163c7-134">url</span><span class="sxs-lookup"><span data-stu-id="163c7-134">url</span></span>    | <span data-ttu-id="163c7-135">Una dirección URL que recupera la siguiente página de cambios disponible, si hay cambios adicionales en el conjunto actual.</span><span class="sxs-lookup"><span data-stu-id="163c7-135">A URL to retrieve the next available page of changes, if there are additional changes in the current set.</span></span>                                        |
| <span data-ttu-id="163c7-136">**@odata.deltaLink**</span><span class="sxs-lookup"><span data-stu-id="163c7-136">**@odata.deltaLink**</span></span> | <span data-ttu-id="163c7-137">url</span><span class="sxs-lookup"><span data-stu-id="163c7-137">url</span></span>    | <span data-ttu-id="163c7-p105">Una dirección URL que se devuelve en lugar de **@odata.nextLink** cuando se han devuelto todos los cambios actuales. Se utiliza para leer el siguiente conjunto de cambios en el futuro.</span><span class="sxs-lookup"><span data-stu-id="163c7-p105">A URL returned instead of **@odata.nextLink** after all current changes have been returned. Used to read the next set of changes in the future.</span></span>  |


## <a name="example-initial-request"></a><span data-ttu-id="163c7-140">Ejemplo (solicitud inicial)</span><span class="sxs-lookup"><span data-stu-id="163c7-140">Example (Initial Request)</span></span>
<span data-ttu-id="163c7-141">Aquí tiene un ejemplo de cómo llamar a esta API para establecer su estado local.</span><span class="sxs-lookup"><span data-stu-id="163c7-141">Here is an example of how to call this API to establish your local state.</span></span>

##### <a name="request"></a><span data-ttu-id="163c7-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="163c7-142">Request</span></span>
<span data-ttu-id="163c7-143">Aquí tiene un ejemplo de la solicitud inicial.</span><span class="sxs-lookup"><span data-stu-id="163c7-143">Here is an example of the initial request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_item_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/delta
```

##### <a name="response"></a><span data-ttu-id="163c7-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="163c7-144">Response</span></span>
<span data-ttu-id="163c7-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="163c7-145">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem",
  "isCollection": true
} -->
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

<span data-ttu-id="163c7-p106">Esta respuesta incluye la primera página de cambios y la propiedad **@odata.nextLink** indica que hay más elementos disponibles en el conjunto actual de elementos. Su aplicación debe continuar solicitando el valor de dirección URL **@odata.nextLink** hasta que se recuperen todas las páginas de elementos.</span><span class="sxs-lookup"><span data-stu-id="163c7-p106">This response includes the first page of changes, and the **@odata.nextLink** property indicates that there are more items available in the current set of items. Your app should continue to request the URL value of **@odata.nextLink** until all pages of items have been retrieved.</span></span>

## <a name="example-last-page-in-a-set"></a><span data-ttu-id="163c7-148">Ejemplo (última página de un conjunto)</span><span class="sxs-lookup"><span data-stu-id="163c7-148">Example (Last page in a set)</span></span>
<span data-ttu-id="163c7-149">Aquí tiene un ejemplo de cómo llamar a esta API para actualizar su estado local.</span><span class="sxs-lookup"><span data-stu-id="163c7-149">Here is an example of how to call this API to update your local state.</span></span>

##### <a name="request"></a><span data-ttu-id="163c7-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="163c7-150">Request</span></span>
<span data-ttu-id="163c7-151">Aquí tiene un ejemplo después de la solicitud inicial.</span><span class="sxs-lookup"><span data-stu-id="163c7-151">Here is an example request after the initial request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_item_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/delta(token='1230919asd190410jlka')
```

##### <a name="response"></a><span data-ttu-id="163c7-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="163c7-152">Response</span></span>
<span data-ttu-id="163c7-153">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="163c7-153">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem",
  "isCollection": true
} -->
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

<span data-ttu-id="163c7-154">Esta respuesta indica que el elemento llamado `folder2` se ha eliminado y el elemento `file.txt` se ha agregado o se ha modificado entre la solicitud inicial y esta solicitud para actualizar el estado local.</span><span class="sxs-lookup"><span data-stu-id="163c7-154">This response indicates that the item named `folder2` was deleted and the item `file.txt` was either added or modified between the initial request and this request to update the local state.</span></span>

<span data-ttu-id="163c7-155">La última página de elementos incluirá la propiedad **@odata.deltaLink**, que proporciona la dirección URL que puede utilizarse posteriormente para recuperar los cambios desde el conjunto actual de elementos.</span><span class="sxs-lookup"><span data-stu-id="163c7-155">The final page of items will include the **@odata.deltaLink** property, which provides the URL that can be used later to retrieve changes since the current set of items.</span></span>

## <a name="remarks"></a><span data-ttu-id="163c7-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="163c7-156">Remarks</span></span>

* <span data-ttu-id="163c7-p107">La fuente delta muestra el estado más reciente de cada elemento, no cada cambio. Si se ha cambiado el nombre de un elemento dos veces, solo aparecerá una vez con el nombre más reciente.</span><span class="sxs-lookup"><span data-stu-id="163c7-p107">The delta feed shows the latest state for each item, not each change. If an item were renamed twice, it would only show up once, with its latest name.</span></span>
* <span data-ttu-id="163c7-p108">El mismo elemento puede aparecer más de una vez en una fuente delta por diversas razones. Debe usar la última repetición que vea.</span><span class="sxs-lookup"><span data-stu-id="163c7-p108">The same item may appear more than once in a delta feed, for various reasons. You should use the last occurrence you see.</span></span>
* <span data-ttu-id="163c7-p109">La propiedad `parentReference` de los elementos no incluirá un valor de **ruta de acceso**. Esto ocurre porque el cambio de nombre de una carpeta no devuelve los descendientes de la carpeta desde **delta**. **Cuando utilice delta, debe hacer siempre un seguimiento de los elementos mediante id**.</span><span class="sxs-lookup"><span data-stu-id="163c7-p109">The `parentReference` property on items will not include a value for **path**. This occurs because renaming a folder does not result in any descendants of the folder being returned from **delta**. **When using delta you should always track items by id**.</span></span>

<span data-ttu-id="163c7-p110">En algunos casos, puede que el servicio no pueda proporcionar una lista de cambios de un token determinado (por ejemplo, si un cliente intenta reutilizar un token anterior después de haber estado desconectado durante mucho tiempo o si ha cambiado el estado del servidor y se requiere un nuevo token). En estos casos, el servicio devolverá un error `HTTP 410 Gone` con una respuesta de error que contiene uno de los códigos de error siguientes y un encabezado `Location` con un nuevo nextLink que comienza una nueva enumeración delta desde cero. Cuando finalice la enumeración completa, compare los elementos devueltos con su estado local y siga estas instrucciones.</span><span class="sxs-lookup"><span data-stu-id="163c7-p110">There may be cases when the service can't provide a list of changes for a given token (for example, if a client tries to reuse an old token after being disconnected for a long time, or if server state has changed and a new token is required). In these cases the service will return an `HTTP 410 Gone` error with an error response containing one of the error codes below, and a `Location` header containing a new nextLink that starts a fresh delta enumeration from scratch. After finishing the full enumeration, compare the returned items with your local state and follow these instructions.</span></span>

| <span data-ttu-id="163c7-167">Tipo de error</span><span class="sxs-lookup"><span data-stu-id="163c7-167">Error Type</span></span>                       | <span data-ttu-id="163c7-168">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="163c7-168">Instructions</span></span>                                                                                                                                                                                                                    |
|:---------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resyncChangesApplyDifferences`  | <span data-ttu-id="163c7-p111">Reemplace cualquier elemento local con la versión del servidor (incluyendo eliminaciones) si está seguro de que el servicio estaba actualizado con sus cambios locales cuando lo sincronizó por última vez. Cargue cualquier cambio local que no conozca el servidor.</span><span class="sxs-lookup"><span data-stu-id="163c7-p111">Replace any local items with the server's version (including deletes) if you're sure that the service was up to date with your local changes when you last sync'd. Upload any local changes that the server doesn't know about.</span></span> |
| `resyncChangesUploadDifferences` | <span data-ttu-id="163c7-171">Cargue cualquier elemento local que el servicio no devolvió y cargue cualquier archivo que difiera de la versión del servidor (mantenga ambas copias si no está seguro de cuál está más actualizada).</span><span class="sxs-lookup"><span data-stu-id="163c7-171">Upload any local items that the service did not return, and upload any files that differ from the server's version (keeping both copies if you're not sure which one is more up-to-date).</span></span>                                       |


<span data-ttu-id="163c7-p112">En OneDrive para la Empresa y SharePoint, solo se admite `delta` en la carpeta `root`, no en otras carpetas. Tampoco devolverá las siguientes propiedades de DriveItem:</span><span class="sxs-lookup"><span data-stu-id="163c7-p112">In OneDrive for Business and SharePoint, `delta` is only supported on the `root` folder, not on other folders. It also will not return the following DriveItem properties:</span></span>

* <span data-ttu-id="163c7-174">**createdBy**</span><span class="sxs-lookup"><span data-stu-id="163c7-174">**createdBy**</span></span>
* <span data-ttu-id="163c7-175">**cTag**</span><span class="sxs-lookup"><span data-stu-id="163c7-175">**cTag**</span></span>
* <span data-ttu-id="163c7-176">**eTag**</span><span class="sxs-lookup"><span data-stu-id="163c7-176">**etag**</span></span>
* <span data-ttu-id="163c7-177">**fileSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="163c7-177">**fileSystemInfo**</span></span>
* <span data-ttu-id="163c7-178">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="163c7-178">**lastModifiedBy**</span></span>
* <span data-ttu-id="163c7-179">**parentReference**</span><span class="sxs-lookup"><span data-stu-id="163c7-179">**parentReference**</span></span>
* <span data-ttu-id="163c7-180">**size**</span><span class="sxs-lookup"><span data-stu-id="163c7-180">**size**</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "Get item delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
