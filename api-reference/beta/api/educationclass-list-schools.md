---
title: Enumerar centros educativos
description: Recupere una lista de los centros educativos en los que se imparte la clase.
author: mmast-msft
ms.openlocfilehash: 8de8e443780797044d451505de0a5e4f72fe34b9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316544"
---
# <a name="list-schools"></a><span data-ttu-id="e5489-103">Enumerar centros educativos</span><span class="sxs-lookup"><span data-stu-id="e5489-103">List schools</span></span>

> <span data-ttu-id="e5489-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e5489-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e5489-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e5489-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e5489-106">Recupere una lista de los centros educativos en los que se imparte la clase.</span><span class="sxs-lookup"><span data-stu-id="e5489-106">Retrieve a list of schools in which the class is taught.</span></span>

## <a name="permissions"></a><span data-ttu-id="e5489-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e5489-107">Permissions</span></span>
<span data-ttu-id="e5489-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e5489-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e5489-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e5489-110">Permission type</span></span>      | <span data-ttu-id="e5489-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e5489-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e5489-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e5489-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="e5489-113">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="e5489-113">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="e5489-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e5489-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="e5489-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="e5489-115">Not supported</span></span>  |
|<span data-ttu-id="e5489-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e5489-116">Application</span></span> | <span data-ttu-id="e5489-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e5489-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="e5489-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e5489-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/schools
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e5489-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e5489-119">Optional query parameters</span></span>
<span data-ttu-id="e5489-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5489-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e5489-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5489-121">Request headers</span></span>
| <span data-ttu-id="e5489-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5489-122">Header</span></span>       | <span data-ttu-id="e5489-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e5489-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e5489-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="e5489-124">Authorization</span></span>  | <span data-ttu-id="e5489-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e5489-p103">Bearer {token}. Required.</span></span>  |


## <a name="request-body"></a><span data-ttu-id="e5489-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e5489-127">Request body</span></span>
<span data-ttu-id="e5489-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e5489-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="e5489-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5489-129">Response</span></span>
<span data-ttu-id="e5489-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationSchool](../resources/educationschool.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5489-130">If successful, this method returns a `200 OK` response code and a collection of [educationSchool](../resources/educationschool.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e5489-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5489-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e5489-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5489-132">Request</span></span>
<span data-ttu-id="e5489-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5489-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_schools"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/11014/schools
```
##### <a name="response"></a><span data-ttu-id="e5489-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5489-134">Response</span></span>
<span data-ttu-id="e5489-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5489-135">The following is an example of the response.</span></span> 

><span data-ttu-id="e5489-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e5489-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
