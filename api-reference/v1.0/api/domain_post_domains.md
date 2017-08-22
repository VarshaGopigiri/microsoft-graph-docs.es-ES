# <a name="create-domain"></a><span data-ttu-id="1096f-101">Crear dominio</span><span class="sxs-lookup"><span data-stu-id="1096f-101">Create domain</span></span>

<span data-ttu-id="1096f-102">Agregue un dominio al inquilino.</span><span class="sxs-lookup"><span data-stu-id="1096f-102">Adds a domain to the tenant.</span></span>

<span data-ttu-id="1096f-p101">**Importante**: No puede utilizar un dominio asociado con su inquilino de Azure AD hasta que se verifique la propiedad. Consulte [Enumerar verificationDnsRecords](domain_list_verificationdnsrecords.md) para obtener más información. Los dominios raíz requieren comprobación. Por ejemplo, contoso.com requiere comprobación. Si se comprueba un dominio raíz, los subdominios de este también se comprueban de forma automática. Por ejemplo, subdominio.contoso.com se comprueba de forma automática si se ha comprobado contoso.com.</span><span class="sxs-lookup"><span data-stu-id="1096f-p101">**Important**: You cannot use an associated domain with your Azure AD tenant until ownership is verified. See [List verificationDnsRecords](domain_list_verificationdnsrecords.md) for details. Root domains require verification. For example, contoso.com requires verification. If a root domain is verified, subdomains of the root domain are automatically verified. For example, subdomain.contoso.com is automatically be verified if contoso.com has been verified.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1096f-109">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1096f-109">Prerequisites</span></span>

<span data-ttu-id="1096f-110">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Domain.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="1096f-110">One of the following **scopes** is required to execute this API: *Domain.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="1096f-111">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1096f-111">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /domains
```
## <a name="request-headers"></a><span data-ttu-id="1096f-112">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1096f-112">Request headers</span></span>
| <span data-ttu-id="1096f-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="1096f-113">Name</span></span>       | <span data-ttu-id="1096f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1096f-114">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1096f-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="1096f-115">Authorization</span></span>  | <span data-ttu-id="1096f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1096f-p102">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="1096f-118">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1096f-118">Content-Type</span></span>  | <span data-ttu-id="1096f-119">application/json</span><span class="sxs-lookup"><span data-stu-id="1096f-119">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="1096f-120">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1096f-120">Request body</span></span>
<span data-ttu-id="1096f-121">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [domain](../resources/domain.md).</span><span class="sxs-lookup"><span data-stu-id="1096f-121">In the request body, supply a JSON representation of [domain](../resources/domain.md) object.</span></span>

> <span data-ttu-id="1096f-p103">El cuerpo de la solicitud contiene la propiedad de id. del dominio nuevo. Id. es la única propiedad que se puede especificar y que es necesaria. El valor de la propiedad de id. es el nombre de dominio completo que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="1096f-p103">The request body contains the id property for the new domain. Id is the only property that can be specified and it is required. The id property value is the fully qualified domain name to create.</span></span>

## <a name="response"></a><span data-ttu-id="1096f-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1096f-125">Response</span></span>

<span data-ttu-id="1096f-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1096f-126">If successful, this method returns `201, Created` response code and [domain](../resources/domain.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1096f-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1096f-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1096f-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1096f-128">Request</span></span>

<span data-ttu-id="1096f-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [domain](../resources/domain.md).</span><span class="sxs-lookup"><span data-stu-id="1096f-129">In the request body, supply a JSON representation of [domain](../resources/domain.md) object.</span></span>

<!-- {
  "blockType": "request",
  "id": "create_domain_from_domains"
}-->
```http
POST https://graph.microsoft.com/V1.0/domains
Content-type: application/json
Content-length: 192

{
  "id": "contoso.com"
}
```

##### <a name="response"></a><span data-ttu-id="1096f-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1096f-130">Response</span></span>
<span data-ttu-id="1096f-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1096f-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domain"
} -->
```http
HTTP/1.1 201 Created
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
  "description": "Create domain",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->