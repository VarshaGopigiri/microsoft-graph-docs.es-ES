---
title: Crear educationAssignmentResource
description: se está creando OData.Type para indicar qué tipo de recurso. Tenga en cuenta que en primer lugar se deben cargar basado en archivos de recursos para las asignaciones **Carpetarecurso**.
ms.openlocfilehash: a2bb810d16c2d0a46fc2e2f4a5938b5779df24af
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084994"
---
# <a name="create-educationassignmentresource"></a><span data-ttu-id="c3550-104">Crear educationAssignmentResource</span><span class="sxs-lookup"><span data-stu-id="c3550-104">Create educationAssignmentResource</span></span>

> <span data-ttu-id="c3550-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c3550-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c3550-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c3550-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c3550-107">Crear un [recurso de asignación](../resources/educationassignmentresource.md).</span><span class="sxs-lookup"><span data-stu-id="c3550-107">Create an [assignment resource](../resources/educationassignmentresource.md).</span></span> <span data-ttu-id="c3550-108">El propio recurso tiene un @odata.type para indicar qué tipo de recurso que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="c3550-108">The resource itself has an @odata.type to indicate which type of resource is being created.</span></span> <span data-ttu-id="c3550-109">Tenga en cuenta que en primer lugar se deben cargar basado en archivos de recursos para las asignaciones **Carpetarecurso**.</span><span class="sxs-lookup"><span data-stu-id="c3550-109">Note that file-based resources must first be uploaded to the assignments **resourceFolder**.</span></span>

## <a name="permissions"></a><span data-ttu-id="c3550-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="c3550-110">Permissions</span></span>
<span data-ttu-id="c3550-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c3550-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c3550-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c3550-113">Permission type</span></span>      | <span data-ttu-id="c3550-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c3550-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c3550-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c3550-115">Delegated (work or school account)</span></span> |  <span data-ttu-id="c3550-116">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c3550-116">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="c3550-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c3550-117">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="c3550-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c3550-118">Not supported.</span></span>  |
|<span data-ttu-id="c3550-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c3550-119">Application</span></span> | <span data-ttu-id="c3550-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c3550-120">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="c3550-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c3550-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/resources
```
## <a name="request-headers"></a><span data-ttu-id="c3550-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c3550-122">Request headers</span></span>
| <span data-ttu-id="c3550-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3550-123">Header</span></span>       | <span data-ttu-id="c3550-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c3550-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c3550-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="c3550-125">Authorization</span></span>  | <span data-ttu-id="c3550-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c3550-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c3550-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c3550-128">Content-Type</span></span>  | <span data-ttu-id="c3550-129">application/json</span><span class="sxs-lookup"><span data-stu-id="c3550-129">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c3550-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c3550-130">Request body</span></span>
<span data-ttu-id="c3550-131">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [educationAssignmentResource](../resources/educationassignmentresource.md) .</span><span class="sxs-lookup"><span data-stu-id="c3550-131">In the request body, supply a JSON representation of the [educationAssignmentResource](../resources/educationassignmentresource.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="c3550-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3550-132">Response</span></span>
<span data-ttu-id="c3550-133">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [educationAssignmentResource](../resources/educationassignmentresource.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c3550-133">If successful, this method returns a `201 Created` response code and an [educationAssignmentResource](../resources/educationassignmentresource.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c3550-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c3550-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c3550-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c3550-135">Request</span></span>
<span data-ttu-id="c3550-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c3550-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "create_educationassignmentresource_from_educationassignment"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/resources
Content-type: application/json
Content-length: 212

{
  "distributeForStudentWork": "false",
  "resource": {
    "displayName": "Bing",
    "link": "https://www.bing.com",
    "@odata.type": "#microsoft.education.assignments.api.educationLinkResource"
  }
}

```
<span data-ttu-id="c3550-137">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [educationAssignmentResource](../resources/educationassignmentresource.md) .</span><span class="sxs-lookup"><span data-stu-id="c3550-137">In the request body, supply a JSON representation of the [educationAssignmentResource](../resources/educationassignmentresource.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="c3550-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3550-138">Response</span></span>
<span data-ttu-id="c3550-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c3550-139">The following is an example of the response.</span></span> 

><span data-ttu-id="c3550-140">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c3550-140">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="c3550-141">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c3550-141">All of the properties will be returned from an actual call.</span></span>


<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignmentResource"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 229

{
  "id": "122333",
  "distributeForStudentWork": false,
  "resource": {
    "displayName": "Bing",
    "link": "https://www.bing.com",
    "@odata.type": "#microsoft.education.assignments.api.educationLinkResource"
  }
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationAssignmentResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
