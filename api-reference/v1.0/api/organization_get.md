# <a name="get-organization"></a><span data-ttu-id="5c24d-101">Get organization</span><span class="sxs-lookup"><span data-stu-id="5c24d-101">Get organization</span></span>

<span data-ttu-id="5c24d-102">Recupera las propiedades y relaciones de la organización actualmente autenticada.</span><span class="sxs-lookup"><span data-stu-id="5c24d-102">Retrieve the properties and relationships of currently authenticated organization.</span></span>
## <a name="permissions"></a><span data-ttu-id="5c24d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="5c24d-103">Permissions</span></span>
<span data-ttu-id="5c24d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5c24d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5c24d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5c24d-106">Permission type</span></span>      | <span data-ttu-id="5c24d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5c24d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5c24d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5c24d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="5c24d-109">User.Read, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5c24d-109">User.Read, Directory.Read.All, Directory.ReadWrite.All</span></span>   |
|<span data-ttu-id="5c24d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5c24d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5c24d-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5c24d-111">Not supported.</span></span>    |
|<span data-ttu-id="5c24d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5c24d-112">Application</span></span> | <span data-ttu-id="5c24d-113">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5c24d-113">Directory.Read.All, Directory.ReadWrite.All</span></span> |

> <span data-ttu-id="5c24d-114">Nota: Las aplicaciones que tienen el permiso User.Read solamente pueden leer las propiedades *id*, *displayName* y *verifiedDomains* de la organización.</span><span class="sxs-lookup"><span data-stu-id="5c24d-114">Note: Applications granted the User.Read permission are able to read only the *id*, *displayName*, and *verifiedDomains* properties of the organization.</span></span>  <span data-ttu-id="5c24d-115">El resto de propiedades devolverá valores `null`.</span><span class="sxs-lookup"><span data-stu-id="5c24d-115">All other properties will return with `null` values.</span></span> <span data-ttu-id="5c24d-116">Para leer todas las propiedades, use Directory.Read.All.</span><span class="sxs-lookup"><span data-stu-id="5c24d-116">To read all properties, use Directory.Read.All.</span></span>

## <a name="http-request"></a><span data-ttu-id="5c24d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5c24d-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /organization

```
## <a name="optional-query-parameters"></a><span data-ttu-id="5c24d-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5c24d-118">Optional query parameters</span></span>
<span data-ttu-id="5c24d-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c24d-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="5c24d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5c24d-120">Request headers</span></span>
| <span data-ttu-id="5c24d-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="5c24d-121">Name</span></span>       | <span data-ttu-id="5c24d-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c24d-122">Type</span></span> | <span data-ttu-id="5c24d-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c24d-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="5c24d-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="5c24d-124">Authorization</span></span>  | <span data-ttu-id="5c24d-125">string</span><span class="sxs-lookup"><span data-stu-id="5c24d-125">string</span></span>  | <span data-ttu-id="5c24d-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5c24d-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5c24d-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5c24d-128">Request body</span></span>
<span data-ttu-id="5c24d-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5c24d-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5c24d-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c24d-130">Response</span></span>

<span data-ttu-id="5c24d-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [organization](../resources/organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c24d-131">If successful, this method returns a `200 OK` response code and [organization](../resources/organization.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="5c24d-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5c24d-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5c24d-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5c24d-133">Request</span></span>
<span data-ttu-id="5c24d-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c24d-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_organization"
}-->
```http
GET https://graph.microsoft.com/v1.0/organization
```
##### <a name="response"></a><span data-ttu-id="5c24d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c24d-135">Response</span></span>
<span data-ttu-id="5c24d-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5c24d-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organization"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 411

{
  "assignedPlans": [
    {
      "assignedDateTime": "datetime-value",
      "capabilityStatus": "capabilityStatus-value",
      "service": "service-value",
      "servicePlanId": "servicePlanId-value"
    }
  ],
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value",
  "country": "country-value",
  "countryLetterCode": "countryLetterCode-value",
  "displayName": "displayName-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get organization",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->