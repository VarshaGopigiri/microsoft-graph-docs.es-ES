# <a name="update-rangeformat"></a><span data-ttu-id="2b14f-101">Actualizar rangeformat</span><span class="sxs-lookup"><span data-stu-id="2b14f-101">Update rangeformat</span></span>

<span data-ttu-id="2b14f-102">Actualizar las propiedades del objeto rangeformat.</span><span class="sxs-lookup"><span data-stu-id="2b14f-102">Update the properties of rangeformat object.</span></span>
## <a name="permissions"></a><span data-ttu-id="2b14f-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="2b14f-103">Permissions</span></span>
<span data-ttu-id="2b14f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2b14f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2b14f-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2b14f-106">Permission type</span></span>      | <span data-ttu-id="2b14f-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2b14f-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2b14f-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2b14f-108">Delegated (work or school account)</span></span> | <span data-ttu-id="2b14f-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2b14f-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2b14f-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2b14f-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2b14f-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b14f-111">Not supported.</span></span>    |
|<span data-ttu-id="2b14f-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2b14f-112">Application</span></span> | <span data-ttu-id="2b14f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b14f-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2b14f-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2b14f-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names/{name}/range/format
PATCH /workbook/worksheets/{id|name}/range(address='<address>')/format
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format
```
## <a name="request-headers"></a><span data-ttu-id="2b14f-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2b14f-115">Request headers</span></span>
| <span data-ttu-id="2b14f-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="2b14f-116">Name</span></span>       | <span data-ttu-id="2b14f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b14f-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="2b14f-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="2b14f-118">Authorization</span></span>  | <span data-ttu-id="2b14f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2b14f-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="2b14f-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="2b14f-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="2b14f-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2b14f-124">Request body</span></span>
<span data-ttu-id="2b14f-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="2b14f-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2b14f-128">Property</span></span>     | <span data-ttu-id="2b14f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b14f-129">Type</span></span>   |<span data-ttu-id="2b14f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b14f-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2b14f-131">columnWidth</span><span class="sxs-lookup"><span data-stu-id="2b14f-131">columnWidth</span></span>|<span data-ttu-id="2b14f-132">doble</span><span class="sxs-lookup"><span data-stu-id="2b14f-132">double</span></span>|<span data-ttu-id="2b14f-p105">Obtiene o establece el ancho de todas las columnas del rango. Si los anchos de columna no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p105">Gets or sets the width of all colums within the range. If the column widths are not uniform, null will be returned.</span></span>|
|<span data-ttu-id="2b14f-135">horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="2b14f-135">horizontalAlignment</span></span>|<span data-ttu-id="2b14f-136">cadena</span><span class="sxs-lookup"><span data-stu-id="2b14f-136">string</span></span>|<span data-ttu-id="2b14f-137">Representa la alineación horizontal del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="2b14f-137">Returns or sets the horizontal alignment for the specified object.</span></span> <span data-ttu-id="2b14f-138">Los valores posibles son: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection` y `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="2b14f-138">The possible values are `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`, , , , or .</span></span>|
|<span data-ttu-id="2b14f-139">rowHeight</span><span class="sxs-lookup"><span data-stu-id="2b14f-139">rowHeight</span></span>|<span data-ttu-id="2b14f-140">doble</span><span class="sxs-lookup"><span data-stu-id="2b14f-140">double</span></span>|<span data-ttu-id="2b14f-p107">Obtiene o establece el alto de todas las filas del rango. Si los altos de fila no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p107">Gets or sets the height of all rows in the range. If the row heights are not uniform null will be returned.</span></span>|
|<span data-ttu-id="2b14f-143">verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="2b14f-143">verticalAlignment</span></span>|<span data-ttu-id="2b14f-144">cadena</span><span class="sxs-lookup"><span data-stu-id="2b14f-144">string</span></span>|<span data-ttu-id="2b14f-145">Representa la alineación vertical del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="2b14f-145">Represents the vertical alignment for the specified object. Possible values are: , , , , .</span></span> <span data-ttu-id="2b14f-146">Los valores posibles son: `Top`, `Center`, `Bottom`, `Justify` y `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="2b14f-146">The possible values are `Top`, `Center`, `Bottom`, `Justify`, `Distributed`, , , , , , , or .</span></span>|
|<span data-ttu-id="2b14f-147">wrapText</span><span class="sxs-lookup"><span data-stu-id="2b14f-147">wrapText</span></span>|<span data-ttu-id="2b14f-148">booleano</span><span class="sxs-lookup"><span data-stu-id="2b14f-148">boolean</span></span>|<span data-ttu-id="2b14f-p109">Indica si Excel ajusta el texto del objeto. Un valor null indica que el intervalo no tiene una configuración de ajuste uniforme.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p109">Indicates if Excel wraps the text in the object. A null value indicates that the entire range doesn't have uniform wrap setting</span></span>|

