---
title: Obtener educationAssignment
description: " los profesores pueden ver todas las asignaciones de una clase."
author: dipakboyed
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 66279d72952a561a5e98be00ae268ca58c5dcc92
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976404"
---
# <a name="get-educationassignment"></a><span data-ttu-id="2a164-103">Obtener educationAssignment</span><span class="sxs-lookup"><span data-stu-id="2a164-103">Get educationAssignment</span></span>

> <span data-ttu-id="2a164-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2a164-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2a164-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2a164-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2a164-106">Obtener las propiedades y relaciones de una asignación.</span><span class="sxs-lookup"><span data-stu-id="2a164-106">Get the properties and relationships of an assignment.</span></span> <span data-ttu-id="2a164-107">Los alumnos sólo pueden ver las asignaciones asignadas a ellos; los profesores pueden ver todas las asignaciones de una clase.</span><span class="sxs-lookup"><span data-stu-id="2a164-107">Students can only see assignments assigned to them; teachers can see all assignments in a class.</span></span>

## <a name="permissions"></a><span data-ttu-id="2a164-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="2a164-108">Permissions</span></span>
<span data-ttu-id="2a164-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2a164-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="2a164-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2a164-111">Permission type</span></span>      | <span data-ttu-id="2a164-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2a164-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2a164-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2a164-113">Delegated (work or school account)</span></span> | <span data-ttu-id="2a164-114">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2a164-114">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span></span> |
|<span data-ttu-id="2a164-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2a164-115">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="2a164-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2a164-116">Not supported.</span></span>  |
|<span data-ttu-id="2a164-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2a164-117">Application</span></span> | <span data-ttu-id="2a164-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2a164-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="2a164-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2a164-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/assignments/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="2a164-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2a164-120">Optional query parameters</span></span>
<span data-ttu-id="2a164-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a164-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2a164-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2a164-122">Request headers</span></span>
| <span data-ttu-id="2a164-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a164-123">Header</span></span>       | <span data-ttu-id="2a164-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2a164-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2a164-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="2a164-125">Authorization</span></span>  | <span data-ttu-id="2a164-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a164-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2a164-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2a164-128">Request body</span></span>
<span data-ttu-id="2a164-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2a164-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2a164-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a164-130">Response</span></span>
<span data-ttu-id="2a164-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [educationAssignment](../resources/educationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a164-131">If successful, this method returns a `200 OK` response code and an [educationAssignment](../resources/educationassignment.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2a164-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a164-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2a164-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2a164-133">Request</span></span>
<span data-ttu-id="2a164-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a164-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_educationassignment"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/11014/assignments/19002
```
##### <a name="response"></a><span data-ttu-id="2a164-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a164-135">Response</span></span>
<span data-ttu-id="2a164-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a164-136">The following is an example of the response.</span></span> 

><span data-ttu-id="2a164-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2a164-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 279

{
  "id": "19002",
  "allowLateSubmissions": true,
  "allowStudentsToAddResourcesToSubmission": true,
  "assignDateTime": "String (timestamp)",
  "assignTo": {"@odata.type": "microsoft.graph.educationAssignmentRecipient"},
  "assignedDateTime": "2014-01-01T00:00:00Z",
  "classId": "11006",
  "createdBy": {
    "user": {
      "displayName": "Susana Rocha",
      "id": "14012",
    }
  },
  "createdDateTime": "2014-01-01T00:00:00Z",
  "displayName": "Mid term exam",
  "dueDateTime": "2014-01-11T00:00:00Z",
  "grading": {
      "@odata.type": "microsoft.graph.educationAssignmentPointsGradeType",
      "maxPoints": 100
  },
  "instructions": {
    "content": "Answer every question correctly",
    "contentType": "Text"
  },
  "lastModifiedBy": {
    "user": {
      "displayName": "Susana Rocha",
      "id": "14012",
    }
  },
  "lastModifiedDateTime": "2014-01-01T00:00:00Z",
  "status": "assigned"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get educationAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
