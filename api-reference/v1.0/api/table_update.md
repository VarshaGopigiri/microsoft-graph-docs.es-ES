# <a name="update-table"></a><span data-ttu-id="e84fc-101">Update table</span><span class="sxs-lookup"><span data-stu-id="e84fc-101">Update table</span></span>

<span data-ttu-id="e84fc-102">Actualiza las propiedades del objeto table.</span><span class="sxs-lookup"><span data-stu-id="e84fc-102">Update the properties of table object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e84fc-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e84fc-103">Prerequisites</span></span>
<span data-ttu-id="e84fc-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="e84fc-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="e84fc-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e84fc-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="e84fc-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e84fc-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}
PATCH /workbook/worksheets/{id|name}/tables/{id|name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="e84fc-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="e84fc-107">Optional request headers</span></span>
| <span data-ttu-id="e84fc-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="e84fc-108">Name</span></span>       | <span data-ttu-id="e84fc-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e84fc-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="e84fc-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="e84fc-110">Authorization</span></span>  | <span data-ttu-id="e84fc-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e84fc-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="e84fc-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e84fc-113">Request body</span></span>
<span data-ttu-id="e84fc-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="e84fc-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="e84fc-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e84fc-117">Property</span></span>     | <span data-ttu-id="e84fc-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="e84fc-118">Type</span></span>   |<span data-ttu-id="e84fc-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="e84fc-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e84fc-120">name</span><span class="sxs-lookup"><span data-stu-id="e84fc-120">name</span></span>|<span data-ttu-id="e84fc-121">string</span><span class="sxs-lookup"><span data-stu-id="e84fc-121">string</span></span>|<span data-ttu-id="e84fc-122">Nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e84fc-122">Name of the table.</span></span>|
|<span data-ttu-id="e84fc-123">showHeaders</span><span class="sxs-lookup"><span data-stu-id="e84fc-123">showHeaders</span></span>|<span data-ttu-id="e84fc-124">boolean</span><span class="sxs-lookup"><span data-stu-id="e84fc-124">boolean</span></span>|<span data-ttu-id="e84fc-p103">Indica si la fila de encabezado está visible o no. Este valor puede establecerse para que muestre o quite la fila de encabezado.</span><span class="sxs-lookup"><span data-stu-id="e84fc-p103">Indicates whether the header row is visible or not. This value can be set to show or remove the header row.</span></span>|
|<span data-ttu-id="e84fc-127">showTotals</span><span class="sxs-lookup"><span data-stu-id="e84fc-127">showTotals</span></span>|<span data-ttu-id="e84fc-128">boolean</span><span class="sxs-lookup"><span data-stu-id="e84fc-128">boolean</span></span>|<span data-ttu-id="e84fc-p104">Indica si la fila de totales está visible o no. Este valor puede establecerse para que muestre o quite la fila de totales.</span><span class="sxs-lookup"><span data-stu-id="e84fc-p104">Indicates whether the total row is visible or not. This value can be set to show or remove the total row.</span></span>|
|<span data-ttu-id="e84fc-131">style</span><span class="sxs-lookup"><span data-stu-id="e84fc-131">style</span></span>|<span data-ttu-id="e84fc-132">string</span><span class="sxs-lookup"><span data-stu-id="e84fc-132">string</span></span>|<span data-ttu-id="e84fc-p105">Valor constante que representa el estilo de tabla. Los valores posibles son: TableStyleLight1 thru TableStyleLight21, TableStyleMedium1 thru TableStyleMedium28, TableStyleStyleDark1 thru TableStyleStyleDark11. También puede especificarse un estilo personalizado definido por el usuario presente en el libro.</span><span class="sxs-lookup"><span data-stu-id="e84fc-p105">Constant value that represents the Table style. Possible values are: TableStyleLight1 thru TableStyleLight21, TableStyleMedium1 thru TableStyleMedium28, TableStyleStyleDark1 thru TableStyleStyleDark11. A custom user-defined style present in the workbook can also be specified.</span></span>|

## <a name="response"></a><span data-ttu-id="e84fc-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e84fc-136">Response</span></span>

<span data-ttu-id="e84fc-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Table](../resources/table.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e84fc-137">If successful, this method returns a `200 OK` response code and updated [Table](../resources/table.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e84fc-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e84fc-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e84fc-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e84fc-139">Request</span></span>
<span data-ttu-id="e84fc-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e84fc-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_table"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}
Content-type: application/json
Content-length: 109

{
  "name": "name-value",
  "showHeaders": true,
  "showTotals": true,
  "style": "style-value"
}
```
##### <a name="response"></a><span data-ttu-id="e84fc-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e84fc-141">Response</span></span>
<span data-ttu-id="e84fc-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e84fc-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.table"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 109

{
  "id": "99",
  "name": "name-value",
  "showHeaders": true,
  "showTotals": true,
  "style": "style-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update table",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
