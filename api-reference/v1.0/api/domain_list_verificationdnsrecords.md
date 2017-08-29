# <a name="list-verificationdnsrecords"></a><span data-ttu-id="a6c89-101">Enumerar verificationDnsRecords</span><span class="sxs-lookup"><span data-stu-id="a6c89-101">List verificationDnsRecords</span></span>

<span data-ttu-id="a6c89-102">Recupere una lista de objetos [domainDnsRecord](../resources/domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="a6c89-102">Retrieve a list of [domainDnsRecord](../resources/domaindnsrecord.md) objects.</span></span>

<span data-ttu-id="a6c89-p101">No puede utilizar un dominio asociado con su inquilino de Azure AD hasta que se verifique la propiedad. Para comprobar la propiedad del dominio, recupere los registros de comprobación del dominio y agregue los detalles al archivo de zona del dominio. Esto puede hacerse a través del registrador de dominios o de la configuración del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="a6c89-p101">You cannot use an associated domain with your Azure AD tenant until ownership is verified. To verify the ownership of the domain, retrieve the domain verification records and add the details to the zone file of the domain. This can be done through the domain registrar or DNS server configuration.</span></span>

<span data-ttu-id="a6c89-p102">Los dominios raíz requieren comprobación. Por ejemplo, contoso.com requiere comprobación. Si se comprueba un dominio raíz, los subdominios de este también se comprueban de forma automática. Por ejemplo, subdominio.contoso.com se comprueba de forma automática si se ha comprobado contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a6c89-p102">Root domains require verification. For example, contoso.com requires verification. If a root domain is verified, subdomains of the root domain are automatically verified. For example, subdomain.contoso.com is automatically be verified if contoso.com has been verified.</span></span>

## <a name="permissions"></a><span data-ttu-id="a6c89-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="a6c89-110">Permissions</span></span>

<span data-ttu-id="a6c89-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a6c89-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="a6c89-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a6c89-113">Permission type</span></span>      | <span data-ttu-id="a6c89-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a6c89-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a6c89-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a6c89-115">Delegated (work or school account)</span></span> | <span data-ttu-id="a6c89-116">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="a6c89-116">Directory.Read.All</span></span>    |
|<span data-ttu-id="a6c89-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a6c89-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a6c89-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a6c89-118">Not supported.</span></span>    |
|<span data-ttu-id="a6c89-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a6c89-119">Application</span></span> | <span data-ttu-id="a6c89-120">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a6c89-120">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a6c89-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a6c89-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}/verificationDnsRecords
```

> <span data-ttu-id="a6c89-122">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="a6c89-122">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="a6c89-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a6c89-123">Optional query parameters</span></span>

<span data-ttu-id="a6c89-124">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6c89-124">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a6c89-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a6c89-125">Request headers</span></span>

| <span data-ttu-id="a6c89-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="a6c89-126">Name</span></span>      |<span data-ttu-id="a6c89-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6c89-127">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a6c89-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="a6c89-128">Authorization</span></span>  | <span data-ttu-id="a6c89-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a6c89-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a6c89-131">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a6c89-131">Content-Type</span></span>  | <span data-ttu-id="a6c89-132">application/json</span><span class="sxs-lookup"><span data-stu-id="a6c89-132">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="a6c89-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a6c89-133">Request body</span></span>

<span data-ttu-id="a6c89-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a6c89-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a6c89-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6c89-135">Response</span></span>

<span data-ttu-id="a6c89-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [domainDnsRecord](../resources/domaindnsrecord.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6c89-136">If successful, this method returns a `200 OK` response code and collection of [domainDnsRecord](../resources/domaindnsrecord.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a6c89-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6c89-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a6c89-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a6c89-138">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_verificationdnsrecords"
}-->
```http
GET https://graph.microsoft.com/V1.0/domains/contoso.com/verificationDnsRecords
```

##### <a name="response"></a><span data-ttu-id="a6c89-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6c89-139">Response</span></span>

<span data-ttu-id="a6c89-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a6c89-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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