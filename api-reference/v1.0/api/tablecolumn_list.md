# <a name="list-tablecolumncollection"></a><span data-ttu-id="6606b-101">List TableColumnCollection</span><span class="sxs-lookup"><span data-stu-id="6606b-101">List TableColumnCollection</span></span>

<span data-ttu-id="6606b-102">Recuperar una lista de objetos tablecolumn.</span><span class="sxs-lookup"><span data-stu-id="6606b-102">Retrieve a list of tablecolumn objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="6606b-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6606b-103">Permissions</span></span>
<span data-ttu-id="6606b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6606b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6606b-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6606b-106">Permission type</span></span>      | <span data-ttu-id="6606b-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6606b-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6606b-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6606b-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6606b-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6606b-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6606b-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6606b-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6606b-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6606b-111">Not supported.</span></span>    |
|<span data-ttu-id="6606b-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6606b-112">Application</span></span> | <span data-ttu-id="6606b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6606b-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6606b-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6606b-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/tables/{id|name}/columns
GET /workbook/worksheets/{id|name}/tables/{id|name}/columns
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6606b-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6606b-115">Optional query parameters</span></span>
<span data-ttu-id="6606b-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6606b-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6606b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6606b-117">Request headers</span></span>
| <span data-ttu-id="6606b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="6606b-118">Name</span></span>      |<span data-ttu-id="6606b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6606b-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="6606b-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="6606b-120">Authorization</span></span>  | <span data-ttu-id="6606b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6606b-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6606b-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6606b-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="6606b-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="6606b-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6606b-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6606b-126">Request body</span></span>
<span data-ttu-id="6606b-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6606b-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6606b-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6606b-128">Response</span></span>

<span data-ttu-id="6606b-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [TableColumn](../resources/tablecolumn.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6606b-129">If successful, this method returns a `200 OK` response code and collection of [TableColumn](../resources/tablecolumn.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6606b-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6606b-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6606b-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6606b-131">Request</span></span>
<span data-ttu-id="6606b-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6606b-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_tablecolumncollection"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns
```
##### <a name="response"></a><span data-ttu-id="6606b-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6606b-133">Response</span></span>
<span data-ttu-id="6606b-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6606b-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableColumn",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 126

{
  "value": [
    {
      "id": 99,
      "name": "name-value",
      "index": 99,
      "values": "values-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List TableColumnCollection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->