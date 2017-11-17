# <a name="update-chartdatalabels"></a><span data-ttu-id="fd88b-101">Actualizar chartdatalabels</span><span class="sxs-lookup"><span data-stu-id="fd88b-101">Update chartdatalabels</span></span>

<span data-ttu-id="fd88b-102">Actualizar las propiedades del objeto chartdatalabels.</span><span class="sxs-lookup"><span data-stu-id="fd88b-102">Update the properties of chartdatalabels object.</span></span>
## <a name="permissions"></a><span data-ttu-id="fd88b-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="fd88b-103">Permissions</span></span>
<span data-ttu-id="fd88b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fd88b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="fd88b-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fd88b-106">Permission type</span></span>      | <span data-ttu-id="fd88b-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fd88b-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fd88b-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fd88b-108">Delegated (work or school account)</span></span> | <span data-ttu-id="fd88b-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fd88b-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="fd88b-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fd88b-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fd88b-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fd88b-111">Not supported.</span></span>    |
|<span data-ttu-id="fd88b-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fd88b-112">Application</span></span> | <span data-ttu-id="fd88b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fd88b-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fd88b-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fd88b-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/datalabels
```
## <a name="optional-request-headers"></a><span data-ttu-id="fd88b-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="fd88b-115">Optional request headers</span></span>
| <span data-ttu-id="fd88b-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="fd88b-116">Name</span></span>       | <span data-ttu-id="fd88b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd88b-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="fd88b-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="fd88b-118">Authorization</span></span>  | <span data-ttu-id="fd88b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fd88b-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fd88b-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fd88b-121">Request body</span></span>
<span data-ttu-id="fd88b-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="fd88b-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="fd88b-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fd88b-125">Property</span></span>     | <span data-ttu-id="fd88b-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd88b-126">Type</span></span>   |<span data-ttu-id="fd88b-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd88b-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fd88b-128">position</span><span class="sxs-lookup"><span data-stu-id="fd88b-128">position</span></span>|<span data-ttu-id="fd88b-129">string</span><span class="sxs-lookup"><span data-stu-id="fd88b-129">string</span></span>|<span data-ttu-id="fd88b-p104">Valor DataLabelPosition que representa la posición de la etiqueta de datos. Valores posibles: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span><span class="sxs-lookup"><span data-stu-id="fd88b-p104">DataLabelPosition value that represents the position of the data label. Possible values are: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span></span>|
|<span data-ttu-id="fd88b-132">separator</span><span class="sxs-lookup"><span data-stu-id="fd88b-132">separator</span></span>|<span data-ttu-id="fd88b-133">string</span><span class="sxs-lookup"><span data-stu-id="fd88b-133">string</span></span>|<span data-ttu-id="fd88b-134">Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="fd88b-134">String representing the separator used for the data labels on a chart.</span></span>|
|<span data-ttu-id="fd88b-135">showBubbleSize</span><span class="sxs-lookup"><span data-stu-id="fd88b-135">showBubbleSize</span></span>|<span data-ttu-id="fd88b-136">boolean</span><span class="sxs-lookup"><span data-stu-id="fd88b-136">boolean</span></span>|<span data-ttu-id="fd88b-137">Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="fd88b-137">Boolean value representing if the data label bubble size is visible or not.</span></span>|
|<span data-ttu-id="fd88b-138">showCategoryName</span><span class="sxs-lookup"><span data-stu-id="fd88b-138">showCategoryName</span></span>|<span data-ttu-id="fd88b-139">boolean</span><span class="sxs-lookup"><span data-stu-id="fd88b-139">boolean</span></span>|<span data-ttu-id="fd88b-140">Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="fd88b-140">Boolean value representing if the data label category name is visible or not.</span></span>|
|<span data-ttu-id="fd88b-141">showLegendKey</span><span class="sxs-lookup"><span data-stu-id="fd88b-141">showLegendKey</span></span>|<span data-ttu-id="fd88b-142">boolean</span><span class="sxs-lookup"><span data-stu-id="fd88b-142">boolean</span></span>|<span data-ttu-id="fd88b-143">Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="fd88b-143">Boolean value representing if the data label legend key is visible or not.</span></span>|
|<span data-ttu-id="fd88b-144">showPercentage</span><span class="sxs-lookup"><span data-stu-id="fd88b-144">showPercentage</span></span>|<span data-ttu-id="fd88b-145">boolean</span><span class="sxs-lookup"><span data-stu-id="fd88b-145">boolean</span></span>|<span data-ttu-id="fd88b-146">Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="fd88b-146">Boolean value representing if the data label percentage is visible or not.</span></span>|
|<span data-ttu-id="fd88b-147">showSeriesName</span><span class="sxs-lookup"><span data-stu-id="fd88b-147">showSeriesName</span></span>|<span data-ttu-id="fd88b-148">boolean</span><span class="sxs-lookup"><span data-stu-id="fd88b-148">boolean</span></span>|<span data-ttu-id="fd88b-149">Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="fd88b-149">Boolean value representing if the data label series name is visible or not.</span></span>|
|<span data-ttu-id="fd88b-150">showValue</span><span class="sxs-lookup"><span data-stu-id="fd88b-150">showValue</span></span>|<span data-ttu-id="fd88b-151">boolean</span><span class="sxs-lookup"><span data-stu-id="fd88b-151">boolean</span></span>|<span data-ttu-id="fd88b-152">Valor booleano que representa si el valor de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="fd88b-152">Boolean value representing if the data label value is visible or not.</span></span>|

## <a name="response"></a><span data-ttu-id="fd88b-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd88b-153">Response</span></span>

<span data-ttu-id="fd88b-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartDataLabels](../resources/chartdatalabels.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fd88b-154">If successful, this method returns a `200 OK` response code and updated [ChartDataLabels](../resources/chartdatalabels.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="fd88b-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fd88b-155">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fd88b-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fd88b-156">Request</span></span>
<span data-ttu-id="fd88b-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fd88b-157">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="fd88b-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd88b-158">Response</span></span>
<span data-ttu-id="fd88b-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fd88b-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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