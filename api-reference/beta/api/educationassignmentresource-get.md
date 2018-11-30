---
title: Obtener educationAssignmentResource
description: 'Obtener las propiedades de un recurso específico en una asignación.  '
ms.openlocfilehash: fb557e72082476e4bcecc6328dd97717f7221d01
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088061"
---
# <a name="get-educationassignmentresource"></a><span data-ttu-id="670c9-103">Obtener educationAssignmentResource</span><span class="sxs-lookup"><span data-stu-id="670c9-103">Get educationAssignmentResource</span></span>

> <span data-ttu-id="670c9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="670c9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="670c9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="670c9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="670c9-106">Obtener las propiedades de un recurso específico en una asignación.</span><span class="sxs-lookup"><span data-stu-id="670c9-106">Get the properties of a specific resource on an assignment.</span></span>  
## <a name="permissions"></a><span data-ttu-id="670c9-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="670c9-107">Permissions</span></span>
<span data-ttu-id="670c9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="670c9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="670c9-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="670c9-110">Permission type</span></span>      | <span data-ttu-id="670c9-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="670c9-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="670c9-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="670c9-112">Delegated (work or school account)</span></span> | <span data-ttu-id="670c9-113">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="670c9-113">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span></span>   |
|<span data-ttu-id="670c9-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="670c9-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="670c9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="670c9-115">Not supported.</span></span>  |
|<span data-ttu-id="670c9-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="670c9-116">Application</span></span> |  <span data-ttu-id="670c9-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="670c9-117">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="670c9-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="670c9-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/assignments/{id}/resources/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="670c9-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="670c9-119">Optional query parameters</span></span>
<span data-ttu-id="670c9-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="670c9-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="670c9-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="670c9-121">Request headers</span></span>
| <span data-ttu-id="670c9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="670c9-122">Header</span></span>       | <span data-ttu-id="670c9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="670c9-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="670c9-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="670c9-124">Authorization</span></span>  | <span data-ttu-id="670c9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="670c9-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="670c9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="670c9-127">Request body</span></span>
<span data-ttu-id="670c9-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="670c9-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="670c9-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="670c9-129">Response</span></span>
<span data-ttu-id="670c9-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [educationAssignmentResource](../resources/educationassignmentresource.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="670c9-130">If successful, this method returns a `200 OK` response code and an [educationAssignmentResource](../resources/educationassignmentresource.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="670c9-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="670c9-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="670c9-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="670c9-132">Request</span></span>
<span data-ttu-id="670c9-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="670c9-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_educationassignmentresource"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/resources/22002
```
##### <a name="response"></a><span data-ttu-id="670c9-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="670c9-134">Response</span></span>
<span data-ttu-id="670c9-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="670c9-135">The following is an example of the response.</span></span> 

><span data-ttu-id="670c9-136">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="670c9-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="670c9-137">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="670c9-137">All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignmentResource"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 842

{
  "distributeForStudentWork": true,
  "id": "22002",
  "resource": {
    "createdBy": {
      "user": {
        "displayName": "Susana Rocha",
        "id": "14012"
      },
    },
    "createdDateTime": "2014-01-01T00:00:00Z",
    "displayName": "Excel workbook 1",
    "lastModifiedBy": {
      "user": {
        "displayName": "Susana Rocha",
        "id": "14012"
      },
    },
    "lastModifiedDateTime": "2014-01-01T00:00:00Z"
  }
}
    
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get educationAssignmentResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->