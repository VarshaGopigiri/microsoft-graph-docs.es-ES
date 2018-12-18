---
title: List users
description: Recupera una lista de objetos de usuario. Estos objetos de usuario incluirán propiedades específicas del ámbito educativo.
author: mmast-msft
ms.openlocfilehash: dd7d086b4471b2938cb5480f9d351a46a27e1f06
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27338503"
---
# <a name="list-users"></a><span data-ttu-id="39dfc-104">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="39dfc-104">List users</span></span>

> <span data-ttu-id="39dfc-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="39dfc-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="39dfc-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="39dfc-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="39dfc-107">Recupera una lista de objetos de usuario.</span><span class="sxs-lookup"><span data-stu-id="39dfc-107">Retrieve a list of user objects.</span></span> <span data-ttu-id="39dfc-108">Estos objetos de usuario incluirán propiedades específicas del ámbito educativo.</span><span class="sxs-lookup"><span data-stu-id="39dfc-108">These user objects will include education-specific properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="39dfc-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="39dfc-109">Permissions</span></span>
<span data-ttu-id="39dfc-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="39dfc-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="39dfc-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="39dfc-112">Permission type</span></span>      | <span data-ttu-id="39dfc-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="39dfc-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="39dfc-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="39dfc-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="39dfc-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39dfc-115">Not supported.</span></span>  |
|<span data-ttu-id="39dfc-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="39dfc-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="39dfc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39dfc-117">Not supported.</span></span>  |
|<span data-ttu-id="39dfc-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="39dfc-118">Application</span></span> | <span data-ttu-id="39dfc-119">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="39dfc-119">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="39dfc-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="39dfc-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/users
```
## <a name="optional-query-parameters"></a><span data-ttu-id="39dfc-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="39dfc-121">Optional query parameters</span></span>
<span data-ttu-id="39dfc-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39dfc-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="39dfc-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="39dfc-123">Request headers</span></span>
| <span data-ttu-id="39dfc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39dfc-124">Header</span></span>       | <span data-ttu-id="39dfc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="39dfc-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="39dfc-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="39dfc-126">Authorization</span></span>  | <span data-ttu-id="39dfc-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="39dfc-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="39dfc-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="39dfc-129">Request body</span></span>
<span data-ttu-id="39dfc-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="39dfc-130">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="39dfc-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39dfc-131">Response</span></span>
<span data-ttu-id="39dfc-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationUser](../resources/educationuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39dfc-132">If successful, this method returns a `200 OK` response code and a collection of [educationUser](../resources/educationuser.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="39dfc-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39dfc-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="39dfc-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="39dfc-134">Request</span></span>
<span data-ttu-id="39dfc-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39dfc-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_users"
}-->
```http
GET https://graph.microsoft.com/beta/education/users
```
##### <a name="response"></a><span data-ttu-id="39dfc-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39dfc-136">Response</span></span>
<span data-ttu-id="39dfc-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39dfc-137">The following is an example of the response.</span></span> 

><span data-ttu-id="39dfc-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="39dfc-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
