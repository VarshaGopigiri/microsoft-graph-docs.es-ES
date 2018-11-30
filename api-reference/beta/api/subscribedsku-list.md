---
title: Enumerar subscribedSkus
description: Recupera la lista de suscripciones comerciales que ha adquirido una organización.
ms.openlocfilehash: c20e72344c56765dd24c89d6d6c1d0aa24244f2e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086672"
---
# <a name="list-subscribedskus"></a><span data-ttu-id="60971-103">Enumerar subscribedSkus</span><span class="sxs-lookup"><span data-stu-id="60971-103">List subscribedSkus</span></span>

> <span data-ttu-id="60971-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="60971-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="60971-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="60971-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="60971-106">Recupera la lista de suscripciones comerciales que ha adquirido una organización.</span><span class="sxs-lookup"><span data-stu-id="60971-106">Retrieve the list of commercial subscriptions that an organization has acquired.</span></span>

## <a name="permissions"></a><span data-ttu-id="60971-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="60971-107">Permissions</span></span>
<span data-ttu-id="60971-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="60971-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="60971-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="60971-110">Permission type</span></span>      | <span data-ttu-id="60971-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="60971-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="60971-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="60971-112">Delegated (work or school account)</span></span> | <span data-ttu-id="60971-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="60971-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="60971-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="60971-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="60971-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="60971-115">Not supported.</span></span>    |
|<span data-ttu-id="60971-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="60971-116">Application</span></span> | <span data-ttu-id="60971-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="60971-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="60971-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="60971-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /subscribedSkus
```
## <a name="optional-query-parameters"></a><span data-ttu-id="60971-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="60971-119">Optional query parameters</span></span>
<span data-ttu-id="60971-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60971-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="60971-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="60971-121">Request headers</span></span>
| <span data-ttu-id="60971-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="60971-122">Name</span></span>       | <span data-ttu-id="60971-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="60971-123">Type</span></span> | <span data-ttu-id="60971-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="60971-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="60971-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="60971-125">Authorization</span></span>  | <span data-ttu-id="60971-126">string</span><span class="sxs-lookup"><span data-stu-id="60971-126">string</span></span>  | <span data-ttu-id="60971-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="60971-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="60971-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="60971-129">Request body</span></span>
<span data-ttu-id="60971-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="60971-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="60971-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60971-131">Response</span></span>

<span data-ttu-id="60971-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [subscribedSku](../resources/subscribedsku.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60971-132">If successful, this method returns a `200 OK` response code and collection of [subscribedSku](../resources/subscribedsku.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="60971-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="60971-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="60971-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="60971-134">Request</span></span>
<span data-ttu-id="60971-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="60971-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscribedskus"
}-->
```http
GET https://graph.microsoft.com/beta/subscribedSkus
```
##### <a name="response"></a><span data-ttu-id="60971-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60971-136">Response</span></span>
<span data-ttu-id="60971-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="60971-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.subscribedSku",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 547

{
  "value": [
    {
      "capabilityStatus": "capabilityStatus-value",
      "consumedUnits": 99,
      "prepaidUnits": {
        "enabled": 99,
        "suspended": 99,
        "warning": 99
      },
      "servicePlans": [
        {
          "servicePlanId": "servicePlanId-value",
          "servicePlanName": "servicePlanName-value",
          "provisioningStatus": "provisioningStatus-value",
          "appliesTo": "appliesTo-value"
        }
      ],
      "skuId": "skuId-value",
      "skuPartNumber": "skuPartNumber-value"
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