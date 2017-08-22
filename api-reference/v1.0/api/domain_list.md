# <a name="list-domains"></a><span data-ttu-id="c17ab-101">Enumerar dominios</span><span class="sxs-lookup"><span data-stu-id="c17ab-101">List domains</span></span>

<span data-ttu-id="c17ab-102">Recuperar una lista de objetos de dominio.</span><span class="sxs-lookup"><span data-stu-id="c17ab-102">Retrieve a list of domain objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c17ab-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c17ab-103">Prerequisites</span></span>
<span data-ttu-id="c17ab-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All* o *Domain.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="c17ab-104">One of the following **scopes** is required to execute this API: *Directory.Read.All* or *Domain.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="c17ab-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c17ab-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c17ab-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c17ab-106">Optional query parameters</span></span>
<span data-ttu-id="c17ab-107">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c17ab-107">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c17ab-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c17ab-108">Request headers</span></span>
| <span data-ttu-id="c17ab-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="c17ab-109">Name</span></span>      |<span data-ttu-id="c17ab-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c17ab-110">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c17ab-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="c17ab-111">Authorization</span></span>  | <span data-ttu-id="c17ab-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c17ab-p101">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="c17ab-114">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c17ab-114">Accept</span></span>         | <span data-ttu-id="c17ab-115">application/json;</span><span class="sxs-lookup"><span data-stu-id="c17ab-115">application/json;</span></span> |

## <a name="request-body"></a><span data-ttu-id="c17ab-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c17ab-116">Request body</span></span>
<span data-ttu-id="c17ab-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c17ab-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c17ab-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c17ab-118">Response</span></span>

<span data-ttu-id="c17ab-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c17ab-119">If successful, this method returns a `200 OK` response code and collection of [domain](../resources/domain.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c17ab-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c17ab-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c17ab-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c17ab-121">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_domains"
}-->
```http
GET https://graph.microsoft.com/V1.0/domains
```
##### <a name="response"></a><span data-ttu-id="c17ab-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c17ab-122">Response</span></span>
<span data-ttu-id="c17ab-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c17ab-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domain",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 245

{
  "value": [
    {
      "authenticationType": "authenticationType-value",
      "availabilityStatus": "availabilityStatus-value",
      "isAdminManaged": true,
      "isDefault": true,
      "isInitial": true,
      "isRoot": true,
      "name": "contoso.com",
      "supportedServices": [
        "Email",
        "OfficeCommunicationsOnline"
      ]
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List domains",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->