---
title: Lista educationAssignmentResources
description: Obtener todos los recursos asociados con esta asignación.
author: dipakboyed
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 0fa0a5b46d7f40b1d1e8b6d265b12f84384e2c50
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936203"
---
# <a name="list-educationassignmentresources"></a><span data-ttu-id="658a8-103">Lista educationAssignmentResources</span><span class="sxs-lookup"><span data-stu-id="658a8-103">List educationAssignmentResources</span></span>

> <span data-ttu-id="658a8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="658a8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="658a8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="658a8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="658a8-106">Obtener todos los recursos asociados con esta asignación.</span><span class="sxs-lookup"><span data-stu-id="658a8-106">Get all the resources associated with this assignment.</span></span>

## <a name="permissions"></a><span data-ttu-id="658a8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="658a8-107">Permissions</span></span>
<span data-ttu-id="658a8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="658a8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="658a8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="658a8-110">Permission type</span></span>      | <span data-ttu-id="658a8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="658a8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="658a8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="658a8-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="658a8-113">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="658a8-113">EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="658a8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="658a8-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="658a8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="658a8-115">Not supported.</span></span>  |
|<span data-ttu-id="658a8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="658a8-116">Application</span></span> | <span data-ttu-id="658a8-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="658a8-117">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="658a8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="658a8-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/assignments/{id}/resources
```
## <a name="optional-query-parameters"></a><span data-ttu-id="658a8-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="658a8-119">Optional query parameters</span></span>
<span data-ttu-id="658a8-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="658a8-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="658a8-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="658a8-121">Request headers</span></span>
| <span data-ttu-id="658a8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="658a8-122">Header</span></span>       | <span data-ttu-id="658a8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="658a8-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="658a8-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="658a8-124">Authorization</span></span>  | <span data-ttu-id="658a8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="658a8-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="658a8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="658a8-127">Request body</span></span>
<span data-ttu-id="658a8-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="658a8-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="658a8-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="658a8-129">Response</span></span>
<span data-ttu-id="658a8-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [educationAssignmentResource](../resources/educationassignmentresource.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="658a8-130">If successful, this method returns a `200 OK` response code and a collection of [educationAssignmentResource](../resources/educationassignmentresource.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="658a8-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="658a8-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="658a8-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="658a8-132">Request</span></span>
<span data-ttu-id="658a8-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="658a8-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_resources"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/11012/assignments/19002/resources
```
##### <a name="response"></a><span data-ttu-id="658a8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="658a8-134">Response</span></span>
<span data-ttu-id="658a8-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="658a8-135">The following is an example of the response.</span></span> 

><span data-ttu-id="658a8-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="658a8-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignmentResource",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1011

{
  "value": [
    {
      "distributeForStudentWork": false,
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
      },
      "id": "850f51b7-1df9-4ec0-bd62-64a0214b9cbf"
    },
    {
      "distributeForStudentWork": true,
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
      },
      "id": "f2387c3b-ec39-4bf2-a399-d7242677f024"
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
