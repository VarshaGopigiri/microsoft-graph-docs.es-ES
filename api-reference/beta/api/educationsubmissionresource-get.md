---
title: Obtener educationSubmissionResource
description: " lista de recursos y se deben considerar trabajo en proceso por un estudiante. Este recurso se empaqueta con un puntero al recurso de asignación posible si se copió desde la asignación."
ms.openlocfilehash: 1bba0b8b4e89b0f3bc564f48187cfe46fc49cf46
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083308"
---
# <a name="get-educationsubmissionresource"></a><span data-ttu-id="c064c-104">Obtener educationSubmissionResource</span><span class="sxs-lookup"><span data-stu-id="c064c-104">Get educationSubmissionResource</span></span>

> <span data-ttu-id="c064c-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c064c-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c064c-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c064c-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c064c-107">Recupera las propiedades de un recurso específico asociado con el envío.</span><span class="sxs-lookup"><span data-stu-id="c064c-107">Retrieves the properties of a specific resource associated with the submission.</span></span> <span data-ttu-id="c064c-108">Este recurso se encuentra en la lista de recursos de "trabajo" y se debe considerar trabajo en proceso por un estudiante.</span><span class="sxs-lookup"><span data-stu-id="c064c-108">This resource is in the "working" resource list and should be considered work in process by a student.</span></span> <span data-ttu-id="c064c-109">Este recurso se empaqueta con un puntero al recurso de asignación posible si se copió desde la asignación.</span><span class="sxs-lookup"><span data-stu-id="c064c-109">This resource is wrapped with a possible pointer back to the assignment resource if it was copied from the assignment.</span></span>

## <a name="permissions"></a><span data-ttu-id="c064c-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="c064c-110">Permissions</span></span>
<span data-ttu-id="c064c-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c064c-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c064c-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c064c-113">Permission type</span></span>      | <span data-ttu-id="c064c-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c064c-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c064c-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c064c-115">Delegated (work or school account)</span></span> |  <span data-ttu-id="c064c-116">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c064c-116">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="c064c-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c064c-117">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="c064c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c064c-118">Not supported.</span></span>  |
|<span data-ttu-id="c064c-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c064c-119">Application</span></span> | <span data-ttu-id="c064c-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c064c-120">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="c064c-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c064c-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/assignments/{id}/submissions/{id}/resources/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c064c-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c064c-122">Optional query parameters</span></span>
<span data-ttu-id="c064c-123">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c064c-123">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c064c-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c064c-124">Request headers</span></span>
| <span data-ttu-id="c064c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c064c-125">Header</span></span>       | <span data-ttu-id="c064c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c064c-126">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c064c-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="c064c-127">Authorization</span></span>  | <span data-ttu-id="c064c-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c064c-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c064c-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c064c-130">Request body</span></span>
<span data-ttu-id="c064c-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c064c-131">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="c064c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c064c-132">Response</span></span>
<span data-ttu-id="c064c-133">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [educationSubmissionResource](../resources/educationsubmissionresource.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c064c-133">If successful, this method returns a `200 OK` response code and an [educationSubmissionResource](../resources/educationsubmissionresource.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c064c-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c064c-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c064c-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c064c-135">Request</span></span>
<span data-ttu-id="c064c-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c064c-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_educationsubmissionresource"
}-->
```http 
GET https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/resources/f2387c3b-ec39-4bf2-a399-d7242677f024
```
##### <a name="response"></a><span data-ttu-id="c064c-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c064c-137">Response</span></span>
<span data-ttu-id="c064c-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c064c-138">The following is an example of the response.</span></span> 

><span data-ttu-id="c064c-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c064c-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSubmissionResource"
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
      "fileUrl": "https://graph.microsoft.com/v1.0/drives/b!8-QjN2tsv0WyGnTv7vOvnQkmGHbbeMNLqYKONmHLVnvCVmBYIGpeTZ_iul5AdW9f/items/017NJZI27BCN2QI2H7HJGLIVPXR6SD2DH6"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get educationSubmissionResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
