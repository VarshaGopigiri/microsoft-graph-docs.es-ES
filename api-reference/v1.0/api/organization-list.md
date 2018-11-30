---
title: List organization
description: Recupera una lista de objetos organization.
ms.openlocfilehash: 9a66fac482e5bc4a6fe822210ae274abdb725360
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032485"
---
# <a name="list-organization"></a><span data-ttu-id="1b230-103">List organization</span><span class="sxs-lookup"><span data-stu-id="1b230-103">List organization</span></span>



<span data-ttu-id="1b230-104">Recupera una lista de objetos organization.</span><span class="sxs-lookup"><span data-stu-id="1b230-104">Retrieve a list of organization objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="1b230-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1b230-105">Permissions</span></span>
<span data-ttu-id="1b230-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1b230-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1b230-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1b230-108">Permission type</span></span>      | <span data-ttu-id="1b230-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1b230-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1b230-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1b230-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1b230-111">User.Read, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1b230-111">User.Read, Directory.Read.All, Directory.ReadWrite.All</span></span>   |
|<span data-ttu-id="1b230-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1b230-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1b230-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b230-113">Not supported.</span></span>    |
|<span data-ttu-id="1b230-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1b230-114">Application</span></span> | <span data-ttu-id="1b230-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1b230-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

> <span data-ttu-id="1b230-116">Nota: Las aplicaciones que tienen el permiso User.Read solamente pueden leer las propiedades *id*, *displayName* y *verifiedDomains* de la organización.</span><span class="sxs-lookup"><span data-stu-id="1b230-116">Note: Applications granted the User.Read permission are able to read only the *id*, *displayName*, and *verifiedDomains* properties of the organization.</span></span>  <span data-ttu-id="1b230-117">El resto de propiedades devolverá valores `null`.</span><span class="sxs-lookup"><span data-stu-id="1b230-117">All other properties will return with `null` values.</span></span> <span data-ttu-id="1b230-118">Para leer todas las propiedades, use Directory.Read.All.</span><span class="sxs-lookup"><span data-stu-id="1b230-118">To read all properties, use Directory.Read.All.</span></span>

## <a name="http-request"></a><span data-ttu-id="1b230-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1b230-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /organization
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1b230-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1b230-120">Optional query parameters</span></span>
<span data-ttu-id="1b230-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b230-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="1b230-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1b230-122">Request headers</span></span>
| <span data-ttu-id="1b230-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="1b230-123">Name</span></span>       | <span data-ttu-id="1b230-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b230-124">Type</span></span> | <span data-ttu-id="1b230-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b230-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="1b230-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="1b230-126">Authorization</span></span>  | <span data-ttu-id="1b230-127">string</span><span class="sxs-lookup"><span data-stu-id="1b230-127">string</span></span>  | <span data-ttu-id="1b230-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1b230-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1b230-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1b230-130">Request body</span></span>
<span data-ttu-id="1b230-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1b230-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1b230-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b230-132">Response</span></span>

<span data-ttu-id="1b230-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [organization](../resources/organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b230-133">If successful, this method returns a `200 OK` response code and collection of [organization](../resources/organization.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1b230-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b230-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1b230-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1b230-135">Request</span></span>
<span data-ttu-id="1b230-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1b230-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_organization"
}-->
```http
GET https://graph.microsoft.com/beta/organization
```
##### <a name="response"></a><span data-ttu-id="1b230-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b230-137">Response</span></span>
<span data-ttu-id="1b230-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1b230-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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