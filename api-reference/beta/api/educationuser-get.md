---
title: Obtener educationUser
description: Recupere las propiedades y relaciones de un usuario.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: adcdc634129dc2d4e58941a86d52989e774535e3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956482"
---
# <a name="get-educationuser"></a><span data-ttu-id="1d6f2-103">Obtener educationUser</span><span class="sxs-lookup"><span data-stu-id="1d6f2-103">Get educationUser</span></span>

> <span data-ttu-id="1d6f2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d6f2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d6f2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d6f2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1d6f2-106">Recupere las propiedades y relaciones de un usuario.</span><span class="sxs-lookup"><span data-stu-id="1d6f2-106">Retrieve the properties and relationships of a user.</span></span>

## <a name="permissions"></a><span data-ttu-id="1d6f2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1d6f2-107">Permissions</span></span>
<span data-ttu-id="1d6f2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d6f2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d6f2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d6f2-110">Permission type</span></span>      | <span data-ttu-id="1d6f2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d6f2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1d6f2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d6f2-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="1d6f2-113">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="1d6f2-113">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="1d6f2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d6f2-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="1d6f2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d6f2-115">Not supported.</span></span>  |
|<span data-ttu-id="1d6f2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d6f2-116">Application</span></span> | <span data-ttu-id="1d6f2-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d6f2-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 
## <a name="http-request"></a><span data-ttu-id="1d6f2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d6f2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me
GET /education/users/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1d6f2-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1d6f2-119">Optional query parameters</span></span>
<span data-ttu-id="1d6f2-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d6f2-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1d6f2-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d6f2-121">Request headers</span></span>
| <span data-ttu-id="1d6f2-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d6f2-122">Header</span></span>       | <span data-ttu-id="1d6f2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1d6f2-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="1d6f2-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="1d6f2-124">Authorization</span></span>  | <span data-ttu-id="1d6f2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1d6f2-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1d6f2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d6f2-127">Request body</span></span>
<span data-ttu-id="1d6f2-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1d6f2-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="1d6f2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d6f2-129">Response</span></span>
<span data-ttu-id="1d6f2-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationUser](../resources/educationuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d6f2-130">If successful, this method returns a `200 OK` response code and an [educationUser](../resources/educationuser.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1d6f2-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d6f2-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1d6f2-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d6f2-132">Request</span></span>
<span data-ttu-id="1d6f2-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d6f2-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_educationuser"
}-->
```http
GET https://graph.microsoft.com/beta/education/users/13012
```
##### <a name="response"></a><span data-ttu-id="1d6f2-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d6f2-134">Response</span></span>
<span data-ttu-id="1d6f2-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d6f2-135">The following is an example of the response.</span></span> 

><span data-ttu-id="1d6f2-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d6f2-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationUser"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 508

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
  },
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get educationUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
