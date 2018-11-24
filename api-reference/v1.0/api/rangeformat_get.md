# <a name="get-rangeformat"></a><span data-ttu-id="d3591-101">Get RangeFormat</span><span class="sxs-lookup"><span data-stu-id="d3591-101">Get RangeFormat</span></span>

<span data-ttu-id="d3591-102">Recuperar las propiedades y relaciones del objeto rangeformat.</span><span class="sxs-lookup"><span data-stu-id="d3591-102">Retrieve the properties and relationships of rangeformat object.</span></span>
## <a name="permissions"></a><span data-ttu-id="d3591-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d3591-103">Permissions</span></span>
<span data-ttu-id="d3591-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d3591-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d3591-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d3591-106">Permission type</span></span>      | <span data-ttu-id="d3591-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d3591-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d3591-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d3591-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d3591-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d3591-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d3591-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d3591-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d3591-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d3591-111">Not supported.</span></span>    |
|<span data-ttu-id="d3591-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d3591-112">Application</span></span> | <span data-ttu-id="d3591-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d3591-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d3591-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d3591-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/format
GET /workbook/worksheets/{id|name}/range(address='<address>')/format
GET /workbook/tables/{id|name}/columns/{id|name}/range/format
```
## <a name="optional-query-parameters"></a><span data-ttu-id="d3591-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d3591-115">Optional query parameters</span></span>
<span data-ttu-id="d3591-116">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3591-116">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d3591-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d3591-117">Request headers</span></span>
| <span data-ttu-id="d3591-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="d3591-118">Name</span></span>      |<span data-ttu-id="d3591-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3591-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d3591-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="d3591-120">Authorization</span></span>  | <span data-ttu-id="d3591-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d3591-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d3591-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d3591-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="d3591-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d3591-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d3591-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d3591-126">Request body</span></span>
<span data-ttu-id="d3591-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d3591-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d3591-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3591-128">Response</span></span>

<span data-ttu-id="d3591-129">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y [WorkbookRangeFormat](../resources/rangeformat.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3591-129">If successful, this method returns a `200 OK` response code and [WorkbookRangeFormat](../resources/rangeformat.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d3591-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d3591-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d3591-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d3591-131">Request</span></span>
<span data-ttu-id="d3591-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d3591-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_rangeformat"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/format
```
##### <a name="response"></a><span data-ttu-id="d3591-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3591-133">Response</span></span>
<span data-ttu-id="d3591-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d3591-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeFormat"
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
  "description": "Get RangeFormat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->