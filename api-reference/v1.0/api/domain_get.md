# <a name="get-domain"></a><span data-ttu-id="1f71f-101">Obtener dominio</span><span class="sxs-lookup"><span data-stu-id="1f71f-101">Get domain</span></span>

<span data-ttu-id="1f71f-102">Recupere las propiedades y las relaciones del objeto domain.</span><span class="sxs-lookup"><span data-stu-id="1f71f-102">Retrieve the properties and relationships of domain object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1f71f-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1f71f-103">Prerequisites</span></span>

<span data-ttu-id="1f71f-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All* o *Domain.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="1f71f-104">One of the following **scopes** is required to execute this API: *Directory.Read.All* or *Domain.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="1f71f-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1f71f-105">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}
```

> <span data-ttu-id="1f71f-106">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="1f71f-106">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="1f71f-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1f71f-107">Optional query parameters</span></span>

<span data-ttu-id="1f71f-108">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1f71f-108">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1f71f-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1f71f-109">Request headers</span></span>

| <span data-ttu-id="1f71f-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f71f-110">Name</span></span>      |<span data-ttu-id="1f71f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f71f-111">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="1f71f-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="1f71f-112">Authorization</span></span>  | <span data-ttu-id="1f71f-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1f71f-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1f71f-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1f71f-115">Content-Type</span></span>  | <span data-ttu-id="1f71f-116">application/json</span><span class="sxs-lookup"><span data-stu-id="1f71f-116">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="1f71f-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1f71f-117">Request body</span></span>
<span data-ttu-id="1f71f-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1f71f-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1f71f-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f71f-119">Response</span></span>

<span data-ttu-id="1f71f-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1f71f-120">If successful, this method returns a `200 OK` response code and [domain](../resources/domain.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1f71f-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1f71f-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1f71f-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1f71f-122">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_domain"
}-->
```http
GET https://graph.microsoft.com/V1.0/domains/contoso.com
```
##### <a name="response"></a><span data-ttu-id="1f71f-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f71f-123">Response</span></span>
<span data-ttu-id="1f71f-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1f71f-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domain"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 192

{
  "authenticationType": "authenticationType-value",
  "availabilityStatus": "availabilityStatus-value",
  "id": "contoso.com",
  "isAdminManaged": true,
  "isDefault": true,
  "isInitial": true,
  "isRoot": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get domain",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->