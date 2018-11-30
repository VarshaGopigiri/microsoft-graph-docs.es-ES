---
title: Obtener educationSubmission
description: 'Recuperar un envío determinado. Un objeto de envío representa el trabajo de un alumno para una asignación. Los recursos asociados con el envío representan este trabajo. Sólo el alumno a que se asigna el envío puede ver y modificar la presentación. Un profesor tiene acceso total a todos los envíos. '
ms.openlocfilehash: 016e8d2e04377ec24fa55ad940fb97364786f433
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086932"
---
# <a name="get-educationsubmission"></a><span data-ttu-id="64e55-107">Obtener educationSubmission</span><span class="sxs-lookup"><span data-stu-id="64e55-107">Get educationSubmission</span></span>

> <span data-ttu-id="64e55-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="64e55-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="64e55-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="64e55-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="64e55-110">Recuperar un envío determinado.</span><span class="sxs-lookup"><span data-stu-id="64e55-110">Retrieve a particular submission.</span></span> <span data-ttu-id="64e55-111">Un objeto de envío representa el trabajo de un alumno para una asignación.</span><span class="sxs-lookup"><span data-stu-id="64e55-111">A submission object represents a student's work for an assignment.</span></span> <span data-ttu-id="64e55-112">Los recursos asociados con el envío representan este trabajo.</span><span class="sxs-lookup"><span data-stu-id="64e55-112">Resources associated with the submission represent this work.</span></span> <span data-ttu-id="64e55-113">Sólo el alumno a que se asigna el envío puede ver y modificar la presentación.</span><span class="sxs-lookup"><span data-stu-id="64e55-113">Only the student the submission is assigned to can see and modify the submission.</span></span> <span data-ttu-id="64e55-114">Un profesor tiene acceso total a todos los envíos.</span><span class="sxs-lookup"><span data-stu-id="64e55-114">A teacher has full access to all submissions.</span></span> 

<span data-ttu-id="64e55-115">La categoría y los comentarios de un profesor también forman parte de este objeto.</span><span class="sxs-lookup"><span data-stu-id="64e55-115">The grade and feedback from a teacher are also part of this object.</span></span> <span data-ttu-id="64e55-116">Profesores sólo pueden agregar o cambiar remuneración y comentarios.</span><span class="sxs-lookup"><span data-stu-id="64e55-116">Only teachers can add or change grades and feedback.</span></span> <span data-ttu-id="64e55-117">Los alumnos no verán la calificación o comentarios hasta que se ha publicado la asignación.</span><span class="sxs-lookup"><span data-stu-id="64e55-117">Students will not see the grade or feedback until the assignment has been released.</span></span> <span data-ttu-id="64e55-118">Los permisos básicos no incluir comentarios y calificación pero incluye todo lo demás.</span><span class="sxs-lookup"><span data-stu-id="64e55-118">The Basic permissions do not include grade and feedback but do include everything else.</span></span>

## <a name="permissions"></a><span data-ttu-id="64e55-119">Permisos</span><span class="sxs-lookup"><span data-stu-id="64e55-119">Permissions</span></span>
<span data-ttu-id="64e55-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="64e55-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="64e55-122">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="64e55-122">Permission type</span></span>      | <span data-ttu-id="64e55-123">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="64e55-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="64e55-124">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="64e55-124">Delegated (work or school account)</span></span> |  <span data-ttu-id="64e55-125">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="64e55-125">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span></span> |
|<span data-ttu-id="64e55-126">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="64e55-126">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="64e55-127">No admitida.</span><span class="sxs-lookup"><span data-stu-id="64e55-127">Not supported.</span></span>  |
|<span data-ttu-id="64e55-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="64e55-128">Application</span></span> | <span data-ttu-id="64e55-129">No admitida.</span><span class="sxs-lookup"><span data-stu-id="64e55-129">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="64e55-130">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="64e55-130">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/assignments/{id}/submissions/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="64e55-131">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="64e55-131">Optional query parameters</span></span>
<span data-ttu-id="64e55-132">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64e55-132">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="64e55-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="64e55-133">Request headers</span></span>
| <span data-ttu-id="64e55-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64e55-134">Header</span></span>       | <span data-ttu-id="64e55-135">Valor</span><span class="sxs-lookup"><span data-stu-id="64e55-135">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="64e55-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="64e55-136">Authorization</span></span>  | <span data-ttu-id="64e55-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64e55-p106">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="64e55-139">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="64e55-139">Request body</span></span>
<span data-ttu-id="64e55-140">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="64e55-140">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="64e55-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64e55-141">Response</span></span>
<span data-ttu-id="64e55-142">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [educationSubmission](../resources/educationsubmission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64e55-142">If successful, this method returns a `200 OK` response code and an [educationSubmission](../resources/educationsubmission.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="64e55-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="64e55-143">Example</span></span>
##### <a name="request"></a><span data-ttu-id="64e55-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="64e55-144">Request</span></span>
<span data-ttu-id="64e55-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64e55-145">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_educationsubmission"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/11010/assignments/19002/submissions/33223
```
##### <a name="response"></a><span data-ttu-id="64e55-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64e55-146">Response</span></span>
<span data-ttu-id="64e55-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64e55-147">The following is an example of the response.</span></span> 

><span data-ttu-id="64e55-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="64e55-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSubmission"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 712

{
    "feedback": {
      text: {
        "content": "Good work!",
        "contentType": "Text"
      },
      feedbackDateTime: "2014-01-01T00:00:00Z",
      feedbackBy: {
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
        },
        "gradedDateTime": "2014-01-01T00:00:00Z"
      },
      "id": "33223",
      "recipient": {
        "userId": "13015"
      },
      "releasedBy": {
          "user": {
            "displayName": "Susana Rocha",
            "id": "14012"
          },
        },
      "releasedDateTime": "2014-01-01T00:00:00Z",
      "resourcesFolderUrl": "https://graph.microsoft.com/v1.0/drives/b!8-QjN2tsv0WyGnTv7vOvnQkmGHbbeMNLqYKONmHLVnvCVmBYIGpeT456457AdW9f/items/017NJZI25NOB5XZNLABF7646XAMDZTQQ6T",
      "status": "working",
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
  "description": "Get educationSubmission",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->