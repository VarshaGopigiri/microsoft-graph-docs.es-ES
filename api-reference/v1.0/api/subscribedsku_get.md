# <a name="get-subscribedsku"></a><span data-ttu-id="6bf4a-101">Obtener subscribedSku</span><span class="sxs-lookup"><span data-stu-id="6bf4a-101">Get subscribedSku</span></span>
<span data-ttu-id="6bf4a-102">Recupere una suscripción comercial específica que ha adquirido una organización.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-102">Retrieve a specific commercial subscription that an organization has acquired.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6bf4a-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6bf4a-103">Prerequisites</span></span>
<span data-ttu-id="6bf4a-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="6bf4a-104">One of the following **scopes** is required to execute this API: *Directory.Read.All*, *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="6bf4a-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6bf4a-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /subscribedSkus/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6bf4a-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6bf4a-106">Optional query parameters</span></span>
<span data-ttu-id="6bf4a-107">Este método **no** es compatible con los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="6bf4a-107">This method does **not** support the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="6bf4a-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6bf4a-108">Request headers</span></span>
| <span data-ttu-id="6bf4a-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="6bf4a-109">Name</span></span>       | <span data-ttu-id="6bf4a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="6bf4a-110">Type</span></span> | <span data-ttu-id="6bf4a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6bf4a-111">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6bf4a-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="6bf4a-112">Authorization</span></span>  | <span data-ttu-id="6bf4a-113">string</span><span class="sxs-lookup"><span data-stu-id="6bf4a-113">string</span></span>  | <span data-ttu-id="6bf4a-p101">&lt;token&gt; de portador. *Obligatorio*</span><span class="sxs-lookup"><span data-stu-id="6bf4a-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6bf4a-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6bf4a-116">Request body</span></span>
<span data-ttu-id="6bf4a-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6bf4a-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6bf4a-118">Response</span></span>

<span data-ttu-id="6bf4a-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscribedSku](../resources/subscribedsku.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-119">If successful, this method returns a `200 OK` response code and [subscribedSku](../resources/subscribedsku.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6bf4a-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6bf4a-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6bf4a-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6bf4a-121">Request</span></span>
<span data-ttu-id="6bf4a-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscribedsku"
}-->
```http
GET https://graph.microsoft.com/v1.0/subscribedSkus/{id}
```
##### <a name="response"></a><span data-ttu-id="6bf4a-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6bf4a-123">Response</span></span>
<span data-ttu-id="6bf4a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.subscribedSku"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#subscribedSkus/$entity",
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
        },
        {
            "servicePlanId": "9f431833-0334-42de-a7dc-70aa40db46db",
            "servicePlanName": "LOCKBOX_ENTERPRISE",
            "provisioningStatus": "Success",
            "appliesTo": "User"
        }
    ],
    "skuId": "c7df2760-2c81-4ef7-b578-5b5392b571df",
    "skuPartNumber": "ENTERPRISEPREMIUM",
    "appliesTo": "User"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get subscribedSku",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
