# <a name="update-rangeformat"></a><span data-ttu-id="6ba78-101">Update rangeformat</span><span class="sxs-lookup"><span data-stu-id="6ba78-101">Update rangeformat</span></span>

<span data-ttu-id="6ba78-102">Actualizar las propiedades del objeto rangeformat.</span><span class="sxs-lookup"><span data-stu-id="6ba78-102">Update the properties of rangeformat object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6ba78-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6ba78-103">Permissions</span></span>
<span data-ttu-id="6ba78-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6ba78-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6ba78-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ba78-106">Permission type</span></span>      | <span data-ttu-id="6ba78-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ba78-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6ba78-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ba78-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6ba78-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6ba78-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6ba78-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ba78-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6ba78-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ba78-111">Not supported.</span></span>    |
|<span data-ttu-id="6ba78-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ba78-112">Application</span></span> | <span data-ttu-id="6ba78-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ba78-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6ba78-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ba78-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range/format
PATCH /workbook/worksheets/{id|name}/range(address='<address>')/format
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format
```
## <a name="optional-request-headers"></a><span data-ttu-id="6ba78-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="6ba78-115">Optional request headers</span></span>
| <span data-ttu-id="6ba78-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="6ba78-116">Name</span></span>       | <span data-ttu-id="6ba78-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ba78-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="6ba78-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="6ba78-118">Authorization</span></span>  | <span data-ttu-id="6ba78-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6ba78-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba78-121">Request body</span></span>
<span data-ttu-id="6ba78-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="6ba78-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6ba78-125">Property</span></span>     | <span data-ttu-id="6ba78-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ba78-126">Type</span></span>   |<span data-ttu-id="6ba78-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ba78-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6ba78-128">columnWidth</span><span class="sxs-lookup"><span data-stu-id="6ba78-128">columnWidth</span></span>|<span data-ttu-id="6ba78-129">double</span><span class="sxs-lookup"><span data-stu-id="6ba78-129">double</span></span>|<span data-ttu-id="6ba78-p104">Obtiene o establece el ancho de todas las columnas del rango. Si los anchos de columna no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p104">Gets or sets the width of all colums within the range. If the column widths are not uniform, null will be returned.</span></span>|
|<span data-ttu-id="6ba78-132">horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="6ba78-132">horizontalAlignment</span></span>|<span data-ttu-id="6ba78-133">string</span><span class="sxs-lookup"><span data-stu-id="6ba78-133">string</span></span>|<span data-ttu-id="6ba78-p105">Representa la alineación horizontal del objeto especificado. Valores posibles: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p105">Represents the horizontal alignment for the specified object. Possible values are: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span></span>|
|<span data-ttu-id="6ba78-136">rowHeight</span><span class="sxs-lookup"><span data-stu-id="6ba78-136">rowHeight</span></span>|<span data-ttu-id="6ba78-137">double</span><span class="sxs-lookup"><span data-stu-id="6ba78-137">double</span></span>|<span data-ttu-id="6ba78-p106">Obtiene o establece el alto de todas las filas del rango. Si los altos de fila no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p106">Gets or sets the height of all rows in the range. If the row heights are not uniform null will be returned.</span></span>|
|<span data-ttu-id="6ba78-140">verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="6ba78-140">verticalAlignment</span></span>|<span data-ttu-id="6ba78-141">string</span><span class="sxs-lookup"><span data-stu-id="6ba78-141">string</span></span>|<span data-ttu-id="6ba78-p107">Representa la alineación vertical del objeto especificado. Valores posibles: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p107">Represents the vertical alignment for the specified object. Possible values are: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span></span>|
|<span data-ttu-id="6ba78-144">wrapText</span><span class="sxs-lookup"><span data-stu-id="6ba78-144">wrapText</span></span>|<span data-ttu-id="6ba78-145">boolean</span><span class="sxs-lookup"><span data-stu-id="6ba78-145">boolean</span></span>|<span data-ttu-id="6ba78-p108">Indica si Excel ajusta el texto del objeto. Un valor null indica que el intervalo no tiene una configuración de ajuste uniforme.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p108">Indicates if Excel wraps the text in the object. A null value indicates that the entire range doesn't have uniform wrap setting</span></span>|

## <a name="response"></a><span data-ttu-id="6ba78-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ba78-148">Response</span></span>

<span data-ttu-id="6ba78-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [RangeFormat](../resources/rangeformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ba78-149">If successful, this method returns a `200 OK` response code and updated [RangeFormat](../resources/rangeformat.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6ba78-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ba78-150">Example</span></span>

### <a name="update-the-format-fill-and-font-properties-in-three-table-cells"></a><span data-ttu-id="6ba78-151">Actualizar las propiedades de fuente, el relleno y el formato de tres celdas de la tabla</span><span class="sxs-lookup"><span data-stu-id="6ba78-151">Update the format, fill, and font properties in three table cells</span></span>

<span data-ttu-id="6ba78-152">Los ejemplos siguientes muestran cómo actualizar las propiedades de [RangeFormat](../resources/rangeformat.md), [RangeFill](../resources/rangefill.md) y las propiedades de [RangeFont](../resources/rangefont.md) para un rango especificado.</span><span class="sxs-lookup"><span data-stu-id="6ba78-152">The following examples demonstrate how to update properties of the [RangeFormat](../resources/rangeformat.md), [RangeFill](../resources/rangefill.md), and [RangeFont](../resources/rangefont.md) properties of a specified range.</span></span>

<span data-ttu-id="6ba78-153">El resultado de este conjunto de solicitudes es una tabla con tres celdas con un formato como el de las tres celdas superiores de la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="6ba78-153">The result of this set of requests is a table with three cells formatted like the top three cells in the image below.</span></span>

![Tabla de gráfico de Excel con tres celdas en las que se han actualizado las propiedades de fuente, el relleno y el formato.](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/ExcelRangeFormatting.png)

##### <a name="request"></a><span data-ttu-id="6ba78-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba78-155">Request</span></span>
<span data-ttu-id="6ba78-156">Esta solicitud actualiza la alineación vertical, el alto de fila y el alto de columna de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="6ba78-156">This request updates the vertical alignment, row height, and column height of the first cell.</span></span> 

<!-- {
  "blockType": "request",
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
##### <a name="response"></a><span data-ttu-id="6ba78-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ba78-157">Response</span></span>
<span data-ttu-id="6ba78-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFormat"
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

##### <a name="request"></a><span data-ttu-id="6ba78-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba78-161">Request</span></span>
<span data-ttu-id="6ba78-162">Esta solicitud actualiza el estilo de fuente, el tamaño y el color de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="6ba78-162">This request updates the font style, size, and color of the first cell.</span></span> 

<!-- {
  "blockType": "request",
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
##### <a name="response"></a><span data-ttu-id="6ba78-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ba78-163">Response</span></span>
<span data-ttu-id="6ba78-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFont"
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

##### <a name="request"></a><span data-ttu-id="6ba78-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba78-167">Request</span></span>
<span data-ttu-id="6ba78-168">Esta solicitud actualiza el color de fondo de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="6ba78-168">This request updates the background color of the first cell.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_rangeformat_fill"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$A$1')/format/fill
Content-type: application/json

{
  "color": "#FF0000"
}
```
##### <a name="response"></a><span data-ttu-id="6ba78-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ba78-169">Response</span></span>
<span data-ttu-id="6ba78-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFill"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "color": "#FF0000"
}
```
##### <a name="request"></a><span data-ttu-id="6ba78-173">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba78-173">Request</span></span>
<span data-ttu-id="6ba78-174">Esta solicitud actualiza la alineación vertical, la alineación horizontal, el alto de fila y el alto de la columna de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="6ba78-174">This request updates the vertical alignment, horizontal alignment, row height, and column height of the second cell.</span></span> 

<!-- {
  "blockType": "request",
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
##### <a name="response"></a><span data-ttu-id="6ba78-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ba78-175">Response</span></span>
<span data-ttu-id="6ba78-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFormat"
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

##### <a name="request"></a><span data-ttu-id="6ba78-179">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba78-179">Request</span></span>
<span data-ttu-id="6ba78-180">Esta solicitud actualiza el estilo de fuente y el tamaño de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="6ba78-180">This request updates the font style and size of the second cell.</span></span> 

<!-- {
  "blockType": "request",
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
##### <a name="response"></a><span data-ttu-id="6ba78-181">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ba78-181">Response</span></span>
<span data-ttu-id="6ba78-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFont"
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

##### <a name="request"></a><span data-ttu-id="6ba78-185">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba78-185">Request</span></span>
<span data-ttu-id="6ba78-186">Esta solicitud actualiza el color de fondo de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="6ba78-186">This request updates the background color of the second cell.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_rangeformat_fill_two"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$B$1')/format/fill
Content-type: application/json

{
  "color": "#00FF00"
}
```
##### <a name="response"></a><span data-ttu-id="6ba78-187">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ba78-187">Response</span></span>
<span data-ttu-id="6ba78-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFill"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "color": "#00FF00"
}
```

##### <a name="request"></a><span data-ttu-id="6ba78-191">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba78-191">Request</span></span>
<span data-ttu-id="6ba78-192">Esta solicitud actualiza la alineación horizontal, la alineación vertical, el alto de fila y el alto de la columna de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="6ba78-192">This request updates the horizontal alignment, vertical alignment, row height, and column height of the third cell.</span></span> 

<!-- {
  "blockType": "request",
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
##### <a name="response"></a><span data-ttu-id="6ba78-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ba78-193">Response</span></span>
<span data-ttu-id="6ba78-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFormat"
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

##### <a name="request"></a><span data-ttu-id="6ba78-197">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba78-197">Request</span></span>
<span data-ttu-id="6ba78-198">Esta solicitud actualiza el estilo de fuente, el tamaño y el color de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="6ba78-198">This request updates the font style, size, and color of the third cell.</span></span> <span data-ttu-id="6ba78-199">Tenga en cuenta que la propiedad de subrayado toma como valores **simple** o **doble**.</span><span class="sxs-lookup"><span data-stu-id="6ba78-199">Note that the underline property takes **Single** or **Double** as values.</span></span>

<!-- {
  "blockType": "request",
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
##### <a name="response"></a><span data-ttu-id="6ba78-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ba78-200">Response</span></span>
<span data-ttu-id="6ba78-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFont"
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

##### <a name="request"></a><span data-ttu-id="6ba78-204">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba78-204">Request</span></span>
<span data-ttu-id="6ba78-205">Esta solicitud actualiza el color de fondo de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="6ba78-205">This request updates the background color of the third cell.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_rangeformat_fill_three"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$C$1')/format/fill
Content-type: application/json

{
  "color": "#0000FF"
}
```
##### <a name="response"></a><span data-ttu-id="6ba78-206">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ba78-206">Response</span></span>
<span data-ttu-id="6ba78-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ba78-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFill"
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
  "tocPath": ""
}-->