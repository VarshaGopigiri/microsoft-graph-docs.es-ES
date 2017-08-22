# <a name="list-buckets"></a><span data-ttu-id="b29e9-101">Enumerar depósitos</span><span class="sxs-lookup"><span data-stu-id="b29e9-101">List buckets</span></span>

<span data-ttu-id="b29e9-102">Recuperar una lista de objetos **plannerbucket**.</span><span class="sxs-lookup"><span data-stu-id="b29e9-102">Retrieve a list of **plannerbucket** objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b29e9-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b29e9-103">Prerequisites</span></span>
<span data-ttu-id="b29e9-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="b29e9-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="b29e9-105">*Group.Read.All*</span><span class="sxs-lookup"><span data-stu-id="b29e9-105">*Group.Read.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="b29e9-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b29e9-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/buckets
```
## <a name="optional-query-parameters"></a><span data-ttu-id="b29e9-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b29e9-107">Optional query parameters</span></span>
<span data-ttu-id="b29e9-108">Este método requiere que se especifique un [filter](http://graph.microsoft.io/docs/overview/query_parameters) de planId.</span><span class="sxs-lookup"><span data-stu-id="b29e9-108">This method requires planId [filter](http://graph.microsoft.io/docs/overview/query_parameters) to be specified.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b29e9-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b29e9-109">Request headers</span></span>
| <span data-ttu-id="b29e9-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="b29e9-110">Name</span></span>      |<span data-ttu-id="b29e9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b29e9-111">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="b29e9-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="b29e9-112">Authorization</span></span>  | <span data-ttu-id="b29e9-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b29e9-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b29e9-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b29e9-115">Request body</span></span>
<span data-ttu-id="b29e9-116">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b29e9-116">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b29e9-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b29e9-117">Response</span></span>

<span data-ttu-id="b29e9-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [plannerBucket](../resources/plannerbucket.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b29e9-118">If successful, this method returns a `200 OK` response code and collection of [plannerBucket](../resources/plannerbucket.md) objects in the response body.</span></span>

<span data-ttu-id="b29e9-p102">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="b29e9-p102">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>
## <a name="example"></a><span data-ttu-id="b29e9-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b29e9-122">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b29e9-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b29e9-123">Request</span></span>
<span data-ttu-id="b29e9-124">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b29e9-124">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_buckets"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/buckets
```
##### <a name="response"></a><span data-ttu-id="b29e9-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b29e9-125">Response</span></span>
<span data-ttu-id="b29e9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b29e9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerBucket",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 251

{
  "value": [
    {
      "@odata.etag": "W/\"JzEtQnVja2V0QEBAQEBAQEBAQEBAQEBARCc=\"",
      "name": "To do",
      "planId": "2txjA-BMZEq-bKi6Wfj5aGQAB1OJ",
      "orderHint": "85752723360752+",
      "id": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List buckets",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->