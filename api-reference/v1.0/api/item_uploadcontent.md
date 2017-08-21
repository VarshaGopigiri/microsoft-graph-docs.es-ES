# <a name="upload-or-replace-the-contents-of-a-driveitem"></a><span data-ttu-id="eb5e1-101">Cargar o reemplazar el contenido de un objeto driveItem</span><span class="sxs-lookup"><span data-stu-id="eb5e1-101">Upload or replace the contents of a driveItem</span></span>

<span data-ttu-id="eb5e1-p101">La API de carga simple le permite proporcionar el contenido de un archivo nuevo o actualizar el contenido de un archivo existente en una sola llamada API. Este método solo admite archivos de hasta 4 MB de tamaño.</span><span class="sxs-lookup"><span data-stu-id="eb5e1-p101">The simple upload API allows you to provide the contents of a new file or update the contents of an existing file in a single API call. This method only supports files up to 4MB in size.</span></span>

<span data-ttu-id="eb5e1-104">Para cargar archivos grandes, consulte [Upload large files with an upload session](item_createuploadsession.md) (Cargar archivos grandes con una sesión de carga).</span><span class="sxs-lookup"><span data-stu-id="eb5e1-104">To upload large files see [Upload large files with an upload session](item_createuploadsession.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eb5e1-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eb5e1-105">Prerequisites</span></span>
<span data-ttu-id="eb5e1-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="eb5e1-106">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="eb5e1-107">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eb5e1-107">Files.ReadWrite</span></span>
* <span data-ttu-id="eb5e1-108">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb5e1-108">Files.ReadWrite.All</span></span>
* <span data-ttu-id="eb5e1-109">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb5e1-109">Sites.ReadWrite.All</span></span>


## <a name="http-request"></a><span data-ttu-id="eb5e1-110">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb5e1-110">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /me/drive/items/{parent-id}:/{filename}:/content
PUT /me/drive/root:/{parent-path}/{filename}:/content
PUT /me/drive/items/{parent-id}/children/{filename}/content
PUT /groups/{id}/drive/items/{parent-id}/children/{filename}/content
```

## <a name="request-body"></a><span data-ttu-id="eb5e1-111">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb5e1-111">Request body</span></span>
<span data-ttu-id="eb5e1-112">El contenido del cuerpo de la solicitud debe ser la secuencia binaria del archivo que se cargará.</span><span class="sxs-lookup"><span data-stu-id="eb5e1-112">The contents of the request body should be the binary stream of the file to be uploaded.</span></span>

## <a name="response"></a><span data-ttu-id="eb5e1-113">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb5e1-113">Response</span></span>

<span data-ttu-id="eb5e1-114">Si se ejecuta correctamente, este método devuelve un objeto [driveItem](../resources/driveitem.md) en el cuerpo de la respuesta del archivo que se ha creado.</span><span class="sxs-lookup"><span data-stu-id="eb5e1-114">If successful, this method returns a [driveItem](../resources/driveitem.md) object in the response body for the newly created file.</span></span>

## <a name="example"></a><span data-ttu-id="eb5e1-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb5e1-115">Example</span></span>
<span data-ttu-id="eb5e1-116">En este ejemplo, se carga un archivo mediante la ruta de acceso al OneDrive del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="eb5e1-116">This example uploads a file by path to the signed-in user's OneDrive.</span></span>

<!-- {
  "blockType": "request",
  "name": "upload_item"
}-->
```http
PUT /me/drive/root:/{item-path}:/content
Content-type: text/plain

The contents of the file goes here.
```

##### <a name="response"></a><span data-ttu-id="eb5e1-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb5e1-117">Response</span></span>

<span data-ttu-id="eb5e1-118">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb5e1-118">The following example shows the response.</span></span>

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
