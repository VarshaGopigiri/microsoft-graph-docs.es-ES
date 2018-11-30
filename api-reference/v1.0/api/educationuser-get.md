---
title: Obtener educationUser
description: Recupere las propiedades y relaciones de un usuario.
ms.openlocfilehash: ecf762db4061694ee07d9212d4b542597313b9e0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029158"
---
# <a name="get-educationuser"></a><span data-ttu-id="e185d-103">Obtener educationUser</span><span class="sxs-lookup"><span data-stu-id="e185d-103">Get educationUser</span></span>

<span data-ttu-id="e185d-104">Recupere las propiedades y relaciones de un usuario.</span><span class="sxs-lookup"><span data-stu-id="e185d-104">Retrieve the properties and relationships of a user.</span></span>

## <a name="permissions"></a><span data-ttu-id="e185d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e185d-105">Permissions</span></span>
<span data-ttu-id="e185d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e185d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e185d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e185d-108">Permission type</span></span>      | <span data-ttu-id="e185d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e185d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e185d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e185d-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="e185d-111">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="e185d-111">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="e185d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e185d-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="e185d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e185d-113">Not supported.</span></span>  |
|<span data-ttu-id="e185d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e185d-114">Application</span></span> | <span data-ttu-id="e185d-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e185d-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 
## <a name="http-request"></a><span data-ttu-id="e185d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e185d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me
GET /education/users/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e185d-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e185d-117">Optional query parameters</span></span>
<span data-ttu-id="e185d-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e185d-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e185d-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e185d-119">Request headers</span></span>
| <span data-ttu-id="e185d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e185d-120">Header</span></span>       | <span data-ttu-id="e185d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e185d-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e185d-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="e185d-122">Authorization</span></span>  | <span data-ttu-id="e185d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e185d-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e185d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e185d-125">Request body</span></span>
<span data-ttu-id="e185d-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e185d-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="e185d-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e185d-127">Response</span></span>
<span data-ttu-id="e185d-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationUser](../resources/educationuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e185d-128">If successful, this method returns a `200 OK` response code and an [educationUser](../resources/educationuser.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e185d-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e185d-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e185d-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e185d-130">Request</span></span>
<span data-ttu-id="e185d-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e185d-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_educationuser"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/users/{user-id}
```
##### <a name="response"></a><span data-ttu-id="e185d-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e185d-132">Response</span></span>
<span data-ttu-id="e185d-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e185d-133">The following is an example of the response.</span></span> 

><span data-ttu-id="e185d-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e185d-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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