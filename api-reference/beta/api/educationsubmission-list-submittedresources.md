---
title: Lista submittedResources
description: Lista de los recursos que se han enviado oficialmente para la clasificación. El estudiante que posee el envío no puede cambiar la lista enviada sin volver a enviar la asignación. Este es un contenedor para el recurso real y puede contener un puntero al recurso de asignación real si este recurso se copió desde la asignación.
author: dipakboyed
ms.openlocfilehash: 9689d9687127006f38884107d0b015e571fd6ab0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27356143"
---
# <a name="list-submittedresources"></a><span data-ttu-id="bcf8b-105">Lista submittedResources</span><span class="sxs-lookup"><span data-stu-id="bcf8b-105">List submittedResources</span></span>

> <span data-ttu-id="bcf8b-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bcf8b-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bcf8b-108">Lista de los recursos que se han enviado oficialmente para la clasificación.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-108">List the resources that have officially been submitted for grading.</span></span> <span data-ttu-id="bcf8b-109">El estudiante que posee el envío no puede cambiar la lista enviada sin volver a enviar la asignación.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-109">The student who owns the submission cannot change the submitted list without resubmitting the assignment.</span></span> <span data-ttu-id="bcf8b-110">Este es un contenedor para el recurso real y puede contener un puntero al recurso de asignación real si este recurso se copió desde la asignación.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-110">This is a wrapper around the real resource and can contain a pointer back to the actual assignment resource if this resource was copied from the assignment.</span></span>

## <a name="permissions"></a><span data-ttu-id="bcf8b-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="bcf8b-111">Permissions</span></span>
<span data-ttu-id="bcf8b-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bcf8b-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bcf8b-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bcf8b-114">Permission type</span></span>      | <span data-ttu-id="bcf8b-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bcf8b-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bcf8b-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bcf8b-116">Delegated (work or school account)</span></span> |  <span data-ttu-id="bcf8b-117">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bcf8b-117">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="bcf8b-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bcf8b-118">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="bcf8b-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-119">Not supported.</span></span>  |
|<span data-ttu-id="bcf8b-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bcf8b-120">Application</span></span> | <span data-ttu-id="bcf8b-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-121">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="bcf8b-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bcf8b-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/assignments/{id}/submissions/{id}/submittedResources
```
## <a name="optional-query-parameters"></a><span data-ttu-id="bcf8b-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bcf8b-123">Optional query parameters</span></span>
<span data-ttu-id="bcf8b-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="bcf8b-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bcf8b-125">Request headers</span></span>
| <span data-ttu-id="bcf8b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcf8b-126">Header</span></span>       | <span data-ttu-id="bcf8b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bcf8b-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="bcf8b-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="bcf8b-128">Authorization</span></span>  | <span data-ttu-id="bcf8b-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="bcf8b-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bcf8b-131">Request body</span></span>
<span data-ttu-id="bcf8b-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-132">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="bcf8b-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcf8b-133">Response</span></span>
<span data-ttu-id="bcf8b-134">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [educationSubmissionResource](../resources/educationsubmissionresource.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-134">If successful, this method returns a `200 OK` response code and a collection of [educationSubmissionResource](../resources/educationsubmissionresource.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bcf8b-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bcf8b-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bcf8b-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bcf8b-136">Request</span></span>
<span data-ttu-id="bcf8b-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_submittedresources"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/submittedResources
```
##### <a name="response"></a><span data-ttu-id="bcf8b-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcf8b-138">Response</span></span>
<span data-ttu-id="bcf8b-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-139">The following is an example of the response.</span></span> 

><span data-ttu-id="bcf8b-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSubmittedSubmissionResource",
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
        "link": "https://www.microsoft.com
        },
        "@odata.type": "microsoft.graph.educationSubmittedSubmissionResource" 
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List submittedResources",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->