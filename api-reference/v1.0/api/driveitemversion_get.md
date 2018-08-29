# <a name="get-a-driveitemversion-resource"></a><span data-ttu-id="a808f-101">Obtener un recurso DriveItemVersion</span><span class="sxs-lookup"><span data-stu-id="a808f-101">Get a DriveItemVersion resource (preview)</span></span>

<span data-ttu-id="a808f-102">Recupere los metadatos de una versión específica de un recurso [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="a808f-102">Retrieve the metadata for a specific version of a [DriveItem](../resources/driveitem.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="a808f-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="a808f-103">Permissions</span></span>

<span data-ttu-id="a808f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a808f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a808f-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a808f-106">Permission type</span></span>      | <span data-ttu-id="a808f-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a808f-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a808f-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a808f-108">Delegated (work or school account)</span></span> | <span data-ttu-id="a808f-109">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All y Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a808f-109">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="a808f-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a808f-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a808f-111">Files.Read, Files.ReadWrite, Files.Read.All y Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a808f-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="a808f-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a808f-112">Application</span></span> | <span data-ttu-id="a808f-113">Files.Read.All, Files.ReadWrite.All, Sites.Read.All y Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a808f-113">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |


## <a name="http-request"></a><span data-ttu-id="a808f-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a808f-114">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /drives/{drive-id}/items/{item-id}/versions/{version-id}
GET /groups/{group-id}/drive/{item-id}/versions/{version-id}
GET /me/drive/items/{item-id}/versions/{version-id}
GET /sites/{site-id}/drive/items/{item-id}/versions/{version-id}
GET /users/{user-id}/drive/items/{item-id}/versions/{version-id}
```

## <a name="response"></a><span data-ttu-id="a808f-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a808f-115">Response</span></span>

<span data-ttu-id="a808f-116">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [DriveItemVersion](../resources/driveitemversion.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a808f-116">If successful, this method returns a `200 OK` response code and a [DriveItemVersion](../resources/driveitemversion.md) object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="a808f-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a808f-117">Example</span></span>

<span data-ttu-id="a808f-118">Este ejemplo recupera una versión de un archivo en la unidad del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="a808f-118">This example retrieves a version of a file in the current user's drive.</span></span>

### <a name="http-request"></a><span data-ttu-id="a808f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a808f-119">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-single-version", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/versions/{version-id}
```

### <a name="response"></a><span data-ttu-id="a808f-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a808f-120">Response</span></span>

<span data-ttu-id="a808f-121">Devuelve una colección de versiones:</span><span class="sxs-lookup"><span data-stu-id="a808f-121">This returns a collection of versions:</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItemVersion", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "id": "D4990684-58CE-4FAB-9B87-D6C49E74F298",
    "lastModifiedBy": {
    "user": {
        "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
        "displayName": "Ryan Gregg"
    }
    },
    "lastModifiedDateTime": "2017-09-14T12:34:53.912Z",
    "size": 123
}
```

## <a name="remarks"></a><span data-ttu-id="a808f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a808f-122">Remarks</span></span>

<span data-ttu-id="a808f-123">OneDrive no conserva todos los metadatos de las versiones anteriores de un archivo.</span><span class="sxs-lookup"><span data-stu-id="a808f-123">OneDrive does not preserve the complete metadata for previous versions of a file.</span></span>

<span data-ttu-id="a808f-124">Cuando la aplicación recupera la lista de versiones disponibles de un archivo, se devuelve un recurso [DriveItemVersion](../resources/driveItemVersion.md) que proporciona la información disponible sobre la versión específica.</span><span class="sxs-lookup"><span data-stu-id="a808f-124">When your app retrieves the list of available versions for a file, a [DriveItemVersion](../resources/driveItemVersion.md) resource is returned that provides the available information about the specific version.</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "List, review, and download previous versions of a driveItem",
  "keywords": "version, version history, versions",
  "section": "documentation",
  "tocPath": "Items/Version history"
} -->
