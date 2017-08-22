# <a name="create-table"></a><span data-ttu-id="ba683-101">Create Table</span><span class="sxs-lookup"><span data-stu-id="ba683-101">Create Table</span></span>

<span data-ttu-id="ba683-102">Use esta API para crear un objeto Table.</span><span class="sxs-lookup"><span data-stu-id="ba683-102">Use this API to create a new Table.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ba683-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ba683-103">Prerequisites</span></span>
<span data-ttu-id="ba683-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="ba683-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="ba683-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ba683-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="ba683-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ba683-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/tables/add

```
## <a name="request-headers"></a><span data-ttu-id="ba683-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ba683-107">Request headers</span></span>
| <span data-ttu-id="ba683-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="ba683-108">Name</span></span>       | <span data-ttu-id="ba683-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba683-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ba683-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="ba683-110">Authorization</span></span>  | <span data-ttu-id="ba683-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ba683-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="ba683-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ba683-113">Request body</span></span>
<span data-ttu-id="ba683-114">En el cuerpo de la solicitud, proporcione los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="ba683-114">In the request body, supply following parameters.</span></span> 

### <a name="request-parameters"></a><span data-ttu-id="ba683-115">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ba683-115">Request parameters</span></span>
| <span data-ttu-id="ba683-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="ba683-116">Name</span></span>           | <span data-ttu-id="ba683-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="ba683-117">Type</span></span>      |<span data-ttu-id="ba683-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba683-118">Description</span></span>|
|:---------------|:----------|:----------|
| <span data-ttu-id="ba683-119">Dirección</span><span class="sxs-lookup"><span data-stu-id="ba683-119">Address</span></span>  | <span data-ttu-id="ba683-120">string</span><span class="sxs-lookup"><span data-stu-id="ba683-120">string</span></span>| <span data-ttu-id="ba683-p102">Dirección de intervalo. Si llama a esta API desde la ruta de acceso `worksheets/{id or name}/tables/add`, no tiene que proporcionar el prefijo del nombre de hoja en la dirección. En cambio, si la llama desde la ruta de acceso `workbook/tables/add`, deberá proporcionar el nombre de la hoja en la que se debe crear la tabla (ejemplo: `sheet1!A1:D4`)</span><span class="sxs-lookup"><span data-stu-id="ba683-p102">Range address. If you are calling this API off of `worksheets/{id or name}/tables/add` path, there is no need to for sheet name prefix in the address. However, if you are calling this off of `workbook/tables/add` path, then supply the sheet name on which the table needs to be created (example: `sheet1!A1:D4`)</span></span>|
| <span data-ttu-id="ba683-124">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="ba683-124">hasHeaders</span></span>  | <span data-ttu-id="ba683-125">boolean</span><span class="sxs-lookup"><span data-stu-id="ba683-125">boolean</span></span>|<span data-ttu-id="ba683-p103">Valor booleano que indica si el intervalo tiene etiquetas de columna. Si el origen no contiene encabezados (es decir, cuando esta propiedad se establece en false), Excel generará de forma automática el encabezado desplazando los datos hacia abajo una fila.</span><span class="sxs-lookup"><span data-stu-id="ba683-p103">Boolean value that indicates whether the range has column labels. If the source does not contain headers (i.e,. when this property set to false), Excel will automatically generate header shifting the data down by one row.</span></span>|

## <a name="response"></a><span data-ttu-id="ba683-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba683-129">Response</span></span>

<span data-ttu-id="ba683-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [Table](../resources/table.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba683-130">If successful, this method returns `201, Created` response code and [Table](../resources/table.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ba683-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba683-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ba683-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ba683-132">Request</span></span>
<span data-ttu-id="ba683-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ba683-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_table_from_worksheet"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/tables/$/add
Content-type: application/json
Content-length: 109

{
  "address": "A1:D8",
  "hasHeaders": false
}
```
##### <a name="response"></a><span data-ttu-id="ba683-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba683-134">Response</span></span>
<span data-ttu-id="ba683-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ba683-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.table"
} -->
```http
HTTP/1.1 201 Created
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
  "description": "Create Table",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
