# <a name="list-organization"></a><span data-ttu-id="42261-101">List organization</span><span class="sxs-lookup"><span data-stu-id="42261-101">List organization</span></span>

<span data-ttu-id="42261-102">Recupera una lista de objetos organization.</span><span class="sxs-lookup"><span data-stu-id="42261-102">Retrieve a list of organization objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="42261-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="42261-103">Permissions</span></span>
<span data-ttu-id="42261-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="42261-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="42261-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="42261-106">Permission type</span></span>      | <span data-ttu-id="42261-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="42261-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="42261-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="42261-108">Delegated (work or school account)</span></span> | <span data-ttu-id="42261-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="42261-109">Not supported.</span></span>    | 
|<span data-ttu-id="42261-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="42261-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="42261-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="42261-111">Not supported.</span></span>    | 
|<span data-ttu-id="42261-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="42261-112">Application</span></span> | <span data-ttu-id="42261-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="42261-113">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="42261-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="42261-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /organization
```
## <a name="optional-query-parameters"></a><span data-ttu-id="42261-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="42261-115">Optional query parameters</span></span>
<span data-ttu-id="42261-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="42261-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="42261-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="42261-117">Request headers</span></span>
| <span data-ttu-id="42261-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="42261-118">Name</span></span>       | <span data-ttu-id="42261-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="42261-119">Type</span></span> | <span data-ttu-id="42261-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="42261-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="42261-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="42261-121">Authorization</span></span>  | <span data-ttu-id="42261-122">string</span><span class="sxs-lookup"><span data-stu-id="42261-122">string</span></span>  | <span data-ttu-id="42261-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="42261-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="42261-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="42261-125">Request body</span></span>
<span data-ttu-id="42261-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="42261-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="42261-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42261-127">Response</span></span>

<span data-ttu-id="42261-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [organization](../resources/organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="42261-128">If successful, this method returns a `200 OK` response code and collection of [organization](../resources/organization.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="42261-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="42261-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="42261-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="42261-130">Request</span></span>
<span data-ttu-id="42261-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="42261-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_organization"
}-->
```http
GET https://graph.microsoft.com/v1.0/organization
```
##### <a name="response"></a><span data-ttu-id="42261-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42261-132">Response</span></span>
<span data-ttu-id="42261-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="42261-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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