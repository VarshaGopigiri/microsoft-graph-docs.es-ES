# <a name="upload-or-replace-the-contents-of-a-driveitem"></a><span data-ttu-id="5df02-101">Cargar o reemplazar el contenido de un objeto driveItem</span><span class="sxs-lookup"><span data-stu-id="5df02-101">Upload or replace the contents of a driveItem</span></span>

<span data-ttu-id="5df02-p101">La API de carga simple le permite proporcionar el contenido de un archivo nuevo o actualizar el contenido de un archivo existente en una sola llamada API. Este método solo admite archivos de hasta 4 MB de tamaño.</span><span class="sxs-lookup"><span data-stu-id="5df02-p101">The simple upload API allows you to provide the contents of a new file or update the contents of an existing file in a single API call. This method only supports files up to 4MB in size.</span></span>

<span data-ttu-id="5df02-104">Para cargar archivos grandes, consulte [Upload large files with an upload session](item_createuploadsession.md) (Cargar archivos grandes con una sesión de carga).</span><span class="sxs-lookup"><span data-stu-id="5df02-104">To upload large files see [Upload large files with an upload session](item_createuploadsession.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="5df02-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="5df02-105">Permissions</span></span>
<span data-ttu-id="5df02-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5df02-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5df02-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5df02-108">Permission type</span></span>      | <span data-ttu-id="5df02-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5df02-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5df02-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5df02-110">Delegated (work or school account)</span></span> | <span data-ttu-id="5df02-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5df02-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="5df02-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5df02-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5df02-113">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5df02-113">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="5df02-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5df02-114">Application</span></span> | <span data-ttu-id="5df02-115">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5df02-115">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5df02-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5df02-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /me/drive/items/{parent-id}:/{filename}:/content
PUT /me/drive/root:/{parent-path}/{filename}:/content
PUT /me/drive/items/{parent-id}/children/{filename}/content
PUT /groups/{id}/drive/items/{parent-id}/children/{filename}/content
```

## <a name="request-body"></a><span data-ttu-id="5df02-117">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="5df02-117">Request body</span></span>
<span data-ttu-id="5df02-118">El contenido del cuerpo de la solicitud debe ser la secuencia binaria del archivo que se cargará.</span><span class="sxs-lookup"><span data-stu-id="5df02-118">The contents of the request body should be the binary stream of the file to be uploaded.</span></span>

## <a name="response"></a><span data-ttu-id="5df02-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5df02-119">Response</span></span>

<span data-ttu-id="5df02-120">Si se ejecuta correctamente, este método devuelve un objeto [driveItem](../resources/driveitem.md) en el cuerpo de la respuesta del archivo que se ha creado.</span><span class="sxs-lookup"><span data-stu-id="5df02-120">If successful, this method returns a [driveItem](../resources/driveitem.md) object in the response body for the newly created file.</span></span>

## <a name="example"></a><span data-ttu-id="5df02-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5df02-121">Example</span></span>
<span data-ttu-id="5df02-122">En este ejemplo, se carga un archivo mediante la ruta de acceso al OneDrive del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="5df02-122">This example uploads a file by path to the signed-in user's OneDrive.</span></span>

<!-- {
  "blockType": "request",
  "name": "upload_item"
}-->
```http
PUT /me/drive/root:/{item-path}:/content
Content-type: text/plain

The contents of the file goes here.
```

##### <a name="response"></a><span data-ttu-id="5df02-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5df02-123">Response</span></span>

<span data-ttu-id="5df02-124">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5df02-124">The following example shows the response.</span></span>

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
