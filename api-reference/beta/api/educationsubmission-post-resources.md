---
title: Crear educationSubmissionResource
description: 'Agrega un recurso a la lista de recursos. Esta acción sólo puede realizarse por los estudiantes a quien se asigna este envío. Esta acción no se realizará correctamente si no está establecido el indicador **allowStudentsToAddResources** en true. Si desea que el autor de la llamada crear un nuevo recurso de archivo, se debe cargar el archivo a la carpeta de recursos que está asociada con el envío. Si el archivo no existe o no está en esa carpeta, se producirá un error en la solicitud POST. '
author: dipakboyed
ms.openlocfilehash: 71d06e996213c133ed9c48d5d3e320a785e122ae
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321304"
---
# <a name="create-educationsubmissionresource"></a><span data-ttu-id="a05b2-107">Crear educationSubmissionResource</span><span class="sxs-lookup"><span data-stu-id="a05b2-107">Create educationSubmissionResource</span></span>

> <span data-ttu-id="a05b2-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a05b2-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a05b2-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a05b2-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a05b2-110">Agrega un recurso a la lista de recursos.</span><span class="sxs-lookup"><span data-stu-id="a05b2-110">Adds a resource to the resources list.</span></span> <span data-ttu-id="a05b2-111">Esta acción sólo puede realizarse por los estudiantes a quien se asigna este envío.</span><span class="sxs-lookup"><span data-stu-id="a05b2-111">This action can only be done by the student to whom this submission is assigned.</span></span> <span data-ttu-id="a05b2-112">Esta acción no se realizará correctamente si no está establecido el indicador **allowStudentsToAddResources** en true.</span><span class="sxs-lookup"><span data-stu-id="a05b2-112">This action will not succeed if the **allowStudentsToAddResources** flag is not set to true.</span></span> <span data-ttu-id="a05b2-113">Si desea que el autor de la llamada crear un nuevo recurso de archivo, se debe cargar el archivo a la carpeta de recursos que está asociada con el envío.</span><span class="sxs-lookup"><span data-stu-id="a05b2-113">If the caller wants to create a new file-based resource, the file must be uploaded to the resources folder that is associated with the submission.</span></span> <span data-ttu-id="a05b2-114">Si el archivo no existe o no está en esa carpeta, se producirá un error en la solicitud POST.</span><span class="sxs-lookup"><span data-stu-id="a05b2-114">If the file does not exist or is not in that folder, the POST request will fail.</span></span> 

## <a name="permissions"></a><span data-ttu-id="a05b2-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="a05b2-115">Permissions</span></span>
<span data-ttu-id="a05b2-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a05b2-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a05b2-118">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a05b2-118">Permission type</span></span>      | <span data-ttu-id="a05b2-119">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a05b2-119">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a05b2-120">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a05b2-120">Delegated (work or school account)</span></span> |  <span data-ttu-id="a05b2-121">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a05b2-121">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="a05b2-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a05b2-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a05b2-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a05b2-123">Not supported.</span></span>  |
|<span data-ttu-id="a05b2-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a05b2-124">Application</span></span> | <span data-ttu-id="a05b2-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a05b2-125">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="a05b2-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a05b2-126">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/submissions/{id}/resources

```
## <a name="request-headers"></a><span data-ttu-id="a05b2-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a05b2-127">Request headers</span></span>
| <span data-ttu-id="a05b2-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a05b2-128">Header</span></span>       | <span data-ttu-id="a05b2-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a05b2-129">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a05b2-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="a05b2-130">Authorization</span></span>  | <span data-ttu-id="a05b2-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a05b2-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a05b2-133">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a05b2-133">Content-Type</span></span>  | <span data-ttu-id="a05b2-134">application/json</span><span class="sxs-lookup"><span data-stu-id="a05b2-134">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a05b2-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a05b2-135">Request body</span></span>
<span data-ttu-id="a05b2-136">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [educationSubmissionResource](../resources/educationsubmissionresource.md) .</span><span class="sxs-lookup"><span data-stu-id="a05b2-136">In the request body, supply a JSON representation of the [educationSubmissionResource](../resources/educationsubmissionresource.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="a05b2-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a05b2-137">Response</span></span>
<span data-ttu-id="a05b2-138">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [educationSubmissionResource](../resources/educationsubmissionresource.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a05b2-138">If successful, this method returns a `201 Created` response code and an [educationSubmissionResource](../resources/educationsubmissionresource.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a05b2-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a05b2-139">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a05b2-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a05b2-140">Request</span></span>
<span data-ttu-id="a05b2-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a05b2-141">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "create_educationsubmissionresource_from_educationsubmission"
}-->
```
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/resources
Content-type: application/json
Content-length: 1097

{
  "assignmentResourceUrl": "https://graph.microsoft.com/v1.0/drives/b!8-QjN2tsv0WyGnTv7vOvnQkmGHbbeMNLqYKONmHLVnvCVmBYIGpeT456457AdW9f/items/017NJZI25NOB5XZNLABF7646XAMDZTQQ6T",
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
  "@odata.type": "microsoft.graph.educationResource"
}

```

##### <a name="response"></a><span data-ttu-id="a05b2-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a05b2-142">Response</span></span>
<span data-ttu-id="a05b2-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a05b2-143">The following is an example of the response.</span></span> 

><span data-ttu-id="a05b2-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a05b2-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSubmissionResource"
} -->
```http
HTTP/1.1 201 Created
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
  }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationSubmissionResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->