<span data-ttu-id="2f2fa-p101">Elimina un [DriveItem](../resources/driveitem.md) mediante su identificador o la ruta de acceso. Tenga en cuenta que si elimina elementos con este método moverá los elementos a la Papelera de reciclaje en lugar de eliminarlos permanentemente.</span><span class="sxs-lookup"><span data-stu-id="2f2fa-p101">Delete a [DriveItem](../resources/driveitem.md) by using its ID or path. Note that deleting items using this method will move the items to the recycle bin instead of permanently deleting the item.</span></span>

Elimina un [DriveItem](../resources/driveitem.md) mediante su identificador o la ruta de acceso. Tenga en cuenta que si elimina elementos con este método moverá los elementos a la Papelera de reciclaje en lugar de eliminarlos permanentemente.

## <span data-ttu-id="2f2fa-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2f2fa-104">Prerequisites</span></span>
<a id="prerequisites" class="xliff"></a>
<span data-ttu-id="2f2fa-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="2f2fa-105">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="2f2fa-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2f2fa-106">Files.ReadWrite</span></span>
* <span data-ttu-id="2f2fa-107">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2f2fa-107">Files.ReadWrite.All</span></span>
* <span data-ttu-id="2f2fa-108">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2f2fa-108">Sites.ReadWrite.All</span></span>

## <span data-ttu-id="2f2fa-109">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2f2fa-109">HTTP request</span></span>
<a id="http-request" class="xliff"></a>

<!-- { "blockType": "ignored" } -->
```
DELETE /me/drive/items/{item-id}
DELETE /me/drive/root:/{item-path}
DELETE /drives/{drive-id}/items/{item-id}
DELETE /groups/{group-id}/drive/items/{item-id}
```

## <span data-ttu-id="2f2fa-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2f2fa-110">Request headers</span></span>
<a id="request-headers" class="xliff"></a>

| <span data-ttu-id="2f2fa-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="2f2fa-111">Name</span></span>          | <span data-ttu-id="2f2fa-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f2fa-112">Type</span></span>   | <span data-ttu-id="2f2fa-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f2fa-113">Description</span></span>                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f2fa-114">if-match</span><span class="sxs-lookup"><span data-stu-id="2f2fa-114">if-match</span></span>      | <span data-ttu-id="2f2fa-115">String</span><span class="sxs-lookup"><span data-stu-id="2f2fa-115">String</span></span> | <span data-ttu-id="2f2fa-116">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="2f2fa-116">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span> |

## <span data-ttu-id="2f2fa-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2f2fa-117">Request body</span></span>
<a id="request-body" class="xliff"></a>
<span data-ttu-id="2f2fa-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2f2fa-118">Do not supply a request body for this method.</span></span>

## <span data-ttu-id="2f2fa-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2f2fa-119">Example</span></span>
<a id="example" class="xliff"></a>

<span data-ttu-id="2f2fa-120">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2f2fa-120">Here is an example of how to call this API.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete-item"
}-->
```
DELETE https://graph.microsoft.com/v1.0/me/drive/items/{item-id}
```

## <span data-ttu-id="2f2fa-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f2fa-121">Response</span></span>
<a id="response" class="xliff"></a>

<span data-ttu-id="2f2fa-122">Si se ejecuta correctamente, esta llamada devuelve una respuesta `204 No Content` para indicar que el recurso se ha eliminado y no había nada que devolver.</span><span class="sxs-lookup"><span data-stu-id="2f2fa-122">If successful, this call returns a `204 No Content` response to indicate that resource was deleted and there was nothing to return.</span></span>

<!-- { "blockType": "response" } -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete item",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Delete item"
}-->
