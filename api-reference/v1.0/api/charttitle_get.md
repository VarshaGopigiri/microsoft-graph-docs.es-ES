# <a name="get-charttitle"></a><span data-ttu-id="c2ee4-101">Get ChartTitle</span><span class="sxs-lookup"><span data-stu-id="c2ee4-101">Get ChartTitle</span></span>

<span data-ttu-id="c2ee4-102">Recupera las propiedades y relaciones del objeto charttitle.</span><span class="sxs-lookup"><span data-stu-id="c2ee4-102">Retrieve the properties and relationships of charttitle object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c2ee4-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c2ee4-103">Prerequisites</span></span>
<span data-ttu-id="c2ee4-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="c2ee4-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="c2ee4-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c2ee4-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="c2ee4-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2ee4-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts(<name>)/title
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c2ee4-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c2ee4-107">Optional query parameters</span></span>
<span data-ttu-id="c2ee4-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2ee4-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c2ee4-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c2ee4-109">Request headers</span></span>
| <span data-ttu-id="c2ee4-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="c2ee4-110">Name</span></span>      |<span data-ttu-id="c2ee4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2ee4-111">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c2ee4-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="c2ee4-112">Authorization</span></span>  | <span data-ttu-id="c2ee4-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c2ee4-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="c2ee4-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c2ee4-115">Request body</span></span>
<span data-ttu-id="c2ee4-116">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c2ee4-116">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c2ee4-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2ee4-117">Response</span></span>

<span data-ttu-id="c2ee4-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartTitle](../resources/charttitle.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2ee4-118">If successful, this method returns a `200 OK` response code and [ChartTitle](../resources/charttitle.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c2ee4-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2ee4-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c2ee4-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2ee4-120">Request</span></span>
<span data-ttu-id="c2ee4-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c2ee4-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_charttitle"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/title
```
##### <a name="response"></a><span data-ttu-id="c2ee4-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2ee4-122">Response</span></span>
<span data-ttu-id="c2ee4-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2ee4-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartTitle"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 64

{
  "overlay": true,
  "text": "text-value",
  "visible": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get ChartTitle",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->