## <a name="response"></a><span data-ttu-id="2b14f-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b14f-151">Response</span></span>

<span data-ttu-id="2b14f-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookRangeFormat](../resources/rangeformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2b14f-152">If successful, this method returns a `200 OK` response code and updated [message](../resources/rangeformat.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2b14f-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b14f-153">Example</span></span>

### <a name="update-the-format-fill-and-font-properties-in-three-table-cells"></a><span data-ttu-id="2b14f-154">Actualizar las propiedades de fuente, el relleno y el formato de tres celdas de la tabla</span><span class="sxs-lookup"><span data-stu-id="2b14f-154">Update the format, fill, and font properties in three table cells</span></span>

<span data-ttu-id="2b14f-155">Los ejemplos siguientes muestran cómo actualizar las propiedades de las propiedades [WorkbookRangeFormat](../resources/rangeformat.md), [WorkbookRangeFill](../resources/rangefill.md)y [WorkbookRangeFont](../resources/rangefont.md) de un intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="2b14f-155">The following examples demonstrate how to update properties of the [RangeFormat](../resources/rangeformat.md), [RangeFill](../resources/rangefill.md), and [RangeFont](../resources/rangefont.md) properties of a specified range.</span></span>

<span data-ttu-id="2b14f-156">El resultado de este conjunto de solicitudes es una tabla con tres celdas con un formato como el de las tres celdas superiores de la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="2b14f-156">The result of this set of requests is a table with three cells formatted like the top three cells in the image below.</span></span>

![Tabla de gráfico de Excel con tres celdas en las que se han actualizado las propiedades de fuente, el relleno y el formato.](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/ExcelRangeFormatting.png)

##### <a name="request"></a><span data-ttu-id="2b14f-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b14f-158">Request</span></span>
<span data-ttu-id="2b14f-159">Esta solicitud actualiza la alineación vertical, el alto de fila y el alto de columna de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="2b14f-159">This request updates the vertical alignment, row height, and column height of the first cell.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_rangeformat"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$A$1')/format
Content-type: application/json

{
  "columnWidth": 135,
  "verticalAlignment": "Top",
  "rowHeight": 49,
  "wrapText": false
}
```
##### <a name="response"></a><span data-ttu-id="2b14f-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b14f-160">Response</span></span>
<span data-ttu-id="2b14f-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "columnWidth": 135,
    "horizontalAlignment": "General",
    "rowHeight": 49,
    "verticalAlignment": "Top",
    "wrapText": false
}
```

##### <a name="request"></a><span data-ttu-id="2b14f-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b14f-164">Request</span></span>
<span data-ttu-id="2b14f-165">Esta solicitud actualiza el estilo de fuente, el tamaño y el color de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="2b14f-165">This request updates the font style, size, and color of the first cell.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_rangeformat_font"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$A$1')/format/font
Content-type: application/json

{
  "bold": true,
  "color": "#4B180E",
  "size": 26
}
```
##### <a name="response"></a><span data-ttu-id="2b14f-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b14f-166">Response</span></span>
<span data-ttu-id="2b14f-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeFont"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "bold": true,
    "color": "#4B180E",
    "italic": false,
    "name": "Calibri",
    "size": 26,
    "underline": "None"
}
```

##### <a name="request"></a><span data-ttu-id="2b14f-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b14f-170">Request</span></span>
<span data-ttu-id="2b14f-171">Esta solicitud actualiza el color de fondo de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="2b14f-171">This request updates the background color of the first cell.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_rangeformat_fill"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$A$1')/format/fill
Content-type: application/json

{
  "color": "#FF0000"
}
```
##### <a name="response"></a><span data-ttu-id="2b14f-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b14f-172">Response</span></span>
<span data-ttu-id="2b14f-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeFill"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "color": "#FF0000"
}
```
##### <a name="request"></a><span data-ttu-id="2b14f-176">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b14f-176">Request</span></span>
<span data-ttu-id="2b14f-177">Esta solicitud actualiza la alineación vertical, la alineación horizontal, el alto de fila y el alto de la columna de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="2b14f-177">This request updates the vertical alignment, horizontal alignment, row height, and column height of the second cell.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_rangeformat_two"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$B$1')/format
Content-type: application/json

{
  "columnWidth": 135,
  "horizontalAlignment": "Center",
  "verticalAlignment": "Center",
  "rowHeight": 49,
  "wrapText": false
}
```
##### <a name="response"></a><span data-ttu-id="2b14f-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b14f-178">Response</span></span>
<span data-ttu-id="2b14f-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "columnWidth": 135,
    "horizontalAlignment": "Center",
    "rowHeight": 49,
    "verticalAlignment": "Center",
    "wrapText": false
}
```

##### <a name="request"></a><span data-ttu-id="2b14f-182">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b14f-182">Request</span></span>
<span data-ttu-id="2b14f-183">Esta solicitud actualiza el estilo de fuente y el tamaño de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="2b14f-183">This request updates the font style and size of the second cell.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_rangeformat_font_two"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$B$1')/format/font
Content-type: application/json

{
  "italic": true,
  "size": 26
}
```
##### <a name="response"></a><span data-ttu-id="2b14f-184">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b14f-184">Response</span></span>
<span data-ttu-id="2b14f-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeFont"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "bold": false,
    "color": "#000000",
    "italic": true,
    "name": "Calibri",
    "size": 26,
    "underline": "None"
}
```

##### <a name="request"></a><span data-ttu-id="2b14f-188">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b14f-188">Request</span></span>
<span data-ttu-id="2b14f-189">Esta solicitud actualiza el color de fondo de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="2b14f-189">This request updates the background color of the second cell.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_rangeformat_fill_two"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$B$1')/format/fill
Content-type: application/json

{
  "color": "#00FF00"
}
```
##### <a name="response"></a><span data-ttu-id="2b14f-190">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b14f-190">Response</span></span>
<span data-ttu-id="2b14f-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeFill"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "color": "#00FF00"
}
```

##### <a name="request"></a><span data-ttu-id="2b14f-194">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b14f-194">Request</span></span>
<span data-ttu-id="2b14f-195">Esta solicitud actualiza la alineación horizontal, la alineación vertical, el alto de fila y el alto de la columna de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="2b14f-195">This request updates the horizontal alignment, vertical alignment, row height, and column height of the third cell.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_rangeformat_three"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$C$1')/format
Content-type: application/json

{
  "columnWidth": 135,
  "horizontalAlignment": "Right",
  "verticalAlignment": "Top",
  "rowHeight": 49,
  "wrapText": false
}
```
##### <a name="response"></a><span data-ttu-id="2b14f-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b14f-196">Response</span></span>
<span data-ttu-id="2b14f-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "columnWidth": 135,
    "horizontalAlignment": "Right",
    "rowHeight": 49,
    "verticalAlignment": "Top",
    "wrapText": false
}
```

##### <a name="request"></a><span data-ttu-id="2b14f-200">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b14f-200">Request</span></span>
<span data-ttu-id="2b14f-201">Esta solicitud actualiza el estilo de fuente, el tamaño y el color de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="2b14f-201">This request updates the font style, size, and color of the third cell.</span></span> <span data-ttu-id="2b14f-202">Tenga en cuenta que la propiedad de subrayado toma como valores **simple** o **doble**.</span><span class="sxs-lookup"><span data-stu-id="2b14f-202">Note that the underline property takes **Single** or **Double** as values.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_rangeformat_font_three"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$C$1')/format/font
Content-type: application/json

{
  "underline": "Single",
  "color": "#FFFFFF",
  "size": 26
}
```
##### <a name="response"></a><span data-ttu-id="2b14f-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b14f-203">Response</span></span>
<span data-ttu-id="2b14f-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeFont"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "bold": false,
    "color": "#FFFFFF",
    "italic": false,
    "name": "Calibri",
    "size": 26,
    "underline": "Single"
}
```

##### <a name="request"></a><span data-ttu-id="2b14f-207">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b14f-207">Request</span></span>
<span data-ttu-id="2b14f-208">Esta solicitud actualiza el color de fondo de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="2b14f-208">This request updates the background color of the third cell.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_rangeformat_fill_three"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='$C$1')/format/fill
Content-type: application/json

{
  "color": "#0000FF"
}
```
##### <a name="response"></a><span data-ttu-id="2b14f-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b14f-209">Response</span></span>
<span data-ttu-id="2b14f-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b14f-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeFill"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "color": "#0000FF"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update rangeformat",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Error: update_rangeformat_font_three/underline:
      Expected type String but actual was Single. Property: underline, actual value: 'Single'"
  ],
  "tocPath": ""
}-->