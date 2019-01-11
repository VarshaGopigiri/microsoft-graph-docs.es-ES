---
title: Crear educationUser
description: Cree otro usuario.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 1636d137ae1a5b8938a59acf60a5eaae578e83f7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892158"
---
# <a name="create-educationuser"></a><span data-ttu-id="e16cd-103">Crear educationUser</span><span class="sxs-lookup"><span data-stu-id="e16cd-103">Create educationUser</span></span>

> <span data-ttu-id="e16cd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e16cd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e16cd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e16cd-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e16cd-106">Cree otro usuario.</span><span class="sxs-lookup"><span data-stu-id="e16cd-106">Create a new user.</span></span>

<!-- Add some additional text to better distinguish this method from the user_post_users (https://developer.microsoft.com/graph/docs/api-reference/v1.0/api/user_post_users) topic. -->

## <a name="permissions"></a><span data-ttu-id="e16cd-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e16cd-107">Permissions</span></span>
<span data-ttu-id="e16cd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e16cd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e16cd-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e16cd-110">Permission type</span></span>      | <span data-ttu-id="e16cd-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e16cd-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e16cd-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e16cd-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="e16cd-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e16cd-113">Not supported.</span></span>  |
|<span data-ttu-id="e16cd-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e16cd-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="e16cd-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e16cd-115">Not supported.</span></span>  |
|<span data-ttu-id="e16cd-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e16cd-116">Application</span></span> | <span data-ttu-id="e16cd-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e16cd-117">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="e16cd-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e16cd-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/users
```
## <a name="request-headers"></a><span data-ttu-id="e16cd-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e16cd-119">Request headers</span></span>
| <span data-ttu-id="e16cd-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e16cd-120">Header</span></span>       | <span data-ttu-id="e16cd-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e16cd-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e16cd-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="e16cd-122">Authorization</span></span>  | <span data-ttu-id="e16cd-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e16cd-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="e16cd-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e16cd-125">Content-Type</span></span>  | <span data-ttu-id="e16cd-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e16cd-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e16cd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e16cd-127">Request body</span></span>
<span data-ttu-id="e16cd-128">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationUser](../resources/educationuser.md).</span><span class="sxs-lookup"><span data-stu-id="e16cd-128">In the request body, supply a JSON representation of an [educationUser](../resources/educationuser.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="e16cd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e16cd-129">Response</span></span>
<span data-ttu-id="e16cd-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [educationUser](../resources/educationuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e16cd-130">If successful, this method returns a `201 Created` response code and an [educationUser](../resources/educationuser.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e16cd-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e16cd-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e16cd-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e16cd-132">Request</span></span>
<span data-ttu-id="e16cd-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e16cd-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationuser_from_educationroot"
}-->
```http
POST https://graph.microsoft.com/beta/education/users
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

##### <a name="response"></a><span data-ttu-id="e16cd-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e16cd-134">Response</span></span>
<span data-ttu-id="e16cd-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e16cd-135">The following is an example of the response.</span></span> 

><span data-ttu-id="e16cd-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e16cd-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
