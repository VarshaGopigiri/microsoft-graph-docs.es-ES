---
title: Actualizar educationassignment
description: Actualizar el objeto de asignación. Sólo los profesores en la clase pueden hacerlo. Tenga en cuenta que no se puede usar una solicitud de revisión para cambiar el estado de una asignación. Utilice la acción de publicación para cambiar el estado de la asignación.
ms.openlocfilehash: 8b23b7ac4b971856ed7a96b4991fca2e5220d069
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085896"
---
# <a name="update-educationassignment"></a><span data-ttu-id="34f15-106">Actualizar educationassignment</span><span class="sxs-lookup"><span data-stu-id="34f15-106">Update educationassignment</span></span>

> <span data-ttu-id="34f15-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="34f15-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="34f15-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="34f15-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="34f15-109">Actualizar el objeto de asignación.</span><span class="sxs-lookup"><span data-stu-id="34f15-109">Update the assignment object.</span></span> <span data-ttu-id="34f15-110">Sólo los profesores en la clase pueden hacerlo.</span><span class="sxs-lookup"><span data-stu-id="34f15-110">Only teachers in the class can do this.</span></span> <span data-ttu-id="34f15-111">Tenga en cuenta que no se puede usar una solicitud de revisión para cambiar el estado de una asignación.</span><span class="sxs-lookup"><span data-stu-id="34f15-111">Note that you can't use a PATCH request to change the status of an assignment.</span></span> <span data-ttu-id="34f15-112">Use la acción [Publicar](../api/educationassignment-publish.md) para cambiar el estado de asignación.</span><span class="sxs-lookup"><span data-stu-id="34f15-112">Use the [publish](../api/educationassignment-publish.md) action to change the assignment status.</span></span>

