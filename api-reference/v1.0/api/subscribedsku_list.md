# <a name="list-subscribedskus"></a><span data-ttu-id="24ecb-101">Enumerar subscribedSkus</span><span class="sxs-lookup"><span data-stu-id="24ecb-101">List subscribedSkus</span></span>
<span data-ttu-id="24ecb-102">Recupera la lista de suscripciones comerciales que ha adquirido una organización.</span><span class="sxs-lookup"><span data-stu-id="24ecb-102">Retrieve the list of commercial subscriptions that an organization has acquired.</span></span>

## <a name="permissions"></a><span data-ttu-id="24ecb-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="24ecb-103">Permissions</span></span>
<span data-ttu-id="24ecb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="24ecb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="24ecb-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="24ecb-106">Permission type</span></span>      | <span data-ttu-id="24ecb-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="24ecb-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="24ecb-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="24ecb-108">Delegated (work or school account)</span></span> | <span data-ttu-id="24ecb-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="24ecb-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="24ecb-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="24ecb-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="24ecb-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="24ecb-111">Not supported.</span></span>    |
|<span data-ttu-id="24ecb-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="24ecb-112">Application</span></span> | <span data-ttu-id="24ecb-113">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="24ecb-113">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="24ecb-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="24ecb-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /subscribedSkus
```
## <a name="optional-query-parameters"></a><span data-ttu-id="24ecb-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="24ecb-115">Optional query parameters</span></span>
<span data-ttu-id="24ecb-116">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="24ecb-116">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="24ecb-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="24ecb-117">Request headers</span></span>
| <span data-ttu-id="24ecb-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="24ecb-118">Name</span></span>       | <span data-ttu-id="24ecb-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="24ecb-119">Type</span></span> | <span data-ttu-id="24ecb-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="24ecb-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="24ecb-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="24ecb-121">Authorization</span></span>  | <span data-ttu-id="24ecb-122">string</span><span class="sxs-lookup"><span data-stu-id="24ecb-122">string</span></span>  | <span data-ttu-id="24ecb-p102">&lt;token&gt; de portador. *Obligatorio*</span><span class="sxs-lookup"><span data-stu-id="24ecb-p102">Bearer &lt;token&gt;. *Required*</span></span> |

## <a name="request-body"></a><span data-ttu-id="24ecb-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="24ecb-125">Request body</span></span>
<span data-ttu-id="24ecb-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="24ecb-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="24ecb-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="24ecb-127">Response</span></span>

<span data-ttu-id="24ecb-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [subscribedSku](../resources/subscribedsku.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="24ecb-128">If successful, this method returns a `200 OK` response code and collection of [subscribedSku](../resources/subscribedsku.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="24ecb-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="24ecb-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="24ecb-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="24ecb-130">Request</span></span>
<span data-ttu-id="24ecb-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="24ecb-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscribedskus"
}-->
```http
GET https://graph.microsoft.com/v1.0/subscribedSkus
```
##### <a name="response"></a><span data-ttu-id="24ecb-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="24ecb-132">Response</span></span>
<span data-ttu-id="24ecb-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="24ecb-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#subscribedSkus",
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
