# <a name="download-the-contents-of-a-driveitem"></a><span data-ttu-id="6cb24-101">Descargar el contenido de un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="6cb24-101">Download the contents of a DriveItem</span></span>

<span data-ttu-id="6cb24-p101">Descargue el contenido de un objeto driveItem. Solo se puede descargar un objeto driveItem con la propiedad **file**.</span><span class="sxs-lookup"><span data-stu-id="6cb24-p101">Download the contents for a driveItem. Only driveItem with the **file** property can be downloaded.</span></span>

## <a name="permissions"></a><span data-ttu-id="6cb24-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="6cb24-104">Permissions</span></span>
<span data-ttu-id="6cb24-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6cb24-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6cb24-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6cb24-107">Permission type</span></span>      | <span data-ttu-id="6cb24-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6cb24-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6cb24-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6cb24-109">Delegated (work or school account)</span></span> | <span data-ttu-id="6cb24-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6cb24-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="6cb24-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6cb24-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6cb24-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6cb24-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="6cb24-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6cb24-113">Application</span></span> | <span data-ttu-id="6cb24-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6cb24-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6cb24-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6cb24-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root:/{item-path}:/content
GET /me/drive/items/{item-id}/content
GET /drives/items/{item-id}/content
GET /groups/{group-id}/drive/items/{item-id}/content
```

## <a name="request-headers"></a><span data-ttu-id="6cb24-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6cb24-116">Request headers</span></span>

| <span data-ttu-id="6cb24-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="6cb24-117">Name</span></span>          | <span data-ttu-id="6cb24-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6cb24-118">Value</span></span>  | <span data-ttu-id="6cb24-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cb24-119">Description</span></span>                                                                                                                                              |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb24-120">if-none-match</span><span class="sxs-lookup"><span data-stu-id="6cb24-120">if-none-match</span></span> | <span data-ttu-id="6cb24-121">String</span><span class="sxs-lookup"><span data-stu-id="6cb24-121">String</span></span> | <span data-ttu-id="6cb24-122">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="6cb24-122">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6cb24-123">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="6cb24-123">Request body</span></span>
<span data-ttu-id="6cb24-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6cb24-124">Do not supply a request body for this method.</span></span>

## <a name="example"></a><span data-ttu-id="6cb24-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6cb24-125">Example</span></span>
<span data-ttu-id="6cb24-126">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6cb24-126">Here is an example of how to call this API.</span></span>


<!-- { "blockType": "request", "name": "driveitem-download-contents" } -->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/content
```

##### <a name="response"></a><span data-ttu-id="6cb24-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6cb24-127">Response</span></span>
<span data-ttu-id="6cb24-p103">Devuelve una respuesta `302 Found` que redirige a una URL de descarga autenticada previamente para el archivo. Se trata de la misma dirección URL disponible mediante la propiedad `@microsoft.graph.downloadUrl` del objeto DriveItem.</span><span class="sxs-lookup"><span data-stu-id="6cb24-p103">Returns a `302 Found` response redirecting to a pre-authenticated download URL for the file. This is the same URL available through the `@microsoft.graph.downloadUrl` property on the DriveItem.</span></span>

<span data-ttu-id="6cb24-p104">Para descargar el contenido del archivo, la aplicación tendrá que seguir el encabezado `Location` de la respuesta. Muchas bibliotecas de cliente HTTP seguirán de forma automática el redireccionamiento 302 e iniciarán la descarga del archivo de forma inmediata.</span><span class="sxs-lookup"><span data-stu-id="6cb24-p104">To download the contents of the file your application will need to follow the `Location` header in the response. Many HTTP client libraries will automatically follow the 302 redirection and start downloading the file immedately.</span></span>

<span data-ttu-id="6cb24-132">Las URL de descarga autenticadas previamente solo son válidas durante un breve período de tiempo (unos minutos) y no requieren un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="6cb24-132">Pre-authenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to download.</span></span>

<!-- { "blockType": "response", "@odata.type": "stream" } -->
```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

## <a name="partial-range-downloads"></a><span data-ttu-id="6cb24-133">Descargas de rango parcial</span><span class="sxs-lookup"><span data-stu-id="6cb24-133">Partial range downloads</span></span>

<span data-ttu-id="6cb24-p105">Para descargar un rango parcial de bytes del archivo, la aplicación puede usar el encabezado `Range` como se especifica en [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). Tenga en cuenta que debe anexar el encabezado `Range` a la dirección URL `@microsoft.graph.downloadUrl` real y no a la solicitud de `/content`.</span><span class="sxs-lookup"><span data-stu-id="6cb24-p105">To download a partial range of bytes from the file, your app can use the `Range` header as specified in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). Note that you must append the `Range` header to the actual `@microsoft.graph.downloadUrl` URL and not to the request for `/content`.</span></span>

<!-- { "blockType": "request", "name": "driveitem-get-partial-content" } -->
```http
GET https://b0mpua-by3301.files.1drv.com/y23vmag
Range: bytes=0-1023
```

<span data-ttu-id="6cb24-p106">Esto devolverá una respuesta `HTTP 206 Partial Content` con el rango de solicitud de bytes del archivo. Si no se puede generar el rango, se puede omitir el encabezado Range y se devolverá una respuesta `HTTP 200` con el contenido completo del archivo.</span><span class="sxs-lookup"><span data-stu-id="6cb24-p106">This will return an `HTTP 206 Partial Content` response with the request range of bytes from the file. If the range cannot be generated the Range header may be ignored and an `HTTP 200` response would be returned with the full contents of the file.</span></span>

<!-- { "blockType": "response", "@odata.type": "stream" } -->
```http
HTTP/1.1 206 Partial Content
Content-Range: bytes 0-1023/2048

<first 1024 bytes of file>
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Download item",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Download file"
}-->
