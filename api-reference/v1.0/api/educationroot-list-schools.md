---
title: Enumerar educationSchools
description: Recupere una lista de todos los objetos de centro educativo.
author: mmast-msft
ms.openlocfilehash: 361c0ae0f15244b78fcbd13bc7c190c0e53bf079
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27305876"
---
# <a name="list-educationschools"></a><span data-ttu-id="972ea-103">Enumerar educationSchools</span><span class="sxs-lookup"><span data-stu-id="972ea-103">List educationSchools</span></span>

<span data-ttu-id="972ea-104">Recupere una lista de todos los objetos de centro educativo.</span><span class="sxs-lookup"><span data-stu-id="972ea-104">Retrieve a list of all school objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="972ea-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="972ea-105">Permissions</span></span>
<span data-ttu-id="972ea-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="972ea-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="972ea-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="972ea-108">Permission type</span></span>      | <span data-ttu-id="972ea-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="972ea-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="972ea-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="972ea-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="972ea-111">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="972ea-111">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="972ea-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="972ea-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="972ea-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="972ea-113">Not supported.</span></span>  |
|<span data-ttu-id="972ea-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="972ea-114">Application</span></span> | <span data-ttu-id="972ea-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="972ea-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="972ea-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="972ea-116">HTTP request</span></span>
<span data-ttu-id="972ea-117"><!-- { "blockType": "ignored" } -->''' escuelas/educación/GET de http</span><span class="sxs-lookup"><span data-stu-id="972ea-117"><!-- { "blockType": "ignored" } --> \`\`\`http GET /education/schools</span></span>
```
## Optional query parameters
This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.

## Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |

## Request body
Do not supply a request body for this method.
## Response
If successful, this method returns a `200 OK` response code and a collection of [educationSchool](../resources/educationschool.md) objects in the response body.
## Example
##### Request
The following is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_schools"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/schools
```
##### <a name="response"></a><span data-ttu-id="972ea-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="972ea-118">Response</span></span>
<span data-ttu-id="972ea-119">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="972ea-119">The following is an example of the response.</span></span> 

><span data-ttu-id="972ea-p102">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="972ea-p102">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSchool",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 345

{
  "value": [
    {
      "id": "10001",
      "displayName": "Contoso High School",
      "description": "Public 9-12 high school",
      "status": "active",
      "externalSource": "sis",
      "principalEmail": "amyr@contoso.com",
      "principalName": "Amy Roebuck",
      "externalPrincipalId": "14007",
      "highestGrade": "12",
      "lowestGrade": "9",
      "schoolNumber": "10001",
      "address": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
      "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
      },
      "externalId": "10001",
      "fax": "+1 (253) 555-0101",
      "phone": "+1 (253) 555-0102",
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List schools",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
