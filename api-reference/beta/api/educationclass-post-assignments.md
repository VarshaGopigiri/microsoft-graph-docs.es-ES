---
title: Crear educationAssignment
description: 'Crea una nueva asignación. Sólo los profesores en una clase pueden crear una asignación. Inician las asignaciones en el estado de borrador, lo que significa que los alumnos no verán la asignación hasta que se llama a publicar.  '
localization_priority: Normal
ms.openlocfilehash: 6bcc1f44be9d811335d24cea7502c0752052c5ab
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824188"
---
# <a name="create-educationassignment"></a><span data-ttu-id="45a79-105">Crear educationAssignment</span><span class="sxs-lookup"><span data-stu-id="45a79-105">Create educationAssignment</span></span>

> <span data-ttu-id="45a79-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="45a79-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="45a79-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="45a79-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="45a79-108">Crea una nueva asignación.</span><span class="sxs-lookup"><span data-stu-id="45a79-108">Creates a new assignment.</span></span> <span data-ttu-id="45a79-109">Sólo los profesores en una clase pueden crear una asignación.</span><span class="sxs-lookup"><span data-stu-id="45a79-109">Only teachers in a class can create an assignment.</span></span> <span data-ttu-id="45a79-110">Inician las asignaciones en el estado de borrador, lo que significa que los alumnos no verán la asignación hasta que se llama a publicar.</span><span class="sxs-lookup"><span data-stu-id="45a79-110">Assignments start in the Draft state, which means that students will not see the assignment until publish is called.</span></span>  

## <a name="permissions"></a><span data-ttu-id="45a79-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="45a79-111">Permissions</span></span>
<span data-ttu-id="45a79-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="45a79-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="45a79-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="45a79-114">Permission type</span></span>      | <span data-ttu-id="45a79-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="45a79-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="45a79-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="45a79-116">Delegated (work or school account)</span></span> |  <span data-ttu-id="45a79-117">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="45a79-117">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="45a79-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="45a79-118">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="45a79-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45a79-119">Not supported.</span></span>  |
|<span data-ttu-id="45a79-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="45a79-120">Application</span></span> | <span data-ttu-id="45a79-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45a79-121">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="45a79-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="45a79-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments

```
## <a name="request-headers"></a><span data-ttu-id="45a79-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="45a79-123">Request headers</span></span>
| <span data-ttu-id="45a79-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45a79-124">Header</span></span>       | <span data-ttu-id="45a79-125">Valor</span><span class="sxs-lookup"><span data-stu-id="45a79-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="45a79-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="45a79-126">Authorization</span></span>  | <span data-ttu-id="45a79-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="45a79-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="45a79-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="45a79-129">Content-Type</span></span>  | <span data-ttu-id="45a79-130">application/json</span><span class="sxs-lookup"><span data-stu-id="45a79-130">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="45a79-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="45a79-131">Request body</span></span>
<span data-ttu-id="45a79-132">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [educationAssignment](../resources/educationassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="45a79-132">In the request body, supply a JSON representation of an [educationAssignment](../resources/educationassignment.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="45a79-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45a79-133">Response</span></span>
<span data-ttu-id="45a79-134">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [educationAssignment](../resources/educationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45a79-134">If successful, this method returns a `201 Created` response code and an [educationAssignment](../resources/educationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="45a79-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="45a79-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="45a79-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="45a79-136">Request</span></span>
<span data-ttu-id="45a79-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="45a79-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "create_educationassignment_from_educationclass"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11019/assignments
Content-type: application/json
Content-length: 279

{ 
  "dueDateTime": "2014-02-01T00:00:00Z",
  "displayName": "Midterm 1",
    "instructions":  {
      "contentType": "Text",
      "content": "Read chapters 1 through 3"
    },
      "grading": {
        "@odata.type": "#microsoft.education.assignments.api.educationAssignmentPointsGradeType",
        "maxPoints": 100
      },
      "assignTo": {
        "@odata.type": "#microsoft.education.assignments.api.educationAssignmentClassRecipient"
      },
      "status":"draft",
      "allowStudentsToAddResourcesToSubmission": true
}
```
<span data-ttu-id="45a79-138">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [educationAssignment](../resources/educationassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="45a79-138">In the request body, supply a JSON representation of an [educationAssignment](../resources/educationassignment.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="45a79-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45a79-139">Response</span></span>
<span data-ttu-id="45a79-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45a79-140">The following is an example of the response.</span></span> 

><span data-ttu-id="45a79-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="45a79-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignment"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 279

{
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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
