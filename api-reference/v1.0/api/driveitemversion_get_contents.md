# <a name="download-contents-of-a-driveitemversion-resource"></a><span data-ttu-id="9508b-101">Descargar contenido de un recurso DriveItemVersion</span><span class="sxs-lookup"><span data-stu-id="9508b-101">Download contents of a DriveItemVersion resource (preview)</span></span>

<span data-ttu-id="9508b-102">Recupere el contenido de una versión específica de un recurso [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="9508b-102">Retrieve the contents of a specific version of a [DriveItem](../resources/driveitem.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="9508b-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9508b-103">Permissions</span></span>

<span data-ttu-id="9508b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9508b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9508b-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9508b-106">Permission type</span></span>      | <span data-ttu-id="9508b-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9508b-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9508b-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9508b-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9508b-109">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All y Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9508b-109">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="9508b-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9508b-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9508b-111">Files.Read, Files.ReadWrite, Files.Read.All y Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9508b-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="9508b-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9508b-112">Application</span></span> | <span data-ttu-id="9508b-113">Files.Read.All, Files.ReadWrite.All, Sites.Read.All y Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9508b-113">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |


## <a name="http-request"></a><span data-ttu-id="9508b-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9508b-114">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /drives/{drive-id}/items/{item-id}/versions/{version-id}/content
GET /groups/{group-id}/drive/{item-id}/versions/{version-id}/content
GET /me/drive/items/{item-id}/versions/{version-id}/content
GET /sites/{site-id}/drive/items/{item-id}/versions/{version-id}/content
GET /users/{user-id}/drive/items/{item-id}/versions/{version-id}/content
```

## <a name="response"></a><span data-ttu-id="9508b-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9508b-115">Response</span></span>

<span data-ttu-id="9508b-116">Devuelve una respuesta `302 Found` que redirige a una dirección URL de descarga autenticada previamente para los bytes del archivo.</span><span class="sxs-lookup"><span data-stu-id="9508b-116">Returns a `302 Found` response redirecting to a pre-authenticated download URL for the bytes of the file.</span></span>

<span data-ttu-id="9508b-p102">Para descargar el contenido del archivo, la aplicación tendrá que seguir el encabezado `Location` de la respuesta. Muchas bibliotecas de cliente HTTP seguirán de forma automática el redireccionamiento 302 e iniciarán la descarga del archivo de forma inmediata.</span><span class="sxs-lookup"><span data-stu-id="9508b-p102">To download the contents of the file your application will need to follow the `Location` header in the response. Many HTTP client libraries will automatically follow the 302 redirection and start downloading the file immedately.</span></span>

<span data-ttu-id="9508b-119">Las URL de descarga autenticadas previamente solo son válidas durante un breve período de tiempo (unos minutos) y no requieren un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="9508b-119">Pre-authenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to download.</span></span>

## <a name="example"></a><span data-ttu-id="9508b-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9508b-120">Example</span></span>

<span data-ttu-id="9508b-121">Este ejemplo recupera una versión de un archivo en la unidad del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="9508b-121">This example retrieves a version of a file in the current user's drive.</span></span>

### <a name="http-request"></a><span data-ttu-id="9508b-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9508b-122">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-version-contents", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/versions/{version-id}/content
```

### <a name="response"></a><span data-ttu-id="9508b-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9508b-123">Response</span></span>

<span data-ttu-id="9508b-124">Esto devuelve una redirección donde se puede descargar el contenido de la versión.</span><span class="sxs-lookup"><span data-stu-id="9508b-124">This returns a redirect to where the contents of the version can be downloaded.</span></span>

<!-- { "blockType": "response", "isEmpty": true  } -->

```http
HTTP/1.1 302 Found
Location: https://onedrive.com/34FF49D6...
```


## <a name="remarks"></a><span data-ttu-id="9508b-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9508b-125">Remarks</span></span>

<span data-ttu-id="9508b-126">OneDrive no conserva todos los metadatos de las versiones anteriores de un archivo.</span><span class="sxs-lookup"><span data-stu-id="9508b-126">OneDrive does not preserve the complete metadata for previous versions of a file.</span></span>

<span data-ttu-id="9508b-127">Cuando la aplicación recupera la lista de versiones disponibles de un archivo, se devuelve un recurso [DriveItemVersion](../resources/driveItemVersion.md) que proporciona la información disponible sobre la versión específica.</span><span class="sxs-lookup"><span data-stu-id="9508b-127">When your app retrieves the list of available versions for a file, a [DriveItemVersion](../resources/driveItemVersion.md) resource is returned that provides the available information about the specific version.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "List, review, and download previous versions of a driveItem",
  "keywords": "version, version history, versions",
  "section": "documentation",
  "tocPath": "Items/Version history"
} -->
