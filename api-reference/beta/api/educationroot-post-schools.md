---
title: Crear educationSchool
description: Cree un centro educativo.
ms.openlocfilehash: 2007da0974b42b305c66b617dfe4d6fd5eb0e4c9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083362"
---
# <a name="create-educationschool"></a><span data-ttu-id="99628-103">Crear educationSchool</span><span class="sxs-lookup"><span data-stu-id="99628-103">Create educationSchool</span></span>

> <span data-ttu-id="99628-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="99628-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="99628-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="99628-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="99628-106">Cree un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="99628-106">Create a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="99628-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="99628-107">Permissions</span></span>
<span data-ttu-id="99628-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="99628-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="99628-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="99628-110">Permission type</span></span>      | <span data-ttu-id="99628-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="99628-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="99628-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="99628-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="99628-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99628-113">Not supported.</span></span>  |
|<span data-ttu-id="99628-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="99628-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="99628-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99628-115">Not supported.</span></span>  |
|<span data-ttu-id="99628-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="99628-116">Application</span></span> | <span data-ttu-id="99628-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="99628-117">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="99628-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="99628-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/schools
```
## <a name="request-headers"></a><span data-ttu-id="99628-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="99628-119">Request headers</span></span>
| <span data-ttu-id="99628-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99628-120">Header</span></span>       | <span data-ttu-id="99628-121">Valor</span><span class="sxs-lookup"><span data-stu-id="99628-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="99628-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="99628-122">Authorization</span></span>  | <span data-ttu-id="99628-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="99628-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="99628-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="99628-125">Content-Type</span></span>  | <span data-ttu-id="99628-126">application/json</span><span class="sxs-lookup"><span data-stu-id="99628-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="99628-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="99628-127">Request body</span></span>
<span data-ttu-id="99628-128">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationSchool](../resources/educationschool.md).</span><span class="sxs-lookup"><span data-stu-id="99628-128">In the request body, supply a JSON representation of an [educationSchool](../resources/educationschool.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="99628-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99628-129">Response</span></span>
<span data-ttu-id="99628-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [educationSchool](../resources/educationschool.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99628-130">If successful, this method returns a `201 Created` response code and an [educationSchool](../resources/educationschool.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="99628-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="99628-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="99628-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="99628-132">Request</span></span>
<span data-ttu-id="99628-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="99628-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationschool_from_educationroot"
}-->
```http
POST https://graph.microsoft.com/beta/education/schools
Content-type: application/json
Content-length: 292

{
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
  "externalId": "10002",
  "fax": "+1 (253) 555-0101",
  "phone": "+1 (253) 555-0102",
}
```

##### <a name="response"></a><span data-ttu-id="99628-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99628-134">Response</span></span>
<span data-ttu-id="99628-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99628-135">The following is an example of the response.</span></span> 

><span data-ttu-id="99628-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="99628-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSchool"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 292

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationSchool",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->