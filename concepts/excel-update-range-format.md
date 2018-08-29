# <a name="update-a-range-format-in-excel-with-microsoft-graph"></a><span data-ttu-id="48e66-101">Actualizar el formato de un rango en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="48e66-101">Update a range format in Excel with Microsoft Graph</span></span>

<span data-ttu-id="48e66-102">En los ejemplos siguientes, se muestra cómo actualizar las propiedades de [RangeFormat](../api-reference/v1.0/resources/rangeformat.md), [RangeFill](../api-reference/v1.0/resources/rangefill.md) y [RangeFont](../api-reference/v1.0/resources/rangefont.md) de un rango especificado.</span><span class="sxs-lookup"><span data-stu-id="48e66-102">The following examples demonstrate how to update properties of the [RangeFormat](../api-reference/v1.0/resources/rangeformat.md), [RangeFill](../api-reference/v1.0/resources/rangefill.md), and [RangeFont](../api-reference/v1.0/resources/rangefont.md) properties of a specified range.</span></span>

<span data-ttu-id="48e66-103">El resultado de este conjunto de solicitudes es una tabla con tres celdas con un formato como el de las tres celdas superiores de la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="48e66-103">The result of this set of requests is a table with three cells formatted like the top three cells in the image below.</span></span>

![Tabla de gráfico de Excel con tres celdas en las que se han actualizado las propiedades de fuente, el relleno y el formato.](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/ExcelRangeFormatting.png)

##### <a name="request"></a><span data-ttu-id="48e66-105">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48e66-105">Request</span></span>
<span data-ttu-id="48e66-106">Esta solicitud actualiza la alineación vertical, el alto de fila y el alto de columna de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="48e66-106">This request updates the vertical alignment, row height, and column height of the first cell.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["Sheet1"],
  "name": "update_rangeformat"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$A$1')/format
Content-type: application/json

{
  "columnWidth": 135,
  "verticalAlignment": "Top",
  "rowHeight": 49,
  "wrapText": false
}
```
##### <a name="response"></a><span data-ttu-id="48e66-107">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48e66-107">Response</span></span>
<span data-ttu-id="48e66-p101">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48e66-p101">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="48e66-111">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48e66-111">Request</span></span>
<span data-ttu-id="48e66-112">Esta solicitud actualiza el estilo de fuente, el tamaño y el color de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="48e66-112">This request updates the font style, size, and color of the first cell.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["Sheet1"],
  "name": "update_rangeformat_font"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$A$1')/format/font
Content-type: application/json

{
  "bold": true,
  "color": "#4B180E",
  "size": 26
}
```
##### <a name="response"></a><span data-ttu-id="48e66-113">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48e66-113">Response</span></span>
<span data-ttu-id="48e66-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48e66-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="48e66-117">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48e66-117">Request</span></span>
<span data-ttu-id="48e66-118">Esta solicitud actualiza el color de fondo de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="48e66-118">This request updates the background color of the first cell.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["Sheet1"],
  "name": "update_rangeformat_fill"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$A$1')/format/fill
Content-type: application/json

{
  "color": "#FF0000"
}
```
##### <a name="response"></a><span data-ttu-id="48e66-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48e66-119">Response</span></span>
<span data-ttu-id="48e66-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48e66-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
##### <a name="request"></a><span data-ttu-id="48e66-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48e66-123">Request</span></span>
<span data-ttu-id="48e66-124">Esta solicitud actualiza la alineación vertical, la alineación horizontal, el alto de fila y el alto de la columna de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="48e66-124">This request updates the vertical alignment, horizontal alignment, row height, and column height of the second cell.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["Sheet1"],
  "name": "update_rangeformat_two"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$B$1')/format
Content-type: application/json

{
  "columnWidth": 135,
  "horizontalAlignment": "Center",
  "verticalAlignment": "Center",
  "rowHeight": 49,
  "wrapText": false
}
```
##### <a name="response"></a><span data-ttu-id="48e66-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48e66-125">Response</span></span>
<span data-ttu-id="48e66-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48e66-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="48e66-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48e66-129">Request</span></span>
<span data-ttu-id="48e66-130">Esta solicitud actualiza el estilo de fuente y el tamaño de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="48e66-130">This request updates the font style and size of the second cell.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["Sheet1"],
  "name": "update_rangeformat_font_two"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$B$1')/format/font
