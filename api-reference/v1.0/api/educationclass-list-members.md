---
title: Enumerar miembros
description: Recupera los profesores y alumnos de una clase. Tenga en cuenta que si se usa el token delegado, los miembros solo pueden ser vistos por otros miembros de la clase.
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 83d1f6e52e11afc60c84977676279ae02182e047
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972589"
---
# <a name="list-members"></a><span data-ttu-id="9fdfc-104">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="9fdfc-104">List members</span></span>

<span data-ttu-id="9fdfc-105">Recupera los profesores y alumnos de una clase.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-105">Retrieves the teachers and students for a class.</span></span> <span data-ttu-id="9fdfc-106">Tenga en cuenta que si se usa el token delegado, los miembros solo pueden ser vistos por otros miembros de la clase.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-106">Note that if the delegated token is used, members can only be seen by other members of the class.</span></span>

## <a name="permissions"></a><span data-ttu-id="9fdfc-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9fdfc-107">Permissions</span></span>
<span data-ttu-id="9fdfc-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9fdfc-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9fdfc-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9fdfc-110">Permission type</span></span>      | <span data-ttu-id="9fdfc-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9fdfc-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9fdfc-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9fdfc-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="9fdfc-113">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="9fdfc-113">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="9fdfc-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9fdfc-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="9fdfc-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="9fdfc-115">Not supported</span></span>  |
|<span data-ttu-id="9fdfc-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9fdfc-116">Application</span></span> | <span data-ttu-id="9fdfc-117">EduRoster.Read.All, EduRoster.ReadWrite.All más Member.Read.Hidden</span><span class="sxs-lookup"><span data-stu-id="9fdfc-117">EduRoster.Read.All, EduRoster.ReadWrite.All plus Member.Read.Hidden</span></span> | 

## <a name="http-request"></a><span data-ttu-id="9fdfc-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9fdfc-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/members
```
## <a name="optional-query-parameters"></a><span data-ttu-id="9fdfc-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9fdfc-119">Optional query parameters</span></span>
<span data-ttu-id="9fdfc-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9fdfc-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9fdfc-121">Request headers</span></span>
| <span data-ttu-id="9fdfc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fdfc-122">Header</span></span>       | <span data-ttu-id="9fdfc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9fdfc-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9fdfc-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="9fdfc-124">Authorization</span></span>  | <span data-ttu-id="9fdfc-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9fdfc-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9fdfc-127">Request body</span></span>
<span data-ttu-id="9fdfc-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="9fdfc-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9fdfc-129">Response</span></span>
<span data-ttu-id="9fdfc-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationUser](../resources/educationuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-130">If successful, this method returns a `200 OK` response code and a collection of [educationUser](../resources/educationuser.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9fdfc-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9fdfc-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9fdfc-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9fdfc-132">Request</span></span>
<span data-ttu-id="9fdfc-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_members"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/classes/{class-id}/members
```
##### <a name="response"></a><span data-ttu-id="9fdfc-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9fdfc-134">Response</span></span>
<span data-ttu-id="9fdfc-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-135">The following is an example of the response.</span></span> 

><span data-ttu-id="9fdfc-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9fdfc-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
      "id": "13013",
      "displayName": "Ora Klein",
      "givenName": "Ora",
      "middleName": " ",
      "surname": "Klein",
      "mail": "OraK@contoso.com",
      "mobilePhone": "+1 (253) 555-0101",
      "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
      },
      "externalSource": "School of Fine Art",
      "mailingAddress": {
        "city": "Buffalo",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "NY",
        "street": "12345 Main St."
      },
      "primaryRole": "teacher",
      "residenceAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
      "teacher": {
        "externalId": "13013",
        "teacherNumber": "8802",
      }
    },
    {
      "id": "13005",
      "displayName": "Erna Parker",
      "givenName": "Erna",
      "middleName": " ",
      "surname": "Parker",
      "mail": "ernap@contoso.com",
      "mobilePhone": "+1 (253) 555-0104",
      "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
      },
      "externalSource": "School of Fine Art",
      "mailingAddress": {
        "city": "Buffalo",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "NY",
        "street": "12345 Main St."
      },
      "student": {
        "birthDate": "2001-01-01T00:00:00Z",
        "externalId": "13005",
        "gender": "female",
        "grade": "9",
        "graduationYear": "2019",
        "studentNumber": "13005",
      },
      "primaryRole": "student",
      "residenceAddress": {
        "city": "Long Beach",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Maple St."
      },
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List members",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
