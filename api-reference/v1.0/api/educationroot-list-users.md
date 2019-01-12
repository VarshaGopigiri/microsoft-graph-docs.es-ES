---
title: List users
description: Recupera una lista de objetos de usuario. Estos objetos de usuario incluirán propiedades específicas del ámbito educativo.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 9c3614815dd2d43f0b1c43a2ad90eeca73a4782c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982473"
---
# <a name="list-users"></a><span data-ttu-id="ce9f3-104">List users</span><span class="sxs-lookup"><span data-stu-id="ce9f3-104">List users</span></span>

<span data-ttu-id="ce9f3-105">Recupera una lista de objetos de usuario.</span><span class="sxs-lookup"><span data-stu-id="ce9f3-105">Retrieve a list of user objects.</span></span> <span data-ttu-id="ce9f3-106">Estos objetos de usuario incluirán propiedades específicas del ámbito educativo.</span><span class="sxs-lookup"><span data-stu-id="ce9f3-106">These user objects will include education-specific properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="ce9f3-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ce9f3-107">Permissions</span></span>
<span data-ttu-id="ce9f3-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ce9f3-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ce9f3-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ce9f3-110">Permission type</span></span>      | <span data-ttu-id="ce9f3-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ce9f3-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ce9f3-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ce9f3-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="ce9f3-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce9f3-113">Not supported.</span></span>  |
|<span data-ttu-id="ce9f3-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ce9f3-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="ce9f3-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce9f3-115">Not supported.</span></span>  |
|<span data-ttu-id="ce9f3-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ce9f3-116">Application</span></span> | <span data-ttu-id="ce9f3-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ce9f3-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="ce9f3-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ce9f3-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/users
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ce9f3-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ce9f3-119">Optional query parameters</span></span>
<span data-ttu-id="ce9f3-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce9f3-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ce9f3-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ce9f3-121">Request headers</span></span>
| <span data-ttu-id="ce9f3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce9f3-122">Header</span></span>       | <span data-ttu-id="ce9f3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ce9f3-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ce9f3-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ce9f3-124">Authorization</span></span>  | <span data-ttu-id="ce9f3-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ce9f3-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ce9f3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ce9f3-127">Request body</span></span>
<span data-ttu-id="ce9f3-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ce9f3-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="ce9f3-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce9f3-129">Response</span></span>
<span data-ttu-id="ce9f3-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationUser](../resources/educationuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce9f3-130">If successful, this method returns a `200 OK` response code and a collection of [educationUser](../resources/educationuser.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ce9f3-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce9f3-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ce9f3-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ce9f3-132">Request</span></span>
<span data-ttu-id="ce9f3-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce9f3-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_users"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/users
```
##### <a name="response"></a><span data-ttu-id="ce9f3-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce9f3-134">Response</span></span>
<span data-ttu-id="ce9f3-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce9f3-135">The following is an example of the response.</span></span> 

><span data-ttu-id="ce9f3-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ce9f3-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
      "middleName": null,
      "surname": "Matheson",
      "mail": "DionM@contoso.com",
      "mobilePhone": "+1 (253) 555-0101",
      "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012"
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
