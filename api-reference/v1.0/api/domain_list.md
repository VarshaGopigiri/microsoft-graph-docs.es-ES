# <a name="list-domains"></a><span data-ttu-id="b2cdf-101">Enumerar dominios</span><span class="sxs-lookup"><span data-stu-id="b2cdf-101">List domains</span></span>

<span data-ttu-id="b2cdf-102">Recupera una lista de objetos de dominio.</span><span class="sxs-lookup"><span data-stu-id="b2cdf-102">Retrieve a list of domain objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="b2cdf-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="b2cdf-103">Permissions</span></span>
<span data-ttu-id="b2cdf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b2cdf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b2cdf-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b2cdf-106">Permission type</span></span>      | <span data-ttu-id="b2cdf-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b2cdf-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b2cdf-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b2cdf-108">Delegated (work or school account)</span></span> | <span data-ttu-id="b2cdf-109">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="b2cdf-109">Directory.Read.All</span></span>    |
|<span data-ttu-id="b2cdf-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b2cdf-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b2cdf-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2cdf-111">Not supported.</span></span>    |
|<span data-ttu-id="b2cdf-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b2cdf-112">Application</span></span> | <span data-ttu-id="b2cdf-113">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b2cdf-113">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b2cdf-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b2cdf-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains
```
## <a name="optional-query-parameters"></a><span data-ttu-id="b2cdf-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b2cdf-115">Optional query parameters</span></span>
<span data-ttu-id="b2cdf-116">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b2cdf-116">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b2cdf-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b2cdf-117">Request headers</span></span>
| <span data-ttu-id="b2cdf-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="b2cdf-118">Name</span></span>      |<span data-ttu-id="b2cdf-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2cdf-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="b2cdf-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="b2cdf-120">Authorization</span></span>  | <span data-ttu-id="b2cdf-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b2cdf-p102">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="b2cdf-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b2cdf-123">Accept</span></span>         | <span data-ttu-id="b2cdf-124">application/json;</span><span class="sxs-lookup"><span data-stu-id="b2cdf-124">application/json;</span></span> |

## <a name="request-body"></a><span data-ttu-id="b2cdf-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b2cdf-125">Request body</span></span>
<span data-ttu-id="b2cdf-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b2cdf-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b2cdf-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2cdf-127">Response</span></span>

<span data-ttu-id="b2cdf-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b2cdf-128">If successful, this method returns a `200 OK` response code and collection of [domain](../resources/domain.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b2cdf-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b2cdf-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b2cdf-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b2cdf-130">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_domains"
}-->
```http
GET https://graph.microsoft.com/v1.0/domains
```
##### <a name="response"></a><span data-ttu-id="b2cdf-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2cdf-131">Response</span></span>
<span data-ttu-id="b2cdf-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b2cdf-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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