---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Recuperar miniaturas de un archivo o una carpeta
localization_priority: Normal
ms.openlocfilehash: 48ea0b1f876fff28affc68895aed58a063df1513
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27813716"
---
# <a name="list-thumbnails-for-a-driveitem"></a><span data-ttu-id="86a0e-102">Enumerar miniaturas de un DriveItem</span><span class="sxs-lookup"><span data-stu-id="86a0e-102">List thumbnails for a DriveItem</span></span>

> <span data-ttu-id="86a0e-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="86a0e-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="86a0e-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="86a0e-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="86a0e-105">Recupere una colección de recursos de [ThumbnailSet](../resources/thumbnailset.md) de un recurso de [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="86a0e-105">Retrieve a collection of [ThumbnailSet](../resources/thumbnailset.md) resources for a [DriveItem](../resources/driveitem.md) resource.</span></span>

<span data-ttu-id="86a0e-p102">Un DriveItem puede estar representado por cero o más recursos [ThumbnailSet](../resources/thumbnailset.md). Cada **thumbnailSet** puede tener uno o varios objetos en [**miniatura**](../resources/thumbnail.md), que son imágenes que representan el elemento. Por ejemplo, un **thumbnailSet** puede incluir objetos en **miniatura**, los más comunes son `small`, `medium` o `large`.</span><span class="sxs-lookup"><span data-stu-id="86a0e-p102">A DriveItem can be represented by zero or more [ThumbnailSet](../resources/thumbnailset.md) resources. Each **thumbnailSet** can have one or more [**thumbnail**](../resources/thumbnail.md) objects, which are images that represent the item. For example, a **thumbnailSet** may include **thumbnail** objects, such as common ones including `small`, `medium`, or `large`.</span></span>

<span data-ttu-id="86a0e-p103">Hay muchas maneras de trabajar con miniaturas en OneDrive. Aquí tiene las más comunes:</span><span class="sxs-lookup"><span data-stu-id="86a0e-p103">There are many ways to work with thumbnails on OneDrive. Here are the most common ones:</span></span>

* <span data-ttu-id="86a0e-111">Enumerar las miniaturas disponibles para un elemento</span><span class="sxs-lookup"><span data-stu-id="86a0e-111">Enumerate available thumbnails for an item</span></span>
* <span data-ttu-id="86a0e-112">Recuperar una sola miniatura para un elemento</span><span class="sxs-lookup"><span data-stu-id="86a0e-112">Retrieve a single thumbnail for an item</span></span>
* <span data-ttu-id="86a0e-113">Recuperar el contenido de miniaturas</span><span class="sxs-lookup"><span data-stu-id="86a0e-113">Retrieve thumbnail content</span></span>
* <span data-ttu-id="86a0e-114">Recuperar miniaturas para varios elementos en una sola solicitud</span><span class="sxs-lookup"><span data-stu-id="86a0e-114">Retrieve thumbnails for multiple items in a single request</span></span>
* <span data-ttu-id="86a0e-115">Recuperar los tamaños personalizados de miniaturas</span><span class="sxs-lookup"><span data-stu-id="86a0e-115">Retrieve custom thumbnail sizes</span></span>
* <span data-ttu-id="86a0e-116">Cargar una miniatura personalizada para un elemento </span><span class="sxs-lookup"><span data-stu-id="86a0e-116">Upload a custom thumbnail for an item</span></span>
* <span data-ttu-id="86a0e-117">Determinar si existe una miniatura cargada personalizada</span><span class="sxs-lookup"><span data-stu-id="86a0e-117">Determine if a custom uploaded thumbnail exists</span></span>


## <a name="permissions"></a><span data-ttu-id="86a0e-118">Permisos</span><span class="sxs-lookup"><span data-stu-id="86a0e-118">Permissions</span></span>

<span data-ttu-id="86a0e-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="86a0e-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="86a0e-121">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="86a0e-121">Permission type</span></span>      | <span data-ttu-id="86a0e-122">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="86a0e-122">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="86a0e-123">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="86a0e-123">Delegated (work or school account)</span></span> | <span data-ttu-id="86a0e-124">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="86a0e-124">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="86a0e-125">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="86a0e-125">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="86a0e-126">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="86a0e-126">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="86a0e-127">Aplicación</span><span class="sxs-lookup"><span data-stu-id="86a0e-127">Application</span></span> | <span data-ttu-id="86a0e-128">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="86a0e-128">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="86a0e-129">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="86a0e-129">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/thumbnails
GET /groups/{group-id}/drive/items/{item-id}/thumbnails
GET /me/drive/items/{item-id}/thumbnails
GET /sites/{site-id}/drive/items/{item-id}/thumbnails
GET /users/{user-id}/drive/items/{item-id}/thumbnails
```

## <a name="optional-query-parameters"></a><span data-ttu-id="86a0e-130">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="86a0e-130">Optional query parameters</span></span>

<span data-ttu-id="86a0e-131">Este método admite el [parámetro de consulta OData](/graph/query-parameters) `$select` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86a0e-131">This method supports the `$select` [OData puery parameter](/graph/query-parameters) to customize the response.</span></span>

## <a name="response"></a><span data-ttu-id="86a0e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86a0e-132">Response</span></span>

<span data-ttu-id="86a0e-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ThumbnailSet](../resources/thumbnailset.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86a0e-133">If successful, this method returns a `200 OK` response code and collection of [ThumbnailSet](../resources/thumbnailset.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="86a0e-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86a0e-134">Example</span></span>

<span data-ttu-id="86a0e-135">Aquí tiene un ejemplo de la solicitud que recupera las miniaturas disponibles de un elemento en el OneDrive del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="86a0e-135">Here is an example of the request which retrieves available thumbnails for an item in the current user's OneDrive.</span></span>

<!-- { "blockType": "request", "name": "enum-item-thumbnails", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/thumbnails
```

<span data-ttu-id="86a0e-136">Esta devuelve una matriz de **thumbnailSets** disponibles para el elemento.</span><span class="sxs-lookup"><span data-stu-id="86a0e-136">This returns an array of available **thumbnailSets** for the item.</span></span> <span data-ttu-id="86a0e-137">Cualquier elemento de una unidad puede tener cero o más miniaturas.</span><span class="sxs-lookup"><span data-stu-id="86a0e-137">Any item in a drive can have zero or more thumbnails.</span></span>

<span data-ttu-id="86a0e-138">**Nota:** Puede usar el parámetro de cadena de consulta _select_ para controlar qué tamaños de miniatura se devuelven en **ThumbnailSet**.</span><span class="sxs-lookup"><span data-stu-id="86a0e-138">**Note:** You can use the _select_ query string parameter to control which thumbnail sizes are returned in the **ThumbnailSet**.</span></span>
<span data-ttu-id="86a0e-139">Por ejemplo, `/thumbnails?select=medium` recupera solo las miniaturas medianas.</span><span class="sxs-lookup"><span data-stu-id="86a0e-139">For example, `/thumbnails?select=medium` retrieves only the medium sized thumbnails.</span></span>


### <a name="response"></a><span data-ttu-id="86a0e-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86a0e-140">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.thumbnailSet)" } -->

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

## <a name="get-a-single-thumbnail"></a><span data-ttu-id="86a0e-141">Obtener una única miniatura</span><span class="sxs-lookup"><span data-stu-id="86a0e-141">Get a single thumbnail</span></span>

<span data-ttu-id="86a0e-142">Recupere los metadatos de una sola miniatura y un tamaño solicitándolo directamente en una solicitud.</span><span class="sxs-lookup"><span data-stu-id="86a0e-142">Retrieve the metadata for a single thumbnail and size by addressing it directly in a request.</span></span>

### <a name="http-request"></a><span data-ttu-id="86a0e-143">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="86a0e-143">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-one-thumbnail", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/thumbnails/{thumb-id}/{size}
```

### <a name="path-parameters"></a><span data-ttu-id="86a0e-144">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="86a0e-144">Path parameters</span></span>

| <span data-ttu-id="86a0e-145">Nombre</span><span class="sxs-lookup"><span data-stu-id="86a0e-145">Name</span></span>         | <span data-ttu-id="86a0e-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="86a0e-146">Type</span></span>   | <span data-ttu-id="86a0e-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="86a0e-147">Description</span></span>                                                                              |
|:-------------|:-------|:-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86a0e-148">**item-id**</span><span class="sxs-lookup"><span data-stu-id="86a0e-148">**item-id**</span></span>  | <span data-ttu-id="86a0e-149">string</span><span class="sxs-lookup"><span data-stu-id="86a0e-149">string</span></span> | <span data-ttu-id="86a0e-150">El identificador único para el elemento al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="86a0e-150">The unique identifier for the item referenced.</span></span>                                           |
| <span data-ttu-id="86a0e-151">**thumb-id**</span><span class="sxs-lookup"><span data-stu-id="86a0e-151">**thumb-id**</span></span> | <span data-ttu-id="86a0e-152">número</span><span class="sxs-lookup"><span data-stu-id="86a0e-152">number</span></span> | <span data-ttu-id="86a0e-153">El índice de la miniatura, normalmente de 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="86a0e-153">The index of the thumbnail, usually 0-4.</span></span> <span data-ttu-id="86a0e-154">Si existe una miniatura personalizada, su índice es 0.</span><span class="sxs-lookup"><span data-stu-id="86a0e-154">If there is a custom thumbnail, its index is 0.</span></span> |
| <span data-ttu-id="86a0e-155">**size**</span><span class="sxs-lookup"><span data-stu-id="86a0e-155">**size**</span></span>     | <span data-ttu-id="86a0e-156">cadena</span><span class="sxs-lookup"><span data-stu-id="86a0e-156">string</span></span> | <span data-ttu-id="86a0e-157">El tamaño de la miniatura solicitada.</span><span class="sxs-lookup"><span data-stu-id="86a0e-157">The size of the thumbnail requested.</span></span> <span data-ttu-id="86a0e-158">Puede ser uno de los tamaños estándares enumerados a continuación o uno personalizado.</span><span class="sxs-lookup"><span data-stu-id="86a0e-158">This can be one of the standard sizes listed below or a custom size.</span></span> |

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.thumbnail" } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "width": 100,
  "height": 100,
  "url": "https://onedrive.com/asd123a/asdjlkasjdkasdjlk.jpg"
}
```

## <a name="retrieve-thumbnail-binary-content"></a><span data-ttu-id="86a0e-159">Recuperar el contenido binario de miniaturas</span><span class="sxs-lookup"><span data-stu-id="86a0e-159">Retrieve thumbnail binary content</span></span>

<span data-ttu-id="86a0e-160">Puede recuperar directamente el contenido de la miniatura solicitando la propiedad **content** de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="86a0e-160">You can directly retrieve the content of the thumbnail by requesting the **content** property of the thumbnail.</span></span>

### <a name="http-request"></a><span data-ttu-id="86a0e-161">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="86a0e-161">HTTP request</span></span>

<!-- { "blockType": "request", "name":"get-thumbnail-content", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/thumbnails/{thumb-id}/{size}/content
```

### <a name="response"></a><span data-ttu-id="86a0e-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86a0e-162">Response</span></span>

<span data-ttu-id="86a0e-163">El servicio responde con un redireccionamiento a la dirección URL de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="86a0e-163">The service responds with a redirect to the thumbnail URL.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

<span data-ttu-id="86a0e-164">Las direcciones URL de la miniatura son seguras en caché.</span><span class="sxs-lookup"><span data-stu-id="86a0e-164">Thumbnail URLs are cache-safe.</span></span> <span data-ttu-id="86a0e-165">La dirección URL cambiará si el elemento cambia de manera que necesite generar una nueva miniatura.</span><span class="sxs-lookup"><span data-stu-id="86a0e-165">The URL will change, if the item changes in a way that requires a new thumbnail to be generated.</span></span>


## <a name="getting-thumbnails-while-listing-driveitems"></a><span data-ttu-id="86a0e-166">Obtención de miniaturas al enumerar recursos DriveItem</span><span class="sxs-lookup"><span data-stu-id="86a0e-166">Getting thumbnails while listing DriveItems</span></span>

<span data-ttu-id="86a0e-167">Si está recuperando una lista de recursos DriveItem para mostrar, puede usar el parámetro de cadena de consulta _$expand_ para que también incluya las miniaturas de esos recursos.</span><span class="sxs-lookup"><span data-stu-id="86a0e-167">If you are retrieving a list of DriveItem resources to display, you can use the _$expand_ query string parameter to also include the thumbnails for those resources.</span></span>
<span data-ttu-id="86a0e-168">Esto permite que su aplicación recupere miniaturas y elementos en una única solicitud, en lugar de emitir varias solicitudes.</span><span class="sxs-lookup"><span data-stu-id="86a0e-168">This enables your app to retrieve thumbnails and items in a single request, instead of issuing many requests.</span></span>

### <a name="http-request"></a><span data-ttu-id="86a0e-169">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="86a0e-169">HTTP request</span></span>

<!-- { "blockType": "request", "name":"get-thumbnail-while-listing", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/children?$expand=thumbnails
```

### <a name="response"></a><span data-ttu-id="86a0e-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86a0e-170">Response</span></span>

<span data-ttu-id="86a0e-171">Las respuestas del servicio con la lista de recursos DriveItem y sus miniaturas.</span><span class="sxs-lookup"><span data-stu-id="86a0e-171">The service responses with the list of DriveItems and their thumbnails.</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItem)", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "182331E8-2788-4932-B52A-A6550577043F",
      "name": "my photo.jpg",
      "thumbnails": [
        {
          "small": { "width": 96,
                     "height": 96,
                     "url": "https://sn3302files..."
                   }
        }
      ]
    },
    {
      "id": "2D223953-A56B-4D9B-ADF3-13E7820673A2",
      "name": "presentation.pptx",
      "thumbnails": [
        {
          "small": { "width": 96,
                     "height": 96,
                     "url": "https://sn3302files..."
                   }
        }
      ]
    }
  ]
}
```

## <a name="size-values"></a><span data-ttu-id="86a0e-172">Valores de tamaño</span><span class="sxs-lookup"><span data-stu-id="86a0e-172">Size values</span></span>

<span data-ttu-id="86a0e-p111">Esta tabla define los tamaños posibles de las miniaturas. Puede solicitar cualquier tamaño de miniatura arbitrario, pero es probable que existan valores definidos y que se devuelva un valor rápidamente:</span><span class="sxs-lookup"><span data-stu-id="86a0e-p111">This table defines the possible thumbnail sizes. While you can request any arbitrary thumbnail size, the defined values are likely to exist and return a value quickly:</span></span>

| <span data-ttu-id="86a0e-175">Nombre</span><span class="sxs-lookup"><span data-stu-id="86a0e-175">Name</span></span>           | <span data-ttu-id="86a0e-176">Resolución</span><span class="sxs-lookup"><span data-stu-id="86a0e-176">Resolution</span></span>  | <span data-ttu-id="86a0e-177">Relación de aspecto</span><span class="sxs-lookup"><span data-stu-id="86a0e-177">Aspect Ratio</span></span> | <span data-ttu-id="86a0e-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="86a0e-178">Description</span></span>                                                          |
|:---------------|:------------|:-------------|:---------------------------------------------------------------------|
| `small`        | <span data-ttu-id="86a0e-179">borde más largo 96</span><span class="sxs-lookup"><span data-stu-id="86a0e-179">96 longest</span></span>  | <span data-ttu-id="86a0e-180">Original</span><span class="sxs-lookup"><span data-stu-id="86a0e-180">Original</span></span>     | <span data-ttu-id="86a0e-181">Miniatura pequeña y muy comprimida recortada en una relación de aspecto cuadrada.</span><span class="sxs-lookup"><span data-stu-id="86a0e-181">Small, highly compressed thumbnail cropped to a square aspect ratio.</span></span> |
| `medium`       | <span data-ttu-id="86a0e-182">borde más largo 176</span><span class="sxs-lookup"><span data-stu-id="86a0e-182">176 longest</span></span> | <span data-ttu-id="86a0e-183">Original</span><span class="sxs-lookup"><span data-stu-id="86a0e-183">Original</span></span>     | <span data-ttu-id="86a0e-184">Miniatura recortada al tamaño estándar del elemento para la vista web de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="86a0e-184">Cropped to the standard item size for the OneDrive web view.</span></span>         |
| `large`        | <span data-ttu-id="86a0e-185">borde más largo 800</span><span class="sxs-lookup"><span data-stu-id="86a0e-185">800 longest</span></span> | <span data-ttu-id="86a0e-186">Original</span><span class="sxs-lookup"><span data-stu-id="86a0e-186">Original</span></span>     | <span data-ttu-id="86a0e-187">Miniatura con el borde más largo cambiado a un tamaño de 800 píxeles.</span><span class="sxs-lookup"><span data-stu-id="86a0e-187">Thumbnail with the longest edge resized to 800 pixels.</span></span>               |
| `smallSquare`  | <span data-ttu-id="86a0e-188">96x96</span><span class="sxs-lookup"><span data-stu-id="86a0e-188">96x96</span></span>       | <span data-ttu-id="86a0e-189">Recorte cuadrado</span><span class="sxs-lookup"><span data-stu-id="86a0e-189">Square Crop</span></span>  | <span data-ttu-id="86a0e-190">Miniatura de cuadrado pequeño</span><span class="sxs-lookup"><span data-stu-id="86a0e-190">Small square thumbnail</span></span>                                               |
| `mediumSquare` | <span data-ttu-id="86a0e-191">176x176</span><span class="sxs-lookup"><span data-stu-id="86a0e-191">176x176</span></span>     | <span data-ttu-id="86a0e-192">Recorte cuadrado</span><span class="sxs-lookup"><span data-stu-id="86a0e-192">Square Crop</span></span>  | <span data-ttu-id="86a0e-193">Miniatura de cuadrado pequeño</span><span class="sxs-lookup"><span data-stu-id="86a0e-193">Small square thumbnail</span></span>                                               |
| `largeSquare`  | <span data-ttu-id="86a0e-194">800x800</span><span class="sxs-lookup"><span data-stu-id="86a0e-194">800x800</span></span>     | <span data-ttu-id="86a0e-195">Recorte cuadrado</span><span class="sxs-lookup"><span data-stu-id="86a0e-195">Square Crop</span></span>  | <span data-ttu-id="86a0e-196">Miniatura de cuadrado grande</span><span class="sxs-lookup"><span data-stu-id="86a0e-196">Large square thumbnail</span></span>                                               |

## <a name="requesting-custom-thumbnail-sizes"></a><span data-ttu-id="86a0e-197">Solicitar tamaños personalizados de miniaturas</span><span class="sxs-lookup"><span data-stu-id="86a0e-197">Requesting custom thumbnail sizes</span></span>

<span data-ttu-id="86a0e-198">Además de los tamaños definidos, la aplicación puede solicitar un tamaño de miniatura personalizado especificando las dimensiones de la miniatura prefijada con `c`.</span><span class="sxs-lookup"><span data-stu-id="86a0e-198">In addition to the defined sizes, your app can request a custom thumbnail size by specifying the dimensions of the thumbnail prefixed with `c`.</span></span>
<span data-ttu-id="86a0e-199">Por ejemplo, si su aplicación necesita miniaturas de tamaño 300x400, puede solicitar ese tamaño de esta forma:</span><span class="sxs-lookup"><span data-stu-id="86a0e-199">For example if your app needs thumbnails that are 300x400, it can request that size like this:</span></span>

<!-- { "name": "get-thumbnail-custom-size", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/thumbnails?select=c300x400_Crop
```

