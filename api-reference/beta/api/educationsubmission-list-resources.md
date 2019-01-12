---
title: Recursos de la lista
description: Lista de los recursos asociados con este envío. El objeto **submissionResource** es que un contenedor alrededor del objeto de recurso real el alumno está trabajando en. El contenedor también incluye un puntero a los recursos de la asignación, si esto se copió desde la asignación durante el proceso de asignar. Estos recursos son la copia de trabajo de la asignación. El **submittedResources** son los recursos que se han enviado oficialmente a ser clasificados.
author: dipakboyed
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: bff80bd7975171f277cb8e6e6ee08cfd250a67ff
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975381"
---
# <a name="list-resources"></a><span data-ttu-id="0de3f-107">Recursos de la lista</span><span class="sxs-lookup"><span data-stu-id="0de3f-107">List resources</span></span>

> <span data-ttu-id="0de3f-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0de3f-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0de3f-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0de3f-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0de3f-110">Lista de los recursos asociados con este envío.</span><span class="sxs-lookup"><span data-stu-id="0de3f-110">List the resources associated with this submission.</span></span> <span data-ttu-id="0de3f-111">El objeto **submissionResource** es que un contenedor alrededor del objeto de recurso real el alumno está trabajando en.</span><span class="sxs-lookup"><span data-stu-id="0de3f-111">The **submissionResource** object is a wrapper around the actual resource object the student is working on.</span></span> <span data-ttu-id="0de3f-112">El contenedor también incluye un puntero a los recursos de la asignación, si esto se copió desde la asignación durante el proceso de asignar.</span><span class="sxs-lookup"><span data-stu-id="0de3f-112">The wrapper also includes a pointer to the resources on the assignment if this was copied from the assignment during the assign process.</span></span> <span data-ttu-id="0de3f-113">Estos recursos son la copia de trabajo de la asignación.</span><span class="sxs-lookup"><span data-stu-id="0de3f-113">These resources are the working copy of the assignment.</span></span> <span data-ttu-id="0de3f-114">El **submittedResources** son los recursos que se han enviado oficialmente a ser clasificados.</span><span class="sxs-lookup"><span data-stu-id="0de3f-114">The **submittedResources** are the resources that have officially been submitted to be graded.</span></span>

## <a name="permissions"></a><span data-ttu-id="0de3f-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="0de3f-115">Permissions</span></span>
<span data-ttu-id="0de3f-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0de3f-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0de3f-118">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0de3f-118">Permission type</span></span>      | <span data-ttu-id="0de3f-119">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0de3f-119">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0de3f-120">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0de3f-120">Delegated (work or school account)</span></span> |  <span data-ttu-id="0de3f-121">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0de3f-121">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="0de3f-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0de3f-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0de3f-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0de3f-123">Not supported.</span></span>   |
|<span data-ttu-id="0de3f-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0de3f-124">Application</span></span> | <span data-ttu-id="0de3f-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0de3f-125">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="0de3f-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0de3f-126">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /educationClasses/assignments/{id}/submissions/{id}/resources
```
## <a name="optional-query-parameters"></a><span data-ttu-id="0de3f-127">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0de3f-127">Optional query parameters</span></span>
<span data-ttu-id="0de3f-128">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0de3f-128">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0de3f-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0de3f-129">Request headers</span></span>
| <span data-ttu-id="0de3f-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0de3f-130">Header</span></span>       | <span data-ttu-id="0de3f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0de3f-131">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0de3f-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="0de3f-132">Authorization</span></span>  | <span data-ttu-id="0de3f-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0de3f-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0de3f-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0de3f-135">Request body</span></span>
<span data-ttu-id="0de3f-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0de3f-136">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="0de3f-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0de3f-137">Response</span></span>
<span data-ttu-id="0de3f-138">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [educationSubmissionResource](../resources/educationsubmissionresource.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0de3f-138">If successful, this method returns a `200 OK` response code and a collection of [educationSubmissionResource](../resources/educationsubmissionresource.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0de3f-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0de3f-139">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0de3f-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0de3f-140">Request</span></span>
<span data-ttu-id="0de3f-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0de3f-141">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_resources"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/<id>/assignments/<id>/submissions/<id>/resources
```
##### <a name="response"></a><span data-ttu-id="0de3f-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0de3f-142">Response</span></span>
<span data-ttu-id="0de3f-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0de3f-143">The following is an example of the response.</span></span> 

><span data-ttu-id="0de3f-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0de3f-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSubmissionResource",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1045

{
  "value": [
    {
      "assignmentResourceUrl": "https://graph.microsoft.com/v1.0/drives/b!8-QjN2tsv0WyGnTv7vOvnQkmGHbbeMNLqYKONmHLVnvCVmBYIGpeT456457AdW9f/items/017NJZI25NOB5XZNLABF7646XAMDZTQQ6T",
      "id": "f2387c3b-ec39-4bf2-a399-d7242677f024",
      "resource": {
          "@odata.type": "#microsoft.graph.educationLinkResource",
          "displayName": "Microsoft Homepage",
          "createdDateTime": "2017-10-21T07:52:45.5675913Z",
          "createdBy": {
              "application": null,
              "device": null,
              "user": {
                  "id": "63cc91d2-59c7-4732-9594-35b91a26b340",
                  "displayName": null
              }
          },
          "lastModifiedDateTime": "2017-10-21T07:52:45.5675913Z",
          "lastModifiedBy": {
              "application": null,
              "device": null,
              "user": {
                  "id": "63cc91d2-59c7-4732-9594-35b91a26b340",
                  "displayName": null
              }
          },
          "link": "https://www.microsoft.com"
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List resources",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
