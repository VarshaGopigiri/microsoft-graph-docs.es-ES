---
title: Actualizar educationsubmission
description: Agregue una calificación y comentarios a una presentación. Profesores solo pueden realizar esta operación. Tenga en cuenta que no tiene acceso a las propiedades de remuneración el permiso básico y, por lo tanto, no se puede escribir en calificación o comentarios. Esta acción no liberar remuneración y los comentarios al alumno. Un profesor debe realizar una acción de liberación explícita para los datos de calificación que se devuelven a los estudiantes.
ms.openlocfilehash: 64e9313c30ce97c2bdbfdb9d3b7fb3077208ab1d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087795"
---
# <a name="update-educationsubmission"></a><span data-ttu-id="7644d-107">Actualizar educationsubmission</span><span class="sxs-lookup"><span data-stu-id="7644d-107">Update educationsubmission</span></span>

> <span data-ttu-id="7644d-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7644d-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7644d-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7644d-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7644d-110">Agregue una calificación y comentarios a una presentación.</span><span class="sxs-lookup"><span data-stu-id="7644d-110">Add a grade and feedback to a submission.</span></span> <span data-ttu-id="7644d-111">Profesores solo pueden realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="7644d-111">Only teachers can perform this operation.</span></span> <span data-ttu-id="7644d-112">Tenga en cuenta que no tiene acceso a las propiedades de remuneración el permiso básico y, por lo tanto, no se puede escribir en calificación o comentarios.</span><span class="sxs-lookup"><span data-stu-id="7644d-112">Note that the Basic permission does not have access to the grade properties, and therefore cannot write to grade or feedback.</span></span> <span data-ttu-id="7644d-113">Esta acción no liberar remuneración y los comentarios al alumno.</span><span class="sxs-lookup"><span data-stu-id="7644d-113">This action does not release the grade and feedback to the student.</span></span> <span data-ttu-id="7644d-114">Un profesor debe realizar una acción de liberación explícita para los datos de calificación que se devuelven a los estudiantes.</span><span class="sxs-lookup"><span data-stu-id="7644d-114">A teacher must take an explicit release action for the grade data to be returned to the student.</span></span>

## <a name="permissions"></a><span data-ttu-id="7644d-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="7644d-115">Permissions</span></span>
<span data-ttu-id="7644d-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7644d-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7644d-118">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7644d-118">Permission type</span></span>      | <span data-ttu-id="7644d-119">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7644d-119">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7644d-120">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7644d-120">Delegated (work or school account)</span></span> |  <span data-ttu-id="7644d-121">EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7644d-121">EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="7644d-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7644d-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7644d-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7644d-123">Not supported.</span></span>   |
|<span data-ttu-id="7644d-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7644d-124">Application</span></span> | <span data-ttu-id="7644d-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7644d-125">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="7644d-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7644d-126">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/classes/{id}/assignments/{id}/submissions/{id}
```
## <a name="request-headers"></a><span data-ttu-id="7644d-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7644d-127">Request headers</span></span>
| <span data-ttu-id="7644d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7644d-128">Header</span></span>       | <span data-ttu-id="7644d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="7644d-129">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7644d-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="7644d-130">Authorization</span></span>  | <span data-ttu-id="7644d-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7644d-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7644d-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7644d-133">Request body</span></span>
<span data-ttu-id="7644d-134">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="7644d-134">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="7644d-135">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7644d-135">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="7644d-136">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="7644d-136">For best performance, don't include existing values that haven't changed.</span></span>

<!-- Provide the property descriptions. -->

| <span data-ttu-id="7644d-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7644d-137">Property</span></span>     | <span data-ttu-id="7644d-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="7644d-138">Type</span></span>   |<span data-ttu-id="7644d-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="7644d-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7644d-140">comentarios</span><span class="sxs-lookup"><span data-stu-id="7644d-140">feedback</span></span>|<span data-ttu-id="7644d-141">educationFeedback</span><span class="sxs-lookup"><span data-stu-id="7644d-141">educationFeedback</span></span>||
|<span data-ttu-id="7644d-142">grade</span><span class="sxs-lookup"><span data-stu-id="7644d-142">grade</span></span>|<span data-ttu-id="7644d-143">educationAssignmentGrade</span><span class="sxs-lookup"><span data-stu-id="7644d-143">educationAssignmentGrade</span></span>||

## <a name="response"></a><span data-ttu-id="7644d-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7644d-144">Response</span></span>
<span data-ttu-id="7644d-145">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [educationSubmission](../resources/educationsubmission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7644d-145">If successful, this method returns a `200 OK` response code and an updated [educationSubmission](../resources/educationsubmission.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7644d-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7644d-146">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7644d-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7644d-147">Request</span></span>
<span data-ttu-id="7644d-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7644d-148">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "update_educationsubmission"
}-->
```http
PATCH https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7
Content-type: application/json
Content-length: 658

{
  "feedback": {
    "text": {
      "content": "Good work!",
      "contentType": "Text"
    },
    "feedbackDateTime": "2014-01-01T00:00:00Z",
    "feedbackBy": {
      "user": {
        "displayName": "Susana Rocha",
        "id": "14012"
      },
      "@odata.type": "microsoft.graph.identitySet"
    },
    "@odata.type": "microsoft.graph.educationFeedback"
  },
  "grade": {
      "gradedBy": {
      "user": {
        "displayName": "Susana Rocha",
        "id": "14012"
      },
      "@odata.type": "microsoft.graph.identitySet"
    },
    "gradedDateTime": "2014-01-01T00:00:00Z",
    "@odata.type": "microsoft.graph.educationAssignmentGrade"
  }
}
```
##### <a name="response"></a><span data-ttu-id="7644d-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7644d-149">Response</span></span>
<span data-ttu-id="7644d-150">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7644d-150">The following is an example of the response.</span></span> 

><span data-ttu-id="7644d-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7644d-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSubmission"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1217

{
  "feedback": {
    "text": {
      "content": "Good work!",
      "contentType": "Text"
    },
    "feedbackDateTime": "2014-01-01T00:00:00Z",
    "feedbackBy": {
      "user": {
        "displayName": "Susana Rocha",
        "id": "14012"
      }
    },
    "@odata.type": "microsoft.graph.educationFeedback"
  },
  "grade": {
         "gradedBy": {
          "user": {
            "displayName": "Susana Rocha",
            "id": "14012"
          },
          "@odata.type": "microsoft.graph.identitySet"
        },
        "gradedDateTime": "2014-01-01T00:00:00Z",
        "@odata.type": "microsoft.graph.educationAssignmentGrade"
  },
  "id": "850f51b7",
  "recipient": {
    userId:"dsfewsddf",
    "@odata.type": "#microsoft.graph.educationSubmissionRecipient"
  },
  "releasedBy": {
    "user": {
      "displayName": "Susana Rocha",
      "id": "14012"
    },
  },
  "releasedDateTime": "2014-01-01T00:00:00Z",
  "resourcesFolderUrl": "String",
  "status": "completed",
  "submittedBy": {
    "user": {
      "displayName": "Susana Rocha",
      "id": "14012"
    },
  },
  "submittedDateTime": "2014-01-01T00:00:00Z"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update educationsubmission",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
