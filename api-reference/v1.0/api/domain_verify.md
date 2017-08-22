# <a name="domain-verify"></a><span data-ttu-id="f772a-101">dominio: verify</span><span class="sxs-lookup"><span data-stu-id="f772a-101">domain: verify</span></span>

<span data-ttu-id="f772a-102">Valide la propiedad del dominio.</span><span class="sxs-lookup"><span data-stu-id="f772a-102">Validates the ownership of the domain.</span></span>

> <span data-ttu-id="f772a-p101">**Importante:** Solo se aplica a un dominio sin verificar. En el caso de un dominio sin verificar, la propiedad isVerified del [dominio](../resources/domain.md) es falsa.</span><span class="sxs-lookup"><span data-stu-id="f772a-p101">**Important:** Only applies to an unverified domain. For an unverified domain, the isVerified property of the [domain](../resources/domain.md) is false.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f772a-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f772a-105">Prerequisites</span></span>

<span data-ttu-id="f772a-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All* o *Domain.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="f772a-106">One of the following **scopes** is required to execute this API: *Directory.Read.All* or *Domain.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="f772a-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f772a-107">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /domains/{id}/verify
```

> <span data-ttu-id="f772a-108">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="f772a-108">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f772a-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f772a-109">Request headers</span></span>

| <span data-ttu-id="f772a-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="f772a-110">Name</span></span>       | <span data-ttu-id="f772a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f772a-111">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f772a-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="f772a-112">Authorization</span></span>  | <span data-ttu-id="f772a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f772a-p102">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="f772a-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f772a-115">Content-Type</span></span>  | <span data-ttu-id="f772a-116">application/json</span><span class="sxs-lookup"><span data-stu-id="f772a-116">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="f772a-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f772a-117">Request body</span></span>

## <a name="response"></a><span data-ttu-id="f772a-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f772a-118">Response</span></span>

<span data-ttu-id="f772a-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200, OK` y el objeto [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f772a-119">If successful, this method returns `200, OK` response code and [domain](../resources/domain.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f772a-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f772a-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f772a-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f772a-121">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "domain_verify"
}-->
```http
POST https://graph.microsoft.com/V1.0/domains/contoso.com/verify
```

##### <a name="response"></a><span data-ttu-id="f772a-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f772a-122">Response</span></span>
<span data-ttu-id="f772a-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f772a-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "isAdminManaged": true,
  "isDefault": true,
  "isInitial": true,
  "isRoot": true,
  "name": "contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domain: verify",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->