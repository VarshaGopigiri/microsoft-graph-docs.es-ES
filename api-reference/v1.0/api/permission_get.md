# <a name="get-permission"></a><span data-ttu-id="58e7e-101">Obtener permiso</span><span class="sxs-lookup"><span data-stu-id="58e7e-101">Get permission</span></span>

<span data-ttu-id="58e7e-102">Recupere las propiedades y las relaciones del objeto de permiso.</span><span class="sxs-lookup"><span data-stu-id="58e7e-102">Retrieve the properties and relationships of permission object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="58e7e-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="58e7e-103">Prerequisites</span></span>
<span data-ttu-id="58e7e-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="58e7e-104">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="58e7e-105">Files.Read</span><span class="sxs-lookup"><span data-stu-id="58e7e-105">Files.Read</span></span>
* <span data-ttu-id="58e7e-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="58e7e-106">Files.ReadWrite</span></span>
* <span data-ttu-id="58e7e-107">Files.Read.All</span><span class="sxs-lookup"><span data-stu-id="58e7e-107">Files.Read.All</span></span>
* <span data-ttu-id="58e7e-108">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="58e7e-108">Files.ReadWrite.All</span></span>
* <span data-ttu-id="58e7e-109">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="58e7e-109">Sites.Read.All</span></span>
* <span data-ttu-id="58e7e-110">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="58e7e-110">Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="58e7e-111">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="58e7e-111">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/items/{item-id}/permissions/{perm-id}
GET /me/drive/root:/{path}:/permissions/{perm-id}
GET /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
GET /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="58e7e-112">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="58e7e-112">Optional query parameters</span></span>
<span data-ttu-id="58e7e-113">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58e7e-113">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-body"></a><span data-ttu-id="58e7e-114">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="58e7e-114">Request body</span></span>
<span data-ttu-id="58e7e-115">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="58e7e-115">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="58e7e-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58e7e-116">Response</span></span>

<span data-ttu-id="58e7e-117">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [Permission](../resources/permission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58e7e-117">If successful, this method returns a `200 OK` response code and [Permission](../resources/permission.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="58e7e-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58e7e-118">Example</span></span>

##### <a name="request"></a><span data-ttu-id="58e7e-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="58e7e-119">Request</span></span>

<span data-ttu-id="58e7e-120">Aquí tiene un ejemplo de la solicitud para acceder a un permiso en la carpeta raíz.</span><span class="sxs-lookup"><span data-stu-id="58e7e-120">Here is an example of the request to access a permission on the root folder.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_permission"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/permissions/{perm-id}
```
##### <a name="response"></a><span data-ttu-id="58e7e-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58e7e-121">Response</span></span>
<span data-ttu-id="58e7e-122">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58e7e-122">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.permission"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 762

{
  "grantedTo": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "efee1b77-fb3b-4f65-99d6-274c11914d12"
    }
  },
  "id": "1",
  "roles": [ "write" ]
}
```

## <a name="remarks"></a><span data-ttu-id="58e7e-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58e7e-123">Remarks</span></span>

<span data-ttu-id="58e7e-124">El recurso [Permission](../resources/permission.md) usa _facetas_ para proporcionar información sobre el tipo de permiso que representa el recurso.</span><span class="sxs-lookup"><span data-stu-id="58e7e-124">The [Permission](../resources/permission.md) resource uses _facets_ to provide information about the kind of permission represented by the resource.</span></span>

<span data-ttu-id="58e7e-p101">Los permisos con una faceta [**link**](../resources/sharinglink.md) representan vínculos para compartir creados en el elemento. Los vínculos para compartir contienen un token único que proporciona acceso al elemento a cualquier usuario con el vínculo.</span><span class="sxs-lookup"><span data-stu-id="58e7e-p101">Permissions with a [**link**](../resources/sharinglink.md) facet represent sharing links created on the item. Sharing links contain a unique token that provides access to the item for anyone with the link.</span></span>

<span data-ttu-id="58e7e-127">Los permisos con una faceta [**invitation**](../resources/sharinginvitation.md) representan los permisos agregados al invitar a usuarios o grupos específicos para que tengan acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="58e7e-127">Permissions with a [**invitation**](../resources/sharinginvitation.md) facet represent permissions added by inviting specific users or groups to have access to the file.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get permission",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Get permission"
}-->
