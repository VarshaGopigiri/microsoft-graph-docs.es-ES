# <a name="track-changes-for-a-drive"></a><span data-ttu-id="56517-101">Control de cambios de una unidad</span><span class="sxs-lookup"><span data-stu-id="56517-101">Track changes for a Drive</span></span>

<span data-ttu-id="56517-102">Este método permite que su aplicación realice el control de cambios de una unidad y de sus elementos secundarios con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="56517-102">This method allows your app to track changes to a drive and its children over time.</span></span>

<span data-ttu-id="56517-p101">La aplicación comienza llamando a `delta` sin ningún parámetro. El servicio comienza enumerando la jerarquía de la unidad, devuelve páginas de elementos y también `@odata.nextLink` o `@odata.deltaLink`, tal y como se describe a continuación. La aplicación debe continuar la llamada con `@odata.nextLink` hasta que ya no se devuelva `@odata.nextLink` o hasta que la respuesta contenga un conjunto de cambios vacío.</span><span class="sxs-lookup"><span data-stu-id="56517-p101">Your app begins by calling `delta` without any parameters. The service starts enumerating the drive's hierarchy, returning pages of items and either an `@odata.nextLink` or an `@odata.deltaLink`, as described below. Your app should continue calling with the `@odata.nextLink` until you no longer see an `@odata.nextLink` returned, or you see a response with an empty set of changes.</span></span>

<span data-ttu-id="56517-p102">Una vez que termine de recibir todos los cambios, puede aplicarlos a su estado local. Para comprobar si hay cambios en el futuro, llame a `delta` con el `@odata.deltaLink` de la respuesta anterior.</span><span class="sxs-lookup"><span data-stu-id="56517-p102">After you have finished receiving all the changes, you may apply them to your local state. To check for changes in the future, call `delta` again with the `@odata.deltaLink` from the previous response.</span></span>

<span data-ttu-id="56517-p103">Los elementos eliminados se devuelven con la [faceta `deleted`](../resources/deleted.md). Los elementos con este conjunto de propiedades deben ser eliminados de su estado local.</span><span class="sxs-lookup"><span data-stu-id="56517-p103">Deleted items are returned with the [`deleted` facet](../resources/deleted.md). Items with this property set should be removed from your local state.</span></span> 

<span data-ttu-id="56517-110">**Nota:** solo debe eliminar una carpeta de forma local si está vacía después de sincronizar todos los cambios.</span><span class="sxs-lookup"><span data-stu-id="56517-110">**Note:** you should only delete a folder locally if it is empty after syncing all the changes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="56517-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="56517-111">Prerequisites</span></span>
<span data-ttu-id="56517-112">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="56517-112">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="56517-113">Files.Read</span><span class="sxs-lookup"><span data-stu-id="56517-113">Files.Read</span></span>
* <span data-ttu-id="56517-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="56517-114">Files.ReadWrite</span></span>
* <span data-ttu-id="56517-115">Files.Read.All</span><span class="sxs-lookup"><span data-stu-id="56517-115">Files.Read.All</span></span>
* <span data-ttu-id="56517-116">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="56517-116">Files.ReadWrite.All</span></span>
* <span data-ttu-id="56517-117">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="56517-117">Sites.Read.All</span></span>
* <span data-ttu-id="56517-118">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="56517-118">Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="56517-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="56517-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root/delta
GET /drives/{drive-id}/root/delta
GET /groups/{group-id}/drive/root/delta
```

## <a name="optional-query-parameters"></a><span data-ttu-id="56517-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="56517-120">Optional query parameters</span></span>
<span data-ttu-id="56517-121">Este método admite los [parámetros de consulta OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) `$select`, `$expand` y `$top` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56517-121">This method supports `$select`, `$expand`, and `$top` [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to customize the response.</span></span>

## <a name="request-body"></a><span data-ttu-id="56517-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="56517-122">Request body</span></span>
<span data-ttu-id="56517-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="56517-123">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="56517-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56517-124">Response</span></span>

<span data-ttu-id="56517-125">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de recursos [DriveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56517-125">If successful, this method returns a `200 OK` response code and a collection of [DriveItem](../resources/driveitem.md) resources in the response body.</span></span>

<span data-ttu-id="56517-126">Además de la colección de DriveItems, la respuesta también incluirá una de las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="56517-126">In addition to the collection of DriveItems, the response will also include one of the following properties:</span></span>

| <span data-ttu-id="56517-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="56517-127">Name</span></span>                 | <span data-ttu-id="56517-128">Valor</span><span class="sxs-lookup"><span data-stu-id="56517-128">Value</span></span>  | <span data-ttu-id="56517-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="56517-129">Description</span></span>                                                                                                                                      |
|:---------------------|:-------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56517-130">**@odata.nextLink**</span><span class="sxs-lookup"><span data-stu-id="56517-130">**@odata.nextLink**</span></span>  | <span data-ttu-id="56517-131">url</span><span class="sxs-lookup"><span data-stu-id="56517-131">url</span></span>    | <span data-ttu-id="56517-132">Una dirección URL que recupera la siguiente página de cambios disponible, si hay cambios adicionales en el conjunto actual.</span><span class="sxs-lookup"><span data-stu-id="56517-132">A URL to retrieve the next available page of changes, if there are additional changes in the current set.</span></span>                                        |
| <span data-ttu-id="56517-133">**@odata.deltaLink**</span><span class="sxs-lookup"><span data-stu-id="56517-133">**@odata.deltaLink**</span></span> | <span data-ttu-id="56517-134">url</span><span class="sxs-lookup"><span data-stu-id="56517-134">url</span></span>    | <span data-ttu-id="56517-p104">Una dirección URL que se devuelve en lugar de **@odata.nextLink** cuando se han devuelto todos los cambios actuales. Se utiliza para leer el siguiente conjunto de cambios en el futuro.</span><span class="sxs-lookup"><span data-stu-id="56517-p104">A URL returned instead of **@odata.nextLink** after all current changes have been returned. Used to read the next set of changes in the future.</span></span>  |


## <a name="example-initial-request"></a><span data-ttu-id="56517-137">Ejemplo (solicitud inicial)</span><span class="sxs-lookup"><span data-stu-id="56517-137">Example (Initial Request)</span></span>
<span data-ttu-id="56517-138">Aquí tiene un ejemplo de cómo llamar a esta API para establecer su estado local.</span><span class="sxs-lookup"><span data-stu-id="56517-138">Here is an example of how to call this API to establish your local state.</span></span>

##### <a name="request"></a><span data-ttu-id="56517-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="56517-139">Request</span></span>
<span data-ttu-id="56517-140">Aquí tiene un ejemplo de la solicitud inicial.</span><span class="sxs-lookup"><span data-stu-id="56517-140">Here is an example of the initial request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_item_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/delta
```

