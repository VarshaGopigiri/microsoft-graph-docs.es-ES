---
title: Enumerar educationUsers
description: Recupere una lista de usuarios de un centro educativo.
author: mmast-msft
ms.openlocfilehash: d282c2df8f78b38e8e21adff115f1af8b11bc1db
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314220"
---
# <a name="list-educationusers"></a><span data-ttu-id="27874-103">Enumerar educationUsers</span><span class="sxs-lookup"><span data-stu-id="27874-103">List educationUsers</span></span>

<span data-ttu-id="27874-104">Recupere una lista de usuarios de un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="27874-104">Retrieve a list of users at a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="27874-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="27874-105">Permissions</span></span>
<span data-ttu-id="27874-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="27874-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="27874-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="27874-108">Permission type</span></span>      | <span data-ttu-id="27874-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="27874-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="27874-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="27874-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="27874-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="27874-111">Not supported.</span></span>  |
|<span data-ttu-id="27874-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="27874-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="27874-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="27874-113">Not supported.</span></span>  |
|<span data-ttu-id="27874-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="27874-114">Application</span></span> | <span data-ttu-id="27874-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="27874-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="27874-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="27874-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/schools/{id}/users
```
## <a name="optional-query-parameters"></a><span data-ttu-id="27874-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="27874-117">Optional query parameters</span></span>
<span data-ttu-id="27874-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27874-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="27874-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="27874-119">Request headers</span></span>
| <span data-ttu-id="27874-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27874-120">Header</span></span>       | <span data-ttu-id="27874-121">Valor</span><span class="sxs-lookup"><span data-stu-id="27874-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="27874-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="27874-122">Authorization</span></span>  | <span data-ttu-id="27874-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="27874-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="27874-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="27874-125">Request body</span></span>
<span data-ttu-id="27874-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="27874-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="27874-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27874-127">Response</span></span>
<span data-ttu-id="27874-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationUser](../resources/educationuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27874-128">If successful, this method returns a `200 OK` response code and a collection of [educationUser](../resources/educationuser.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="27874-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="27874-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="27874-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="27874-130">Request</span></span>
<span data-ttu-id="27874-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="27874-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_users"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/schools/{school-id}/users
```
##### <a name="response"></a><span data-ttu-id="27874-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27874-132">Response</span></span>
<span data-ttu-id="27874-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27874-133">The following is an example of the response.</span></span> 

><span data-ttu-id="27874-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="27874-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationUser",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 593

{
  "value": [
    {
      "id": "13012",
      "displayName": "Dion Matheson",
      "givenName": "Dion",
      "middleName": " ",
      "surname": "Matheson",
      "mail": "DionM@contoso.com",
      "mobilePhone": "+1 (253) 555-0101",
      "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
      },
      "externalSource": "sis",
      "mailingAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
      "primaryRole": "student",
      "residenceAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List users",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
