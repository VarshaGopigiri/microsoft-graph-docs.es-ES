---
title: Crear educationUser
description: Cree otro usuario.
author: mmast-msft
ms.openlocfilehash: 4d55d1678dca04e4ad8745e687931b6382f96486
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303503"
---
# <a name="create-educationuser"></a><span data-ttu-id="accd6-103">Crear educationUser</span><span class="sxs-lookup"><span data-stu-id="accd6-103">Create educationUser</span></span>

<span data-ttu-id="accd6-104">Cree otro usuario.</span><span class="sxs-lookup"><span data-stu-id="accd6-104">Create a new user.</span></span>

<!-- Add some additional text to better distinguish this method from the user_post_users (https://developer.microsoft.com/graph/docs/api-reference/v1.0/api/user_post_users) topic. -->

## <a name="permissions"></a><span data-ttu-id="accd6-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="accd6-105">Permissions</span></span>
<span data-ttu-id="accd6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="accd6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="accd6-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="accd6-108">Permission type</span></span>      | <span data-ttu-id="accd6-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="accd6-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="accd6-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="accd6-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="accd6-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="accd6-111">Not supported.</span></span>  |
|<span data-ttu-id="accd6-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="accd6-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="accd6-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="accd6-113">Not supported.</span></span>  |
|<span data-ttu-id="accd6-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="accd6-114">Application</span></span> | <span data-ttu-id="accd6-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="accd6-115">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="accd6-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="accd6-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/users
```
## <a name="request-headers"></a><span data-ttu-id="accd6-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="accd6-117">Request headers</span></span>
| <span data-ttu-id="accd6-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="accd6-118">Header</span></span>       | <span data-ttu-id="accd6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="accd6-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="accd6-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="accd6-120">Authorization</span></span>  | <span data-ttu-id="accd6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="accd6-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="accd6-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="accd6-123">Content-Type</span></span>  | <span data-ttu-id="accd6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="accd6-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="accd6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="accd6-125">Request body</span></span>
<span data-ttu-id="accd6-126">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationUser](../resources/educationuser.md).</span><span class="sxs-lookup"><span data-stu-id="accd6-126">In the request body, supply a JSON representation of an [educationUser](../resources/educationuser.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="accd6-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="accd6-127">Response</span></span>
<span data-ttu-id="accd6-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [educationUser](../resources/educationuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="accd6-128">If successful, this method returns a `201 Created` response code and an [educationUser](../resources/educationuser.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="accd6-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="accd6-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="accd6-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="accd6-130">Request</span></span>
<span data-ttu-id="accd6-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="accd6-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationuser_from_educationroot"
}-->
```http
POST https://graph.microsoft.com/v1.0/education/users
Content-type: application/json
Content-length: 508

{
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
```

##### <a name="response"></a><span data-ttu-id="accd6-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="accd6-132">Response</span></span>
<span data-ttu-id="accd6-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="accd6-133">The following is an example of the response.</span></span> 

><span data-ttu-id="accd6-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="accd6-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationUser"
} -->
```http
HTTP/1.1 201 Created
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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->