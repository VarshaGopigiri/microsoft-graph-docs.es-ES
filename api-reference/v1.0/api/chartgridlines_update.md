# <a name="update-chartgridlines"></a><span data-ttu-id="72ab3-101">Actualizar chartgridlines</span><span class="sxs-lookup"><span data-stu-id="72ab3-101">Update chartgridlines</span></span>

<span data-ttu-id="72ab3-102">Actualiza las propiedades del objeto chartgridlines.</span><span class="sxs-lookup"><span data-stu-id="72ab3-102">Update the properties of chartgridlines object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="72ab3-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="72ab3-103">Prerequisites</span></span>
<span data-ttu-id="72ab3-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="72ab3-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="72ab3-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="72ab3-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="72ab3-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="72ab3-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/minorgridlines
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/majorgridlines
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/majorgridlines
```
## <a name="optional-request-headers"></a><span data-ttu-id="72ab3-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="72ab3-107">Optional request headers</span></span>
| <span data-ttu-id="72ab3-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="72ab3-108">Name</span></span>       | <span data-ttu-id="72ab3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="72ab3-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="72ab3-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="72ab3-110">Authorization</span></span>  | <span data-ttu-id="72ab3-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="72ab3-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="72ab3-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="72ab3-113">Request body</span></span>
<span data-ttu-id="72ab3-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="72ab3-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="72ab3-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72ab3-117">Property</span></span>     | <span data-ttu-id="72ab3-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="72ab3-118">Type</span></span>   |<span data-ttu-id="72ab3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="72ab3-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="72ab3-120">visible</span><span class="sxs-lookup"><span data-stu-id="72ab3-120">visible</span></span>|<span data-ttu-id="72ab3-121">boolean</span><span class="sxs-lookup"><span data-stu-id="72ab3-121">boolean</span></span>|<span data-ttu-id="72ab3-122">Valor booleano que representa si las líneas de cuadrícula del eje están visibles o no.</span><span class="sxs-lookup"><span data-stu-id="72ab3-122">Boolean value representing if the axis gridlines are visible or not.</span></span>|

## <a name="response"></a><span data-ttu-id="72ab3-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72ab3-123">Response</span></span>

<span data-ttu-id="72ab3-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartGridlines](../resources/chartgridlines.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72ab3-124">If successful, this method returns a `200 OK` response code and updated [ChartGridlines](../resources/chartgridlines.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="72ab3-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="72ab3-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="72ab3-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="72ab3-126">Request</span></span>
<span data-ttu-id="72ab3-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="72ab3-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartgridlines"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/minorgridlines
Content-type: application/json
Content-length: 21

{
  "visible": true
}
```
##### <a name="response"></a><span data-ttu-id="72ab3-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72ab3-128">Response</span></span>
<span data-ttu-id="72ab3-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="72ab3-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartGridLines"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 21

{
  "visible": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartgridlines",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->