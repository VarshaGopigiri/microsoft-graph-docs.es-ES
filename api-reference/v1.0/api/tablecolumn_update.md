# <a name="update-tablecolumn"></a><span data-ttu-id="e823d-101">Update tablecolumn</span><span class="sxs-lookup"><span data-stu-id="e823d-101">Update tablecolumn</span></span>

<span data-ttu-id="e823d-102">Actualiza las propiedades del objeto tablecolumn.</span><span class="sxs-lookup"><span data-stu-id="e823d-102">Update the properties of tablecolumn object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e823d-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e823d-103">Prerequisites</span></span>
<span data-ttu-id="e823d-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="e823d-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="e823d-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e823d-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="e823d-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e823d-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}/columns/{id|name}
PATCH /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="e823d-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="e823d-107">Optional request headers</span></span>
| <span data-ttu-id="e823d-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="e823d-108">Name</span></span>       | <span data-ttu-id="e823d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e823d-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="e823d-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="e823d-110">Authorization</span></span>  | <span data-ttu-id="e823d-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e823d-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="e823d-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e823d-113">Request body</span></span>
<span data-ttu-id="e823d-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="e823d-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="e823d-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e823d-117">Property</span></span>     | <span data-ttu-id="e823d-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="e823d-118">Type</span></span>   |<span data-ttu-id="e823d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="e823d-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e823d-120">values</span><span class="sxs-lookup"><span data-stu-id="e823d-120">values</span></span>|<span data-ttu-id="e823d-121">json</span><span class="sxs-lookup"><span data-stu-id="e823d-121">json</span></span>|<span data-ttu-id="e823d-p103">Representa los valores sin formato del rango especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="e823d-p103">Represents the raw values of the specified range. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>|

## <a name="response"></a><span data-ttu-id="e823d-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e823d-125">Response</span></span>

<span data-ttu-id="e823d-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [TableColumn](../resources/tablecolumn.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e823d-126">If successful, this method returns a `200 OK` response code and updated [TableColumn](../resources/tablecolumn.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e823d-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e823d-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e823d-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e823d-128">Request</span></span>
<span data-ttu-id="e823d-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e823d-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_tablecolumn"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}
Content-type: application/json
Content-length: 81

{
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```
##### <a name="response"></a><span data-ttu-id="e823d-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e823d-130">Response</span></span>
<span data-ttu-id="e823d-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e823d-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableColumn"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 81

{
  "id": 99,
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update tablecolumn",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->