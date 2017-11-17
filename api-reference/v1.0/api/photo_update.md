# <a name="update-photo"></a><span data-ttu-id="d0bd4-101">Update photo</span><span class="sxs-lookup"><span data-stu-id="d0bd4-101">Update photo</span></span>

<span data-ttu-id="d0bd4-102">Actualiza las propiedades del objeto photo.</span><span class="sxs-lookup"><span data-stu-id="d0bd4-102">Update the properties of photo object.</span></span>
## <a name="permissions"></a><span data-ttu-id="d0bd4-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d0bd4-103">Permissions</span></span>
<span data-ttu-id="d0bd4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d0bd4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d0bd4-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d0bd4-106">Permission type</span></span>      | <span data-ttu-id="d0bd4-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d0bd4-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d0bd4-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0bd4-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d0bd4-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0bd4-109">Not supported.</span></span>    |
|<span data-ttu-id="d0bd4-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0bd4-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d0bd4-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0bd4-111">Not supported.</span></span>    |
|<span data-ttu-id="d0bd4-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0bd4-112">Application</span></span> | <span data-ttu-id="d0bd4-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0bd4-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d0bd4-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0bd4-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/{id | userPrincipalName}/photo
PATCH /groups/{id}/photo
PATCH /drive/root/createdByUser/photo
```

## <a name="request-headers"></a><span data-ttu-id="d0bd4-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d0bd4-115">Request headers</span></span>
| <span data-ttu-id="d0bd4-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="d0bd4-116">Name</span></span>       | <span data-ttu-id="d0bd4-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0bd4-117">Type</span></span> | <span data-ttu-id="d0bd4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0bd4-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="d0bd4-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d0bd4-119">Authorization</span></span>  | <span data-ttu-id="d0bd4-120">string</span><span class="sxs-lookup"><span data-stu-id="d0bd4-120">string</span></span>  | <span data-ttu-id="d0bd4-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d0bd4-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d0bd4-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d0bd4-123">Request body</span></span>
<span data-ttu-id="d0bd4-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="d0bd4-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="d0bd4-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0bd4-127">Property</span></span>     | <span data-ttu-id="d0bd4-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0bd4-128">Type</span></span>   |<span data-ttu-id="d0bd4-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0bd4-129">Description</span></span>|
|:---------------|:--------|:----------|

## <a name="response"></a><span data-ttu-id="d0bd4-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0bd4-130">Response</span></span>

<span data-ttu-id="d0bd4-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [photo](../resources/photo.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0bd4-131">If successful, this method returns a `200 OK` response code and updated [photo](../resources/photo.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d0bd4-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0bd4-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d0bd4-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0bd4-133">Request</span></span>
<span data-ttu-id="d0bd4-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0bd4-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_photo"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/photo
Content-type: application/json
Content-length: 53

{
  "height": 99,
  "width": 99,
  "id": "id-value"
}
```
##### <a name="response"></a><span data-ttu-id="d0bd4-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0bd4-135">Response</span></span>
<span data-ttu-id="d0bd4-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0bd4-136">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.profilePhoto"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 53

{
  "height": 99,
  "width": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
