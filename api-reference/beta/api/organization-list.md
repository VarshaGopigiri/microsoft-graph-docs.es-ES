---
title: List organization
description: Recupera una lista de objetos organization.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 9dd1489714c4de87f0072ef0498c5acdf008d5ff
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938828"
---
# <a name="list-organization"></a><span data-ttu-id="5d331-103">List organization</span><span class="sxs-lookup"><span data-stu-id="5d331-103">List organization</span></span>

> <span data-ttu-id="5d331-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5d331-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5d331-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5d331-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5d331-106">Recupera una lista de objetos organization.</span><span class="sxs-lookup"><span data-stu-id="5d331-106">Retrieve a list of organization objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="5d331-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5d331-107">Permissions</span></span>
<span data-ttu-id="5d331-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5d331-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5d331-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5d331-110">Permission type</span></span>      | <span data-ttu-id="5d331-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5d331-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5d331-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5d331-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5d331-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d331-113">Not supported.</span></span>    |
|<span data-ttu-id="5d331-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5d331-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5d331-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d331-115">Not supported.</span></span>    |
|<span data-ttu-id="5d331-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5d331-116">Application</span></span> | <span data-ttu-id="5d331-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d331-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5d331-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5d331-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /organization
```
## <a name="optional-query-parameters"></a><span data-ttu-id="5d331-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5d331-119">Optional query parameters</span></span>
<span data-ttu-id="5d331-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d331-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="5d331-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5d331-121">Request headers</span></span>
| <span data-ttu-id="5d331-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="5d331-122">Name</span></span>       | <span data-ttu-id="5d331-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="5d331-123">Type</span></span> | <span data-ttu-id="5d331-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d331-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="5d331-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="5d331-125">Authorization</span></span>  | <span data-ttu-id="5d331-126">string</span><span class="sxs-lookup"><span data-stu-id="5d331-126">string</span></span>  | <span data-ttu-id="5d331-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5d331-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5d331-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5d331-129">Request body</span></span>
<span data-ttu-id="5d331-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5d331-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5d331-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d331-131">Response</span></span>

<span data-ttu-id="5d331-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [organization](../resources/organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d331-132">If successful, this method returns a `200 OK` response code and collection of [organization](../resources/organization.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="5d331-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5d331-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5d331-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5d331-134">Request</span></span>
<span data-ttu-id="5d331-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d331-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_organization"
}-->
```http
GET https://graph.microsoft.com/beta/organization
```
##### <a name="response"></a><span data-ttu-id="5d331-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d331-136">Response</span></span>
<span data-ttu-id="5d331-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5d331-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
