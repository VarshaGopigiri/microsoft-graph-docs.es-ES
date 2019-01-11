---
title: Enumerar centros educativos
description: Recupere una lista de los centros educativos en los que se imparte la clase.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 6bfc94304a1e2eae448848adb75a79989c2b77f0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815431"
---
# <a name="list-schools"></a><span data-ttu-id="f252e-103">Enumerar centros educativos</span><span class="sxs-lookup"><span data-stu-id="f252e-103">List schools</span></span>

<span data-ttu-id="f252e-104">Recupere una lista de los centros educativos en los que se imparte la clase.</span><span class="sxs-lookup"><span data-stu-id="f252e-104">Retrieve a list of schools in which the class is taught.</span></span>

## <a name="permissions"></a><span data-ttu-id="f252e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f252e-105">Permissions</span></span>
<span data-ttu-id="f252e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f252e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f252e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f252e-108">Permission type</span></span>      | <span data-ttu-id="f252e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f252e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f252e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f252e-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="f252e-111">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="f252e-111">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="f252e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f252e-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="f252e-113">No admitido</span><span class="sxs-lookup"><span data-stu-id="f252e-113">Not supported</span></span>  |
|<span data-ttu-id="f252e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f252e-114">Application</span></span> | <span data-ttu-id="f252e-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f252e-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="f252e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f252e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/schools
```
## <a name="optional-query-parameters"></a><span data-ttu-id="f252e-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f252e-117">Optional query parameters</span></span>
<span data-ttu-id="f252e-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f252e-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f252e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f252e-119">Request headers</span></span>
| <span data-ttu-id="f252e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f252e-120">Header</span></span>       | <span data-ttu-id="f252e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f252e-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="f252e-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="f252e-122">Authorization</span></span>  | <span data-ttu-id="f252e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f252e-p102">Bearer {token}. Required.</span></span>  |


## <a name="request-body"></a><span data-ttu-id="f252e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f252e-125">Request body</span></span>
<span data-ttu-id="f252e-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f252e-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="f252e-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f252e-127">Response</span></span>
<span data-ttu-id="f252e-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationSchool](../resources/educationschool.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f252e-128">If successful, this method returns a `200 OK` response code and a collection of [educationSchool](../resources/educationschool.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f252e-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f252e-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f252e-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f252e-130">Request</span></span>
<span data-ttu-id="f252e-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f252e-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_schools"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/classes/{class-id}/schools
```
##### <a name="response"></a><span data-ttu-id="f252e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f252e-132">Response</span></span>
<span data-ttu-id="f252e-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f252e-133">The following is an example of the response.</span></span> 

><span data-ttu-id="f252e-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f252e-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSchool",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 892

{
  "value": [
    {
      "id": "10002",
      "displayName": "Fabrikam High School",
      "description": "Magnate school for the arts. Los Angeles School District",
      "status": "String",
      "externalSource": "String",
      "principalEmail": "AmyR@fabrikam.com",
      "principalName": "Amy Roebuck",
      "externalPrincipalId": "14007",
      "highestGrade": "12",
      "lowestGrade": "9",
      "schoolNumber": "10002",
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
      "externalId": "10002",
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
