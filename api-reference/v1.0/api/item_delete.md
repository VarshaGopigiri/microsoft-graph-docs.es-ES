# <a name="delete-a-driveitem"></a><span data-ttu-id="463fb-101">Delete a DriveItem</span><span class="sxs-lookup"><span data-stu-id="463fb-101">Delete a DriveItem</span></span>

<span data-ttu-id="463fb-p101">Elimina un [DriveItem](../resources/driveitem.md) mediante su identificador o la ruta de acceso. Tenga en cuenta que si elimina elementos con este método moverá los elementos a la Papelera de reciclaje en lugar de eliminarlos permanentemente.</span><span class="sxs-lookup"><span data-stu-id="463fb-p101">Delete a [DriveItem](../resources/driveitem.md) by using its ID or path. Note that deleting items using this method will move the items to the recycle bin instead of permanently deleting the item.</span></span>

## <a name="permissions"></a><span data-ttu-id="463fb-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="463fb-104">Permissions</span></span>
<span data-ttu-id="463fb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="463fb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="463fb-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="463fb-107">Permission type</span></span>      | <span data-ttu-id="463fb-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="463fb-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="463fb-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="463fb-109">Delegated (work or school account)</span></span> | <span data-ttu-id="463fb-110">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="463fb-110">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="463fb-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="463fb-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="463fb-112">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="463fb-112">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="463fb-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="463fb-113">Application</span></span> | <span data-ttu-id="463fb-114">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="463fb-114">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="463fb-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="463fb-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```
DELETE /me/drive/items/{item-id}
DELETE /me/drive/root:/{item-path}
DELETE /drives/{drive-id}/items/{item-id}
DELETE /groups/{group-id}/drive/items/{item-id}
```

## <a name="request-headers"></a><span data-ttu-id="463fb-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="463fb-116">Request headers</span></span>

| <span data-ttu-id="463fb-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="463fb-117">Name</span></span>          | <span data-ttu-id="463fb-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="463fb-118">Type</span></span>   | <span data-ttu-id="463fb-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="463fb-119">Description</span></span>                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="463fb-120">if-match</span><span class="sxs-lookup"><span data-stu-id="463fb-120">if-match</span></span>      | <span data-ttu-id="463fb-121">String</span><span class="sxs-lookup"><span data-stu-id="463fb-121">String</span></span> | <span data-ttu-id="463fb-122">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="463fb-122">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span> |

## <a name="request-body"></a><span data-ttu-id="463fb-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="463fb-123">Request body</span></span>
<span data-ttu-id="463fb-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="463fb-124">Do not supply a request body for this method.</span></span>

## <a name="example"></a><span data-ttu-id="463fb-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="463fb-125">Example</span></span>

<span data-ttu-id="463fb-126">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="463fb-126">Here is an example of how to call this API.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete-item"
}-->
```
DELETE https://graph.microsoft.com/v1.0/me/drive/items/{item-id}
```

## <a name="response"></a><span data-ttu-id="463fb-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="463fb-127">Response</span></span>

<span data-ttu-id="463fb-128">Si se ejecuta correctamente, esta llamada devuelve una respuesta `204 No Content` para indicar que el recurso se ha eliminado y no había nada que devolver.</span><span class="sxs-lookup"><span data-stu-id="463fb-128">If successful, this call returns a `204 No Content` response to indicate that resource was deleted and there was nothing to return.</span></span>

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
