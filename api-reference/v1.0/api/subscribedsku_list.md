# <a name="list-subscribedskus"></a><span data-ttu-id="7056b-101">Enumerar subscribedSkus</span><span class="sxs-lookup"><span data-stu-id="7056b-101">List subscribedSkus</span></span>
<span data-ttu-id="7056b-102">Recupere la lista de suscripciones comerciales que ha adquirido una organización.</span><span class="sxs-lookup"><span data-stu-id="7056b-102">Retrieve the list of commercial subscriptions that an organization has acquired.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7056b-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7056b-103">Prerequisites</span></span>
<span data-ttu-id="7056b-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="7056b-104">One of the following **scopes** is required to execute this API: *Directory.Read.All*, *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="7056b-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7056b-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /subscribedSkus
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7056b-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7056b-106">Optional query parameters</span></span>
<span data-ttu-id="7056b-107">Este método **no** es compatible con los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="7056b-107">This method does **not** support the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="7056b-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7056b-108">Request headers</span></span>
| <span data-ttu-id="7056b-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="7056b-109">Name</span></span>       | <span data-ttu-id="7056b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="7056b-110">Type</span></span> | <span data-ttu-id="7056b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7056b-111">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="7056b-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="7056b-112">Authorization</span></span>  | <span data-ttu-id="7056b-113">string</span><span class="sxs-lookup"><span data-stu-id="7056b-113">string</span></span>  | <span data-ttu-id="7056b-p101">&lt;token&gt; de portador. *Obligatorio*</span><span class="sxs-lookup"><span data-stu-id="7056b-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7056b-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7056b-116">Request body</span></span>
<span data-ttu-id="7056b-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7056b-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7056b-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7056b-118">Response</span></span>

<span data-ttu-id="7056b-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [subscribedSku](../resources/subscribedsku.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7056b-119">If successful, this method returns a `200 OK` response code and collection of [subscribedSku](../resources/subscribedsku.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7056b-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7056b-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7056b-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7056b-121">Request</span></span>
<span data-ttu-id="7056b-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7056b-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscribedskus"
}-->
```http
GET https://graph.microsoft.com/v1.0/subscribedSkus
```
##### <a name="response"></a><span data-ttu-id="7056b-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7056b-123">Response</span></span>
<span data-ttu-id="7056b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7056b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.subscribedSku",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#subscribedSkus",
    "value": [
        {
            "capabilityStatus": "Enabled",
            "consumedUnits": 14,
            "id": "48a80680-7326-48cd-9935-b556b81d3a4e_c7df2760-2c81-4ef7-b578-5b5392b571df",
            "prepaidUnits": {
                "enabled": 25,
                "suspended": 0,
                "warning": 0
            },
            "servicePlans": [
                {
                    "servicePlanId": "8c098270-9dd4-4350-9b30-ba4703f3b36b",
                    "servicePlanName": "ADALLOM_S_O365",
                    "provisioningStatus": "Success",
                    "appliesTo": "User"
                }
            ],
            "skuId": "c7df2760-2c81-4ef7-b578-5b5392b571df",
            "skuPartNumber": "ENTERPRISEPREMIUM",
            "appliesTo": "User"
        },
        {
            "capabilityStatus": "Suspended",
            "consumedUnits": 14,
            "id": "48a80680-7326-48cd-9935-b556b81d3a4e_d17b27af-3f49-4822-99f9-56a661538792",
            "prepaidUnits": {
                "enabled": 0,
                "suspended": 25,
                "warning": 0
            },
            "servicePlans": [
                {
                    "servicePlanId": "f9646fb2-e3b2-4309-95de-dc4833737456",
                    "servicePlanName": "CRMSTANDARD",
                    "provisioningStatus": "Disabled",
                    "appliesTo": "User"
                }
            ],
            "skuId": "d17b27af-3f49-4822-99f9-56a661538792",
            "skuPartNumber": "CRMSTANDARD",
            "appliesTo": "User"
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List subscribedSkus",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
