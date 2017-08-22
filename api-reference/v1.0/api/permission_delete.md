# <a name="delete-permission"></a><span data-ttu-id="3be58-101">Delete permission</span><span class="sxs-lookup"><span data-stu-id="3be58-101">Delete permission</span></span>

<span data-ttu-id="3be58-102">Quita el acceso a un [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="3be58-102">Remove access to a [DriveItem](../resources/driveitem.md).</span></span>

<span data-ttu-id="3be58-p101">Solo se pueden eliminar los permisos no heredados. La propiedad **inheritedFrom** debe ser `null`.</span><span class="sxs-lookup"><span data-stu-id="3be58-p101">Only permissions that are not inherited can be deleted. The **inheritedFrom** property must be `null`.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3be58-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3be58-105">Prerequisites</span></span>
<span data-ttu-id="3be58-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="3be58-106">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="3be58-107">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3be58-107">Files.ReadWrite</span></span>
* <span data-ttu-id="3be58-108">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3be58-108">Files.ReadWrite.All</span></span>
* <span data-ttu-id="3be58-109">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3be58-109">Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="3be58-110">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3be58-110">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
DELETE /me/drive/items/{item-id}/permissions/{perm-id}
DELETE /me/drive/root:/{path}:/permissions/{perm-id}
DELETE /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
DELETE /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
```

## <a name="request-headers"></a><span data-ttu-id="3be58-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3be58-111">Request headers</span></span>

| <span data-ttu-id="3be58-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="3be58-112">Name</span></span>          | <span data-ttu-id="3be58-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="3be58-113">Type</span></span>   | <span data-ttu-id="3be58-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3be58-114">Description</span></span>                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3be58-115">if-match</span><span class="sxs-lookup"><span data-stu-id="3be58-115">if-match</span></span>      | <span data-ttu-id="3be58-116">string</span><span class="sxs-lookup"><span data-stu-id="3be58-116">string</span></span> | <span data-ttu-id="3be58-117">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="3be58-117">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3be58-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3be58-118">Request body</span></span>
<span data-ttu-id="3be58-119">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3be58-119">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3be58-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3be58-120">Response</span></span>

<span data-ttu-id="3be58-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3be58-p102">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3be58-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3be58-123">Example</span></span>

##### <a name="request"></a><span data-ttu-id="3be58-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3be58-124">Request</span></span>

<span data-ttu-id="3be58-125">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3be58-125">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_permission"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/drive/root/items/{item-id}/permissions/{perm-id}
```

##### <a name="response"></a><span data-ttu-id="3be58-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3be58-126">Response</span></span>

<span data-ttu-id="3be58-127">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3be58-127">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="remarks"></a><span data-ttu-id="3be58-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3be58-128">Remarks</span></span>

* <span data-ttu-id="3be58-129">Los [Drives](../resources/drive.md) con un **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en la DriveItem raíz.</span><span class="sxs-lookup"><span data-stu-id="3be58-129">[Drives](../resources/drive.md) with a **driveType** of `personal` (OneDrive Personal) cannot create or modify permissions on the root DriveItem.</span></span> 

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete permission",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Delete permission"
}-->