##### <a name="response"></a><span data-ttu-id="56517-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56517-141">Response</span></span>
<span data-ttu-id="56517-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56517-142">Here is an example of the response.</span></span>

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

<span data-ttu-id="56517-p105">Esta respuesta incluye la primera página de cambios y la propiedad **@odata.nextLink** indica que hay más elementos disponibles en el conjunto actual de elementos. Su aplicación debe continuar solicitando el valor de dirección URL **@odata.nextLink** hasta que se recuperen todas las páginas de elementos.</span><span class="sxs-lookup"><span data-stu-id="56517-p105">This response includes the first page of changes, and the **@odata.nextLink** property indicates that there are more items available in the current set of items. Your app should continue to request the URL value of **@odata.nextLink** until all pages of items have been retrieved.</span></span>

## <a name="example-last-page-in-a-set"></a><span data-ttu-id="56517-145">Ejemplo (última página de un conjunto)</span><span class="sxs-lookup"><span data-stu-id="56517-145">Example (Last page in a set)</span></span>
<span data-ttu-id="56517-146">Aquí tiene un ejemplo de cómo llamar a esta API para actualizar su estado local.</span><span class="sxs-lookup"><span data-stu-id="56517-146">Here is an example of how to call this API to update your local state.</span></span>

##### <a name="request"></a><span data-ttu-id="56517-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="56517-147">Request</span></span>
<span data-ttu-id="56517-148">Aquí tiene un ejemplo después de la solicitud inicial.</span><span class="sxs-lookup"><span data-stu-id="56517-148">Here is an example request after the initial request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_item_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/delta(token='1230919asd190410jlka')
```

##### <a name="response"></a><span data-ttu-id="56517-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56517-149">Response</span></span>
<span data-ttu-id="56517-150">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56517-150">Here is an example of the response.</span></span>

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

<span data-ttu-id="56517-151">Esta respuesta indica que el elemento llamado `folder2` se ha eliminado y el elemento `file.txt` se ha agregado o se ha modificado entre la solicitud inicial y esta solicitud para actualizar el estado local.</span><span class="sxs-lookup"><span data-stu-id="56517-151">This response indicates that the item named `folder2` was deleted and the item `file.txt` was either added or modified between the initial request and this request to update the local state.</span></span>

<span data-ttu-id="56517-152">La última página de elementos incluirá la propiedad **@odata.deltaLink**, que proporciona la dirección URL que puede utilizarse posteriormente para recuperar los cambios desde el conjunto actual de elementos.</span><span class="sxs-lookup"><span data-stu-id="56517-152">The final page of items will include the **@odata.deltaLink** property, which provides the URL that can be used later to retrieve changes since the current set of items.</span></span>

## <a name="remarks"></a><span data-ttu-id="56517-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56517-153">Remarks</span></span>

* <span data-ttu-id="56517-p106">La fuente delta muestra el estado más reciente de cada elemento, no cada cambio. Si se ha cambiado el nombre de un elemento dos veces, solo aparecerá una vez con el nombre más reciente.</span><span class="sxs-lookup"><span data-stu-id="56517-p106">The delta feed shows the latest state for each item, not each change. If an item were renamed twice, it would only show up once, with its latest name.</span></span>
* <span data-ttu-id="56517-p107">El mismo elemento puede aparecer más de una vez en una fuente delta por diversas razones. Debe usar la última repetición que vea.</span><span class="sxs-lookup"><span data-stu-id="56517-p107">The same item may appear more than once in a delta feed, for various reasons. You should use the last occurrence you see.</span></span>
* <span data-ttu-id="56517-p108">La propiedad `parentReference` de los elementos no incluirá un valor de **ruta de acceso**. Esto ocurre porque el cambio de nombre de una carpeta no devuelve los descendientes de la carpeta desde **delta**. **Cuando utilice delta, debe hacer siempre un seguimiento de los elementos mediante id**.</span><span class="sxs-lookup"><span data-stu-id="56517-p108">The `parentReference` property on items will not include a value for **path**. This occurs because renaming a folder does not result in any descendants of the folder being returned from **delta**. **When using delta you should always track items by id**.</span></span>

<span data-ttu-id="56517-p109">En algunos casos, puede que el servicio no pueda proporcionar una lista de cambios de un token determinado (por ejemplo, si un cliente intenta reutilizar un token anterior después de haber estado desconectado durante mucho tiempo o si ha cambiado el estado del servidor y se requiere un nuevo token). En estos casos, el servicio devolverá un error `HTTP 410 Gone` con una respuesta de error que contiene uno de los códigos de error siguientes y un encabezado `Location` con un nuevo nextLink que comienza una nueva enumeración delta desde cero. Cuando finalice la enumeración completa, compare los elementos devueltos con su estado local y siga estas instrucciones.</span><span class="sxs-lookup"><span data-stu-id="56517-p109">There may be cases when the service can't provide a list of changes for a given token (for example, if a client tries to reuse an old token after being disconnected for a long time, or if server state has changed and a new token is required). In these cases the service will return an `HTTP 410 Gone` error with an error response containing one of the error codes below, and a `Location` header containing a new nextLink that starts a fresh delta enumeration from scratch. After finishing the full enumeration, compare the returned items with your local state and follow these instructions.</span></span>

| <span data-ttu-id="56517-164">Tipo de error</span><span class="sxs-lookup"><span data-stu-id="56517-164">Error Type</span></span>                       | <span data-ttu-id="56517-165">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="56517-165">Instructions</span></span>                                                                                                                                                                                                                    |
|:---------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resyncChangesApplyDifferences`  | <span data-ttu-id="56517-p110">Reemplace cualquier elemento local con la versión del servidor (incluyendo eliminaciones) si está seguro de que el servicio estaba actualizado con sus cambios locales cuando lo sincronizó por última vez. Cargue cualquier cambio local que no conozca el servidor.</span><span class="sxs-lookup"><span data-stu-id="56517-p110">Replace any local items with the server's version (including deletes) if you're sure that the service was up to date with your local changes when you last sync'd. Upload any local changes that the server doesn't know about.</span></span> |
| `resyncChangesUploadDifferences` | <span data-ttu-id="56517-168">Cargue cualquier elemento local que el servicio no devolvió y cargue cualquier archivo que difiera de la versión del servidor (mantenga ambas copias si no está seguro de cuál está más actualizada).</span><span class="sxs-lookup"><span data-stu-id="56517-168">Upload any local items that the service did not return, and upload any files that differ from the server's version (keeping both copies if you're not sure which one is more up-to-date).</span></span>                                       |


