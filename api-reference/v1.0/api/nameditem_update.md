# <a name="update-nameditem"></a><span data-ttu-id="c98e6-101">Update nameditem</span><span class="sxs-lookup"><span data-stu-id="c98e6-101">Update nameditem</span></span>

<span data-ttu-id="c98e6-102">Actualiza las propiedades del objeto nameditem.</span><span class="sxs-lookup"><span data-stu-id="c98e6-102">Update the properties of nameditem object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c98e6-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c98e6-103">Prerequisites</span></span>
<span data-ttu-id="c98e6-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="c98e6-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="c98e6-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c98e6-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="c98e6-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c98e6-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)
```
## <a name="optional-request-headers"></a><span data-ttu-id="c98e6-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="c98e6-107">Optional request headers</span></span>
| <span data-ttu-id="c98e6-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="c98e6-108">Name</span></span>       | <span data-ttu-id="c98e6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c98e6-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="c98e6-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="c98e6-110">Authorization</span></span>  | <span data-ttu-id="c98e6-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c98e6-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="c98e6-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c98e6-113">Request body</span></span>
<span data-ttu-id="c98e6-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c98e6-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c98e6-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c98e6-117">Property</span></span>     | <span data-ttu-id="c98e6-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="c98e6-118">Type</span></span>   |<span data-ttu-id="c98e6-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c98e6-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c98e6-120">visible</span><span class="sxs-lookup"><span data-stu-id="c98e6-120">visible</span></span>|<span data-ttu-id="c98e6-121">boolean</span><span class="sxs-lookup"><span data-stu-id="c98e6-121">boolean</span></span>|<span data-ttu-id="c98e6-122">Especifica si el objeto está visible o no.</span><span class="sxs-lookup"><span data-stu-id="c98e6-122">Specifies whether the object is visible or not.</span></span>|
|<span data-ttu-id="c98e6-123">comment</span><span class="sxs-lookup"><span data-stu-id="c98e6-123">comment</span></span>|   <span data-ttu-id="c98e6-124">string</span><span class="sxs-lookup"><span data-stu-id="c98e6-124">string</span></span>  |<span data-ttu-id="c98e6-125">Representa el comentario asociado a este nombre.</span><span class="sxs-lookup"><span data-stu-id="c98e6-125">Represents the comment associated with this name.</span></span>|

## <a name="response"></a><span data-ttu-id="c98e6-126">Response</span><span class="sxs-lookup"><span data-stu-id="c98e6-126">Response</span></span>

<span data-ttu-id="c98e6-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [NamedItem](../resources/nameditem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c98e6-127">If successful, this method returns a `200 OK` response code and updated [NamedItem](../resources/nameditem.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c98e6-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c98e6-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c98e6-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c98e6-129">Request</span></span>
<span data-ttu-id="c98e6-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c98e6-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_nameditem"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)
Content-type: application/json
Content-length: 87

{
  "type": "type-value",
  "scope": "scope-value",
  "comment": "comment-value",
  "value": {
  },
  "visible": true
}
```
##### <a name="response"></a><span data-ttu-id="c98e6-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c98e6-131">Response</span></span>
<span data-ttu-id="c98e6-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c98e6-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.namedItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 87

{
  "name": "name-value",
  "type": "type-value",
  "value": {
  },
  "visible": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update nameditem",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
