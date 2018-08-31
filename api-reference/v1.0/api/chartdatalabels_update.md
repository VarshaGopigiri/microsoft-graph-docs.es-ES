# <a name="update-chartdatalabels"></a><span data-ttu-id="d0be4-101">Actualizar chartdatalabels</span><span class="sxs-lookup"><span data-stu-id="d0be4-101">Update chartdatalabels</span></span>

<span data-ttu-id="d0be4-102">Actualizar las propiedades del objeto chartdatalabels.</span><span class="sxs-lookup"><span data-stu-id="d0be4-102">Update the properties of chartdatalabels object.</span></span>
## <a name="permissions"></a><span data-ttu-id="d0be4-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d0be4-103">Permissions</span></span>
<span data-ttu-id="d0be4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d0be4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d0be4-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d0be4-106">Permission type</span></span>      | <span data-ttu-id="d0be4-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d0be4-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d0be4-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0be4-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d0be4-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0be4-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d0be4-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0be4-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d0be4-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0be4-111">Not supported.</span></span>    |
|<span data-ttu-id="d0be4-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0be4-112">Application</span></span> | <span data-ttu-id="d0be4-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0be4-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d0be4-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0be4-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}/dataLabels
```
## <a name="optional-request-headers"></a><span data-ttu-id="d0be4-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="d0be4-115">Optional request headers</span></span>
| <span data-ttu-id="d0be4-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="d0be4-116">Name</span></span>       | <span data-ttu-id="d0be4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0be4-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="d0be4-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="d0be4-118">Authorization</span></span>  | <span data-ttu-id="d0be4-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d0be4-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d0be4-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d0be4-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="d0be4-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d0be4-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d0be4-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d0be4-124">Request body</span></span>
<span data-ttu-id="d0be4-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="d0be4-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="d0be4-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0be4-128">Property</span></span>     | <span data-ttu-id="d0be4-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0be4-129">Type</span></span>   |<span data-ttu-id="d0be4-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0be4-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d0be4-131">position</span><span class="sxs-lookup"><span data-stu-id="d0be4-131">position</span></span>|<span data-ttu-id="d0be4-132">cadena</span><span class="sxs-lookup"><span data-stu-id="d0be4-132">string</span></span>|<span data-ttu-id="d0be4-133">Valor de DataLabelPosition que representa la posición de la etiqueta de datos.</span><span class="sxs-lookup"><span data-stu-id="d0be4-133">DataLabelPosition value that represents the position of the data label. Possible values are: , , , , , , , , , , .</span></span> <span data-ttu-id="d0be4-134">Los valores posibles son: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit` y `Callout`.</span><span class="sxs-lookup"><span data-stu-id="d0be4-134">The possible values are `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`, or .</span></span>|
|<span data-ttu-id="d0be4-135">separator</span><span class="sxs-lookup"><span data-stu-id="d0be4-135">separator</span></span>|<span data-ttu-id="d0be4-136">cadena</span><span class="sxs-lookup"><span data-stu-id="d0be4-136">string</span></span>|<span data-ttu-id="d0be4-137">Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="d0be4-137">String representing the separator used for the data labels on a chart.</span></span>|
|<span data-ttu-id="d0be4-138">showBubbleSize</span><span class="sxs-lookup"><span data-stu-id="d0be4-138">showBubbleSize</span></span>|<span data-ttu-id="d0be4-139">booleano</span><span class="sxs-lookup"><span data-stu-id="d0be4-139">boolean</span></span>|<span data-ttu-id="d0be4-140">Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="d0be4-140">Boolean value representing if the data label bubble size is visible or not.</span></span>|
|<span data-ttu-id="d0be4-141">showCategoryName</span><span class="sxs-lookup"><span data-stu-id="d0be4-141">showCategoryName</span></span>|<span data-ttu-id="d0be4-142">booleano</span><span class="sxs-lookup"><span data-stu-id="d0be4-142">boolean</span></span>|<span data-ttu-id="d0be4-143">Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="d0be4-143">Boolean value representing if the data label category name is visible or not.</span></span>|
|<span data-ttu-id="d0be4-144">showLegendKey</span><span class="sxs-lookup"><span data-stu-id="d0be4-144">showLegendKey</span></span>|<span data-ttu-id="d0be4-145">booleano</span><span class="sxs-lookup"><span data-stu-id="d0be4-145">boolean</span></span>|<span data-ttu-id="d0be4-146">Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="d0be4-146">Boolean value representing if the data label legend key is visible or not.</span></span>|
|<span data-ttu-id="d0be4-147">showPercentage</span><span class="sxs-lookup"><span data-stu-id="d0be4-147">showPercentage</span></span>|<span data-ttu-id="d0be4-148">booleano</span><span class="sxs-lookup"><span data-stu-id="d0be4-148">boolean</span></span>|<span data-ttu-id="d0be4-149">Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="d0be4-149">Boolean value representing if the data label percentage is visible or not.</span></span>|
|<span data-ttu-id="d0be4-150">showSeriesName</span><span class="sxs-lookup"><span data-stu-id="d0be4-150">showSeriesName</span></span>|<span data-ttu-id="d0be4-151">booleano</span><span class="sxs-lookup"><span data-stu-id="d0be4-151">boolean</span></span>|<span data-ttu-id="d0be4-152">Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="d0be4-152">Boolean value representing if the data label series name is visible or not.</span></span>|
|<span data-ttu-id="d0be4-153">showValue</span><span class="sxs-lookup"><span data-stu-id="d0be4-153">showValue</span></span>|<span data-ttu-id="d0be4-154">booleano</span><span class="sxs-lookup"><span data-stu-id="d0be4-154">boolean</span></span>|<span data-ttu-id="d0be4-155">Valor booleano que representa si el valor de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="d0be4-155">Boolean value representing if the data label value is visible or not.</span></span>|

## <a name="response"></a><span data-ttu-id="d0be4-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0be4-156">Response</span></span>

<span data-ttu-id="d0be4-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookChartDataLabels](../resources/chartdatalabels.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0be4-157">If successful, this method returns a `200 OK` response code and updated [message](../resources/chartdatalabels.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d0be4-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0be4-158">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d0be4-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0be4-159">Request</span></span>
<span data-ttu-id="d0be4-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0be4-160">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartdatalabels"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/dataLabels
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
##### <a name="response"></a><span data-ttu-id="d0be4-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0be4-161">Response</span></span>
<span data-ttu-id="d0be4-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d0be4-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartDataLabels"
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