## <a name="permissions"></a><span data-ttu-id="34f15-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="34f15-113">Permissions</span></span>
<span data-ttu-id="34f15-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="34f15-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="34f15-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="34f15-116">Permission type</span></span>      | <span data-ttu-id="34f15-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="34f15-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="34f15-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="34f15-118">Delegated (work or school account)</span></span> |  <span data-ttu-id="34f15-119">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34f15-119">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="34f15-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="34f15-120">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="34f15-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="34f15-121">Not supported.</span></span>  |
|<span data-ttu-id="34f15-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="34f15-122">Application</span></span> | <span data-ttu-id="34f15-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="34f15-123">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="34f15-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="34f15-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/classes/{id}/assignments/{id}
```
## <a name="request-headers"></a><span data-ttu-id="34f15-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="34f15-125">Request headers</span></span>
| <span data-ttu-id="34f15-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34f15-126">Header</span></span>       | <span data-ttu-id="34f15-127">Valor</span><span class="sxs-lookup"><span data-stu-id="34f15-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="34f15-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="34f15-128">Authorization</span></span>  | <span data-ttu-id="34f15-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="34f15-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="34f15-131">Content-Type</span><span class="sxs-lookup"><span data-stu-id="34f15-131">Content-Type</span></span>  | <span data-ttu-id="34f15-132">application/json</span><span class="sxs-lookup"><span data-stu-id="34f15-132">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="34f15-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="34f15-133">Request body</span></span>
<span data-ttu-id="34f15-134">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="34f15-134">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="34f15-135">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="34f15-135">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="34f15-136">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="34f15-136">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="34f15-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34f15-137">Property</span></span>     | <span data-ttu-id="34f15-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="34f15-138">Type</span></span>   |<span data-ttu-id="34f15-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="34f15-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="34f15-140">allowLateSubmissions</span><span class="sxs-lookup"><span data-stu-id="34f15-140">allowLateSubmissions</span></span>|<span data-ttu-id="34f15-141">Booleano</span><span class="sxs-lookup"><span data-stu-id="34f15-141">Boolean</span></span>| <span data-ttu-id="34f15-142">Si se pueden enviar envíos después de la fecha de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="34f15-142">Whether submissions can be submitted after the due date.</span></span>|
|<span data-ttu-id="34f15-143">allowStudentsToAddResourcesToSubmission</span><span class="sxs-lookup"><span data-stu-id="34f15-143">allowStudentsToAddResourcesToSubmission</span></span>|<span data-ttu-id="34f15-144">Booleano</span><span class="sxs-lookup"><span data-stu-id="34f15-144">Boolean</span></span>| <span data-ttu-id="34f15-145">Si un estudiante puede agregar recursos a una presentación.</span><span class="sxs-lookup"><span data-stu-id="34f15-145">Whether a student can add resources to a submission.</span></span> <span data-ttu-id="34f15-146">Indica si los únicos elementos en el envío proceden de la lista de recursos de la asignación.</span><span class="sxs-lookup"><span data-stu-id="34f15-146">Indicated whether the only items on the submission came from the assignment resource list.</span></span> |
|<span data-ttu-id="34f15-147">assignDateTime</span><span class="sxs-lookup"><span data-stu-id="34f15-147">assignDateTime</span></span>|<span data-ttu-id="34f15-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="34f15-148">DateTimeOffset</span></span>| <span data-ttu-id="34f15-149">Fecha de que la asignación debe publicarse a los alumnos.</span><span class="sxs-lookup"><span data-stu-id="34f15-149">Date the assignment should be published to students.</span></span> |
|<span data-ttu-id="34f15-150">assignTo</span><span class="sxs-lookup"><span data-stu-id="34f15-150">assignTo</span></span>|<span data-ttu-id="34f15-151">educationAssignmentRecipient</span><span class="sxs-lookup"><span data-stu-id="34f15-151">educationAssignmentRecipient</span></span>| <span data-ttu-id="34f15-152">Alumnos que obtener la asignación.</span><span class="sxs-lookup"><span data-stu-id="34f15-152">Students who get the assignment.</span></span>|
|<span data-ttu-id="34f15-153">displayName</span><span class="sxs-lookup"><span data-stu-id="34f15-153">displayName</span></span>|<span data-ttu-id="34f15-154">String</span><span class="sxs-lookup"><span data-stu-id="34f15-154">String</span></span>| <span data-ttu-id="34f15-155">Nombre de asignación.</span><span class="sxs-lookup"><span data-stu-id="34f15-155">Name of assignment.</span></span> |
|<span data-ttu-id="34f15-156">dueDateTime</span><span class="sxs-lookup"><span data-stu-id="34f15-156">dueDateTime</span></span>|<span data-ttu-id="34f15-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="34f15-157">DateTimeOffset</span></span>| <span data-ttu-id="34f15-158">Asignación de fecha es de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="34f15-158">Date assignment is due.</span></span> |
|<span data-ttu-id="34f15-159">Puntuar</span><span class="sxs-lookup"><span data-stu-id="34f15-159">grading</span></span>|<span data-ttu-id="34f15-160">educationAssignmentGradeType</span><span class="sxs-lookup"><span data-stu-id="34f15-160">educationAssignmentGradeType</span></span>| <span data-ttu-id="34f15-161">¿Cómo se corregirán la asignación.</span><span class="sxs-lookup"><span data-stu-id="34f15-161">How the assignment will be graded.</span></span>|
|<span data-ttu-id="34f15-162">instrucciones</span><span class="sxs-lookup"><span data-stu-id="34f15-162">instructions</span></span>|<span data-ttu-id="34f15-163">itemBody</span><span class="sxs-lookup"><span data-stu-id="34f15-163">itemBody</span></span>| <span data-ttu-id="34f15-164">Instrucciones que se proporcionará a los alumnos junto con la asignación.</span><span class="sxs-lookup"><span data-stu-id="34f15-164">Instructions to be given to the students along with the assignment.</span></span> |

## <a name="response"></a><span data-ttu-id="34f15-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34f15-165">Response</span></span>
<span data-ttu-id="34f15-166">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [educationAssignment](../resources/educationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34f15-166">If successful, this method returns a `200 OK` response code and an updated [educationAssignment](../resources/educationassignment.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="34f15-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34f15-167">Example</span></span>
##### <a name="request"></a><span data-ttu-id="34f15-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34f15-168">Request</span></span>
<span data-ttu-id="34f15-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34f15-169">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_educationassignment"
}-->
```http
PATCH https://graph.microsoft.com/beta/education/classes/11021/assignments/19002
Content-type: application/json
Content-length: 279

{
  "displayName": "Week 1 reading assignment",
  "instructions": {
    "contentType": "Text",
    "content": "Read chapters 1 through 3"
  },
  "dueDateTime": "2014-02-01T00:00:00Z"
}
```
##### <a name="response"></a><span data-ttu-id="34f15-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34f15-170">Response</span></span>
<span data-ttu-id="34f15-171">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34f15-171">The following is an example of the response.</span></span> 

><span data-ttu-id="34f15-172">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="34f15-172">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="34f15-173">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="34f15-173">All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 279

{
  "classId": "11021",
  "displayName": "Week 1 reading assignment",
  "instructions": {
    "contentType": "Text",
    "content": "Read chapters 1 through 3"
  },
  "dueDateTime": "2014-02-01T00:00:00Z",
  "assignDateTime": "2014-01-01T00:00:00Z",
  "assignedDateTime": "2014-01-01T00:00:00Z"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update educationassignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->