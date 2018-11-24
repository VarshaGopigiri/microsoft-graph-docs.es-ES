# <a name="list-serviceconfigurationrecords"></a><span data-ttu-id="35f43-101">Enumerar serviceConfigurationRecords</span><span class="sxs-lookup"><span data-stu-id="35f43-101">List serviceConfigurationRecords</span></span>

<span data-ttu-id="35f43-102">Recupera una lista de los objetos [domainDnsRecord](../resources/domaindnsrecord.md) necesarios para habilitar los servicios para el dominio.</span><span class="sxs-lookup"><span data-stu-id="35f43-102">Retrieves a list of [domainDnsRecord](../resources/domaindnsrecord.md) objects needed to enable services for the domain.</span></span>

<span data-ttu-id="35f43-p101">Utilice la lista devuelta para agregar registros en el archivo de zona del dominio. Esto puede hacerse a través del registrador de dominios o de la configuración del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="35f43-p101">Use the returned list to add records to the zone file of the domain. This can be done through the domain registrar or DNS server configuration.</span></span>

## <a name="permissions"></a><span data-ttu-id="35f43-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="35f43-105">Permissions</span></span>

<span data-ttu-id="35f43-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="35f43-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="35f43-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="35f43-108">Permission type</span></span>      | <span data-ttu-id="35f43-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="35f43-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="35f43-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="35f43-110">Delegated (work or school account)</span></span> | <span data-ttu-id="35f43-111">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="35f43-111">Directory.Read.All</span></span>    |
|<span data-ttu-id="35f43-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="35f43-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="35f43-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="35f43-113">Not supported.</span></span>    |
|<span data-ttu-id="35f43-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="35f43-114">Application</span></span> | <span data-ttu-id="35f43-115">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="35f43-115">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="35f43-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="35f43-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/contoso.com/serviceConfigurationRecords
```

## <a name="optional-query-parameters"></a><span data-ttu-id="35f43-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="35f43-117">Optional query parameters</span></span>

<span data-ttu-id="35f43-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35f43-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="35f43-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="35f43-119">Request headers</span></span>

| <span data-ttu-id="35f43-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="35f43-120">Name</span></span>      |<span data-ttu-id="35f43-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="35f43-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="35f43-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="35f43-122">Authorization</span></span>  | <span data-ttu-id="35f43-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="35f43-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="35f43-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="35f43-125">Content-Type</span></span>  | <span data-ttu-id="35f43-126">application/json</span><span class="sxs-lookup"><span data-stu-id="35f43-126">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="35f43-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="35f43-127">Request body</span></span>

<span data-ttu-id="35f43-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="35f43-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="35f43-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35f43-129">Response</span></span>

<span data-ttu-id="35f43-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [domainDnsRecord](../resources/domaindnsrecord.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35f43-130">If successful, this method returns a `200 OK` response code and collection of [domainDnsRecord](../resources/domaindnsrecord.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="35f43-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35f43-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="35f43-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="35f43-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_serviceconfigurationrecords"
}-->
```http
GET https://graph.microsoft.com/v1.0/domains/{domain-name}/serviceConfigurationRecords
```
##### <a name="response"></a><span data-ttu-id="35f43-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35f43-133">Response</span></span>
<span data-ttu-id="35f43-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="35f43-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "@odata.type":"microsoft.graph.domainDnsMxRecord",
      "isOptional": false,
      "label": "contoso.com",
      "recordType": "Mx",
      "supportedService": "Email",
      "ttl": 3600,
      "mailExchange": "contoso-com.mail.protection.outlook.com",
      "preference": 0
    },
    {
      "@odata.type":"microsoft.graph.domainDnsTxtRecord",
      "isOptional": false,
      "label": "contoso.com",
      "recordType": "Txt",
      "supportedService": "Email",
      "ttl": 3600,
      "text": "v=spf1 include: spf.protection.outlook.com ~all"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List serviceConfigurationRecords",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->