# <a name="get-organization"></a><span data-ttu-id="67413-101">Get organization</span><span class="sxs-lookup"><span data-stu-id="67413-101">Get organization</span></span>

<span data-ttu-id="67413-102">Recupera las propiedades y relaciones de la organización actualmente autenticada.</span><span class="sxs-lookup"><span data-stu-id="67413-102">Retrieve the properties and relationships of currently authenticated organization.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="67413-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="67413-103">Prerequisites</span></span>
<span data-ttu-id="67413-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="67413-104">One of the following **scopes** is required to execute this API:</span></span> 
## <a name="http-request"></a><span data-ttu-id="67413-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="67413-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /organization

```
## <a name="optional-query-parameters"></a><span data-ttu-id="67413-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="67413-106">Optional query parameters</span></span>
<span data-ttu-id="67413-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="67413-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="67413-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="67413-108">Request headers</span></span>
| <span data-ttu-id="67413-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="67413-109">Name</span></span>       | <span data-ttu-id="67413-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="67413-110">Type</span></span> | <span data-ttu-id="67413-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="67413-111">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="67413-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="67413-112">Authorization</span></span>  | <span data-ttu-id="67413-113">string</span><span class="sxs-lookup"><span data-stu-id="67413-113">string</span></span>  | <span data-ttu-id="67413-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="67413-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="67413-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="67413-116">Request body</span></span>
<span data-ttu-id="67413-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="67413-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="67413-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67413-118">Response</span></span>

<span data-ttu-id="67413-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [organization](../resources/organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="67413-119">If successful, this method returns a `200 OK` response code and [organization](../resources/organization.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="67413-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="67413-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="67413-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="67413-121">Request</span></span>
<span data-ttu-id="67413-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="67413-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_organization"
}-->
```http
GET https://graph.microsoft.com/v1.0/organization
```
##### <a name="response"></a><span data-ttu-id="67413-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67413-123">Response</span></span>
<span data-ttu-id="67413-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="67413-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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