<span data-ttu-id="56517-p111">En OneDrive para la Empresa y SharePoint, solo se admite `delta` en la carpeta `root`, no en otras carpetas. Tampoco devolverá las siguientes propiedades de DriveItem:</span><span class="sxs-lookup"><span data-stu-id="56517-p111">In OneDrive for Business and SharePoint, `delta` is only supported on the `root` folder, not on other folders. It also will not return the following DriveItem properties:</span></span>

* <span data-ttu-id="56517-171">**createdBy**</span><span class="sxs-lookup"><span data-stu-id="56517-171">**createdBy**</span></span>
* <span data-ttu-id="56517-172">**cTag**</span><span class="sxs-lookup"><span data-stu-id="56517-172">**cTag**</span></span>
* <span data-ttu-id="56517-173">**eTag**</span><span class="sxs-lookup"><span data-stu-id="56517-173">**etag**</span></span>
* <span data-ttu-id="56517-174">**fileSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="56517-174">**fileSystemInfo**</span></span>
* <span data-ttu-id="56517-175">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="56517-175">**lastModifiedBy**</span></span>
* <span data-ttu-id="56517-176">**parentReference**</span><span class="sxs-lookup"><span data-stu-id="56517-176">**parentReference**</span></span>
* <span data-ttu-id="56517-177">**size**</span><span class="sxs-lookup"><span data-stu-id="56517-177">**size**</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "Get item delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
