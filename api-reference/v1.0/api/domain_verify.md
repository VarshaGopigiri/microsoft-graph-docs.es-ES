# <a name="domain-verify"></a><span data-ttu-id="74935-101">dominio: verify</span><span class="sxs-lookup"><span data-stu-id="74935-101">domain: verify</span></span>

<span data-ttu-id="74935-102">Valida la propiedad del dominio.</span><span class="sxs-lookup"><span data-stu-id="74935-102">Validates the ownership of the domain.</span></span>

> <span data-ttu-id="74935-p101">**Importante:** Solo se aplica a un dominio sin verificar. En el caso de un dominio sin verificar, la propiedad isVerified del [dominio](../resources/domain.md) es falsa.</span><span class="sxs-lookup"><span data-stu-id="74935-p101">**Important:** Only applies to an unverified domain. For an unverified domain, the isVerified property of the [domain](../resources/domain.md) is false.</span></span>

## <a name="permissions"></a><span data-ttu-id="74935-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="74935-105">Permissions</span></span>

<span data-ttu-id="74935-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="74935-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="74935-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="74935-108">Permission type</span></span>      | <span data-ttu-id="74935-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="74935-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="74935-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="74935-110">Delegated (work or school account)</span></span> | <span data-ttu-id="74935-111">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="74935-111">Directory.Read.All</span></span>    |
|<span data-ttu-id="74935-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="74935-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="74935-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74935-113">Not supported.</span></span>    |
|<span data-ttu-id="74935-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="74935-114">Application</span></span> | <span data-ttu-id="74935-115">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="74935-115">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="74935-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74935-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /domains/{id}/verify
```

> <span data-ttu-id="74935-117">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="74935-117">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="74935-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74935-118">Request headers</span></span>

| <span data-ttu-id="74935-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="74935-119">Name</span></span>       | <span data-ttu-id="74935-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="74935-120">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="74935-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="74935-121">Authorization</span></span>  | <span data-ttu-id="74935-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="74935-p103">Bearer {token}. Required.</span></span>|
| <span data-ttu-id="74935-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="74935-124">Content-Type</span></span>  | <span data-ttu-id="74935-125">application/json</span><span class="sxs-lookup"><span data-stu-id="74935-125">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="74935-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="74935-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="74935-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74935-127">Response</span></span>

<span data-ttu-id="74935-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200, OK` y el objeto [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74935-128">If successful, this method returns `200, OK` response code and [domain](../resources/domain.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="74935-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74935-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="74935-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="74935-130">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "domain_verify"
}-->
```http
POST https://graph.microsoft.com/V1.0/domains/contoso.com/verify
```

##### <a name="response"></a><span data-ttu-id="74935-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74935-131">Response</span></span>
<span data-ttu-id="74935-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="74935-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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