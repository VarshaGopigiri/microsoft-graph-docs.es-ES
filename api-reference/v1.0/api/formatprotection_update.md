# <a name="update-formatprotection"></a><span data-ttu-id="398a2-101">Update formatprotection</span><span class="sxs-lookup"><span data-stu-id="398a2-101">Update formatprotection</span></span>

<span data-ttu-id="398a2-102">Actualiza las propiedades del objeto formatprotection.</span><span class="sxs-lookup"><span data-stu-id="398a2-102">Update the properties of formatprotection object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="398a2-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="398a2-103">Prerequisites</span></span>
<span data-ttu-id="398a2-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="398a2-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="398a2-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="398a2-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="398a2-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="398a2-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range/format/protection
PATCH /workbook/worksheets/{id|name}/range(<address>)/format/protection
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format/protection
```
## <a name="optional-request-headers"></a><span data-ttu-id="398a2-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="398a2-107">Optional request headers</span></span>
| <span data-ttu-id="398a2-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="398a2-108">Name</span></span>       | <span data-ttu-id="398a2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="398a2-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="398a2-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="398a2-110">Authorization</span></span>  | <span data-ttu-id="398a2-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="398a2-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="398a2-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="398a2-113">Request body</span></span>
<span data-ttu-id="398a2-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="398a2-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="398a2-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="398a2-117">Property</span></span>     | <span data-ttu-id="398a2-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="398a2-118">Type</span></span>   |<span data-ttu-id="398a2-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="398a2-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="398a2-120">formulaHidden</span><span class="sxs-lookup"><span data-stu-id="398a2-120">formulaHidden</span></span>|<span data-ttu-id="398a2-121">boolean</span><span class="sxs-lookup"><span data-stu-id="398a2-121">boolean</span></span>|<span data-ttu-id="398a2-p103">Indica si Excel oculta la fórmula de las celdas del rango. Un valor null indica que el rango no tiene una configuración de fórmula oculta uniforme.</span><span class="sxs-lookup"><span data-stu-id="398a2-p103">Indicates if Excel hides the formula for the cells in the range. A null value indicates that the entire range doesn't have uniform formula hidden setting.</span></span>|
|<span data-ttu-id="398a2-124">locked</span><span class="sxs-lookup"><span data-stu-id="398a2-124">locked</span></span>|<span data-ttu-id="398a2-125">boolean</span><span class="sxs-lookup"><span data-stu-id="398a2-125">boolean</span></span>|<span data-ttu-id="398a2-p104">Indica si Excel bloquea las celdas del objeto. Un valor nulo indica que todo el rango no tiene una configuración de bloqueo uniforme.</span><span class="sxs-lookup"><span data-stu-id="398a2-p104">Indicates if Excel locks the cells in the object. A null value indicates that the entire range doesn't have uniform lock setting.</span></span>|

## <a name="response"></a><span data-ttu-id="398a2-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="398a2-128">Response</span></span>

<span data-ttu-id="398a2-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [FormatProtection](../resources/formatprotection.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="398a2-129">If successful, this method returns a `200 OK` response code and updated [FormatProtection](../resources/formatprotection.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="398a2-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="398a2-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="398a2-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="398a2-131">Request</span></span>
<span data-ttu-id="398a2-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="398a2-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_formatprotection"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/format/protection
Content-type: application/json
Content-length: 45

{
  "locked": true,
  "formulaHidden": true
}
```
##### <a name="response"></a><span data-ttu-id="398a2-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="398a2-133">Response</span></span>
<span data-ttu-id="398a2-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="398a2-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.formatProtection"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "locked": true,
  "formulaHidden": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update formatprotection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->