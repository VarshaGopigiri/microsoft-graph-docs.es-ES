---
title: Actualizar educationAssignmentResource
description: 'Actualizar las propiedades de recurso asociado con una asignación. Sólo los profesores en una clase pueden cambiar los objetos de recurso de asignación.  '
ms.openlocfilehash: 761dc4f656a41d8d984443b17d87b1b0961a2a8b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084030"
---
# <a name="update-educationassignmentresource"></a><span data-ttu-id="a6abc-104">Actualizar educationAssignmentResource</span><span class="sxs-lookup"><span data-stu-id="a6abc-104">Update educationAssignmentResource</span></span>

> <span data-ttu-id="a6abc-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a6abc-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a6abc-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a6abc-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a6abc-107">Actualizar las propiedades de recurso asociado con una asignación.</span><span class="sxs-lookup"><span data-stu-id="a6abc-107">Update the properties of resource associated with an assignment.</span></span> <span data-ttu-id="a6abc-108">Sólo los profesores en una clase pueden cambiar los objetos de recurso de asignación.</span><span class="sxs-lookup"><span data-stu-id="a6abc-108">Only teachers in a class can change assignment resource objects.</span></span>  

## <a name="permissions"></a><span data-ttu-id="a6abc-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="a6abc-109">Permissions</span></span>
<span data-ttu-id="a6abc-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a6abc-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a6abc-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a6abc-112">Permission type</span></span>      | <span data-ttu-id="a6abc-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a6abc-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a6abc-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a6abc-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="a6abc-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a6abc-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>   |
|<span data-ttu-id="a6abc-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a6abc-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="a6abc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a6abc-117">Not supported.</span></span>  |
|<span data-ttu-id="a6abc-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a6abc-118">Application</span></span> | <span data-ttu-id="a6abc-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a6abc-119">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="a6abc-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a6abc-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/classes/{id}/assignments/{id}/resources/{id}
```
## <a name="request-headers"></a><span data-ttu-id="a6abc-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a6abc-121">Request headers</span></span>
| <span data-ttu-id="a6abc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6abc-122">Header</span></span>       | <span data-ttu-id="a6abc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a6abc-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a6abc-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="a6abc-124">Authorization</span></span>  | <span data-ttu-id="a6abc-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a6abc-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a6abc-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a6abc-127">Content-Type</span></span>  | <span data-ttu-id="a6abc-128">application/json</span><span class="sxs-lookup"><span data-stu-id="a6abc-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a6abc-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a6abc-129">Request body</span></span>
<span data-ttu-id="a6abc-130">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="a6abc-130">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="a6abc-131">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a6abc-131">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="a6abc-132">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="a6abc-132">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="a6abc-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a6abc-133">Property</span></span>     | <span data-ttu-id="a6abc-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6abc-134">Type</span></span>   |<span data-ttu-id="a6abc-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6abc-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a6abc-136">distributeForStudentWork</span><span class="sxs-lookup"><span data-stu-id="a6abc-136">distributeForStudentWork</span></span>|<span data-ttu-id="a6abc-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="a6abc-137">Boolean</span></span>| <span data-ttu-id="a6abc-138">Indica si este recurso se debe copiar al objeto de recurso de cada student cuando se publicó la asignación.</span><span class="sxs-lookup"><span data-stu-id="a6abc-138">Indicates whether this resource should be copied to each student's resource object when the assignment is published.</span></span>|
|<span data-ttu-id="a6abc-139">resource</span><span class="sxs-lookup"><span data-stu-id="a6abc-139">resource</span></span>|<span data-ttu-id="a6abc-140">educationResource</span><span class="sxs-lookup"><span data-stu-id="a6abc-140">educationResource</span></span>| <span data-ttu-id="a6abc-141">Objeto de recurso.</span><span class="sxs-lookup"><span data-stu-id="a6abc-141">Resource object.</span></span> |

## <a name="response"></a><span data-ttu-id="a6abc-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6abc-142">Response</span></span>
<span data-ttu-id="a6abc-143">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [educationAssignmentResource](../resources/educationassignmentresource.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6abc-143">If successful, this method returns a `200 OK` response code and an updated [educationAssignmentResource](../resources/educationassignmentresource.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a6abc-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6abc-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a6abc-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a6abc-145">Request</span></span>
<span data-ttu-id="a6abc-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a6abc-146">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "update_educationassignmentresource"
}-->
```http
PATCH https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/resources/850f51b7-1df9-4ec0-bd62-64a0214b9cbf
Content-type: application/json
Content-length: 822

{
  "distributeForStudentWork": "false"
}
```
##### <a name="response"></a><span data-ttu-id="a6abc-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6abc-147">Response</span></span>
<span data-ttu-id="a6abc-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6abc-148">The following is an example of the response.</span></span> 

><span data-ttu-id="a6abc-149">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="a6abc-149">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="a6abc-150">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a6abc-150">All of the properties will be returned from an actual call.</span></span>


<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignmentResource"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 832

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
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update educationassignmentresource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
