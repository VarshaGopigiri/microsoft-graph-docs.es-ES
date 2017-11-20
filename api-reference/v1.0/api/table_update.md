# <a name="update-table"></a><span data-ttu-id="6d2e1-101">Update table</span><span class="sxs-lookup"><span data-stu-id="6d2e1-101">Update table</span></span>

<span data-ttu-id="6d2e1-102">Actualizar las propiedades del objeto table.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-102">Update the properties of table object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6d2e1-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6d2e1-103">Permissions</span></span>
<span data-ttu-id="6d2e1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6d2e1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6d2e1-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6d2e1-106">Permission type</span></span>      | <span data-ttu-id="6d2e1-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6d2e1-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6d2e1-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6d2e1-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6d2e1-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6d2e1-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6d2e1-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6d2e1-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6d2e1-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-111">Not supported.</span></span>    |
|<span data-ttu-id="6d2e1-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6d2e1-112">Application</span></span> | <span data-ttu-id="6d2e1-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6d2e1-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6d2e1-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}
PATCH /workbook/worksheets/{id|name}/tables/{id|name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="6d2e1-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="6d2e1-115">Optional request headers</span></span>
| <span data-ttu-id="6d2e1-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="6d2e1-116">Name</span></span>       | <span data-ttu-id="6d2e1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d2e1-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="6d2e1-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="6d2e1-118">Authorization</span></span>  | <span data-ttu-id="6d2e1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6d2e1-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6d2e1-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="6d2e1-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6d2e1-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6d2e1-124">Request body</span></span>
<span data-ttu-id="6d2e1-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="6d2e1-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6d2e1-128">Property</span></span>     | <span data-ttu-id="6d2e1-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d2e1-129">Type</span></span>   |<span data-ttu-id="6d2e1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d2e1-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6d2e1-131">name</span><span class="sxs-lookup"><span data-stu-id="6d2e1-131">name</span></span>|<span data-ttu-id="6d2e1-132">string</span><span class="sxs-lookup"><span data-stu-id="6d2e1-132">string</span></span>|<span data-ttu-id="6d2e1-133">Nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-133">Name of the table.</span></span>|
|<span data-ttu-id="6d2e1-134">showHeaders</span><span class="sxs-lookup"><span data-stu-id="6d2e1-134">showHeaders</span></span>|<span data-ttu-id="6d2e1-135">boolean</span><span class="sxs-lookup"><span data-stu-id="6d2e1-135">boolean</span></span>|<span data-ttu-id="6d2e1-p105">Indica si la fila de encabezado está visible o no. Este valor puede establecerse para que muestre o quite la fila de encabezado.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-p105">Indicates whether the header row is visible or not. This value can be set to show or remove the header row.</span></span>|
|<span data-ttu-id="6d2e1-138">showTotals</span><span class="sxs-lookup"><span data-stu-id="6d2e1-138">showTotals</span></span>|<span data-ttu-id="6d2e1-139">boolean</span><span class="sxs-lookup"><span data-stu-id="6d2e1-139">boolean</span></span>|<span data-ttu-id="6d2e1-p106">Indica si la fila de totales está visible o no. Este valor puede establecerse para que muestre o quite la fila de totales.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-p106">Indicates whether the total row is visible or not. This value can be set to show or remove the total row.</span></span>|
|<span data-ttu-id="6d2e1-142">style</span><span class="sxs-lookup"><span data-stu-id="6d2e1-142">style</span></span>|<span data-ttu-id="6d2e1-143">string</span><span class="sxs-lookup"><span data-stu-id="6d2e1-143">string</span></span>|<span data-ttu-id="6d2e1-p107">Valor constante que representa el estilo de tabla. Los valores posibles son: TableStyleLight1 thru TableStyleLight21, TableStyleMedium1 thru TableStyleMedium28, TableStyleStyleDark1 thru TableStyleStyleDark11. También puede especificarse un estilo personalizado definido por el usuario presente en el libro.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-p107">Constant value that represents the Table style. Possible values are: TableStyleLight1 thru TableStyleLight21, TableStyleMedium1 thru TableStyleMedium28, TableStyleStyleDark1 thru TableStyleStyleDark11. A custom user-defined style present in the workbook can also be specified.</span></span>|

## <a name="response"></a><span data-ttu-id="6d2e1-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d2e1-147">Response</span></span>

<span data-ttu-id="6d2e1-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Table](../resources/table.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-148">If successful, this method returns a `200 OK` response code and updated [Table](../resources/table.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6d2e1-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d2e1-149">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6d2e1-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6d2e1-150">Request</span></span>
<span data-ttu-id="6d2e1-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-151">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="6d2e1-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d2e1-152">Response</span></span>
<span data-ttu-id="6d2e1-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6d2e1-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
