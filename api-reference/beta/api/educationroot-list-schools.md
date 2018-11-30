---
title: Enumerar educationSchools
description: Recupere una lista de todos los objetos de centro educativo.
ms.openlocfilehash: 88ba9591b305c62ce40e059f422cc674f445500d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083352"
---
# <a name="list-educationschools"></a><span data-ttu-id="9b7f9-103">Enumerar educationSchools</span><span class="sxs-lookup"><span data-stu-id="9b7f9-103">List educationSchools</span></span>

> <span data-ttu-id="9b7f9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b7f9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b7f9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b7f9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9b7f9-106">Recupere una lista de todos los objetos de centro educativo.</span><span class="sxs-lookup"><span data-stu-id="9b7f9-106">Retrieve a list of all school objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="9b7f9-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b7f9-107">Permissions</span></span>
<span data-ttu-id="9b7f9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b7f9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9b7f9-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b7f9-110">Permission type</span></span>      | <span data-ttu-id="9b7f9-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b7f9-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9b7f9-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b7f9-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="9b7f9-113">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="9b7f9-113">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="9b7f9-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b7f9-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="9b7f9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b7f9-115">Not supported.</span></span>  |
|<span data-ttu-id="9b7f9-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b7f9-116">Application</span></span> | <span data-ttu-id="9b7f9-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9b7f9-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="9b7f9-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b7f9-118">HTTP request</span></span>
<span data-ttu-id="9b7f9-119"><!-- { "blockType": "ignored" } -->''' escuelas/educación/GET de http</span><span class="sxs-lookup"><span data-stu-id="9b7f9-119"><!-- { "blockType": "ignored" } --> \`\`\`http GET /education/schools</span></span>
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
GET https://graph.microsoft.com/beta/education/schools
```
##### <a name="response"></a><span data-ttu-id="9b7f9-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b7f9-120">Response</span></span>
<span data-ttu-id="9b7f9-121">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b7f9-121">The following is an example of the response.</span></span> 

><span data-ttu-id="9b7f9-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b7f9-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