<span data-ttu-id="86a0e-200">Que responde solo con el tamaño de miniatura personalizado seleccionado:</span><span class="sxs-lookup"><span data-stu-id="86a0e-200">Which responds with just the custom thumbnail size selected:</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.thumbnailSet)" } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "0",
      "c300x400_Crop": { "height": 300, "width": 400, "url": "https://sn3302files.onedrive.com/123"},
    }
  ]
}
```

<span data-ttu-id="86a0e-201">Puede especificar las siguientes opciones después del tamaño de la miniatura solicitado:</span><span class="sxs-lookup"><span data-stu-id="86a0e-201">You can specify the following options after the size of the thumbnail requested:</span></span>

### <a name="examples-of-custom-identifiers"></a><span data-ttu-id="86a0e-202">Ejemplos de identificadores personalizados</span><span class="sxs-lookup"><span data-stu-id="86a0e-202">Examples of custom identifiers</span></span>

| <span data-ttu-id="86a0e-203">Identificador de miniatura</span><span class="sxs-lookup"><span data-stu-id="86a0e-203">Thumbnail identifier</span></span> | <span data-ttu-id="86a0e-204">Resolución</span><span class="sxs-lookup"><span data-stu-id="86a0e-204">Resolution</span></span>             | <span data-ttu-id="86a0e-205">Relación de aspecto</span><span class="sxs-lookup"><span data-stu-id="86a0e-205">Aspect ratio</span></span> | <span data-ttu-id="86a0e-206">Descripción</span><span class="sxs-lookup"><span data-stu-id="86a0e-206">Description</span></span>                                                                                                                                         |
|:---------------------|:-----------------------|:-------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86a0e-207">c300x400</span><span class="sxs-lookup"><span data-stu-id="86a0e-207">c300x400</span></span>             | <span data-ttu-id="86a0e-208">Limitado por un cuadro de 300x400</span><span class="sxs-lookup"><span data-stu-id="86a0e-208">Bounded by 300x400 box</span></span> | <span data-ttu-id="86a0e-209">Original</span><span class="sxs-lookup"><span data-stu-id="86a0e-209">Original</span></span>     | <span data-ttu-id="86a0e-210">Genera una miniatura que se adapta dentro de un cuadro de 300x400 píxeles, manteniendo la relación de aspecto</span><span class="sxs-lookup"><span data-stu-id="86a0e-210">Generate a thumbnail that fits inside a 300x400 pixel box, maintaining aspect ratio</span></span>                                                                 |
| <span data-ttu-id="86a0e-211">c300x400_Crop</span><span class="sxs-lookup"><span data-stu-id="86a0e-211">c300x400_Crop</span></span>        | <span data-ttu-id="86a0e-212">300x400</span><span class="sxs-lookup"><span data-stu-id="86a0e-212">300x400</span></span>                | <span data-ttu-id="86a0e-213">Recortado</span><span class="sxs-lookup"><span data-stu-id="86a0e-213">Cropped</span></span>      | <span data-ttu-id="86a0e-214">Genera una miniatura que tiene 300x400 píxeles.</span><span class="sxs-lookup"><span data-stu-id="86a0e-214">Generate a thumbnail that is 300x400 pixels.</span></span> <span data-ttu-id="86a0e-215">Esto funciona cambiando el tamaño de la imagen para rellenar el cuadro de 300x400 y recortando lo que sobresalga de este.</span><span class="sxs-lookup"><span data-stu-id="86a0e-215">This works by resizing the image to fill the 300x400 box and cropping whatever spills outside the box.</span></span> |

<span data-ttu-id="86a0e-216">**Nota:** La miniatura devuelta puede no coincidir exactamente con las dimensiones en píxeles que se solicitaron, pero coincidirá con la relación de aspecto.</span><span class="sxs-lookup"><span data-stu-id="86a0e-216">**Note:** The thumbnail returned may not exactly match the pixel dimensions that was requested, but will match the aspect ratio.</span></span>
<span data-ttu-id="86a0e-217">En algunos casos, puede devolverse una miniatura más grande que la que se ha solicitado si la miniatura ya existe y se puede escalar fácilmente para ajustarse a la resolución solicitada.</span><span class="sxs-lookup"><span data-stu-id="86a0e-217">In some cases, a larger thumbnail may be returned than was requested, if the thumbnail already exists and can easily be scaled to match the requested resolution.</span></span>

## <a name="remarks"></a><span data-ttu-id="86a0e-218">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86a0e-218">Remarks</span></span>

<span data-ttu-id="86a0e-219">**Nota** En OneDrive para la Empresa y en SharePoint:</span><span class="sxs-lookup"><span data-stu-id="86a0e-219">**Note** In OneDrive for Business and SharePoint:</span></span>

<span data-ttu-id="86a0e-220">El uso de estas llamadas para expandir la colección de miniaturas no funcionará:</span><span class="sxs-lookup"><span data-stu-id="86a0e-220">Using these calls to expand the thumbnails collection will not work:</span></span>

* `GET /drive/root:/{item-path}?expand=children(expand=thumbnails)`
* `GET /drive/items/{item-id}/children?expand=thumbnails`

<span data-ttu-id="86a0e-221">Las miniaturas no se admiten en SharePoint Server 2016.</span><span class="sxs-lookup"><span data-stu-id="86a0e-221">Thumbnails are not supported on SharePoint Server 2016.</span></span>

### <a name="error-responses"></a><span data-ttu-id="86a0e-222">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="86a0e-222">Error responses</span></span>

<span data-ttu-id="86a0e-223">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="86a0e-223">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Get metadata and content for thumbnails of multiple sizes for OneDrive items.",
  "keywords": "thumbnail,content,download,sizes",
  "section": "documentation",
  "tocPath": "Items/Thumbnails"
} -->
