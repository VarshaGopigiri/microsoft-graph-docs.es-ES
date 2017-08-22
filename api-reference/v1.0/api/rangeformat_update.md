# <a name="update-rangeformat"></a><span data-ttu-id="9e016-101">Update rangeformat</span><span class="sxs-lookup"><span data-stu-id="9e016-101">Update rangeformat</span></span>

<span data-ttu-id="9e016-102">Actualiza las propiedades del objeto rangeformat.</span><span class="sxs-lookup"><span data-stu-id="9e016-102">Update the properties of rangeformat object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9e016-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9e016-103">Prerequisites</span></span>
<span data-ttu-id="9e016-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="9e016-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="9e016-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9e016-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="9e016-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9e016-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range/format
PATCH /workbook/worksheets/{id|name}/range(<address>)/format
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format
```
## <a name="optional-request-headers"></a><span data-ttu-id="9e016-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="9e016-107">Optional request headers</span></span>
| <span data-ttu-id="9e016-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="9e016-108">Name</span></span>       | <span data-ttu-id="9e016-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e016-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="9e016-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="9e016-110">Authorization</span></span>  | <span data-ttu-id="9e016-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9e016-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="9e016-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9e016-113">Request body</span></span>
<span data-ttu-id="9e016-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="9e016-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="9e016-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9e016-117">Property</span></span>     | <span data-ttu-id="9e016-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="9e016-118">Type</span></span>   |<span data-ttu-id="9e016-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e016-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9e016-120">columnWidth</span><span class="sxs-lookup"><span data-stu-id="9e016-120">columnWidth</span></span>|<span data-ttu-id="9e016-121">double</span><span class="sxs-lookup"><span data-stu-id="9e016-121">double</span></span>|<span data-ttu-id="9e016-p103">Obtiene o establece el ancho de todas las columnas del rango. Si los anchos de columna no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="9e016-p103">Gets or sets the width of all colums within the range. If the column widths are not uniform, null will be returned.</span></span>|
|<span data-ttu-id="9e016-124">horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="9e016-124">horizontalAlignment</span></span>|<span data-ttu-id="9e016-125">string</span><span class="sxs-lookup"><span data-stu-id="9e016-125">string</span></span>|<span data-ttu-id="9e016-p104">Representa la alineación horizontal del objeto especificado. Valores posibles: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="9e016-p104">Represents the horizontal alignment for the specified object. Possible values are: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span></span>|
|<span data-ttu-id="9e016-128">rowHeight</span><span class="sxs-lookup"><span data-stu-id="9e016-128">rowHeight</span></span>|<span data-ttu-id="9e016-129">double</span><span class="sxs-lookup"><span data-stu-id="9e016-129">double</span></span>|<span data-ttu-id="9e016-p105">Obtiene o establece el alto de todas las filas del rango. Si los altos de fila no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="9e016-p105">Gets or sets the height of all rows in the range. If the row heights are not uniform null will be returned.</span></span>|
|<span data-ttu-id="9e016-132">verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="9e016-132">verticalAlignment</span></span>|<span data-ttu-id="9e016-133">string</span><span class="sxs-lookup"><span data-stu-id="9e016-133">string</span></span>|<span data-ttu-id="9e016-p106">Representa la alineación vertical del objeto especificado. Valores posibles: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="9e016-p106">Represents the vertical alignment for the specified object. Possible values are: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span></span>|
|<span data-ttu-id="9e016-136">wrapText</span><span class="sxs-lookup"><span data-stu-id="9e016-136">wrapText</span></span>|<span data-ttu-id="9e016-137">boolean</span><span class="sxs-lookup"><span data-stu-id="9e016-137">boolean</span></span>|<span data-ttu-id="9e016-p107">Indica si Excel ajusta el texto del objeto. Un valor null indica que el intervalo no tiene una configuración de ajuste uniforme.</span><span class="sxs-lookup"><span data-stu-id="9e016-p107">Indicates if Excel wraps the text in the object. A null value indicates that the entire range doesn't have uniform wrap setting</span></span>|

## <a name="response"></a><span data-ttu-id="9e016-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9e016-140">Response</span></span>

<span data-ttu-id="9e016-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [RangeFormat](../resources/rangeformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9e016-141">If successful, this method returns a `200 OK` response code and updated [RangeFormat](../resources/rangeformat.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9e016-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9e016-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9e016-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9e016-143">Request</span></span>
<span data-ttu-id="9e016-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9e016-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_rangeformat"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/format
Content-type: application/json
Content-length: 96

{
  "columnWidth": 99,
  "horizontalAlignment": "horizontalAlignment-value",
  "rowHeight": 99
}
```
##### <a name="response"></a><span data-ttu-id="9e016-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9e016-145">Response</span></span>
<span data-ttu-id="9e016-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9e016-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 96

{
  "columnWidth": 99,
  "horizontalAlignment": "horizontalAlignment-value",
  "rowHeight": 99
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