# <a name="list-thumbnails-for-a-driveitem"></a><span data-ttu-id="f08ff-101">Enumerar miniaturas de un DriveItem</span><span class="sxs-lookup"><span data-stu-id="f08ff-101">List thumbnails for a DriveItem</span></span>

<span data-ttu-id="f08ff-102">Recupere una colección de recursos de [ThumbnailSet](../resources/thumbnailset.md) de un recurso de [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="f08ff-102">Retrieve a collection of [ThumbnailSet](../resources/thumbnailset.md) resources for a [DriveItem](../resources/driveitem.md) resource.</span></span>

<span data-ttu-id="f08ff-p101">Un DriveItem puede estar representado por cero o más recursos [ThumbnailSet](../resources/thumbnailset.md). Cada **thumbnailSet** puede tener uno o varios objetos en [**miniatura**](../resources/thumbnail.md), que son imágenes que representan el elemento. Por ejemplo, un **thumbnailSet** puede incluir objetos en **miniatura**, los más comunes son `small`, `medium` o `large`.</span><span class="sxs-lookup"><span data-stu-id="f08ff-p101">A DriveItem can be represented by zero or more [ThumbnailSet](../resources/thumbnailset.md) resources. Each **thumbnailSet** can have one or more [**thumbnail**](../resources/thumbnail.md) objects, which are images that represent the item. For example, a **thumbnailSet** may include **thumbnail** objects, such as common ones including `small`, `medium`, or `large`.</span></span>

<span data-ttu-id="f08ff-p102">Hay muchas maneras de trabajar con miniaturas en OneDrive. Aquí tiene las más comunes:</span><span class="sxs-lookup"><span data-stu-id="f08ff-p102">There are many ways to work with thumbnails on OneDrive. Here are the most common ones:</span></span>

* <span data-ttu-id="f08ff-108">Enumerar las miniaturas disponibles para un elemento</span><span class="sxs-lookup"><span data-stu-id="f08ff-108">Enumerate available thumbnails for an item</span></span>
* <span data-ttu-id="f08ff-109">Recuperar una sola miniatura para un elemento</span><span class="sxs-lookup"><span data-stu-id="f08ff-109">Retrieve a single thumbnail for an item</span></span>
* <span data-ttu-id="f08ff-110">Recuperar el contenido de miniaturas</span><span class="sxs-lookup"><span data-stu-id="f08ff-110">Retrieve thumbnail content</span></span>
* <span data-ttu-id="f08ff-111">Recuperar miniaturas para varios elementos en una sola solicitud</span><span class="sxs-lookup"><span data-stu-id="f08ff-111">Retrieve thumbnails for multiple items in a single request</span></span>
* <span data-ttu-id="f08ff-112">Recuperar los tamaños personalizados de miniaturas</span><span class="sxs-lookup"><span data-stu-id="f08ff-112">Retrieve custom thumbnail sizes</span></span>
* <span data-ttu-id="f08ff-113">Cargar una miniatura personalizada para un elemento </span><span class="sxs-lookup"><span data-stu-id="f08ff-113">Upload a custom thumbnail for an item</span></span>
* <span data-ttu-id="f08ff-114">Determinar si existe una miniatura cargada personalizada</span><span class="sxs-lookup"><span data-stu-id="f08ff-114">Determine if a custom uploaded thumbnail exists</span></span>


## <a name="permissions"></a><span data-ttu-id="f08ff-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="f08ff-115">Permissions</span></span>
<span data-ttu-id="f08ff-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f08ff-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f08ff-118">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f08ff-118">Permission type</span></span>      | <span data-ttu-id="f08ff-119">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f08ff-119">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f08ff-120">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f08ff-120">Delegated (work or school account)</span></span> | <span data-ttu-id="f08ff-121">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f08ff-121">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="f08ff-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f08ff-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f08ff-123">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f08ff-123">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="f08ff-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f08ff-124">Application</span></span> | <span data-ttu-id="f08ff-125">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f08ff-125">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f08ff-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f08ff-126">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root:/{item-path}:/thumbnails
GET /me/drive/items/{item-id}/thumbnails
GET /groups/{group-id}/drive/items/{item-id}/thumbnails
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f08ff-127">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f08ff-127">Optional query parameters</span></span>
<span data-ttu-id="f08ff-128">Este método admite el [parámetro de consulta OData](../../../concepts/query_parameters.md) `$select` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f08ff-128">This method supports the `$select` [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-body"></a><span data-ttu-id="f08ff-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f08ff-129">Request body</span></span>
<span data-ttu-id="f08ff-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f08ff-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f08ff-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f08ff-131">Response</span></span>

<span data-ttu-id="f08ff-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ThumbnailSet](../resources/thumbnailset.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f08ff-132">If successful, this method returns a `200 OK` response code and collection of [ThumbnailSet](../resources/thumbnailset.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f08ff-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f08ff-133">Example</span></span>

##### <a name="request"></a><span data-ttu-id="f08ff-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f08ff-134">Request</span></span>

<span data-ttu-id="f08ff-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f08ff-135">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_thumbnails"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/thumbnails
```


##### <a name="response"></a><span data-ttu-id="f08ff-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f08ff-136">Response</span></span>
<span data-ttu-id="f08ff-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f08ff-137">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.thumbnailSet",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "0",
      "small": { "height": 64, "width": 96, "url": "https://sn3302files..."},
      "medium": { "height": 117, "width": 176, "url": "https://sn3302files..."},
      "large": { "height": 533, "width": 800, "url": "https://sn3302files..."}
    }
  ]
}
```

## <a name="retrieve-a-single-thumbnail"></a><span data-ttu-id="f08ff-138">Recuperar una sola miniatura</span><span class="sxs-lookup"><span data-stu-id="f08ff-138">Retrieve a single thumbnail</span></span>

<span data-ttu-id="f08ff-139">Recupere los metadatos de una sola miniatura y un tamaño solicitándolo directamente en una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f08ff-139">Retrieve the metadata for a single thumbnail and size by addressing it directly in a request.</span></span>

## <a name="http-request"></a><span data-ttu-id="f08ff-140">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f08ff-140">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-one-thumbnail" } -->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/thumbnails/{thumb-id}/{size}
```

## <a name="path-parameters"></a><span data-ttu-id="f08ff-141">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="f08ff-141">Path parameters</span></span>

| <span data-ttu-id="f08ff-142">Nombre</span><span class="sxs-lookup"><span data-stu-id="f08ff-142">Name</span></span>         | <span data-ttu-id="f08ff-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="f08ff-143">Type</span></span>   | <span data-ttu-id="f08ff-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="f08ff-144">Description</span></span>                                                                         |
|:-------------|:-------|:------------------------------------------------------------------------------------|
| <span data-ttu-id="f08ff-145">**item-id**</span><span class="sxs-lookup"><span data-stu-id="f08ff-145">**item-id**</span></span>  | <span data-ttu-id="f08ff-146">string</span><span class="sxs-lookup"><span data-stu-id="f08ff-146">string</span></span> | <span data-ttu-id="f08ff-147">El identificador único para el elemento al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="f08ff-147">The unique identifier for the item referenced.</span></span>                                      |
| <span data-ttu-id="f08ff-148">**thumb-id**</span><span class="sxs-lookup"><span data-stu-id="f08ff-148">**thumb-id**</span></span> | <span data-ttu-id="f08ff-149">número</span><span class="sxs-lookup"><span data-stu-id="f08ff-149">number</span></span> | <span data-ttu-id="f08ff-150">El índice de la miniatura, normalmente de 0-4.</span><span class="sxs-lookup"><span data-stu-id="f08ff-150">The index of the thumbnail, usually 0-4.</span></span>                                            |
| <span data-ttu-id="f08ff-151">**size**</span><span class="sxs-lookup"><span data-stu-id="f08ff-151">**size**</span></span>     | <span data-ttu-id="f08ff-152">string</span><span class="sxs-lookup"><span data-stu-id="f08ff-152">string</span></span> | <span data-ttu-id="f08ff-p104">El tamaño de la miniatura solicitada. Debe ser uno de los tamaños estándares enumerados.</span><span class="sxs-lookup"><span data-stu-id="f08ff-p104">The size of the thumbnail requested. This must be one of the standard sizes listed.</span></span> |

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.thumbnail" } -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "width": 100,
  "height": 100,
  "url": "http://onedrive.com/asd123a/asdjlkasjdkasdjlk.jpg"
}
```

## <a name="retrieve-thumbnail-content"></a><span data-ttu-id="f08ff-155">Recuperar el contenido de miniaturas</span><span class="sxs-lookup"><span data-stu-id="f08ff-155">Retrieve thumbnail content</span></span>

<span data-ttu-id="f08ff-156">Puede recuperar directamente el contenido de la miniatura solicitando la propiedad **content** de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="f08ff-156">You can directly retrieve the content of the thumbnail by requesting the **content** property of the thumbnail.</span></span>

## <a name="http-request"></a><span data-ttu-id="f08ff-157">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f08ff-157">HTTP request</span></span>

<!-- { "blockType": "request", "name":"get-thumbnail-content" } -->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/thumbnails/{thumb-id}/{size}/content
```

## <a name="response"></a><span data-ttu-id="f08ff-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f08ff-158">Response</span></span>

<span data-ttu-id="f08ff-159">El servicio responde con un redireccionamiento a la dirección URL de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="f08ff-159">The service responds with a redirect to the thumbnail URL.</span></span>

<!-- { "blockType": "response" } -->
```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

<span data-ttu-id="f08ff-p105">Las direcciones URL de contenido en miniatura se autentican previamente y no requieren la descarga de un encabezado de autorización. Estas direcciones URL son de corta duración, solo son válidas durante unas horas y las aplicaciones no deben almacenarlas en caché.</span><span class="sxs-lookup"><span data-stu-id="f08ff-p105">Thumbnail content URLs are pre-authenticated and do not require an authorization header to be downloaded. These URLs are short lived and only valid for a few hours and should not be cached by apps.</span></span>


## <a name="size-values"></a><span data-ttu-id="f08ff-162">Valores de tamaño</span><span class="sxs-lookup"><span data-stu-id="f08ff-162">Size values</span></span>

<span data-ttu-id="f08ff-p106">Esta tabla define los tamaños posibles de las miniaturas. Puede solicitar cualquier tamaño de miniatura arbitrario, pero es probable que existan valores definidos y que se devuelva un valor rápidamente:</span><span class="sxs-lookup"><span data-stu-id="f08ff-p106">This table defines the possible thumbnail sizes. While you can request any arbitrary thumbnail size, the defined values are likely to exist and return a value quickly:</span></span>

| <span data-ttu-id="f08ff-165">Nombre</span><span class="sxs-lookup"><span data-stu-id="f08ff-165">Name</span></span>           | <span data-ttu-id="f08ff-166">Resolución</span><span class="sxs-lookup"><span data-stu-id="f08ff-166">Resolution</span></span>  | <span data-ttu-id="f08ff-167">Relación de aspecto</span><span class="sxs-lookup"><span data-stu-id="f08ff-167">Aspect Ratio</span></span> | <span data-ttu-id="f08ff-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="f08ff-168">Description</span></span>                                                          |
|:---------------|:------------|:-------------|:---------------------------------------------------------------------|
| `small`        | <span data-ttu-id="f08ff-169">borde más largo 96</span><span class="sxs-lookup"><span data-stu-id="f08ff-169">96 longest</span></span>  | <span data-ttu-id="f08ff-170">Original</span><span class="sxs-lookup"><span data-stu-id="f08ff-170">Original</span></span>     | <span data-ttu-id="f08ff-171">Miniatura pequeña y muy comprimida recortada en una relación de aspecto cuadrada.</span><span class="sxs-lookup"><span data-stu-id="f08ff-171">Small, highly compressed thumbnail cropped to a square aspect ratio.</span></span> |
| `medium`       | <span data-ttu-id="f08ff-172">borde más largo 176</span><span class="sxs-lookup"><span data-stu-id="f08ff-172">176 longest</span></span> | <span data-ttu-id="f08ff-173">Original</span><span class="sxs-lookup"><span data-stu-id="f08ff-173">Original</span></span>     | <span data-ttu-id="f08ff-174">Miniatura recortada al tamaño estándar del elemento para la vista web de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="f08ff-174">Cropped to the standard item size for the OneDrive web view.</span></span>         |
| `large`        | <span data-ttu-id="f08ff-175">borde más largo 800</span><span class="sxs-lookup"><span data-stu-id="f08ff-175">800 longest</span></span> | <span data-ttu-id="f08ff-176">Original</span><span class="sxs-lookup"><span data-stu-id="f08ff-176">Original</span></span>     | <span data-ttu-id="f08ff-177">Miniatura con el borde más largo cambiado a un tamaño de 800 píxeles.</span><span class="sxs-lookup"><span data-stu-id="f08ff-177">Thumbnail with the longest edge resized to 800 pixels.</span></span>               |

## <a name="remarks"></a><span data-ttu-id="f08ff-178">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f08ff-178">Remarks</span></span>

<span data-ttu-id="f08ff-179">**Nota** En OneDrive para la Empresa y en SharePoint:</span><span class="sxs-lookup"><span data-stu-id="f08ff-179">**Note** In OneDrive for Business and SharePoint:</span></span>

* <span data-ttu-id="f08ff-180">El uso de estas llamadas para expandir la colección de miniaturas no funcionará: `GET /drive/root:/{item-path}?expand=children(expand=thumbnails)`
  `GET /drive/items/{item-id}/children?expand=thumbnails`</span><span class="sxs-lookup"><span data-stu-id="f08ff-180">Using these calls to expand the thumbnails collection will not work: `GET /drive/root:/{item-path}?expand=children(expand=thumbnails)`
  `GET /drive/items/{item-id}/children?expand=thumbnails`</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get metadata and content for thumbnails of multiple sizes for OneDrive items.",
  "keywords": "thumbnail,content,download,sizes",
  "section": "documentation",
  "tocPath": "OneDrive/Item/List thumbnails"
} -->
