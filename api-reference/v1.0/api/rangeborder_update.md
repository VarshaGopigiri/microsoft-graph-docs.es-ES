# <a name="update-rangeborder"></a><span data-ttu-id="dda8d-101">Update rangeborder</span><span class="sxs-lookup"><span data-stu-id="dda8d-101">Update rangeborder</span></span>

<span data-ttu-id="dda8d-102">Actualiza las propiedades del objeto rangeborder.</span><span class="sxs-lookup"><span data-stu-id="dda8d-102">Update the properties of rangeborder object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dda8d-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dda8d-103">Prerequisites</span></span>
<span data-ttu-id="dda8d-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="dda8d-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="dda8d-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dda8d-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="dda8d-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dda8d-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range/format/borders(<sideIndex>)
PATCH /workbook/worksheets/{id|name}/range(<address>)/format/borders(<sideIndex>)
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format/borders(<sideIndex>)
```
## <a name="optional-request-headers"></a><span data-ttu-id="dda8d-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="dda8d-107">Optional request headers</span></span>
| <span data-ttu-id="dda8d-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="dda8d-108">Name</span></span>       | <span data-ttu-id="dda8d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dda8d-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="dda8d-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="dda8d-110">Authorization</span></span>  | <span data-ttu-id="dda8d-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dda8d-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="dda8d-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dda8d-113">Request body</span></span>
<span data-ttu-id="dda8d-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="dda8d-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="dda8d-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dda8d-117">Property</span></span>     | <span data-ttu-id="dda8d-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="dda8d-118">Type</span></span>   |<span data-ttu-id="dda8d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="dda8d-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dda8d-120">color</span><span class="sxs-lookup"><span data-stu-id="dda8d-120">color</span></span>|<span data-ttu-id="dda8d-121">string</span><span class="sxs-lookup"><span data-stu-id="dda8d-121">string</span></span>|<span data-ttu-id="dda8d-122">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="dda8d-122">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|
|<span data-ttu-id="dda8d-123">style</span><span class="sxs-lookup"><span data-stu-id="dda8d-123">style</span></span>|<span data-ttu-id="dda8d-124">string</span><span class="sxs-lookup"><span data-stu-id="dda8d-124">string</span></span>|<span data-ttu-id="dda8d-p103">Una de las constantes de estilo de línea que especifica el estilo de línea del borde. Valores posibles: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.</span><span class="sxs-lookup"><span data-stu-id="dda8d-p103">One of the constants of line style specifying the line style for the border. Possible values are: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.</span></span>|
|<span data-ttu-id="dda8d-127">weight</span><span class="sxs-lookup"><span data-stu-id="dda8d-127">weight</span></span>|<span data-ttu-id="dda8d-128">string</span><span class="sxs-lookup"><span data-stu-id="dda8d-128">string</span></span>|<span data-ttu-id="dda8d-p104">Especifica el grosor del borde alrededor de un rango. Valores posibles: `Hairline`, `Thin`, `Medium`, `Thick`.</span><span class="sxs-lookup"><span data-stu-id="dda8d-p104">Specifies the weight of the border around a range. Possible values are: `Hairline`, `Thin`, `Medium`, `Thick`.</span></span>|

## <a name="response"></a><span data-ttu-id="dda8d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dda8d-131">Response</span></span>

<span data-ttu-id="dda8d-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [RangeBorder](../resources/rangeborder.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dda8d-132">If successful, this method returns a `200 OK` response code and updated [RangeBorder](../resources/rangeborder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="dda8d-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dda8d-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dda8d-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dda8d-134">Request</span></span>
<span data-ttu-id="dda8d-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dda8d-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_rangeborder"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/format/borders(<sideIndex>)
Content-type: application/json
Content-length: 136

{
  "color": "color-value",
  "style": "style-value",
  "sideIndex": "sideIndex-value",
  "weight": "weight-value"
}
```
##### <a name="response"></a><span data-ttu-id="dda8d-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dda8d-136">Response</span></span>
<span data-ttu-id="dda8d-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dda8d-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeBorder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 136

{
  "id": "id-value",
  "color": "color-value",
  "style": "style-value",
  "sideIndex": "sideIndex-value",
  "weight": "weight-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update rangeborder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->