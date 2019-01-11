---
title: Obtener educationSubmissionResource
description: Recupera las propiedades de un recurso específico asociado con el envío. Este recurso se encuentra en la lista de recursos 'trabajo' y se debe considerar trabajo en proceso por un estudiante. Este recurso se empaqueta con un puntero al recurso de asignación posible si se copió desde la asignación.
author: dipakboyed
localization_priority: Normal
ms.openlocfilehash: 95a44b2a2e354060a718827ba1c13b9c60391d58
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866076"
---
# <a name="get-educationsubmissionresource"></a><span data-ttu-id="cdef5-105">Obtener educationSubmissionResource</span><span class="sxs-lookup"><span data-stu-id="cdef5-105">Get educationSubmissionResource</span></span>

> <span data-ttu-id="cdef5-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cdef5-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cdef5-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cdef5-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cdef5-108">Recupera las propiedades de un recurso específico asociado con el envío.</span><span class="sxs-lookup"><span data-stu-id="cdef5-108">Retrieves the properties of a specific resource associated with the submission.</span></span> <span data-ttu-id="cdef5-109">Este recurso se encuentra en la lista de recursos de "trabajo" y se debe considerar trabajo en proceso por un estudiante.</span><span class="sxs-lookup"><span data-stu-id="cdef5-109">This resource is in the "working" resource list and should be considered work in process by a student.</span></span> <span data-ttu-id="cdef5-110">Este recurso se empaqueta con un puntero al recurso de asignación posible si se copió desde la asignación.</span><span class="sxs-lookup"><span data-stu-id="cdef5-110">This resource is wrapped with a possible pointer back to the assignment resource if it was copied from the assignment.</span></span>

## <a name="permissions"></a><span data-ttu-id="cdef5-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="cdef5-111">Permissions</span></span>
<span data-ttu-id="cdef5-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cdef5-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cdef5-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cdef5-114">Permission type</span></span>      | <span data-ttu-id="cdef5-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cdef5-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cdef5-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cdef5-116">Delegated (work or school account)</span></span> |  <span data-ttu-id="cdef5-117">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cdef5-117">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="cdef5-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cdef5-118">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="cdef5-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cdef5-119">Not supported.</span></span>  |
|<span data-ttu-id="cdef5-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cdef5-120">Application</span></span> | <span data-ttu-id="cdef5-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cdef5-121">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="cdef5-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cdef5-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/assignments/{id}/submissions/{id}/resources/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="cdef5-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="cdef5-123">Optional query parameters</span></span>
<span data-ttu-id="cdef5-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cdef5-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="cdef5-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cdef5-125">Request headers</span></span>
| <span data-ttu-id="cdef5-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cdef5-126">Header</span></span>       | <span data-ttu-id="cdef5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="cdef5-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="cdef5-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="cdef5-128">Authorization</span></span>  | <span data-ttu-id="cdef5-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cdef5-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="cdef5-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cdef5-131">Request body</span></span>
<span data-ttu-id="cdef5-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cdef5-132">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="cdef5-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cdef5-133">Response</span></span>
<span data-ttu-id="cdef5-134">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [educationSubmissionResource](../resources/educationsubmissionresource.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cdef5-134">If successful, this method returns a `200 OK` response code and an [educationSubmissionResource](../resources/educationsubmissionresource.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="cdef5-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cdef5-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cdef5-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cdef5-136">Request</span></span>
<span data-ttu-id="cdef5-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cdef5-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_educationsubmissionresource"
}-->
```http 
GET https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/resources/f2387c3b-ec39-4bf2-a399-d7242677f024
```
##### <a name="response"></a><span data-ttu-id="cdef5-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cdef5-138">Response</span></span>
<span data-ttu-id="cdef5-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cdef5-139">The following is an example of the response.</span></span> 

><span data-ttu-id="cdef5-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cdef5-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
