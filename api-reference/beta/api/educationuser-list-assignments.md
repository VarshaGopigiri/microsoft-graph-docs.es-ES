---
title: Asignaciones de listas
description: Devuelve una lista de las asignaciones asignadas a un usuario para todas las clases. Este espacio de nombres de utilidad permite que un autor de la llamada buscar las asignaciones de todos los de un estudiante en una única llamada en lugar de tener que solicitar las asignaciones de cada clase. La lista de asignación contiene lo que se necesita para obtener la información detallada para la asignación de espacio de nombres de clase. Todas las otras operaciones en la asignación deben usar el espacio de nombres de clase.
localization_priority: Normal
ms.openlocfilehash: 92a52f38a305515824a34e87bc3d23d16a2be4c7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883207"
---
# <a name="list-assignments"></a><span data-ttu-id="6d0ff-106">Asignaciones de listas</span><span class="sxs-lookup"><span data-stu-id="6d0ff-106">List assignments</span></span>

> <span data-ttu-id="6d0ff-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6d0ff-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6d0ff-109">Devuelve una lista de las asignaciones asignadas a un usuario para todas las clases.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-109">Returns a list of assignments assigned to a user for all classes.</span></span> <span data-ttu-id="6d0ff-110">Este espacio de nombres de utilidad permite que un autor de la llamada buscar las asignaciones de todos los de un estudiante en una única llamada en lugar de tener que solicitar las asignaciones de cada clase.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-110">This utility namespace allows a caller to find all a student's assignments in a single call rather than having to request assignments from each class.</span></span> <span data-ttu-id="6d0ff-111">La lista de asignación contiene lo que se necesita para obtener la información detallada para la asignación de espacio de nombres de clase.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-111">The assignment list contains what is needed to get the detailed information for the assignment from within the class namespace.</span></span> <span data-ttu-id="6d0ff-112">Todas las otras operaciones en la asignación deben usar el espacio de nombres de clase.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-112">All other operations on the assignment should use the class namespace.</span></span>

## <a name="permissions"></a><span data-ttu-id="6d0ff-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="6d0ff-113">Permissions</span></span>
<span data-ttu-id="6d0ff-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6d0ff-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6d0ff-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6d0ff-116">Permission type</span></span>      | <span data-ttu-id="6d0ff-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6d0ff-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6d0ff-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6d0ff-118">Delegated (work or school account)</span></span> | <span data-ttu-id="6d0ff-119">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6d0ff-119">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="6d0ff-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6d0ff-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6d0ff-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-121">Not supported.</span></span>   |
|<span data-ttu-id="6d0ff-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6d0ff-122">Application</span></span> | <span data-ttu-id="6d0ff-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-123">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="6d0ff-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6d0ff-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me/assignments/
GET /education/users/{id}/assignments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6d0ff-125">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6d0ff-125">Optional query parameters</span></span>
<span data-ttu-id="6d0ff-126">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-126">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6d0ff-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6d0ff-127">Request headers</span></span>
| <span data-ttu-id="6d0ff-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d0ff-128">Header</span></span>       | <span data-ttu-id="6d0ff-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6d0ff-129">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6d0ff-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="6d0ff-130">Authorization</span></span>  | <span data-ttu-id="6d0ff-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="6d0ff-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6d0ff-133">Request body</span></span>
<span data-ttu-id="6d0ff-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-134">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="6d0ff-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d0ff-135">Response</span></span>
<span data-ttu-id="6d0ff-136">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [educationAssignment](../resources/educationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-136">If successful, this method returns a `200 OK` response code and a collection of [educationAssignment](../resources/educationassignment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6d0ff-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d0ff-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6d0ff-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6d0ff-138">Request</span></span>
<span data-ttu-id="6d0ff-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-139">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_assignments"
}-->
```http 
GET https://graph.microsoft.com/beta/education/me/assignments
```
##### <a name="response"></a><span data-ttu-id="6d0ff-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d0ff-140">Response</span></span>
<span data-ttu-id="6d0ff-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-141">The following is an example of the response.</span></span> 

><span data-ttu-id="6d0ff-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6d0ff-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
      "assignDateTime": "2014-01-01T00:00:00Z",
      "assignTo": {"@odata.type": "microsoft.graph.educationAssignmentRecipient"},
      "assignedDateTime": "2014-01-01T00:00:00Z",
      "classId": "11010",
      "createdBy": {
        "user": {
            "displayName": "Susana Rocha",
            "id": "14012"
          }
      },
      "createdDateTime": "2014-01-01T00:00:00Z",
      "displayName": "Assignment 1",
      "dueDateTime": "2014-01-01T00:00:00Z",
      "grading": {
        "@odata.type": "#microsoft.graph.educationAssignmentPointsGradeType",
        "maxPoints": 100
      },
      "instructions": {
        "content": "Answer every question correctly",
        "contentType": "Text"
      },
      "lastModifiedBy": {
        "user": {
            "displayName": "Susana Rocha",
            "id": "14012"
          }
      },
      "lastModifiedDateTime": "2014-01-01T00:00:00Z",
      "status": "assigned"
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
