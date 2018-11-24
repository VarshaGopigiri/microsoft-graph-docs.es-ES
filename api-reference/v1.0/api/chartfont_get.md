# <a name="get-chartfont"></a><span data-ttu-id="90473-101">Get ChartFont</span><span class="sxs-lookup"><span data-stu-id="90473-101">Get ChartFont</span></span>

<span data-ttu-id="90473-102">Recuperar las propiedades y relaciones del objeto chartfont.</span><span class="sxs-lookup"><span data-stu-id="90473-102">Retrieve the properties and relationships of chartfont object.</span></span>
## <a name="permissions"></a><span data-ttu-id="90473-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="90473-103">Permissions</span></span>
<span data-ttu-id="90473-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="90473-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="90473-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="90473-106">Permission type</span></span>      | <span data-ttu-id="90473-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="90473-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="90473-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="90473-108">Delegated (work or school account)</span></span> | <span data-ttu-id="90473-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="90473-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="90473-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="90473-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="90473-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90473-111">Not supported.</span></span>    |
|<span data-ttu-id="90473-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="90473-112">Application</span></span> | <span data-ttu-id="90473-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90473-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="90473-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90473-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/format/font
GET /workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/format/font
GET /workbook/worksheets/{id|name}/charts/{name}/axes/categoryaxis/format/font
```
## <a name="optional-query-parameters"></a><span data-ttu-id="90473-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="90473-115">Optional query parameters</span></span>
<span data-ttu-id="90473-116">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90473-116">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="90473-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90473-117">Request headers</span></span>
| <span data-ttu-id="90473-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="90473-118">Name</span></span>      |<span data-ttu-id="90473-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="90473-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="90473-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="90473-120">Authorization</span></span>  | <span data-ttu-id="90473-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90473-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="90473-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="90473-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="90473-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="90473-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="90473-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="90473-126">Request body</span></span>
<span data-ttu-id="90473-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="90473-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="90473-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90473-128">Response</span></span>

<span data-ttu-id="90473-129">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y [WorkbookChartFont](../resources/chartfont.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90473-129">If successful, this method returns a `200 OK` response code and [WorkbookChartFont](../resources/chartfont.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="90473-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90473-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="90473-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90473-131">Request</span></span>
<span data-ttu-id="90473-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="90473-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_chartfont"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/format/font
```
##### <a name="response"></a><span data-ttu-id="90473-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90473-133">Response</span></span>
<span data-ttu-id="90473-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="90473-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartFont"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 134

{
  "bold": true,
  "color": "color-value",
  "italic": true,
  "name": "name-value",
  "size": 99,
  "underline": "underline-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get ChartFont",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->