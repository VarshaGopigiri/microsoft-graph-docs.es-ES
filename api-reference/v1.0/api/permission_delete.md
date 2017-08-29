# <a name="delete-permission"></a><span data-ttu-id="830a1-101">Delete permission</span><span class="sxs-lookup"><span data-stu-id="830a1-101">Delete permission</span></span>

<span data-ttu-id="830a1-102">Quita el acceso a un [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="830a1-102">Remove access to a [DriveItem](../resources/driveitem.md).</span></span>

<span data-ttu-id="830a1-p101">Solo se pueden eliminar los permisos no heredados. La propiedad **inheritedFrom** debe ser `null`.</span><span class="sxs-lookup"><span data-stu-id="830a1-p101">Only permissions that are not inherited can be deleted. The **inheritedFrom** property must be `null`.</span></span>

## <a name="permissions"></a><span data-ttu-id="830a1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="830a1-105">Permissions</span></span>
<span data-ttu-id="830a1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="830a1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="830a1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="830a1-108">Permission type</span></span>      | <span data-ttu-id="830a1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="830a1-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="830a1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="830a1-110">Delegated (work or school account)</span></span> | <span data-ttu-id="830a1-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="830a1-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="830a1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="830a1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="830a1-113">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="830a1-113">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="830a1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="830a1-114">Application</span></span> | <span data-ttu-id="830a1-115">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="830a1-115">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="830a1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="830a1-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
DELETE /me/drive/items/{item-id}/permissions/{perm-id}
DELETE /me/drive/root:/{path}:/permissions/{perm-id}
DELETE /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
DELETE /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
```

## <a name="request-headers"></a><span data-ttu-id="830a1-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="830a1-117">Request headers</span></span>

| <span data-ttu-id="830a1-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="830a1-118">Name</span></span>          | <span data-ttu-id="830a1-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="830a1-119">Type</span></span>   | <span data-ttu-id="830a1-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="830a1-120">Description</span></span>                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="830a1-121">if-match</span><span class="sxs-lookup"><span data-stu-id="830a1-121">if-match</span></span>      | <span data-ttu-id="830a1-122">string</span><span class="sxs-lookup"><span data-stu-id="830a1-122">string</span></span> | <span data-ttu-id="830a1-123">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="830a1-123">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span> |

## <a name="request-body"></a><span data-ttu-id="830a1-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="830a1-124">Request body</span></span>
<span data-ttu-id="830a1-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="830a1-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="830a1-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="830a1-126">Response</span></span>

<span data-ttu-id="830a1-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="830a1-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="830a1-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="830a1-129">Example</span></span>

##### <a name="request"></a><span data-ttu-id="830a1-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="830a1-130">Request</span></span>

<span data-ttu-id="830a1-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="830a1-131">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_permission"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/drive/root/items/{item-id}/permissions/{perm-id}
```

##### <a name="response"></a><span data-ttu-id="830a1-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="830a1-132">Response</span></span>

<span data-ttu-id="830a1-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="830a1-133">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="remarks"></a><span data-ttu-id="830a1-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="830a1-134">Remarks</span></span>

* <span data-ttu-id="830a1-135">Los [Drives](../resources/drive.md) con un **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en la DriveItem raíz.</span><span class="sxs-lookup"><span data-stu-id="830a1-135">[Drives](../resources/drive.md) with a **driveType** of `personal` (OneDrive Personal) cannot create or modify permissions on the root DriveItem.</span></span> 

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete permission",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Delete permission"
}-->
