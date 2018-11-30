---
title: Update rangeformat
description: Actualizar las propiedades del objeto rangeformat.
ms.openlocfilehash: 208e20e650e069c87ff177564b6a0400ba5e94ec
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028956"
---
# <a name="update-rangeformat"></a><span data-ttu-id="c6ef5-103">Update rangeformat</span><span class="sxs-lookup"><span data-stu-id="c6ef5-103">Update rangeformat</span></span>

<span data-ttu-id="c6ef5-104">Actualizar las propiedades del objeto rangeformat.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-104">Update the properties of rangeformat object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c6ef5-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c6ef5-105">Permissions</span></span>
<span data-ttu-id="c6ef5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c6ef5-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c6ef5-108">Permission type</span></span>      | <span data-ttu-id="c6ef5-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c6ef5-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c6ef5-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c6ef5-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c6ef5-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c6ef5-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c6ef5-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c6ef5-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c6ef5-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-113">Not supported.</span></span>    |
|<span data-ttu-id="c6ef5-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c6ef5-114">Application</span></span> | <span data-ttu-id="c6ef5-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c6ef5-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c6ef5-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names/{name}/range/format
PATCH /workbook/worksheets/{id|name}/range(address='<address>')/format
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format
```
## <a name="request-headers"></a><span data-ttu-id="c6ef5-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ef5-117">Request headers</span></span>
| <span data-ttu-id="c6ef5-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="c6ef5-118">Name</span></span>       | <span data-ttu-id="c6ef5-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6ef5-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="c6ef5-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="c6ef5-120">Authorization</span></span>  | <span data-ttu-id="c6ef5-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c6ef5-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c6ef5-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="c6ef5-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c6ef5-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ef5-126">Request body</span></span>
<span data-ttu-id="c6ef5-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c6ef5-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c6ef5-130">Property</span></span>     | <span data-ttu-id="c6ef5-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6ef5-131">Type</span></span>   |<span data-ttu-id="c6ef5-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6ef5-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c6ef5-133">columnWidth</span><span class="sxs-lookup"><span data-stu-id="c6ef5-133">columnWidth</span></span>|<span data-ttu-id="c6ef5-134">double</span><span class="sxs-lookup"><span data-stu-id="c6ef5-134">double</span></span>|<span data-ttu-id="c6ef5-p105">Obtiene o establece el ancho de todas las columnas del rango. Si los anchos de columna no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p105">Gets or sets the width of all colums within the range. If the column widths are not uniform, null will be returned.</span></span>|
|<span data-ttu-id="c6ef5-137">horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="c6ef5-137">horizontalAlignment</span></span>|<span data-ttu-id="c6ef5-138">string</span><span class="sxs-lookup"><span data-stu-id="c6ef5-138">string</span></span>|<span data-ttu-id="c6ef5-139">Representa la alineación horizontal del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-139">Represents the horizontal alignment for the specified object.</span></span> <span data-ttu-id="c6ef5-140">Los valores posibles son: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-140">The possible values are: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span></span>|
|<span data-ttu-id="c6ef5-141">rowHeight</span><span class="sxs-lookup"><span data-stu-id="c6ef5-141">rowHeight</span></span>|<span data-ttu-id="c6ef5-142">double</span><span class="sxs-lookup"><span data-stu-id="c6ef5-142">double</span></span>|<span data-ttu-id="c6ef5-p107">Obtiene o establece el alto de todas las filas del rango. Si los altos de fila no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p107">Gets or sets the height of all rows in the range. If the row heights are not uniform null will be returned.</span></span>|
|<span data-ttu-id="c6ef5-145">verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="c6ef5-145">verticalAlignment</span></span>|<span data-ttu-id="c6ef5-146">string</span><span class="sxs-lookup"><span data-stu-id="c6ef5-146">string</span></span>|<span data-ttu-id="c6ef5-147">Representa la alineación vertical del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-147">Represents the vertical alignment for the specified object.</span></span> <span data-ttu-id="c6ef5-148">Los valores posibles son: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-148">The possible values are: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span></span>|
|<span data-ttu-id="c6ef5-149">wrapText</span><span class="sxs-lookup"><span data-stu-id="c6ef5-149">wrapText</span></span>|<span data-ttu-id="c6ef5-150">boolean</span><span class="sxs-lookup"><span data-stu-id="c6ef5-150">boolean</span></span>|<span data-ttu-id="c6ef5-p109">Indica si Excel ajusta el texto del objeto. Un valor null indica que el intervalo no tiene una configuración de ajuste uniforme.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p109">Indicates if Excel wraps the text in the object. A null value indicates that the entire range doesn't have uniform wrap setting</span></span>|

## <a name="response"></a><span data-ttu-id="c6ef5-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6ef5-153">Response</span></span>

<span data-ttu-id="c6ef5-154">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookRangeFormat](../resources/rangeformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-154">If successful, this method returns a `200 OK` response code and updated [WorkbookRangeFormat](../resources/rangeformat.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c6ef5-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6ef5-155">Example</span></span>

### <a name="update-the-format-fill-and-font-properties-in-three-table-cells"></a><span data-ttu-id="c6ef5-156">Actualizar las propiedades de fuente, el relleno y el formato de tres celdas de la tabla</span><span class="sxs-lookup"><span data-stu-id="c6ef5-156">Update the format, fill, and font properties in three table cells</span></span>

<span data-ttu-id="c6ef5-157">Los ejemplos siguientes muestran cómo actualizar las propiedades de las propiedades [WorkbookRangeFormat](../resources/rangeformat.md), [WorkbookRangeFill](../resources/rangefill.md)y [WorkbookRangeFont](../resources/rangefont.md) de un intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-157">The following examples demonstrate how to update properties of the [WorkbookRangeFormat](../resources/rangeformat.md), [WorkbookRangeFill](../resources/rangefill.md), and [WorkbookRangeFont](../resources/rangefont.md) properties of a specified range.</span></span>

<span data-ttu-id="c6ef5-158">El resultado de este conjunto de solicitudes es una tabla con tres celdas con un formato como el de las tres celdas superiores de la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-158">The result of this set of requests is a table with three cells formatted like the top three cells in the image below.</span></span>

![Tabla de gráfico de Excel con tres celdas en las que se han actualizado las propiedades de fuente, el relleno y el formato.](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/ExcelRangeFormatting.png)

##### <a name="request"></a><span data-ttu-id="c6ef5-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ef5-160">Request</span></span>
<span data-ttu-id="c6ef5-161">Esta solicitud actualiza la alineación vertical, el alto de fila y el alto de columna de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-161">This request updates the vertical alignment, row height, and column height of the first cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c6ef5-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6ef5-162">Response</span></span>
<span data-ttu-id="c6ef5-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c6ef5-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ef5-166">Request</span></span>
<span data-ttu-id="c6ef5-167">Esta solicitud actualiza el estilo de fuente, el tamaño y el color de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-167">This request updates the font style, size, and color of the first cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c6ef5-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6ef5-168">Response</span></span>
<span data-ttu-id="c6ef5-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c6ef5-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ef5-172">Request</span></span>
<span data-ttu-id="c6ef5-173">Esta solicitud actualiza el color de fondo de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-173">This request updates the background color of the first cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c6ef5-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6ef5-174">Response</span></span>
<span data-ttu-id="c6ef5-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
##### <a name="request"></a><span data-ttu-id="c6ef5-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ef5-178">Request</span></span>
<span data-ttu-id="c6ef5-179">Esta solicitud actualiza la alineación vertical, la alineación horizontal, el alto de fila y el alto de la columna de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-179">This request updates the vertical alignment, horizontal alignment, row height, and column height of the second cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c6ef5-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6ef5-180">Response</span></span>
<span data-ttu-id="c6ef5-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c6ef5-184">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ef5-184">Request</span></span>
<span data-ttu-id="c6ef5-185">Esta solicitud actualiza el estilo de fuente y el tamaño de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-185">This request updates the font style and size of the second cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c6ef5-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6ef5-186">Response</span></span>
<span data-ttu-id="c6ef5-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c6ef5-190">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ef5-190">Request</span></span>
<span data-ttu-id="c6ef5-191">Esta solicitud actualiza el color de fondo de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-191">This request updates the background color of the second cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c6ef5-192">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6ef5-192">Response</span></span>
<span data-ttu-id="c6ef5-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c6ef5-196">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ef5-196">Request</span></span>
<span data-ttu-id="c6ef5-197">Esta solicitud actualiza la alineación horizontal, la alineación vertical, el alto de fila y el alto de la columna de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-197">This request updates the horizontal alignment, vertical alignment, row height, and column height of the third cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c6ef5-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6ef5-198">Response</span></span>
<span data-ttu-id="c6ef5-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c6ef5-202">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ef5-202">Request</span></span>
<span data-ttu-id="c6ef5-203">Esta solicitud actualiza el estilo de fuente, el tamaño y el color de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-203">This request updates the font style, size, and color of the third cell.</span></span> <span data-ttu-id="c6ef5-204">Tenga en cuenta que la propiedad de subrayado toma como valores **simple** o **doble**.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-204">Note that the underline property takes **Single** or **Double** as values.</span></span>

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
##### <a name="response"></a><span data-ttu-id="c6ef5-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6ef5-205">Response</span></span>
<span data-ttu-id="c6ef5-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c6ef5-209">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6ef5-209">Request</span></span>
<span data-ttu-id="c6ef5-210">Esta solicitud actualiza el color de fondo de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-210">This request updates the background color of the third cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c6ef5-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6ef5-211">Response</span></span>
<span data-ttu-id="c6ef5-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6ef5-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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