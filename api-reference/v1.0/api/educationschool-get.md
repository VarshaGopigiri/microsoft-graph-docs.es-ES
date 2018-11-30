---
title: Obtener educationSchool
description: Recupere las propiedades y relaciones del objeto de centro educativo.
ms.openlocfilehash: bfa3d680446578e48954f828e6f07fed787e3b95
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029982"
---
# <a name="get-educationschool"></a><span data-ttu-id="516f9-103">Obtener educationSchool</span><span class="sxs-lookup"><span data-stu-id="516f9-103">Get educationSchool</span></span>

<span data-ttu-id="516f9-104">Recupere las propiedades y relaciones del objeto de centro educativo.</span><span class="sxs-lookup"><span data-stu-id="516f9-104">Retrieve the properties and relationships of the school object.</span></span>

## <a name="permissions"></a><span data-ttu-id="516f9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="516f9-105">Permissions</span></span>
<span data-ttu-id="516f9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="516f9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="516f9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="516f9-108">Permission type</span></span>      | <span data-ttu-id="516f9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="516f9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="516f9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="516f9-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="516f9-111">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="516f9-111">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="516f9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="516f9-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="516f9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="516f9-113">Not supported.</span></span>  |
|<span data-ttu-id="516f9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="516f9-114">Application</span></span> | <span data-ttu-id="516f9-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="516f9-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="516f9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="516f9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/schools
GET /education/me/schools
GET /education/users/schools
```
## <a name="optional-query-parameters"></a><span data-ttu-id="516f9-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="516f9-117">Optional query parameters</span></span>
<span data-ttu-id="516f9-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="516f9-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="516f9-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="516f9-119">Request headers</span></span>
| <span data-ttu-id="516f9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="516f9-120">Header</span></span>       | <span data-ttu-id="516f9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="516f9-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="516f9-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="516f9-122">Authorization</span></span>  | <span data-ttu-id="516f9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="516f9-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="516f9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="516f9-125">Request body</span></span>
<span data-ttu-id="516f9-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="516f9-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="516f9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="516f9-127">Response</span></span>
<span data-ttu-id="516f9-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationSchool](../resources/educationschool.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="516f9-128">If successful, this method returns a `200 OK` response code and an [educationSchool](../resources/educationschool.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="516f9-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="516f9-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="516f9-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="516f9-130">Request</span></span>
<span data-ttu-id="516f9-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="516f9-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_educationschool"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/schools/{school-id}
```
##### <a name="response"></a><span data-ttu-id="516f9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="516f9-132">Response</span></span>
<span data-ttu-id="516f9-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="516f9-133">The following is an example of the response.</span></span> 

><span data-ttu-id="516f9-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="516f9-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSchool"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 292

{
  "principalEmail": "AmyRoebuck@contoso.com",
  "principalName": "Amy Roebuck",
  "externalPrincipalId": "14007",
  "lowestGrade": "9",
  "highestGrade": "12"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get educationSchool",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->