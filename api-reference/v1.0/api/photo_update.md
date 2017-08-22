# <a name="update-photo"></a><span data-ttu-id="e9341-101">Update photo</span><span class="sxs-lookup"><span data-stu-id="e9341-101">Update photo</span></span>

<span data-ttu-id="e9341-102">Actualiza las propiedades del objeto photo.</span><span class="sxs-lookup"><span data-stu-id="e9341-102">Update the properties of photo object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e9341-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e9341-103">Prerequisites</span></span>
<span data-ttu-id="e9341-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="e9341-104">One of the following **scopes** is required to execute this API:</span></span>
## <a name="http-request"></a><span data-ttu-id="e9341-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9341-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/{id | userPrincipalName}/photo
PATCH /groups/{id}/photo
PATCH /drive/root/createdByUser/photo
```

## <a name="request-headers"></a><span data-ttu-id="e9341-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9341-106">Request headers</span></span>
| <span data-ttu-id="e9341-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9341-107">Name</span></span>       | <span data-ttu-id="e9341-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9341-108">Type</span></span> | <span data-ttu-id="e9341-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9341-109">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e9341-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="e9341-110">Authorization</span></span>  | <span data-ttu-id="e9341-111">string</span><span class="sxs-lookup"><span data-stu-id="e9341-111">string</span></span>  | <span data-ttu-id="e9341-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9341-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="e9341-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9341-114">Request body</span></span>
<span data-ttu-id="e9341-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="e9341-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="e9341-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9341-118">Property</span></span>     | <span data-ttu-id="e9341-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9341-119">Type</span></span>   |<span data-ttu-id="e9341-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9341-120">Description</span></span>|
|:---------------|:--------|:----------|

## <a name="response"></a><span data-ttu-id="e9341-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9341-121">Response</span></span>

<span data-ttu-id="e9341-122">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [photo](../resources/photo.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9341-122">If successful, this method returns a `200 OK` response code and updated [photo](../resources/photo.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e9341-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9341-123">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e9341-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9341-124">Request</span></span>
<span data-ttu-id="e9341-125">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9341-125">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="e9341-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9341-126">Response</span></span>
<span data-ttu-id="e9341-127">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9341-127">Here is an example of the response.</span></span>
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
