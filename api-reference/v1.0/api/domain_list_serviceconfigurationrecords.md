# <a name="list-serviceconfigurationrecords"></a><span data-ttu-id="68740-101">Enumerar serviceConfigurationRecords</span><span class="sxs-lookup"><span data-stu-id="68740-101">List serviceConfigurationRecords</span></span>

<span data-ttu-id="68740-102">Recupera una lista de los objetos [domainDnsRecord](../resources/domaindnsrecord.md) necesarios para habilitar los servicios para el dominio.</span><span class="sxs-lookup"><span data-stu-id="68740-102">Retrieves a list of [domainDnsRecord](../resources/domaindnsrecord.md) objects needed to enable services for the domain.</span></span>

<span data-ttu-id="68740-p101">Utilice la lista devuelta para agregar registros en el archivo de zona del dominio. Esto puede hacerse a través del registrador de dominios o de la configuración del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="68740-p101">Use the returned list to add records to the zone file of the domain. This can be done through the domain registrar or DNS server configuration.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="68740-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="68740-105">Prerequisites</span></span>

<span data-ttu-id="68740-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All* o *Domain.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="68740-106">One of the following **scopes** is required to execute this API: *Directory.Read.All* or *Domain.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="68740-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="68740-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/contoso.com/serviceConfigurationRecords
```

## <a name="optional-query-parameters"></a><span data-ttu-id="68740-108">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="68740-108">Optional query parameters</span></span>

<span data-ttu-id="68740-109">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68740-109">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="68740-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68740-110">Request headers</span></span>

| <span data-ttu-id="68740-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="68740-111">Name</span></span>      |<span data-ttu-id="68740-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="68740-112">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="68740-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="68740-113">Authorization</span></span>  | <span data-ttu-id="68740-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="68740-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="68740-116">Content-Type</span><span class="sxs-lookup"><span data-stu-id="68740-116">Content-Type</span></span>  | <span data-ttu-id="68740-117">application/json</span><span class="sxs-lookup"><span data-stu-id="68740-117">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="68740-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="68740-118">Request body</span></span>

<span data-ttu-id="68740-119">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="68740-119">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="68740-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68740-120">Response</span></span>

<span data-ttu-id="68740-121">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [domainDnsRecord](../resources/domaindnsrecord.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68740-121">If successful, this method returns a `200 OK` response code and collection of [domainDnsRecord](../resources/domaindnsrecord.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="68740-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68740-122">Example</span></span>
##### <a name="request"></a><span data-ttu-id="68740-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="68740-123">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_serviceconfigurationrecords"
}-->
```http
GET https://graph.microsoft.com/V1.0/domains/contoso.com/serviceConfigurationRecords
```
##### <a name="response"></a><span data-ttu-id="68740-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68740-124">Response</span></span>
<span data-ttu-id="68740-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="68740-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "mailExchange": "contoso-com.mail.protection.outlook.com",
      "preference": 0
    },
    {
      "isOptional": false,
      "label": "contoso.com",
      "recordType": "Txt",
      "supportedServices": "Email",
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