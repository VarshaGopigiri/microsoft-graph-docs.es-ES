# <a name="get-domain"></a><span data-ttu-id="71611-101">Obtener dominio</span><span class="sxs-lookup"><span data-stu-id="71611-101">Get domain</span></span>

<span data-ttu-id="71611-102">Recupere las propiedades y las relaciones del objeto domain.</span><span class="sxs-lookup"><span data-stu-id="71611-102">Retrieve the properties and relationships of domain object.</span></span>

## <a name="permissions"></a><span data-ttu-id="71611-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="71611-103">Permissions</span></span>

<span data-ttu-id="71611-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="71611-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="71611-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71611-106">Permission type</span></span>      | <span data-ttu-id="71611-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71611-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="71611-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71611-108">Delegated (work or school account)</span></span> | <span data-ttu-id="71611-109">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="71611-109">Directory.Read.All</span></span>    |
|<span data-ttu-id="71611-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71611-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="71611-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71611-111">Not supported.</span></span>    |
|<span data-ttu-id="71611-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71611-112">Application</span></span> | <span data-ttu-id="71611-113">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="71611-113">Directory.Read.All, Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="71611-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71611-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}
```

> <span data-ttu-id="71611-115">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="71611-115">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="71611-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="71611-116">Optional query parameters</span></span>

<span data-ttu-id="71611-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71611-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="71611-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71611-118">Request headers</span></span>

| <span data-ttu-id="71611-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="71611-119">Name</span></span>      |<span data-ttu-id="71611-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="71611-120">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="71611-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="71611-121">Authorization</span></span>  | <span data-ttu-id="71611-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="71611-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="71611-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="71611-124">Content-Type</span></span>  | <span data-ttu-id="71611-125">application/json</span><span class="sxs-lookup"><span data-stu-id="71611-125">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="71611-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71611-126">Request body</span></span>
<span data-ttu-id="71611-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="71611-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="71611-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71611-128">Response</span></span>

<span data-ttu-id="71611-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [domain](../resources/domain.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71611-129">If successful, this method returns a `200 OK` response code and [domain](../resources/domain.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="71611-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71611-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="71611-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71611-131">Request</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["contoso.com"],
  "name": "get_domain"
}-->
```http
GET https://graph.microsoft.com/v1.0/domains/contoso.com
```
##### <a name="response"></a><span data-ttu-id="71611-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71611-132">Response</span></span>
<span data-ttu-id="71611-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71611-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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