---
title: Envíos de lista
description: Lista de todos los envíos asociados a esta asignación. Un profesor puede obtener todas las presentaciones mientras un estudiante sólo puede obtener los envíos que están asociadas.
author: dipakboyed
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 2a4de863b69de420e89a9272e532fa889486fc22
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915189"
---
# <a name="list-submissions"></a><span data-ttu-id="2ee0d-104">Envíos de lista</span><span class="sxs-lookup"><span data-stu-id="2ee0d-104">List submissions</span></span>

> <span data-ttu-id="2ee0d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2ee0d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2ee0d-107">Lista de todos los envíos asociados a esta asignación.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-107">List all the submissions associated with this assignment.</span></span> <span data-ttu-id="2ee0d-108">Un profesor puede obtener todas las presentaciones mientras un estudiante sólo puede obtener los envíos que están asociadas.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-108">A teacher can get all the submissions while a student can only get submissions that they are associated with.</span></span>

## <a name="permissions"></a><span data-ttu-id="2ee0d-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="2ee0d-109">Permissions</span></span>
<span data-ttu-id="2ee0d-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2ee0d-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2ee0d-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2ee0d-112">Permission type</span></span>      | <span data-ttu-id="2ee0d-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2ee0d-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2ee0d-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2ee0d-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="2ee0d-115">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2ee0d-115">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="2ee0d-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2ee0d-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="2ee0d-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-117">Not supported.</span></span>  |
|<span data-ttu-id="2ee0d-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2ee0d-118">Application</span></span> | <span data-ttu-id="2ee0d-119">No se admite.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-119">Not Supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="2ee0d-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2ee0d-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/assignments/{id}/submissions
```
## <a name="optional-query-parameters"></a><span data-ttu-id="2ee0d-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2ee0d-121">Optional query parameters</span></span>
<span data-ttu-id="2ee0d-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2ee0d-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2ee0d-123">Request headers</span></span>
| <span data-ttu-id="2ee0d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ee0d-124">Header</span></span>       | <span data-ttu-id="2ee0d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2ee0d-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2ee0d-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="2ee0d-126">Authorization</span></span>  | <span data-ttu-id="2ee0d-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2ee0d-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2ee0d-129">Request body</span></span>
<span data-ttu-id="2ee0d-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-130">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="2ee0d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ee0d-131">Response</span></span>
<span data-ttu-id="2ee0d-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [educationSubmission](../resources/educationsubmission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-132">If successful, this method returns a `200 OK` response code and collection of [educationSubmission](../resources/educationsubmission.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2ee0d-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2ee0d-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2ee0d-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ee0d-134">Request</span></span>
<span data-ttu-id="2ee0d-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_submissions"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions
```
##### <a name="response"></a><span data-ttu-id="2ee0d-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ee0d-136">Response</span></span>
<span data-ttu-id="2ee0d-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-137">The following is an example of the response.</span></span> 

><span data-ttu-id="2ee0d-138">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-138">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="2ee0d-139">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2ee0d-139">All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSubmission",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 873

{
  "value": [
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
        },
        "gradedDateTime": "2014-01-01T00:00:00Z"
      },
      "id": "33223",
      "recipient": {
        "userId": "13015",
        "@Odata.type":"microsoft.graph.educationSubmissionRecipient"
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List submissions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
