# <a name="get-tablerow"></a><span data-ttu-id="d2c84-101">Get TableRow</span><span class="sxs-lookup"><span data-stu-id="d2c84-101">Get TableRow</span></span>

<span data-ttu-id="d2c84-102">Recupera las propiedades y relaciones del objeto tablerow.</span><span class="sxs-lookup"><span data-stu-id="d2c84-102">Retrieve the properties and relationships of tablerow object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d2c84-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d2c84-103">Prerequisites</span></span>
<span data-ttu-id="d2c84-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="d2c84-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="d2c84-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2c84-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="d2c84-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2c84-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/tables/{id|name}/rows(<index>)
GET /workbook/worksheets/{id|name}/tables/{id|name}/rows(<index>)
```
## <a name="optional-query-parameters"></a><span data-ttu-id="d2c84-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d2c84-107">Optional query parameters</span></span>
<span data-ttu-id="d2c84-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2c84-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d2c84-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2c84-109">Request headers</span></span>
| <span data-ttu-id="d2c84-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="d2c84-110">Name</span></span>      |<span data-ttu-id="d2c84-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2c84-111">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d2c84-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="d2c84-112">Authorization</span></span>  | <span data-ttu-id="d2c84-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2c84-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="d2c84-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2c84-115">Request body</span></span>
<span data-ttu-id="d2c84-116">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d2c84-116">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d2c84-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2c84-117">Response</span></span>

<span data-ttu-id="d2c84-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [TableRow](../resources/tablerow.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2c84-118">If successful, this method returns a `200 OK` response code and [TableRow](../resources/tablerow.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d2c84-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2c84-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d2c84-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2c84-120">Request</span></span>
<span data-ttu-id="d2c84-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2c84-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_tablerow"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/rows(<index>)
```
##### <a name="response"></a><span data-ttu-id="d2c84-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2c84-122">Response</span></span>
<span data-ttu-id="d2c84-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2c84-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableRow"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get TableRow",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->