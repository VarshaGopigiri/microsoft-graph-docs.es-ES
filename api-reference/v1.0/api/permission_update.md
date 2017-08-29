# <a name="update-permission"></a><span data-ttu-id="c1e58-101">Update permission</span><span class="sxs-lookup"><span data-stu-id="c1e58-101">Update permission</span></span>

<span data-ttu-id="c1e58-102">Actualiza las propiedades de un permiso aplicando revisiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="c1e58-102">Update the properties of a permission by patching the resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="c1e58-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c1e58-103">Permissions</span></span>

<span data-ttu-id="c1e58-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c1e58-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c1e58-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c1e58-106">Permission type</span></span>      | <span data-ttu-id="c1e58-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c1e58-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c1e58-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c1e58-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c1e58-109">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c1e58-109">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="c1e58-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c1e58-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c1e58-111">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c1e58-111">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="c1e58-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c1e58-112">Application</span></span> | <span data-ttu-id="c1e58-113">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c1e58-113">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c1e58-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c1e58-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH /me/drive/items/{item-id}/permissions/{perm-id}
PATCH /me/drive/root:/{path}:/permissions/{perm-id}
PATCH /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
PATCH /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
```

## <a name="request-headers"></a><span data-ttu-id="c1e58-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c1e58-115">Request headers</span></span>

| <span data-ttu-id="c1e58-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="c1e58-116">Name</span></span>          | <span data-ttu-id="c1e58-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1e58-117">Type</span></span>   | <span data-ttu-id="c1e58-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1e58-118">Description</span></span>                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e58-119">if-match</span><span class="sxs-lookup"><span data-stu-id="c1e58-119">if-match</span></span>      | <span data-ttu-id="c1e58-120">string</span><span class="sxs-lookup"><span data-stu-id="c1e58-120">string</span></span> | <span data-ttu-id="c1e58-121">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="c1e58-121">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c1e58-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c1e58-122">Request body</span></span>
<span data-ttu-id="c1e58-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c1e58-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c1e58-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c1e58-126">Property</span></span>     | <span data-ttu-id="c1e58-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1e58-127">Type</span></span>   | <span data-ttu-id="c1e58-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1e58-128">Description</span></span>                   |
|:-------------|:-------|:------------------------------|
| <span data-ttu-id="c1e58-129">**roles**</span><span class="sxs-lookup"><span data-stu-id="c1e58-129">**roles**</span></span>    | <span data-ttu-id="c1e58-130">String</span><span class="sxs-lookup"><span data-stu-id="c1e58-130">String</span></span> | <span data-ttu-id="c1e58-131">Matriz de tipos de permisos.</span><span class="sxs-lookup"><span data-stu-id="c1e58-131">An array of permission types.</span></span> |

## <a name="response"></a><span data-ttu-id="c1e58-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c1e58-132">Response</span></span>

<span data-ttu-id="c1e58-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [permission](../resources/permission.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c1e58-133">If successful, this method returns a `200 OK` response code and updated [permission](../resources/permission.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c1e58-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c1e58-134">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c1e58-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c1e58-135">Request</span></span>

<span data-ttu-id="c1e58-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c1e58-136">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="c1e58-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c1e58-137">Response</span></span>

<span data-ttu-id="c1e58-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c1e58-138">Here is an example of the response.</span></span>
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
