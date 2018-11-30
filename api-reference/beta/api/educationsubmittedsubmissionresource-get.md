---
title: Obtener educationSubmittedSubmissionResource
description: Devuelve un recurso enviado. Esto estará disponible para un profesor después de que ha enviado un estudiante y estará disponible para los estudiantes después de que el profesor ha publicado la presentación.  Tenga en cuenta que los profesores pueden dejar notas en algunos recursos.
ms.openlocfilehash: 89235ad1d33e86da13ec5f4637af7cda949a940a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083999"
---
# <a name="get-educationsubmittedsubmissionresource"></a><span data-ttu-id="6b743-105">Obtener educationSubmittedSubmissionResource</span><span class="sxs-lookup"><span data-stu-id="6b743-105">Get educationSubmittedSubmissionResource</span></span>

> <span data-ttu-id="6b743-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6b743-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6b743-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6b743-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6b743-108">Devuelve un recurso enviado.</span><span class="sxs-lookup"><span data-stu-id="6b743-108">Returns a submitted resource.</span></span> <span data-ttu-id="6b743-109">Esto estará disponible para un profesor después de que ha enviado un estudiante y estará disponible para los estudiantes después de que el profesor ha publicado la presentación.</span><span class="sxs-lookup"><span data-stu-id="6b743-109">This will be available to a teacher after a student has submitted, and will be available to the student after the teacher has released the submission.</span></span>  <span data-ttu-id="6b743-110">Tenga en cuenta que los profesores pueden dejar notas en algunos recursos.</span><span class="sxs-lookup"><span data-stu-id="6b743-110">Note that teachers can leave notes in some resources.</span></span>

## <a name="permissions"></a><span data-ttu-id="6b743-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="6b743-111">Permissions</span></span>
<span data-ttu-id="6b743-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6b743-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6b743-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6b743-114">Permission type</span></span>      | <span data-ttu-id="6b743-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6b743-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6b743-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6b743-116">Delegated (work or school account)</span></span> |  <span data-ttu-id="6b743-117">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6b743-117">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="6b743-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6b743-118">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="6b743-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6b743-119">Not supported.</span></span>  |
|<span data-ttu-id="6b743-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6b743-120">Application</span></span> | <span data-ttu-id="6b743-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6b743-121">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="6b743-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6b743-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/assignments/{id}/submissions/{id}/submittedResources/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6b743-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6b743-123">Optional query parameters</span></span>
<span data-ttu-id="6b743-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b743-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6b743-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6b743-125">Request headers</span></span>
| <span data-ttu-id="6b743-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b743-126">Header</span></span>       | <span data-ttu-id="6b743-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6b743-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6b743-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="6b743-128">Authorization</span></span>  | <span data-ttu-id="6b743-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6b743-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="6b743-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6b743-131">Request body</span></span>
<span data-ttu-id="6b743-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6b743-132">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="6b743-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b743-133">Response</span></span>
<span data-ttu-id="6b743-134">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [educationSubmissionResource](../resources/educationsubmissionresource.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b743-134">If successful, this method returns a `200 OK` response code and an [educationSubmissionResource](../resources/educationsubmissionresource.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6b743-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b743-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6b743-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6b743-136">Request</span></span>
<span data-ttu-id="6b743-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6b743-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_educationsubmittedsubmissionresource"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/submittedResources/f2387c3b-ec39-4bf2-a399-d7242677f024
```
##### <a name="response"></a><span data-ttu-id="6b743-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b743-138">Response</span></span>
<span data-ttu-id="6b743-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b743-139">The following is an example of the response.</span></span> 

><span data-ttu-id="6b743-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6b743-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSubmittedSubmissionResource"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1152

{
  "assignmentResourceUrl": "https://graph.microsoft.com/v1.0/drives/b!8-QjN2tsv0WyGnTv7vOvnQkmGHbbeMNLqYKONmHLVnvCVmBYIGpeT456457AdW9f/items/017NJZI25NOB5XZNLABF7646XAMDZTQQ6T",
  "id": "f2387c3b-ec39-4bf2-a399-d7242677f024",
  "resource": {
      "@odata.type": "#microsoft.graph.educationWordResource",
      "displayName": "Report.docx",
      "createdDateTime": "2017-10-21T07:52:53.9863696Z",
      "createdBy": {
          "application": null,
          "device": null,
          "user": {
              "id": "63cc91d2-59c7-4732-9594-35b91a26b340",
              "displayName": null
          }
      },
      "lastModifiedDateTime": "2017-10-21T07:52:53.9863696Z",
      "lastModifiedBy": {
          "application": null,
          "device": null,
          "user": {
              "id": "63cc91d2-59c7-4732-9594-35b91a26b340",
              "displayName": null
          }
      },
      "fileUrl": "https://graph.microsoft.com/v1.0/drives/b!8-QjN2tsv0WyGnTv7vOvnQkmGHbbeMNLqYKONmHLVnvCVmBYIGpeTZ_iul5AdW9f/items/017NJZI27BCN2QI2H7HJGLIVPXR6SD2DH6",
      "@odata.type": "microsoft.graph.educationResource"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get educationSubmittedSubmissionResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
