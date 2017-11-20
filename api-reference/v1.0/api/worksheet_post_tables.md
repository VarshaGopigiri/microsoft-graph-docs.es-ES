# <a name="create-table"></a><span data-ttu-id="665db-101">Create Table</span><span class="sxs-lookup"><span data-stu-id="665db-101">Create Table</span></span>

<span data-ttu-id="665db-102">Use esta API para crear un objeto Table.</span><span class="sxs-lookup"><span data-stu-id="665db-102">Use this API to create a new Table.</span></span>
## <a name="permissions"></a><span data-ttu-id="665db-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="665db-103">Permissions</span></span>
<span data-ttu-id="665db-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="665db-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="665db-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="665db-106">Permission type</span></span>      | <span data-ttu-id="665db-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="665db-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="665db-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="665db-108">Delegated (work or school account)</span></span> | <span data-ttu-id="665db-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="665db-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="665db-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="665db-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="665db-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="665db-111">Not supported.</span></span>    |
|<span data-ttu-id="665db-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="665db-112">Application</span></span> | <span data-ttu-id="665db-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="665db-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="665db-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="665db-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/tables/add

```
## <a name="request-headers"></a><span data-ttu-id="665db-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="665db-115">Request headers</span></span>
| <span data-ttu-id="665db-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="665db-116">Name</span></span>       | <span data-ttu-id="665db-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="665db-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="665db-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="665db-118">Authorization</span></span>  | <span data-ttu-id="665db-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="665db-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="665db-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="665db-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="665db-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="665db-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="665db-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="665db-124">Request body</span></span>
<span data-ttu-id="665db-125">En el cuerpo de la solicitud, proporcione los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="665db-125">In the request body, supply following parameters.</span></span> 

### <a name="request-parameters"></a><span data-ttu-id="665db-126">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="665db-126">Request parameters</span></span>
| <span data-ttu-id="665db-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="665db-127">Name</span></span>           | <span data-ttu-id="665db-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="665db-128">Type</span></span>      |<span data-ttu-id="665db-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="665db-129">Description</span></span>|
|:---------------|:----------|:----------|
| <span data-ttu-id="665db-130">Dirección</span><span class="sxs-lookup"><span data-stu-id="665db-130">Address</span></span>  | <span data-ttu-id="665db-131">string</span><span class="sxs-lookup"><span data-stu-id="665db-131">string</span></span>| <span data-ttu-id="665db-p104">Dirección de intervalo. Si llama a esta API desde la ruta de acceso `worksheets/{id or name}/tables/add`, no tiene que proporcionar el prefijo del nombre de hoja en la dirección. En cambio, si la llama desde la ruta de acceso `workbook/tables/add`, deberá proporcionar el nombre de la hoja en la que se debe crear la tabla (ejemplo: `sheet1!A1:D4`)</span><span class="sxs-lookup"><span data-stu-id="665db-p104">Range address. If you are calling this API off of `worksheets/{id or name}/tables/add` path, there is no need to for sheet name prefix in the address. However, if you are calling this off of `workbook/tables/add` path, then supply the sheet name on which the table needs to be created (example: `sheet1!A1:D4`)</span></span>|
| <span data-ttu-id="665db-135">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="665db-135">hasHeaders</span></span>  | <span data-ttu-id="665db-136">boolean</span><span class="sxs-lookup"><span data-stu-id="665db-136">boolean</span></span>|<span data-ttu-id="665db-p105">Valor booleano que indica si el intervalo tiene etiquetas de columna. Si el origen no contiene encabezados (es decir, cuando esta propiedad se establece en false), Excel generará de forma automática el encabezado desplazando los datos hacia abajo una fila.</span><span class="sxs-lookup"><span data-stu-id="665db-p105">Boolean value that indicates whether the range has column labels. If the source does not contain headers (i.e,. when this property set to false), Excel will automatically generate header shifting the data down by one row.</span></span>|

## <a name="response"></a><span data-ttu-id="665db-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="665db-140">Response</span></span>

<span data-ttu-id="665db-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [Table](../resources/table.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="665db-141">If successful, this method returns `201 Created` response code and [Table](../resources/table.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="665db-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="665db-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="665db-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="665db-143">Request</span></span>
<span data-ttu-id="665db-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="665db-144">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="665db-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="665db-145">Response</span></span>
<span data-ttu-id="665db-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="665db-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
