# <a name="get-workbookpivottable"></a><span data-ttu-id="85a15-101">Get workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="85a15-101">Get workbookPivotTable</span></span>

<span data-ttu-id="85a15-102">Recupera las propiedades y relaciones del objeto workbookPivotTable.</span><span class="sxs-lookup"><span data-stu-id="85a15-102">Retrieve the properties and relationships of workbookPivotTable object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="85a15-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="85a15-103">Prerequisites</span></span>
<span data-ttu-id="85a15-104">Se requieren los siguientes **ámbitos** para ejecutar esta API: _Files.Read, Files.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="85a15-104">The following **scopes** are required to execute this API: _Files.Read, Files.ReadWrite_</span></span>

## <a name="http-request"></a><span data-ttu-id="85a15-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="85a15-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root/workbook/worksheets/{id}/pivotTables/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="85a15-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="85a15-106">Optional query parameters</span></span>
<span data-ttu-id="85a15-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85a15-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="85a15-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="85a15-108">Request headers</span></span>
| <span data-ttu-id="85a15-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="85a15-109">Name</span></span>      |<span data-ttu-id="85a15-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="85a15-110">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="85a15-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="85a15-111">Authorization</span></span>  | <span data-ttu-id="85a15-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="85a15-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="85a15-114">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="85a15-114">Workbook-Session-Id</span></span>  | <span data-ttu-id="85a15-p102">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="85a15-p102">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="85a15-117">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="85a15-117">Request body</span></span>
<span data-ttu-id="85a15-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="85a15-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="85a15-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="85a15-119">Response</span></span>

<span data-ttu-id="85a15-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [workbookPivotTable](../resources/workbookpivottable.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85a15-120">If successful, this method returns a `200 OK` response code and [workbookPivotTable](../resources/workbookpivottable.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="85a15-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="85a15-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="85a15-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="85a15-122">Request</span></span>
<span data-ttu-id="85a15-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="85a15-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_workbookpivottable"
}-->
```http
GET https://graph.microsoft.com/v1.0/drive/root/workbook/worksheets/{id}/pivotTables/{id}
```
##### <a name="response"></a><span data-ttu-id="85a15-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="85a15-124">Response</span></span>
<span data-ttu-id="85a15-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="85a15-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookPivotTable"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 46

{
  "id": "id-value",
  "name": "name-value"
}
```
