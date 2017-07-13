<span data-ttu-id="34e59-p101">La API de carga simple le permite proporcionar el contenido de un archivo nuevo o actualizar el contenido de un archivo existente en una sola llamada API. Este método solo admite archivos de hasta 4 MB de tamaño.</span><span class="sxs-lookup"><span data-stu-id="34e59-p101">The simple upload API allows you to provide the contents of a new file or update the contents of an existing file in a single API call. This method only supports files up to 4MB in size.</span></span>

La API de carga simple le permite proporcionar el contenido de un archivo nuevo o actualizar el contenido de un archivo existente en una sola llamada API. Este método solo admite archivos de hasta 4 MB de tamaño.

<span data-ttu-id="34e59-104">Para cargar archivos grandes, consulte [Upload large files with an upload session](item_createuploadsession.md) (Cargar archivos grandes con una sesión de carga).</span><span class="sxs-lookup"><span data-stu-id="34e59-104">To upload large files see [Upload large files with an upload session](item_createuploadsession.md).</span></span>

## <span data-ttu-id="34e59-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="34e59-105">Prerequisites</span></span>
<a id="prerequisites" class="xliff"></a>
<span data-ttu-id="34e59-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="34e59-106">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="34e59-107">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e59-107">Files.ReadWrite</span></span>
* <span data-ttu-id="34e59-108">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="34e59-108">Files.ReadWrite.All</span></span>
* <span data-ttu-id="34e59-109">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="34e59-109">Sites.ReadWrite.All</span></span>


## <span data-ttu-id="34e59-110">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="34e59-110">HTTP request</span></span>
<a id="http-request" class="xliff"></a>
<!-- { "blockType": "ignored" } -->
```http
PUT /me/drive/items/{parent-id}:/{filename}:/content
PUT /me/drive/root:/{parent-path}/{filename}:/content
PUT /me/drive/items/{parent-id}/children/{filename}/content
PUT /groups/{id}/drive/items/{parent-id}/children/{filename}/content
```

## <span data-ttu-id="34e59-111">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="34e59-111">Request body</span></span>
<a id="request-body" class="xliff"></a>
<span data-ttu-id="34e59-112">El contenido del cuerpo de la solicitud debe ser la secuencia binaria del archivo que se cargará.</span><span class="sxs-lookup"><span data-stu-id="34e59-112">The contents of the request body should be the binary stream of the file to be uploaded.</span></span>

## <span data-ttu-id="34e59-113">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34e59-113">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="34e59-114">Si se ejecuta correctamente, este método devuelve un objeto [driveItem](../resources/driveitem.md) en el cuerpo de la respuesta del archivo que se ha creado.</span><span class="sxs-lookup"><span data-stu-id="34e59-114">If successful, this method returns a [driveItem](../resources/driveitem.md) object in the response body for the newly created file.</span></span>

## <span data-ttu-id="34e59-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34e59-115">Example</span></span>
<a id="example" class="xliff"></a>
<span data-ttu-id="34e59-116">En este ejemplo, se carga un archivo mediante la ruta de acceso al OneDrive del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="34e59-116">This example uploads a file by path to the signed-in user's OneDrive.</span></span>

<!-- {
  "blockType": "request",
  "name": "upload_item"
}-->
```http
PUT /me/drive/root:/{item-path}:/content
Content-type: text/plain

The contents of the file goes here.
```

## <span data-ttu-id="34e59-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34e59-117">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="34e59-118">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34e59-118">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem"
} -->
```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "0123456789abc",
  "name": "myfile.jpg",
  "size": 10191,
  "file": { }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Upload item",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
