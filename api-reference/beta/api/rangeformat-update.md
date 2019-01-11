---
title: Update rangeformat
description: Actualizar las propiedades del objeto rangeformat.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 8d7df390628e1f8a4416042efe218e36c516a669
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27873244"
---
# <a name="update-rangeformat"></a><span data-ttu-id="c2c38-103">Update rangeformat</span><span class="sxs-lookup"><span data-stu-id="c2c38-103">Update rangeformat</span></span>

> <span data-ttu-id="c2c38-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c2c38-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c2c38-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c2c38-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c2c38-106">Actualizar las propiedades del objeto rangeformat.</span><span class="sxs-lookup"><span data-stu-id="c2c38-106">Update the properties of rangeformat object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c2c38-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c2c38-107">Permissions</span></span>
<span data-ttu-id="c2c38-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c2c38-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c2c38-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c2c38-110">Permission type</span></span>      | <span data-ttu-id="c2c38-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c2c38-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c2c38-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c2c38-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c2c38-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c2c38-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c2c38-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c2c38-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c2c38-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c2c38-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c2c38-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c2c38-116">Application</span></span> | <span data-ttu-id="c2c38-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c2c38-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c2c38-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2c38-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range/format
PATCH /workbook/worksheets/{id|name}/range(address='<address>')/format
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format
```
## <a name="optional-request-headers"></a><span data-ttu-id="c2c38-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="c2c38-119">Optional request headers</span></span>
| <span data-ttu-id="c2c38-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c2c38-120">Name</span></span>       | <span data-ttu-id="c2c38-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2c38-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="c2c38-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c2c38-122">Authorization</span></span>  | <span data-ttu-id="c2c38-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c2c38-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c2c38-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="c2c38-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c2c38-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c2c38-128">Request body</span></span>
<span data-ttu-id="c2c38-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c2c38-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c2c38-132">Property</span></span>     | <span data-ttu-id="c2c38-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2c38-133">Type</span></span>   |<span data-ttu-id="c2c38-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2c38-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c2c38-135">columnWidth</span><span class="sxs-lookup"><span data-stu-id="c2c38-135">columnWidth</span></span>|<span data-ttu-id="c2c38-136">double</span><span class="sxs-lookup"><span data-stu-id="c2c38-136">double</span></span>|<span data-ttu-id="c2c38-p106">Obtiene o establece el ancho de todas las columnas del rango. Si los anchos de columna no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p106">Gets or sets the width of all colums within the range. If the column widths are not uniform, null will be returned.</span></span>|
|<span data-ttu-id="c2c38-139">horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="c2c38-139">horizontalAlignment</span></span>|<span data-ttu-id="c2c38-140">string</span><span class="sxs-lookup"><span data-stu-id="c2c38-140">string</span></span>|<span data-ttu-id="c2c38-p107">Representa la alineación horizontal del objeto especificado. Valores posibles: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p107">Represents the horizontal alignment for the specified object. Possible values are: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span></span>|
|<span data-ttu-id="c2c38-143">rowHeight</span><span class="sxs-lookup"><span data-stu-id="c2c38-143">rowHeight</span></span>|<span data-ttu-id="c2c38-144">double</span><span class="sxs-lookup"><span data-stu-id="c2c38-144">double</span></span>|<span data-ttu-id="c2c38-p108">Obtiene o establece el alto de todas las filas del rango. Si los altos de fila no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p108">Gets or sets the height of all rows in the range. If the row heights are not uniform null will be returned.</span></span>|
|<span data-ttu-id="c2c38-147">verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="c2c38-147">verticalAlignment</span></span>|<span data-ttu-id="c2c38-148">string</span><span class="sxs-lookup"><span data-stu-id="c2c38-148">string</span></span>|<span data-ttu-id="c2c38-p109">Representa la alineación vertical del objeto especificado. Valores posibles: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p109">Represents the vertical alignment for the specified object. Possible values are: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span></span>|
|<span data-ttu-id="c2c38-151">wrapText</span><span class="sxs-lookup"><span data-stu-id="c2c38-151">wrapText</span></span>|<span data-ttu-id="c2c38-152">boolean</span><span class="sxs-lookup"><span data-stu-id="c2c38-152">boolean</span></span>|<span data-ttu-id="c2c38-p110">Indica si Excel ajusta el texto del objeto. Un valor null indica que el intervalo no tiene una configuración de ajuste uniforme.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p110">Indicates if Excel wraps the text in the object. A null value indicates that the entire range doesn't have uniform wrap setting</span></span>|

## <a name="response"></a><span data-ttu-id="c2c38-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2c38-155">Response</span></span>

<span data-ttu-id="c2c38-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [RangeFormat](../resources/rangeformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2c38-156">If successful, this method returns a `200 OK` response code and updated [RangeFormat](../resources/rangeformat.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c2c38-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2c38-157">Example</span></span>

### <a name="update-the-format-fill-and-font-properties-in-three-table-cells"></a><span data-ttu-id="c2c38-158">Actualizar las propiedades de fuente, el relleno y el formato de tres celdas de la tabla</span><span class="sxs-lookup"><span data-stu-id="c2c38-158">Update the format, fill, and font properties in three table cells</span></span>

<span data-ttu-id="c2c38-159">Los ejemplos siguientes muestran cómo actualizar las propiedades de [RangeFormat](../resources/rangeformat.md), [RangeFill](../resources/rangefill.md) y las propiedades de [RangeFont](../resources/rangefont.md) para un rango especificado.</span><span class="sxs-lookup"><span data-stu-id="c2c38-159">The following examples demonstrate how to update properties of the [RangeFormat](../resources/rangeformat.md), [RangeFill](../resources/rangefill.md), and [RangeFont](../resources/rangefont.md) properties of a specified range.</span></span>

<span data-ttu-id="c2c38-160">El resultado de este conjunto de solicitudes es una tabla con tres celdas con un formato como el de las tres celdas superiores de la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="c2c38-160">The result of this set of requests is a table with three cells formatted like the top three cells in the image below.</span></span>

![Tabla de gráfico de Excel con tres celdas en las que se han actualizado las propiedades de fuente, el relleno y el formato.](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/ExcelRangeFormatting.png)

##### <a name="request"></a><span data-ttu-id="c2c38-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2c38-162">Request</span></span>
<span data-ttu-id="c2c38-163">Esta solicitud actualiza la alineación vertical, el alto de fila y el alto de columna de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="c2c38-163">This request updates the vertical alignment, row height, and column height of the first cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c2c38-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2c38-164">Response</span></span>
<span data-ttu-id="c2c38-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c2c38-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2c38-168">Request</span></span>
<span data-ttu-id="c2c38-169">Esta solicitud actualiza el estilo de fuente, el tamaño y el color de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="c2c38-169">This request updates the font style, size, and color of the first cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c2c38-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2c38-170">Response</span></span>
<span data-ttu-id="c2c38-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c2c38-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2c38-174">Request</span></span>
<span data-ttu-id="c2c38-175">Esta solicitud actualiza el color de fondo de la primera celda.</span><span class="sxs-lookup"><span data-stu-id="c2c38-175">This request updates the background color of the first cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c2c38-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2c38-176">Response</span></span>
<span data-ttu-id="c2c38-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
##### <a name="request"></a><span data-ttu-id="c2c38-180">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2c38-180">Request</span></span>
<span data-ttu-id="c2c38-181">Esta solicitud actualiza la alineación vertical, la alineación horizontal, el alto de fila y el alto de la columna de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="c2c38-181">This request updates the vertical alignment, horizontal alignment, row height, and column height of the second cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c2c38-182">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2c38-182">Response</span></span>
<span data-ttu-id="c2c38-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c2c38-186">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2c38-186">Request</span></span>
<span data-ttu-id="c2c38-187">Esta solicitud actualiza el estilo de fuente y el tamaño de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="c2c38-187">This request updates the font style and size of the second cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c2c38-188">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2c38-188">Response</span></span>
<span data-ttu-id="c2c38-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c2c38-192">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2c38-192">Request</span></span>
<span data-ttu-id="c2c38-193">Esta solicitud actualiza el color de fondo de la segunda celda.</span><span class="sxs-lookup"><span data-stu-id="c2c38-193">This request updates the background color of the second cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c2c38-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2c38-194">Response</span></span>
<span data-ttu-id="c2c38-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c2c38-198">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2c38-198">Request</span></span>
<span data-ttu-id="c2c38-199">Esta solicitud actualiza la alineación horizontal, la alineación vertical, el alto de fila y el alto de la columna de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="c2c38-199">This request updates the horizontal alignment, vertical alignment, row height, and column height of the third cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c2c38-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2c38-200">Response</span></span>
<span data-ttu-id="c2c38-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c2c38-204">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2c38-204">Request</span></span>
<span data-ttu-id="c2c38-205">Esta solicitud actualiza el estilo de fuente, el tamaño y el color de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="c2c38-205">This request updates the font style, size, and color of the third cell.</span></span> <span data-ttu-id="c2c38-206">Tenga en cuenta que la propiedad de subrayado toma como valores **simple** o **doble**.</span><span class="sxs-lookup"><span data-stu-id="c2c38-206">Note that the underline property takes **Single** or **Double** as values.</span></span>

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
##### <a name="response"></a><span data-ttu-id="c2c38-207">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2c38-207">Response</span></span>
<span data-ttu-id="c2c38-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request"></a><span data-ttu-id="c2c38-211">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2c38-211">Request</span></span>
<span data-ttu-id="c2c38-212">Esta solicitud actualiza el color de fondo de la tercera celda.</span><span class="sxs-lookup"><span data-stu-id="c2c38-212">This request updates the background color of the third cell.</span></span> 

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
##### <a name="response"></a><span data-ttu-id="c2c38-213">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2c38-213">Response</span></span>
<span data-ttu-id="c2c38-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2c38-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
