# <a name="update-icon"></a><span data-ttu-id="720c9-101">Update icon</span><span class="sxs-lookup"><span data-stu-id="720c9-101">Update icon</span></span>

<span data-ttu-id="720c9-102">Actualiza las propiedades del objeto icon.</span><span class="sxs-lookup"><span data-stu-id="720c9-102">Update the properties of icon object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="720c9-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="720c9-103">Prerequisites</span></span>
<span data-ttu-id="720c9-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="720c9-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="720c9-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="720c9-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="720c9-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="720c9-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}/sort/fields/icon
PATCH /workbook/worksheets/{id|name}/tables/{id|name}/sort/fields/icon
```
## <a name="optional-request-headers"></a><span data-ttu-id="720c9-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="720c9-107">Optional request headers</span></span>
| <span data-ttu-id="720c9-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="720c9-108">Name</span></span>       | <span data-ttu-id="720c9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="720c9-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="720c9-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="720c9-110">Authorization</span></span>  | <span data-ttu-id="720c9-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="720c9-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="720c9-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="720c9-113">Request body</span></span>
<span data-ttu-id="720c9-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="720c9-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="720c9-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="720c9-117">Property</span></span>     | <span data-ttu-id="720c9-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="720c9-118">Type</span></span>   |<span data-ttu-id="720c9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="720c9-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="720c9-120">index</span><span class="sxs-lookup"><span data-stu-id="720c9-120">index</span></span>|<span data-ttu-id="720c9-121">int</span><span class="sxs-lookup"><span data-stu-id="720c9-121">int</span></span>|<span data-ttu-id="720c9-122">Representa el índice del icono en el conjunto concreto.</span><span class="sxs-lookup"><span data-stu-id="720c9-122">Represents the index of the icon in the given set.</span></span>|
|<span data-ttu-id="720c9-123">set</span><span class="sxs-lookup"><span data-stu-id="720c9-123">set</span></span>|<span data-ttu-id="720c9-124">string</span><span class="sxs-lookup"><span data-stu-id="720c9-124">string</span></span>|<span data-ttu-id="720c9-p103">Representa el conjunto al que pertenece el icono. Valores posibles: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles`, `FiveBoxes`.</span><span class="sxs-lookup"><span data-stu-id="720c9-p103">Represents the set that the icon is part of. Possible values are: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles`, `FiveBoxes`.</span></span>|

## <a name="response"></a><span data-ttu-id="720c9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="720c9-127">Response</span></span>

<span data-ttu-id="720c9-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Icon](../resources/icon.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="720c9-128">If successful, this method returns a `200 OK` response code and updated [Icon](../resources/icon.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="720c9-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="720c9-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="720c9-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="720c9-130">Request</span></span>
<span data-ttu-id="720c9-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="720c9-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_icon"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/fields/icon
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```
##### <a name="response"></a><span data-ttu-id="720c9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="720c9-132">Response</span></span>
<span data-ttu-id="720c9-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="720c9-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.icon"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update icon",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->