# <a name="update-range"></a><span data-ttu-id="01f0c-101">Update range</span><span class="sxs-lookup"><span data-stu-id="01f0c-101">Update range</span></span>

<span data-ttu-id="01f0c-102">Actualiza las propiedades del objeto range.</span><span class="sxs-lookup"><span data-stu-id="01f0c-102">Update the properties of range object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="01f0c-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="01f0c-103">Prerequisites</span></span>
<span data-ttu-id="01f0c-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="01f0c-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="01f0c-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="01f0c-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="01f0c-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01f0c-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range
PATCH /workbook/worksheets/{id|name}/range(address=<range-address>)
PATCH /workbook/tables/{id|name}/columns/{id|name}/range
```
## <a name="optional-request-headers"></a><span data-ttu-id="01f0c-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="01f0c-107">Optional request headers</span></span>
| <span data-ttu-id="01f0c-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="01f0c-108">Name</span></span>       | <span data-ttu-id="01f0c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="01f0c-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="01f0c-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="01f0c-110">Authorization</span></span>  | <span data-ttu-id="01f0c-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01f0c-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="01f0c-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01f0c-113">Request body</span></span>
<span data-ttu-id="01f0c-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="01f0c-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="01f0c-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01f0c-117">Property</span></span>     | <span data-ttu-id="01f0c-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="01f0c-118">Type</span></span>   |<span data-ttu-id="01f0c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="01f0c-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="01f0c-120">columnHidden</span><span class="sxs-lookup"><span data-stu-id="01f0c-120">columnHidden</span></span>|<span data-ttu-id="01f0c-121">boolean</span><span class="sxs-lookup"><span data-stu-id="01f0c-121">boolean</span></span>|<span data-ttu-id="01f0c-122">Representa si todas las columnas del rango actual están ocultas.</span><span class="sxs-lookup"><span data-stu-id="01f0c-122">Represents if all columns of the current range are hidden.</span></span>|
|<span data-ttu-id="01f0c-123">formulas</span><span class="sxs-lookup"><span data-stu-id="01f0c-123">formulas</span></span>|<span data-ttu-id="01f0c-124">json</span><span class="sxs-lookup"><span data-stu-id="01f0c-124">json</span></span>|<span data-ttu-id="01f0c-125">Representa la fórmula en notación de estilo A1.</span><span class="sxs-lookup"><span data-stu-id="01f0c-125">Represents the formula in A1-style notation.</span></span>|
|<span data-ttu-id="01f0c-126">formulasLocal</span><span class="sxs-lookup"><span data-stu-id="01f0c-126">formulasLocal</span></span>|<span data-ttu-id="01f0c-127">json</span><span class="sxs-lookup"><span data-stu-id="01f0c-127">json</span></span>|<span data-ttu-id="01f0c-p103">Representa la fórmula en notación de estilo A1, en el idioma del usuario y en la configuración regional del formato numérico. Por ejemplo, la fórmula "=SUM(A1, 1.5)" en inglés se convertiría en "=SUMME(A1; 1,5)" en alemán.</span><span class="sxs-lookup"><span data-stu-id="01f0c-p103">Represents the formula in A1-style notation, in the user's language and number-formatting locale.  For example, the English "=SUM(A1, 1.5)" formula would become "=SUMME(A1; 1,5)" in German.</span></span>|
|<span data-ttu-id="01f0c-130">formulasR1C1</span><span class="sxs-lookup"><span data-stu-id="01f0c-130">formulasR1C1</span></span>|<span data-ttu-id="01f0c-131">json</span><span class="sxs-lookup"><span data-stu-id="01f0c-131">json</span></span>|<span data-ttu-id="01f0c-132">Representa la fórmula en notación de estilo R1C1.</span><span class="sxs-lookup"><span data-stu-id="01f0c-132">Represents the formula in R1C1-style notation.</span></span>|
|<span data-ttu-id="01f0c-133">numberFormat</span><span class="sxs-lookup"><span data-stu-id="01f0c-133">numberFormat</span></span>|<span data-ttu-id="01f0c-134">json</span><span class="sxs-lookup"><span data-stu-id="01f0c-134">json</span></span>|<span data-ttu-id="01f0c-135">Representa el código de formato numérico de Excel para la celda especificada.</span><span class="sxs-lookup"><span data-stu-id="01f0c-135">Represents Excel's number format code for the given cell.</span></span>|
|<span data-ttu-id="01f0c-136">rowHidden</span><span class="sxs-lookup"><span data-stu-id="01f0c-136">rowHidden</span></span>|<span data-ttu-id="01f0c-137">boolean</span><span class="sxs-lookup"><span data-stu-id="01f0c-137">boolean</span></span>|<span data-ttu-id="01f0c-138">Representa si todas las filas del rango actual están ocultas.</span><span class="sxs-lookup"><span data-stu-id="01f0c-138">Represents if all rows of the current range are hidden.</span></span>|
|<span data-ttu-id="01f0c-139">values</span><span class="sxs-lookup"><span data-stu-id="01f0c-139">values</span></span>|<span data-ttu-id="01f0c-140">json</span><span class="sxs-lookup"><span data-stu-id="01f0c-140">json</span></span>|<span data-ttu-id="01f0c-p104">Representa los valores sin formato del rango especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="01f0c-p104">Represents the raw values of the specified range. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>|

## <a name="response"></a><span data-ttu-id="01f0c-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01f0c-144">Response</span></span>

<span data-ttu-id="01f0c-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Range](../resources/range.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01f0c-145">If successful, this method returns a `200 OK` response code and updated [Range](../resources/range.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="01f0c-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01f0c-146">Example</span></span>
##### <a name="request"></a><span data-ttu-id="01f0c-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01f0c-147">Request</span></span>
<span data-ttu-id="01f0c-p105">Aquí tiene un ejemplo de la solicitud. Actualiza un rango: valores, formato de número y fórmula. La entrada `null` indica a la API que omita la celda para esa entrada en particular. Los valores, el formato de número y las fórmulas se pueden actualizar por separado o conjuntamente en la misma llamada de API.</span><span class="sxs-lookup"><span data-stu-id="01f0c-p105">Here is an example of the request. It updates a range - values, number-format and formula. The `null` input is to instruct the API to ignore the cell for that particular input. The values, number-format and formulas can be independently updated or combined together in the same API call.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_range"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets('sheet1')/range(address='A1:B2')
Content-type: application/json
Content-length: 169

{
"values" : [["Hello", "100"],["1/1/2016", null]],
"formula" : [[null, null], [null, "=B1*2"]],
"numberFormat" : [[null,null], ["m-ddd", null]]
}
```
##### <a name="response"></a><span data-ttu-id="01f0c-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01f0c-152">Response</span></span>
<span data-ttu-id="01f0c-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="01f0c-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update range",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
