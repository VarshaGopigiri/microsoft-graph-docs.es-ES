---
title: List organization
description: Recupera una lista de objetos organization.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 0fbd38f4d3c0e4ceec9f025e9822b635ce6a0d54
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939164"
---
# <a name="list-organization"></a><span data-ttu-id="bc6f7-103">List organization</span><span class="sxs-lookup"><span data-stu-id="bc6f7-103">List organization</span></span>



<span data-ttu-id="bc6f7-104">Recupera una lista de objetos organization.</span><span class="sxs-lookup"><span data-stu-id="bc6f7-104">Retrieve a list of organization objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="bc6f7-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="bc6f7-105">Permissions</span></span>
<span data-ttu-id="bc6f7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bc6f7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bc6f7-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bc6f7-108">Permission type</span></span>      | <span data-ttu-id="bc6f7-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bc6f7-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bc6f7-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bc6f7-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bc6f7-111">User.Read, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bc6f7-111">User.Read, Directory.Read.All, Directory.ReadWrite.All</span></span>   |
|<span data-ttu-id="bc6f7-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bc6f7-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bc6f7-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc6f7-113">Not supported.</span></span>    |
|<span data-ttu-id="bc6f7-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bc6f7-114">Application</span></span> | <span data-ttu-id="bc6f7-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bc6f7-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

> <span data-ttu-id="bc6f7-116">Nota: Las aplicaciones que tienen el permiso User.Read solamente pueden leer las propiedades *id*, *displayName* y *verifiedDomains* de la organización.</span><span class="sxs-lookup"><span data-stu-id="bc6f7-116">Note: Applications granted the User.Read permission are able to read only the *id*, *displayName*, and *verifiedDomains* properties of the organization.</span></span>  <span data-ttu-id="bc6f7-117">El resto de propiedades devolverá valores `null`.</span><span class="sxs-lookup"><span data-stu-id="bc6f7-117">All other properties will return with `null` values.</span></span> <span data-ttu-id="bc6f7-118">Para leer todas las propiedades, use Directory.Read.All.</span><span class="sxs-lookup"><span data-stu-id="bc6f7-118">To read all properties, use Directory.Read.All.</span></span>

## <a name="http-request"></a><span data-ttu-id="bc6f7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc6f7-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /organization
```
## <a name="optional-query-parameters"></a><span data-ttu-id="bc6f7-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bc6f7-120">Optional query parameters</span></span>
<span data-ttu-id="bc6f7-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc6f7-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bc6f7-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc6f7-122">Request headers</span></span>
| <span data-ttu-id="bc6f7-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="bc6f7-123">Name</span></span>       | <span data-ttu-id="bc6f7-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6f7-124">Type</span></span> | <span data-ttu-id="bc6f7-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc6f7-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bc6f7-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="bc6f7-126">Authorization</span></span>  | <span data-ttu-id="bc6f7-127">string</span><span class="sxs-lookup"><span data-stu-id="bc6f7-127">string</span></span>  | <span data-ttu-id="bc6f7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc6f7-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bc6f7-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bc6f7-130">Request body</span></span>
<span data-ttu-id="bc6f7-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bc6f7-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bc6f7-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc6f7-132">Response</span></span>

<span data-ttu-id="bc6f7-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [organization](../resources/organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc6f7-133">If successful, this method returns a `200 OK` response code and collection of [organization](../resources/organization.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bc6f7-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc6f7-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bc6f7-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc6f7-135">Request</span></span>
<span data-ttu-id="bc6f7-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc6f7-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_organization"
}-->
```http
GET https://graph.microsoft.com/beta/organization
```
##### <a name="response"></a><span data-ttu-id="bc6f7-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc6f7-137">Response</span></span>
<span data-ttu-id="bc6f7-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bc6f7-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
