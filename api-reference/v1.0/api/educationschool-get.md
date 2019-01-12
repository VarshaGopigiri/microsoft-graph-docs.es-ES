---
title: Obtener educationSchool
description: Recupere las propiedades y relaciones del objeto de centro educativo.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 6b43360dd6582cb0f9c0f84166eb27e362dd0e0a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976950"
---
# <a name="get-educationschool"></a><span data-ttu-id="ba9a7-103">Obtener educationSchool</span><span class="sxs-lookup"><span data-stu-id="ba9a7-103">Get educationSchool</span></span>

<span data-ttu-id="ba9a7-104">Recupere las propiedades y relaciones del objeto de centro educativo.</span><span class="sxs-lookup"><span data-stu-id="ba9a7-104">Retrieve the properties and relationships of the school object.</span></span>

## <a name="permissions"></a><span data-ttu-id="ba9a7-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ba9a7-105">Permissions</span></span>
<span data-ttu-id="ba9a7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ba9a7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ba9a7-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ba9a7-108">Permission type</span></span>      | <span data-ttu-id="ba9a7-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ba9a7-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ba9a7-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ba9a7-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="ba9a7-111">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="ba9a7-111">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="ba9a7-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ba9a7-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="ba9a7-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba9a7-113">Not supported.</span></span>  |
|<span data-ttu-id="ba9a7-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ba9a7-114">Application</span></span> | <span data-ttu-id="ba9a7-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ba9a7-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="ba9a7-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ba9a7-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/schools
GET /education/me/schools
GET /education/users/schools
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ba9a7-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ba9a7-117">Optional query parameters</span></span>
<span data-ttu-id="ba9a7-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba9a7-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ba9a7-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ba9a7-119">Request headers</span></span>
| <span data-ttu-id="ba9a7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba9a7-120">Header</span></span>       | <span data-ttu-id="ba9a7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ba9a7-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ba9a7-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="ba9a7-122">Authorization</span></span>  | <span data-ttu-id="ba9a7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ba9a7-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ba9a7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ba9a7-125">Request body</span></span>
<span data-ttu-id="ba9a7-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ba9a7-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="ba9a7-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba9a7-127">Response</span></span>
<span data-ttu-id="ba9a7-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationSchool](../resources/educationschool.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba9a7-128">If successful, this method returns a `200 OK` response code and an [educationSchool](../resources/educationschool.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ba9a7-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba9a7-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ba9a7-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ba9a7-130">Request</span></span>
<span data-ttu-id="ba9a7-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ba9a7-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_educationschool"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/schools/{school-id}
```
##### <a name="response"></a><span data-ttu-id="ba9a7-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba9a7-132">Response</span></span>
<span data-ttu-id="ba9a7-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba9a7-133">The following is an example of the response.</span></span> 

><span data-ttu-id="ba9a7-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ba9a7-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
