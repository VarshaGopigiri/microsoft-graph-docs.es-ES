# <a name="update-permission"></a><span data-ttu-id="4b7cc-101">Update permission</span><span class="sxs-lookup"><span data-stu-id="4b7cc-101">Update permission</span></span>

<span data-ttu-id="4b7cc-102">Actualiza las propiedades de un permiso aplicando revisiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-102">Update the properties of a permission by patching the resource.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4b7cc-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4b7cc-103">Prerequisites</span></span>

<span data-ttu-id="4b7cc-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="4b7cc-104">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="4b7cc-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4b7cc-105">Files.ReadWrite</span></span>
* <span data-ttu-id="4b7cc-106">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4b7cc-106">Files.ReadWrite.All</span></span>
* <span data-ttu-id="4b7cc-107">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4b7cc-107">Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="4b7cc-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4b7cc-108">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH /me/drive/items/{item-id}/permissions/{perm-id}
PATCH /me/drive/root:/{path}:/permissions/{perm-id}
PATCH /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
PATCH /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
```

## <a name="request-headers"></a><span data-ttu-id="4b7cc-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4b7cc-109">Request headers</span></span>

| <span data-ttu-id="4b7cc-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="4b7cc-110">Name</span></span>          | <span data-ttu-id="4b7cc-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b7cc-111">Type</span></span>   | <span data-ttu-id="4b7cc-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b7cc-112">Description</span></span>                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b7cc-113">if-match</span><span class="sxs-lookup"><span data-stu-id="4b7cc-113">if-match</span></span>      | <span data-ttu-id="4b7cc-114">string</span><span class="sxs-lookup"><span data-stu-id="4b7cc-114">string</span></span> | <span data-ttu-id="4b7cc-115">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-115">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span> |


## <a name="request-body"></a><span data-ttu-id="4b7cc-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4b7cc-116">Request body</span></span>
<span data-ttu-id="4b7cc-p101">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-p101">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="4b7cc-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4b7cc-120">Property</span></span>     | <span data-ttu-id="4b7cc-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b7cc-121">Type</span></span>   | <span data-ttu-id="4b7cc-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b7cc-122">Description</span></span>                   |
|:-------------|:-------|:------------------------------|
| <span data-ttu-id="4b7cc-123">**roles**</span><span class="sxs-lookup"><span data-stu-id="4b7cc-123">**roles**</span></span>    | <span data-ttu-id="4b7cc-124">String</span><span class="sxs-lookup"><span data-stu-id="4b7cc-124">String</span></span> | <span data-ttu-id="4b7cc-125">Matriz de tipos de permisos.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-125">An array of permission types.</span></span> |

## <a name="response"></a><span data-ttu-id="4b7cc-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4b7cc-126">Response</span></span>

<span data-ttu-id="4b7cc-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [permission](../resources/permission.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-127">If successful, this method returns a `200 OK` response code and updated [permission](../resources/permission.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4b7cc-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4b7cc-128">Example</span></span>

##### <a name="request"></a><span data-ttu-id="4b7cc-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4b7cc-129">Request</span></span>

<span data-ttu-id="4b7cc-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_permission"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/permissions/{perm-id}
Content-type: application/json

{
  "roles": [ "read" ]
}
```
##### <a name="response"></a><span data-ttu-id="4b7cc-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4b7cc-131">Response</span></span>

<span data-ttu-id="4b7cc-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-132">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.permission"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "grantedTo": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "efee1b77-fb3b-4f65-99d6-274c11914d12"
    }
  },
  "id": "1",
  "roles": [ "read" ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update permission",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Update permission"
}-->
