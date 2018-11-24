# <a name="list-organization"></a><span data-ttu-id="9d8cf-101">List organization</span><span class="sxs-lookup"><span data-stu-id="9d8cf-101">List organization</span></span>



<span data-ttu-id="9d8cf-102">Recupera una lista de objetos organization.</span><span class="sxs-lookup"><span data-stu-id="9d8cf-102">Retrieve a list of organization objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="9d8cf-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9d8cf-103">Permissions</span></span>
<span data-ttu-id="9d8cf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9d8cf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9d8cf-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9d8cf-106">Permission type</span></span>      | <span data-ttu-id="9d8cf-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9d8cf-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9d8cf-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9d8cf-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9d8cf-109">User.Read, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9d8cf-109">User.Read, Directory.Read.All, Directory.ReadWrite.All</span></span>   |
|<span data-ttu-id="9d8cf-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9d8cf-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9d8cf-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9d8cf-111">Not supported.</span></span>    |
|<span data-ttu-id="9d8cf-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9d8cf-112">Application</span></span> | <span data-ttu-id="9d8cf-113">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9d8cf-113">Directory.Read.All, Directory.ReadWrite.All</span></span> |

> <span data-ttu-id="9d8cf-114">Nota: Las aplicaciones que tienen el permiso User.Read solamente pueden leer las propiedades *id*, *displayName* y *verifiedDomains* de la organización.</span><span class="sxs-lookup"><span data-stu-id="9d8cf-114">Note: Applications granted the User.Read permission are able to read only the *id*, *displayName*, and *verifiedDomains* properties of the organization.</span></span>  <span data-ttu-id="9d8cf-115">El resto de propiedades devolverá valores `null`.</span><span class="sxs-lookup"><span data-stu-id="9d8cf-115">All other properties will return with `null` values.</span></span> <span data-ttu-id="9d8cf-116">Para leer todas las propiedades, use Directory.Read.All.</span><span class="sxs-lookup"><span data-stu-id="9d8cf-116">To read all properties, use Directory.Read.All.</span></span>

## <a name="http-request"></a><span data-ttu-id="9d8cf-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9d8cf-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /organization
```
## <a name="optional-query-parameters"></a><span data-ttu-id="9d8cf-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9d8cf-118">Optional query parameters</span></span>
<span data-ttu-id="9d8cf-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d8cf-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="9d8cf-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9d8cf-120">Request headers</span></span>
| <span data-ttu-id="9d8cf-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d8cf-121">Name</span></span>       | <span data-ttu-id="9d8cf-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d8cf-122">Type</span></span> | <span data-ttu-id="9d8cf-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d8cf-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9d8cf-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="9d8cf-124">Authorization</span></span>  | <span data-ttu-id="9d8cf-125">string</span><span class="sxs-lookup"><span data-stu-id="9d8cf-125">string</span></span>  | <span data-ttu-id="9d8cf-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9d8cf-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9d8cf-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9d8cf-128">Request body</span></span>
<span data-ttu-id="9d8cf-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9d8cf-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9d8cf-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d8cf-130">Response</span></span>

<span data-ttu-id="9d8cf-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [organization](../resources/organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d8cf-131">If successful, this method returns a `200 OK` response code and collection of [organization](../resources/organization.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9d8cf-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9d8cf-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9d8cf-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9d8cf-133">Request</span></span>
<span data-ttu-id="9d8cf-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9d8cf-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_organization"
}-->
```http
GET https://graph.microsoft.com/beta/organization
```
##### <a name="response"></a><span data-ttu-id="9d8cf-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d8cf-135">Response</span></span>
<span data-ttu-id="9d8cf-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9d8cf-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organization",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 500

{
  "value": [
    {
      "assignedPlans": [
        {
          "assignedDateTime": "2016-10-19T10:37:00Z",
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List organization",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->