Content-type: application/json

{
  "italic": true,
  "size": 26
}
```
##### <a name="response"></a><span data-ttu-id="48e66-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48e66-131">Response</span></span>
<span data-ttu-id="48e66-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48e66-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="48e66-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48e66-135">Request</span></span>
<span data-ttu-id="48e66-136">Esta solicitud actualiza el color de fondo de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="48e66-136">This request updates the background color of the second cell.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["Sheet1"],
  "name": "update_rangeformat_fill_two"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$B$1')/format/fill
Content-type: application/json

{
  "color": "#00FF00"
}
```
##### <a name="response"></a><span data-ttu-id="48e66-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48e66-137">Response</span></span>
<span data-ttu-id="48e66-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48e66-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="48e66-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48e66-141">Request</span></span>
<span data-ttu-id="48e66-142">Esta solicitud actualiza la alineación horizontal, la alineación vertical, el alto de fila y el alto de la columna de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="48e66-142">This request updates the horizontal alignment, vertical alignment, row height, and column height of the third cell.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["Sheet1"],
  "name": "update_rangeformat_three"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$C$1')/format
Content-type: application/json

{
  "columnWidth": 135,
  "horizontalAlignment": "Right",
  "verticalAlignment": "Top",
  "rowHeight": 49,
  "wrapText": false
}
```
##### <a name="response"></a><span data-ttu-id="48e66-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48e66-143">Response</span></span>
<span data-ttu-id="48e66-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48e66-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="48e66-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48e66-147">Request</span></span>
<span data-ttu-id="48e66-148">Esta solicitud actualiza el estilo de fuente, el tamaño y el color de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="48e66-148">This request updates the font style, size, and color of the third cell.</span></span> <span data-ttu-id="48e66-149">Tenga en cuenta que la propiedad de subrayado toma como valores **simple** o **doble**.</span><span class="sxs-lookup"><span data-stu-id="48e66-149">Note that the underline property takes **Single** or **Double** as values.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["Sheet1"],
  "name": "update_rangeformat_font_three"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$C$1')/format/font
Content-type: application/json

{
  "underline": "Single",
  "color": "#FFFFFF",
  "size": 26
}
```
##### <a name="response"></a><span data-ttu-id="48e66-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48e66-150">Response</span></span>
<span data-ttu-id="48e66-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48e66-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="48e66-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48e66-154">Request</span></span>
<span data-ttu-id="48e66-155">Esta solicitud actualiza el color de fondo de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="48e66-155">This request updates the background color of the third cell.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["Sheet1"],
  "name": "update_rangeformat_fill_three"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$C$1')/format/fill
Content-type: application/json

{
  "color": "#0000FF"
}
```
##### <a name="response"></a><span data-ttu-id="48e66-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48e66-156">Response</span></span>
<span data-ttu-id="48e66-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48e66-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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


## <a name="see-also"></a><span data-ttu-id="48e66-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="48e66-160">See also</span></span>
* [<span data-ttu-id="48e66-161">Administrar sesiones en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="48e66-161">Manage sessions in Excel with Microsoft Graph</span></span>](excel-manage-sessions.md)
* [<span data-ttu-id="48e66-162">Escribir en un libro de Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="48e66-162">Write to an Excel workbook using Microsoft Graph</span></span>](excel-write-to-workbook.md)
* [<span data-ttu-id="48e66-163">Usar funciones de libro en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="48e66-163">Use workbook functions in Excel with Microsoft Graph</span></span>](excel-use-functions.md)
* [<span data-ttu-id="48e66-164">Mostrar una imagen de gráfico de Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="48e66-164">Display a chart image in Excel with Microsoft Graph</span></span>](excel-display-chart-image.md)
* [<span data-ttu-id="48e66-165">Usar la API de REST de Excel</span><span class="sxs-lookup"><span data-stu-id="48e66-165">Use the Excel REST API</span></span>](../api-reference/v1.0/resources/excel.md)
