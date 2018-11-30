---
title: Obtener subscribedSku
description: Recupera una suscripción comercial específica que ha adquirido una organización.
ms.openlocfilehash: cf7d8ef7aef8eaabdc30c02c9bf8e71478017823
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030055"
---
# <a name="get-subscribedsku"></a><span data-ttu-id="d2e9e-103">Obtener subscribedSku</span><span class="sxs-lookup"><span data-stu-id="d2e9e-103">Get subscribedSku</span></span>
<span data-ttu-id="d2e9e-104">Recupera una suscripción comercial específica que ha adquirido una organización.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-104">Retrieve a specific commercial subscription that an organization has acquired.</span></span>

## <a name="permissions"></a><span data-ttu-id="d2e9e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d2e9e-105">Permissions</span></span>
<span data-ttu-id="d2e9e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2e9e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="d2e9e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2e9e-108">Permission type</span></span>      | <span data-ttu-id="d2e9e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2e9e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d2e9e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2e9e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d2e9e-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d2e9e-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="d2e9e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2e9e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d2e9e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-113">Not supported.</span></span>    |
|<span data-ttu-id="d2e9e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2e9e-114">Application</span></span> | <span data-ttu-id="d2e9e-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d2e9e-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d2e9e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2e9e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /subscribedSkus/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="d2e9e-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d2e9e-117">Optional query parameters</span></span>
<span data-ttu-id="d2e9e-118">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="d2e9e-118">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="d2e9e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2e9e-119">Request headers</span></span>
| <span data-ttu-id="d2e9e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d2e9e-120">Name</span></span>       | <span data-ttu-id="d2e9e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2e9e-121">Type</span></span> | <span data-ttu-id="d2e9e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2e9e-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="d2e9e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="d2e9e-123">Authorization</span></span>  | <span data-ttu-id="d2e9e-124">string</span><span class="sxs-lookup"><span data-stu-id="d2e9e-124">string</span></span>  | <span data-ttu-id="d2e9e-p102">&lt;token&gt; de portador. *Obligatorio*</span><span class="sxs-lookup"><span data-stu-id="d2e9e-p102">Bearer &lt;token&gt;. *Required*</span></span> |

## <a name="request-body"></a><span data-ttu-id="d2e9e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2e9e-127">Request body</span></span>
<span data-ttu-id="d2e9e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d2e9e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2e9e-129">Response</span></span>

<span data-ttu-id="d2e9e-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscribedSku](../resources/subscribedsku.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-130">If successful, this method returns a `200 OK` response code and [subscribedSku](../resources/subscribedsku.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d2e9e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2e9e-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d2e9e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2e9e-132">Request</span></span>
<span data-ttu-id="d2e9e-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscribedsku"
}-->
```http
GET https://graph.microsoft.com/v1.0/subscribedSkus/{id}
```
##### <a name="response"></a><span data-ttu-id="d2e9e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2e9e-134">Response</span></span>
<span data-ttu-id="d2e9e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.subscribedSku"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#subscribedSkus/$entity",
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
