# <a name="update-formatprotection"></a><span data-ttu-id="4dcdf-101">Update formatprotection</span><span class="sxs-lookup"><span data-stu-id="4dcdf-101">Update formatprotection</span></span>

<span data-ttu-id="4dcdf-102">Actualiza las propiedades del objeto formatprotection.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-102">Update the properties of formatprotection object.</span></span>
## <a name="permissions"></a><span data-ttu-id="4dcdf-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="4dcdf-103">Permissions</span></span>
<span data-ttu-id="4dcdf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4dcdf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4dcdf-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4dcdf-106">Permission type</span></span>      | <span data-ttu-id="4dcdf-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4dcdf-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="4dcdf-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4dcdf-108">Delegated (work or school account)</span></span> | <span data-ttu-id="4dcdf-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4dcdf-109">Files.ReadWrite</span></span>    | 
|<span data-ttu-id="4dcdf-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4dcdf-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4dcdf-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-111">Not supported.</span></span>    | 
|<span data-ttu-id="4dcdf-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4dcdf-112">Application</span></span> | <span data-ttu-id="4dcdf-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-113">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="4dcdf-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4dcdf-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range/format/protection
PATCH /workbook/worksheets/{id|name}/range(<address>)/format/protection
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format/protection
```
## <a name="optional-request-headers"></a><span data-ttu-id="4dcdf-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="4dcdf-115">Optional request headers</span></span>
| <span data-ttu-id="4dcdf-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="4dcdf-116">Name</span></span>       | <span data-ttu-id="4dcdf-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4dcdf-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="4dcdf-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="4dcdf-118">Authorization</span></span>  | <span data-ttu-id="4dcdf-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="4dcdf-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4dcdf-121">Request body</span></span>
<span data-ttu-id="4dcdf-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="4dcdf-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4dcdf-125">Property</span></span>     | <span data-ttu-id="4dcdf-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="4dcdf-126">Type</span></span>   |<span data-ttu-id="4dcdf-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="4dcdf-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4dcdf-128">formulaHidden</span><span class="sxs-lookup"><span data-stu-id="4dcdf-128">formulaHidden</span></span>|<span data-ttu-id="4dcdf-129">boolean</span><span class="sxs-lookup"><span data-stu-id="4dcdf-129">boolean</span></span>|<span data-ttu-id="4dcdf-p104">Indica si Excel oculta la fórmula de las celdas del rango. Un valor null indica que el rango no tiene una configuración de fórmula oculta uniforme.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-p104">Indicates if Excel hides the formula for the cells in the range. A null value indicates that the entire range doesn't have uniform formula hidden setting.</span></span>|
|<span data-ttu-id="4dcdf-132">locked</span><span class="sxs-lookup"><span data-stu-id="4dcdf-132">locked</span></span>|<span data-ttu-id="4dcdf-133">boolean</span><span class="sxs-lookup"><span data-stu-id="4dcdf-133">boolean</span></span>|<span data-ttu-id="4dcdf-p105">Indica si Excel bloquea las celdas del objeto. Un valor nulo indica que todo el rango no tiene una configuración de bloqueo uniforme.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-p105">Indicates if Excel locks the cells in the object. A null value indicates that the entire range doesn't have uniform lock setting.</span></span>|

## <a name="response"></a><span data-ttu-id="4dcdf-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4dcdf-136">Response</span></span>

<span data-ttu-id="4dcdf-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [FormatProtection](../resources/formatprotection.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-137">If successful, this method returns a `200 OK` response code and updated [FormatProtection](../resources/formatprotection.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4dcdf-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4dcdf-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4dcdf-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4dcdf-139">Request</span></span>
<span data-ttu-id="4dcdf-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-140">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="4dcdf-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4dcdf-141">Response</span></span>
<span data-ttu-id="4dcdf-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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