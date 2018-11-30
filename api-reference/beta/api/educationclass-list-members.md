---
title: Enumerar miembros
description: Recupera los profesores y alumnos de una clase. Tenga en cuenta que si se usa el token delegado, los miembros solo pueden ser vistos por otros miembros de la clase.
ms.openlocfilehash: e8f31720733fec3942d4ddb35fa7f2fdac1b26f0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083673"
---
# <a name="list-members"></a><span data-ttu-id="07d3a-104">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="07d3a-104">List members</span></span>

> <span data-ttu-id="07d3a-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="07d3a-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="07d3a-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="07d3a-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="07d3a-107">Recupera los profesores y alumnos de una clase.</span><span class="sxs-lookup"><span data-stu-id="07d3a-107">Retrieves the teachers and students for a class.</span></span> <span data-ttu-id="07d3a-108">Tenga en cuenta que si se usa el token delegado, los miembros solo pueden ser vistos por otros miembros de la clase.</span><span class="sxs-lookup"><span data-stu-id="07d3a-108">Note that if the delegated token is used, members can only be seen by other members of the class.</span></span>

## <a name="permissions"></a><span data-ttu-id="07d3a-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="07d3a-109">Permissions</span></span>
<span data-ttu-id="07d3a-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="07d3a-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="07d3a-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="07d3a-112">Permission type</span></span>      | <span data-ttu-id="07d3a-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="07d3a-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="07d3a-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="07d3a-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="07d3a-115">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="07d3a-115">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="07d3a-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="07d3a-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="07d3a-117">No admitido</span><span class="sxs-lookup"><span data-stu-id="07d3a-117">Not supported</span></span>  |
|<span data-ttu-id="07d3a-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="07d3a-118">Application</span></span> | <span data-ttu-id="07d3a-119">EduRoster.Read.All, EduRoster.ReadWrite.All más Member.Read.Hidden</span><span class="sxs-lookup"><span data-stu-id="07d3a-119">EduRoster.Read.All, EduRoster.ReadWrite.All plus Member.Read.Hidden</span></span> | 

## <a name="http-request"></a><span data-ttu-id="07d3a-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="07d3a-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/members
```
## <a name="optional-query-parameters"></a><span data-ttu-id="07d3a-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="07d3a-121">Optional query parameters</span></span>
<span data-ttu-id="07d3a-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07d3a-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="07d3a-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="07d3a-123">Request headers</span></span>
| <span data-ttu-id="07d3a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07d3a-124">Header</span></span>       | <span data-ttu-id="07d3a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="07d3a-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="07d3a-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="07d3a-126">Authorization</span></span>  | <span data-ttu-id="07d3a-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="07d3a-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="07d3a-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="07d3a-129">Request body</span></span>
<span data-ttu-id="07d3a-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="07d3a-130">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="07d3a-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07d3a-131">Response</span></span>
<span data-ttu-id="07d3a-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationUser](../resources/educationuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07d3a-132">If successful, this method returns a `200 OK` response code and a collection of [educationUser](../resources/educationuser.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="07d3a-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="07d3a-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="07d3a-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="07d3a-134">Request</span></span>
<span data-ttu-id="07d3a-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="07d3a-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_members"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/11016/members
```
##### <a name="response"></a><span data-ttu-id="07d3a-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07d3a-136">Response</span></span>
<span data-ttu-id="07d3a-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07d3a-137">The following is an example of the response.</span></span> 

><span data-ttu-id="07d3a-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="07d3a-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
      "externalId": "13013",
      "teacherNumber": "8802",
      "residenceAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
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
      "primaryRole": "student",
      "externalId": "13005",
      "birthDate": "2001-01-01T00:00:00Z",
      "gender": "female",
      "grade": "9",
      "graduationYear": "2019",
      "studentNumber": "13005",
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