---
title: Enumerar subscribedSkus
description: Recupera la lista de suscripciones comerciales que ha adquirido una organización.
localization_priority: Priority
ms.openlocfilehash: bf382b697976ba264b610afb2946abb094f8ac4f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885242"
---
# <a name="list-subscribedskus"></a><span data-ttu-id="118bd-103">Enumerar subscribedSkus</span><span class="sxs-lookup"><span data-stu-id="118bd-103">List subscribedSkus</span></span>
<span data-ttu-id="118bd-104">Recupera la lista de suscripciones comerciales que ha adquirido una organización.</span><span class="sxs-lookup"><span data-stu-id="118bd-104">Retrieve the list of commercial subscriptions that an organization has acquired.</span></span>

## <a name="permissions"></a><span data-ttu-id="118bd-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="118bd-105">Permissions</span></span>
<span data-ttu-id="118bd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="118bd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="118bd-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="118bd-108">Permission type</span></span>      | <span data-ttu-id="118bd-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="118bd-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="118bd-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="118bd-110">Delegated (work or school account)</span></span> | <span data-ttu-id="118bd-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="118bd-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="118bd-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="118bd-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="118bd-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="118bd-113">Not supported.</span></span>    |
|<span data-ttu-id="118bd-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="118bd-114">Application</span></span> | <span data-ttu-id="118bd-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="118bd-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="118bd-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="118bd-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /subscribedSkus
```
## <a name="optional-query-parameters"></a><span data-ttu-id="118bd-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="118bd-117">Optional query parameters</span></span>
<span data-ttu-id="118bd-118">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="118bd-118">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="118bd-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="118bd-119">Request headers</span></span>
| <span data-ttu-id="118bd-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="118bd-120">Name</span></span>       | <span data-ttu-id="118bd-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="118bd-121">Type</span></span> | <span data-ttu-id="118bd-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="118bd-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="118bd-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="118bd-123">Authorization</span></span>  | <span data-ttu-id="118bd-124">string</span><span class="sxs-lookup"><span data-stu-id="118bd-124">string</span></span>  | <span data-ttu-id="118bd-p102">&lt;token&gt; de portador. *Obligatorio*</span><span class="sxs-lookup"><span data-stu-id="118bd-p102">Bearer &lt;token&gt;. *Required*</span></span> |

## <a name="request-body"></a><span data-ttu-id="118bd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="118bd-127">Request body</span></span>
<span data-ttu-id="118bd-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="118bd-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="118bd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="118bd-129">Response</span></span>

<span data-ttu-id="118bd-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [subscribedSku](../resources/subscribedsku.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="118bd-130">If successful, this method returns a `200 OK` response code and collection of [subscribedSku](../resources/subscribedsku.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="118bd-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="118bd-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="118bd-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="118bd-132">Request</span></span>
<span data-ttu-id="118bd-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="118bd-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscribedskus"
}-->
```http
GET https://graph.microsoft.com/v1.0/subscribedSkus
```
##### <a name="response"></a><span data-ttu-id="118bd-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="118bd-134">Response</span></span>
<span data-ttu-id="118bd-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="118bd-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
