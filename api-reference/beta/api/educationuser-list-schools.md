---
title: Enumerar centros educativos
description: Recupere una lista de centros educativos de un usuario.
author: mmast-msft
ms.openlocfilehash: 35810f4b1928249576ac1216356701489f68feca
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303272"
---
# <a name="list-schools"></a><span data-ttu-id="ef140-103">Enumerar centros educativos</span><span class="sxs-lookup"><span data-stu-id="ef140-103">List schools</span></span>

> <span data-ttu-id="ef140-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ef140-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ef140-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ef140-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ef140-106">Recupere una lista de centros educativos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="ef140-106">Retrieve a list of schools for a user.</span></span>

><span data-ttu-id="ef140-107">**Nota:** Si se usa el token delegado, los miembros solo pueden ver información sobre sus propios centros educativos.</span><span class="sxs-lookup"><span data-stu-id="ef140-107">**Note:** If the delegated token is used, members can only see information about their own schools.</span></span> <span data-ttu-id="ef140-108">Use el recurso `...beta/education/me/schools` en este caso.</span><span class="sxs-lookup"><span data-stu-id="ef140-108">Use the `...beta/education/me/schools` resource in this case.</span></span>

## <a name="permissions"></a><span data-ttu-id="ef140-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="ef140-109">Permissions</span></span>
<span data-ttu-id="ef140-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ef140-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ef140-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ef140-112">Permission type</span></span>      | <span data-ttu-id="ef140-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ef140-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ef140-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ef140-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="ef140-115">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="ef140-115">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="ef140-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ef140-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="ef140-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ef140-117">Not supported.</span></span>  |
|<span data-ttu-id="ef140-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ef140-118">Application</span></span> | <span data-ttu-id="ef140-119">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ef140-119">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="ef140-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ef140-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me/schools
GET /education/users/{id}/schools
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ef140-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ef140-121">Optional query parameters</span></span>
<span data-ttu-id="ef140-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef140-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ef140-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ef140-123">Request headers</span></span>
| <span data-ttu-id="ef140-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef140-124">Header</span></span>       | <span data-ttu-id="ef140-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ef140-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ef140-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="ef140-126">Authorization</span></span>  | <span data-ttu-id="ef140-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ef140-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ef140-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ef140-129">Request body</span></span>
<span data-ttu-id="ef140-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ef140-130">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="ef140-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef140-131">Response</span></span>
<span data-ttu-id="ef140-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationSchool](../resources/educationschool.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef140-132">If successful, this method returns a `200 OK` response code and a collection of [educationSchool](../resources/educationschool.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ef140-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef140-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ef140-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ef140-134">Request</span></span>
<span data-ttu-id="ef140-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef140-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_schools"
}-->
```http
GET https://graph.microsoft.com/beta/education/me/schools
```
##### <a name="response"></a><span data-ttu-id="ef140-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef140-136">Response</span></span>
<span data-ttu-id="ef140-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef140-137">The following is an example of the response.</span></span> 

><span data-ttu-id="ef140-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ef140-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSchool",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 345

{
  "value": [
    {
      "id": "10001",
      "displayName": "Contoso High School",
      "description": "Public 9-12 high school",
      "status": "active",
      "externalSource": "sis",
      "principalEmail": "amyr@contoso.com",
      "principalName": "Amy Roebuck",
      "externalPrincipalId": "14007",
      "highestGrade": "12",
      "lowestGrade": "9",
      "schoolNumber": "10001",
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
      "externalId": "10001",
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