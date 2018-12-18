---
title: Obtener educationSchool
description: Recupere las propiedades y relaciones del objeto de centro educativo.
author: mmast-msft
ms.openlocfilehash: 143d55ce3500f855fd912362f578d385347497c1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313492"
---
# <a name="get-educationschool"></a><span data-ttu-id="ed25f-103">Obtener educationSchool</span><span class="sxs-lookup"><span data-stu-id="ed25f-103">Get educationSchool</span></span>

> <span data-ttu-id="ed25f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ed25f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ed25f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ed25f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ed25f-106">Recupere las propiedades y relaciones del objeto de centro educativo.</span><span class="sxs-lookup"><span data-stu-id="ed25f-106">Retrieve the properties and relationships of the school object.</span></span>

## <a name="permissions"></a><span data-ttu-id="ed25f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ed25f-107">Permissions</span></span>
<span data-ttu-id="ed25f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ed25f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ed25f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ed25f-110">Permission type</span></span>      | <span data-ttu-id="ed25f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ed25f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ed25f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ed25f-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="ed25f-113">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="ed25f-113">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="ed25f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ed25f-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="ed25f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed25f-115">Not supported.</span></span>  |
|<span data-ttu-id="ed25f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ed25f-116">Application</span></span> | <span data-ttu-id="ed25f-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed25f-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="ed25f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ed25f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/schools
GET /education/me/schools
GET /education/users/schools
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ed25f-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ed25f-119">Optional query parameters</span></span>
<span data-ttu-id="ed25f-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed25f-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ed25f-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ed25f-121">Request headers</span></span>
| <span data-ttu-id="ed25f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed25f-122">Header</span></span>       | <span data-ttu-id="ed25f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ed25f-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ed25f-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ed25f-124">Authorization</span></span>  | <span data-ttu-id="ed25f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed25f-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ed25f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ed25f-127">Request body</span></span>
<span data-ttu-id="ed25f-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ed25f-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="ed25f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed25f-129">Response</span></span>
<span data-ttu-id="ed25f-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationSchool](../resources/educationschool.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed25f-130">If successful, this method returns a `200 OK` response code and an [educationSchool](../resources/educationschool.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ed25f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed25f-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ed25f-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ed25f-132">Request</span></span>
<span data-ttu-id="ed25f-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ed25f-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_educationschool"
}-->
```http
GET https://graph.microsoft.com/beta/education/schools/10001
```
##### <a name="response"></a><span data-ttu-id="ed25f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed25f-134">Response</span></span>
<span data-ttu-id="ed25f-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed25f-135">The following is an example of the response.</span></span> 

><span data-ttu-id="ed25f-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ed25f-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
  "schoolPrincipalEmail": "AmyRoebuck@contoso.com",
  "schoolPrincipalName": "Amy Roebuck",
  "externalSchoolPrincipalId": "14007",
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