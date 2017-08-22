# <a name="update-charttitle"></a><span data-ttu-id="fcd40-101">Actualizar charttitle</span><span class="sxs-lookup"><span data-stu-id="fcd40-101">Update charttitle</span></span>

<span data-ttu-id="fcd40-102">Actualiza las propiedades del objeto charttitle.</span><span class="sxs-lookup"><span data-stu-id="fcd40-102">Update the properties of charttitle object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fcd40-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fcd40-103">Prerequisites</span></span>
<span data-ttu-id="fcd40-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="fcd40-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="fcd40-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fcd40-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="fcd40-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fcd40-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/title
```
## <a name="optional-request-headers"></a><span data-ttu-id="fcd40-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="fcd40-107">Optional request headers</span></span>
| <span data-ttu-id="fcd40-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="fcd40-108">Name</span></span>       | <span data-ttu-id="fcd40-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fcd40-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="fcd40-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="fcd40-110">Authorization</span></span>  | <span data-ttu-id="fcd40-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fcd40-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="fcd40-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fcd40-113">Request body</span></span>
<span data-ttu-id="fcd40-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="fcd40-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="fcd40-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fcd40-117">Property</span></span>     | <span data-ttu-id="fcd40-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="fcd40-118">Type</span></span>   |<span data-ttu-id="fcd40-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="fcd40-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fcd40-120">overlay</span><span class="sxs-lookup"><span data-stu-id="fcd40-120">overlay</span></span>|<span data-ttu-id="fcd40-121">boolean</span><span class="sxs-lookup"><span data-stu-id="fcd40-121">boolean</span></span>|<span data-ttu-id="fcd40-122">Valor booleano que representa si el título del gráfico se superpondrá al gráfico o no.</span><span class="sxs-lookup"><span data-stu-id="fcd40-122">Boolean value representing if the chart title will overlay the chart or not.</span></span>|
|<span data-ttu-id="fcd40-123">text</span><span class="sxs-lookup"><span data-stu-id="fcd40-123">text</span></span>|<span data-ttu-id="fcd40-124">string</span><span class="sxs-lookup"><span data-stu-id="fcd40-124">string</span></span>|<span data-ttu-id="fcd40-125">Representa el texto del título de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="fcd40-125">Represents the title text of a chart.</span></span>|
|<span data-ttu-id="fcd40-126">visible</span><span class="sxs-lookup"><span data-stu-id="fcd40-126">visible</span></span>|<span data-ttu-id="fcd40-127">boolean</span><span class="sxs-lookup"><span data-stu-id="fcd40-127">boolean</span></span>|<span data-ttu-id="fcd40-128">Valor booleano que representa la visibilidad de un objeto de título del gráfico.</span><span class="sxs-lookup"><span data-stu-id="fcd40-128">A boolean value the represents the visibility of a chart title object.</span></span>|

## <a name="response"></a><span data-ttu-id="fcd40-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fcd40-129">Response</span></span>

<span data-ttu-id="fcd40-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartTitle](../resources/charttitle.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fcd40-130">If successful, this method returns a `200 OK` response code and updated [ChartTitle](../resources/charttitle.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="fcd40-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fcd40-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fcd40-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fcd40-132">Request</span></span>
<span data-ttu-id="fcd40-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fcd40-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_charttitle"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/title
Content-type: application/json
Content-length: 64

{
  "overlay": true,
  "text": "text-value",
  "visible": true
}
```
##### <a name="response"></a><span data-ttu-id="fcd40-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fcd40-134">Response</span></span>
<span data-ttu-id="fcd40-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fcd40-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartTitle"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 64

{
  "overlay": true,
  "text": "text-value",
  "visible": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update charttitle",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->