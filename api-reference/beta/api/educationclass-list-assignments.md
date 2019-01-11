---
title: Asignaciones de listas
description: Recuperar una lista de objetos de asignación. Se permite un profesor para ver todos los objetos de asignación para la clase. Los alumnos sólo pueden ver las asignaciones que se les haya asignado.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: a58406f26b45ccf3b16b6ff6bfa17e38b52590e7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823922"
---
# <a name="list-assignments"></a><span data-ttu-id="4220e-105">Asignaciones de listas</span><span class="sxs-lookup"><span data-stu-id="4220e-105">List assignments</span></span>

> <span data-ttu-id="4220e-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4220e-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4220e-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4220e-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4220e-108">Recuperar una lista de objetos de asignación.</span><span class="sxs-lookup"><span data-stu-id="4220e-108">Retrieve a list of assignment objects.</span></span> <span data-ttu-id="4220e-109">Se permite un profesor para ver todos los objetos de asignación para la clase.</span><span class="sxs-lookup"><span data-stu-id="4220e-109">A teacher is allowed to see all assignment objects for the class.</span></span> <span data-ttu-id="4220e-110">Los alumnos sólo pueden ver las asignaciones que se les haya asignado.</span><span class="sxs-lookup"><span data-stu-id="4220e-110">Students can only see assignments that are assigned to them.</span></span>

## <a name="permissions"></a><span data-ttu-id="4220e-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="4220e-111">Permissions</span></span>
<span data-ttu-id="4220e-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4220e-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4220e-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4220e-114">Permission type</span></span>      | <span data-ttu-id="4220e-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4220e-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4220e-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4220e-116">Delegated (work or school account)</span></span> | <span data-ttu-id="4220e-117">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4220e-117">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span></span>   |
|<span data-ttu-id="4220e-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4220e-118">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="4220e-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4220e-119">Not supported.</span></span>  |
|<span data-ttu-id="4220e-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4220e-120">Application</span></span> | <span data-ttu-id="4220e-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4220e-121">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="4220e-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4220e-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/assignments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="4220e-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4220e-123">Optional query parameters</span></span>
<span data-ttu-id="4220e-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4220e-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="4220e-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4220e-125">Request headers</span></span>
| <span data-ttu-id="4220e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4220e-126">Header</span></span>       | <span data-ttu-id="4220e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4220e-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4220e-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="4220e-128">Authorization</span></span>  | <span data-ttu-id="4220e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4220e-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4220e-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4220e-131">Request body</span></span>
<span data-ttu-id="4220e-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4220e-132">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="4220e-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4220e-133">Response</span></span>
<span data-ttu-id="4220e-134">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [educationAssignment](../resources/educationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4220e-134">If successful, this method returns a `200 OK` response code and a collection of [educationAssignment](../resources/educationassignment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4220e-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4220e-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4220e-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4220e-136">Request</span></span>
<span data-ttu-id="4220e-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4220e-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_assignments"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/<id>/assignments
```
##### <a name="response"></a><span data-ttu-id="4220e-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4220e-138">Response</span></span>
<span data-ttu-id="4220e-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4220e-139">The following is an example of the response.</span></span> 

><span data-ttu-id="4220e-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4220e-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 344

{
  "value": [
    {
      "id": "19002",
      "allowLateSubmissions": true,
      "allowStudentsToAddResourcesToSubmission": true,
      "assignDateTime": "2014-02-01T00:00:00Z",
      "assignTo": {"@odata.type": "microsoft.graph.educationAssignmentRecipient"},
      "assignedDateTime": "2014-02-01T00:00:00Z",
      "classId": "11018",
      "createdBy": {
          "application": null,
          "device": null,
          "user": {
              "id": "63cc91d2-59c7-4732-9594-35b91a26b340",
              "displayName": null
          }
      },
      "createdDateTime": "2014-02-01T00:00:00Z",
      "displayName": "published",
      "dueDateTime": "2014-02-01T00:00:00Z",
      "grading": {
        "@odata.type": "#microsoft.graph.educationAssignmentPointsGradeType",
        "maxPoints": 100
      },
      "instructions": {
        "contentType": "Text",
        "content": "Read chapters 1 through 3"
      },
      "lastModifiedBy": {
          "application": null,
          "device": null,
          "user": {
              "id": "63cc91d2-59c7-4732-9594-35b91a26b340",
              "displayName": null
          }
      },
      "lastModifiedDateTime": "2014-02-01T00:00:00Z",
      "status": "published"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List assignments",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
