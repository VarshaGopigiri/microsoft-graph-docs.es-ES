# <a name="update-chartdatalabels"></a><span data-ttu-id="32086-101">Actualizar chartdatalabels</span><span class="sxs-lookup"><span data-stu-id="32086-101">Update chartdatalabels</span></span>

<span data-ttu-id="32086-102">Actualiza las propiedades del objeto chartdatalabels.</span><span class="sxs-lookup"><span data-stu-id="32086-102">Update the properties of chartdatalabels object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="32086-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="32086-103">Prerequisites</span></span>
<span data-ttu-id="32086-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="32086-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="32086-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="32086-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="32086-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="32086-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/datalabels
```
## <a name="optional-request-headers"></a><span data-ttu-id="32086-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="32086-107">Optional request headers</span></span>
| <span data-ttu-id="32086-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="32086-108">Name</span></span>       | <span data-ttu-id="32086-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="32086-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="32086-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="32086-110">Authorization</span></span>  | <span data-ttu-id="32086-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="32086-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="32086-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="32086-113">Request body</span></span>
<span data-ttu-id="32086-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="32086-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="32086-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32086-117">Property</span></span>     | <span data-ttu-id="32086-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="32086-118">Type</span></span>   |<span data-ttu-id="32086-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="32086-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="32086-120">position</span><span class="sxs-lookup"><span data-stu-id="32086-120">position</span></span>|<span data-ttu-id="32086-121">string</span><span class="sxs-lookup"><span data-stu-id="32086-121">string</span></span>|<span data-ttu-id="32086-p103">Valor DataLabelPosition que representa la posición de la etiqueta de datos. Valores posibles: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span><span class="sxs-lookup"><span data-stu-id="32086-p103">DataLabelPosition value that represents the position of the data label. Possible values are: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span></span>|
|<span data-ttu-id="32086-124">separator</span><span class="sxs-lookup"><span data-stu-id="32086-124">separator</span></span>|<span data-ttu-id="32086-125">string</span><span class="sxs-lookup"><span data-stu-id="32086-125">string</span></span>|<span data-ttu-id="32086-126">Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="32086-126">String representing the separator used for the data labels on a chart.</span></span>|
|<span data-ttu-id="32086-127">showBubbleSize</span><span class="sxs-lookup"><span data-stu-id="32086-127">showBubbleSize</span></span>|<span data-ttu-id="32086-128">boolean</span><span class="sxs-lookup"><span data-stu-id="32086-128">boolean</span></span>|<span data-ttu-id="32086-129">Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="32086-129">Boolean value representing if the data label bubble size is visible or not.</span></span>|
|<span data-ttu-id="32086-130">showCategoryName</span><span class="sxs-lookup"><span data-stu-id="32086-130">showCategoryName</span></span>|<span data-ttu-id="32086-131">boolean</span><span class="sxs-lookup"><span data-stu-id="32086-131">boolean</span></span>|<span data-ttu-id="32086-132">Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="32086-132">Boolean value representing if the data label category name is visible or not.</span></span>|
|<span data-ttu-id="32086-133">showLegendKey</span><span class="sxs-lookup"><span data-stu-id="32086-133">showLegendKey</span></span>|<span data-ttu-id="32086-134">boolean</span><span class="sxs-lookup"><span data-stu-id="32086-134">boolean</span></span>|<span data-ttu-id="32086-135">Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="32086-135">Boolean value representing if the data label legend key is visible or not.</span></span>|
|<span data-ttu-id="32086-136">showPercentage</span><span class="sxs-lookup"><span data-stu-id="32086-136">showPercentage</span></span>|<span data-ttu-id="32086-137">boolean</span><span class="sxs-lookup"><span data-stu-id="32086-137">boolean</span></span>|<span data-ttu-id="32086-138">Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="32086-138">Boolean value representing if the data label percentage is visible or not.</span></span>|
|<span data-ttu-id="32086-139">showSeriesName</span><span class="sxs-lookup"><span data-stu-id="32086-139">showSeriesName</span></span>|<span data-ttu-id="32086-140">boolean</span><span class="sxs-lookup"><span data-stu-id="32086-140">boolean</span></span>|<span data-ttu-id="32086-141">Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="32086-141">Boolean value representing if the data label series name is visible or not.</span></span>|
|<span data-ttu-id="32086-142">showValue</span><span class="sxs-lookup"><span data-stu-id="32086-142">showValue</span></span>|<span data-ttu-id="32086-143">boolean</span><span class="sxs-lookup"><span data-stu-id="32086-143">boolean</span></span>|<span data-ttu-id="32086-144">Valor booleano que representa si el valor de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="32086-144">Boolean value representing if the data label value is visible or not.</span></span>|

## <a name="response"></a><span data-ttu-id="32086-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32086-145">Response</span></span>

<span data-ttu-id="32086-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartDataLabels](../resources/chartdatalabels.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32086-146">If successful, this method returns a `200 OK` response code and updated [ChartDataLabels](../resources/chartdatalabels.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="32086-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="32086-147">Example</span></span>
##### <a name="request"></a><span data-ttu-id="32086-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="32086-148">Request</span></span>
<span data-ttu-id="32086-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="32086-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartdatalabels"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/datalabels
Content-type: application/json
Content-length: 134

{
  "position": "position-value",
  "showValue": true,
  "showSeriesName": true,
  "showCategoryName": true,
  "showLegendKey": true
}
```
##### <a name="response"></a><span data-ttu-id="32086-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32086-150">Response</span></span>
<span data-ttu-id="32086-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="32086-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartDataLabels"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 134

{
  "position": "position-value",
  "showValue": true,
  "showSeriesName": true,
  "showCategoryName": true,
  "showLegendKey": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartdatalabels",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->