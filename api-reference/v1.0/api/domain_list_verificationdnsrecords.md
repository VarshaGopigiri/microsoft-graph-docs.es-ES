# <a name="list-verificationdnsrecords"></a><span data-ttu-id="5e244-101">Enumerar verificationDnsRecords</span><span class="sxs-lookup"><span data-stu-id="5e244-101">List verificationDnsRecords</span></span>

<span data-ttu-id="5e244-102">Recupere una lista de objetos [domainDnsRecord](../resources/domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="5e244-102">Retrieve a list of [domainDnsRecord](../resources/domaindnsrecord.md) objects.</span></span>

<span data-ttu-id="5e244-p101">No puede utilizar un dominio asociado con su inquilino de Azure AD hasta que se verifique la propiedad. Para comprobar la propiedad del dominio, recupere los registros de comprobación del dominio y agregue los detalles al archivo de zona del dominio. Esto puede hacerse a través del registrador de dominios o de la configuración del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="5e244-p101">You cannot use an associated domain with your Azure AD tenant until ownership is verified. To verify the ownership of the domain, retrieve the domain verification records and add the details to the zone file of the domain. This can be done through the domain registrar or DNS server configuration.</span></span>

<span data-ttu-id="5e244-p102">Los dominios raíz requieren comprobación. Por ejemplo, contoso.com requiere comprobación. Si se comprueba un dominio raíz, los subdominios de este también se comprueban de forma automática. Por ejemplo, subdominio.contoso.com se comprueba de forma automática si se ha comprobado contoso.com.</span><span class="sxs-lookup"><span data-stu-id="5e244-p102">Root domains require verification. For example, contoso.com requires verification. If a root domain is verified, subdomains of the root domain are automatically verified. For example, subdomain.contoso.com is automatically be verified if contoso.com has been verified.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5e244-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5e244-110">Prerequisites</span></span>

<span data-ttu-id="5e244-111">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All* o *Domain.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="5e244-111">One of the following **scopes** is required to execute this API: *Directory.Read.All* or *Domain.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="5e244-112">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5e244-112">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}/verificationDnsRecords
```

> <span data-ttu-id="5e244-113">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="5e244-113">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="5e244-114">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5e244-114">Optional query parameters</span></span>

<span data-ttu-id="5e244-115">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e244-115">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5e244-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5e244-116">Request headers</span></span>

| <span data-ttu-id="5e244-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="5e244-117">Name</span></span>      |<span data-ttu-id="5e244-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e244-118">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="5e244-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="5e244-119">Authorization</span></span>  | <span data-ttu-id="5e244-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e244-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5e244-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5e244-122">Content-Type</span></span>  | <span data-ttu-id="5e244-123">application/json</span><span class="sxs-lookup"><span data-stu-id="5e244-123">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="5e244-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5e244-124">Request body</span></span>

<span data-ttu-id="5e244-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5e244-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5e244-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e244-126">Response</span></span>

<span data-ttu-id="5e244-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [domainDnsRecord](../resources/domaindnsrecord.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e244-127">If successful, this method returns a `200 OK` response code and collection of [domainDnsRecord](../resources/domaindnsrecord.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5e244-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e244-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5e244-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5e244-129">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_verificationdnsrecords"
}-->
```http
GET https://graph.microsoft.com/V1.0/domains/contoso.com/verificationDnsRecords
```

##### <a name="response"></a><span data-ttu-id="5e244-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e244-130">Response</span></span>

<span data-ttu-id="5e244-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5e244-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domainDnsRecord",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 220

{
  "value": [
    {
      "isOptional": false,
      "label": "contoso.com",
      "recordType": "Mx",
      "supportedService": "Email",
      "ttl": 3600,
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List verificationDnsRecords",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->