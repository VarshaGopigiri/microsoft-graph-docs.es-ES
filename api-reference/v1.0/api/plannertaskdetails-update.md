---
title: Actualizar plannertaskdetails
description: Actualizar las propiedades del objeto **plannertaskdetails**.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: cd9bf69fcb458c40c8506ccf2a7d401793e8fbef
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928083"
---
# <a name="update-plannertaskdetails"></a><span data-ttu-id="b6b14-103">Actualizar plannertaskdetails</span><span class="sxs-lookup"><span data-stu-id="b6b14-103">Update plannertaskdetails</span></span>

<span data-ttu-id="b6b14-104">Actualizar las propiedades del objeto **plannertaskdetails**.</span><span class="sxs-lookup"><span data-stu-id="b6b14-104">Update the properties of **plannertaskdetails** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="b6b14-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b6b14-105">Permissions</span></span>
<span data-ttu-id="b6b14-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b6b14-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b6b14-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b6b14-108">Permission type</span></span>      | <span data-ttu-id="b6b14-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b6b14-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b6b14-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6b14-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b6b14-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b6b14-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="b6b14-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6b14-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b6b14-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6b14-113">Not supported.</span></span>    |
|<span data-ttu-id="b6b14-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6b14-114">Application</span></span> | <span data-ttu-id="b6b14-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6b14-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b6b14-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6b14-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/{id}/details
```
## <a name="optional-request-headers"></a><span data-ttu-id="b6b14-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="b6b14-117">Optional request headers</span></span>
| <span data-ttu-id="b6b14-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="b6b14-118">Name</span></span>       | <span data-ttu-id="b6b14-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6b14-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="b6b14-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="b6b14-120">Authorization</span></span>  | <span data-ttu-id="b6b14-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6b14-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b6b14-123">If-Match</span><span class="sxs-lookup"><span data-stu-id="b6b14-123">If-Match</span></span>  | <span data-ttu-id="b6b14-p103">Último valor ETag conocido para que se actualice **plannerTaskDetails**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6b14-p103">Last known ETag value for the **plannerTaskDetails** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b6b14-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6b14-126">Request body</span></span>
<span data-ttu-id="b6b14-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="b6b14-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="b6b14-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b6b14-130">Property</span></span>     | <span data-ttu-id="b6b14-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6b14-131">Type</span></span>   |<span data-ttu-id="b6b14-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6b14-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b6b14-133">checklist</span><span class="sxs-lookup"><span data-stu-id="b6b14-133">checklist</span></span>|[<span data-ttu-id="b6b14-134">plannerChecklistItems</span><span class="sxs-lookup"><span data-stu-id="b6b14-134">plannerChecklistItems</span></span>](../resources/plannerchecklistitems.md)|<span data-ttu-id="b6b14-135">Colección de elementos de la lista de comprobación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6b14-135">The collection of checklist items on the task.</span></span>|
|<span data-ttu-id="b6b14-136">description</span><span class="sxs-lookup"><span data-stu-id="b6b14-136">description</span></span>|<span data-ttu-id="b6b14-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="b6b14-137">String</span></span>|<span data-ttu-id="b6b14-138">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="b6b14-138">Description of the task</span></span>|
|<span data-ttu-id="b6b14-139">previewType</span><span class="sxs-lookup"><span data-stu-id="b6b14-139">previewType</span></span>|<span data-ttu-id="b6b14-140">string</span><span class="sxs-lookup"><span data-stu-id="b6b14-140">string</span></span>|<span data-ttu-id="b6b14-141">Esto establece el tipo de vista previa que se muestra en la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6b14-141">This sets the type of preview that shows up on the task.</span></span> <span data-ttu-id="b6b14-142">Los valores posibles son: `automatic`, `noPreview`, `checklist`, `description`, `reference`.</span><span class="sxs-lookup"><span data-stu-id="b6b14-142">The possible values are: `automatic`, `noPreview`, `checklist`, `description`, `reference`.</span></span> <span data-ttu-id="b6b14-143">Cuando se establece en `automatic` la vista previa que se muestra es elegida por la aplicación de visualización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6b14-143">When set to `automatic` the displayed preview is chosen by the app viewing the task.</span></span>|
|<span data-ttu-id="b6b14-144">references</span><span class="sxs-lookup"><span data-stu-id="b6b14-144">references</span></span>|[<span data-ttu-id="b6b14-145">plannerExternalReferences</span><span class="sxs-lookup"><span data-stu-id="b6b14-145">plannerExternalReferences</span></span>](../resources/plannerexternalreferences.md)|<span data-ttu-id="b6b14-146">La colección de referencias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6b14-146">The collection of references on the task.</span></span>|

## <a name="response"></a><span data-ttu-id="b6b14-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6b14-147">Response</span></span>

<span data-ttu-id="b6b14-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerTaskDetails](../resources/plannertaskdetails.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6b14-148">If successful, this method returns a `200 OK` response code and updated [plannerTaskDetails](../resources/plannertaskdetails.md) object in the response body.</span></span>

<span data-ttu-id="b6b14-p106">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="b6b14-p106">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="b6b14-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6b14-152">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b6b14-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6b14-153">Request</span></span>
<span data-ttu-id="b6b14-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6b14-154">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannertaskdetails"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/tasks/{task-id}/details
Content-type: application/json
Content-length: 857
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "previewType": "noPreview",
  "references": {
    "http%3A//developer%2Emicrosoft%2Ecom":{
      "@odata.type": "microsoft.graph.plannerExternalReference",
      "alias": "Documentation",
      "previewPriority": " !",
      "type": "Other"
    },
    "https%3A//developer%2Emicrosoft%2Ecom/en-us/graph/graph-explorer":{
      "@odata.type": "microsoft.graph.plannerExternalReference",
      "previewPriority": "  !!",
    },
    "http%3A//www%2Ebing%2Ecom": null
  },
  "checklist": {
    "95e27074-6c4a-447a-aa24-9d718a0b86fa":{
      "@odata.type": "microsoft.graph.plannerChecklistItem",
      "title": "Update task details",
      "ischecked": true
    },
    "d280ed1a-9f6b-4f9c-a962-fb4d00dc50ff":{
      "@odata.type": "microsoft.graph.plannerChecklistItem",
      "isChecked": true,
    },
    "a93c93c5-10a6-4167-9551-8bafa09967a7": null
  }
}
```
##### <a name="response"></a><span data-ttu-id="b6b14-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6b14-155">Response</span></span>
<span data-ttu-id="b6b14-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6b14-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerTaskDetails"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1793

{
  "description": "Task details properties:\nchecklist:Sub items\nreferences:Related links",
  "previewType": "automatic",
  "references": {
    "https%3A//developer%2Emicrosoft%2Ecom/en-us/graph/graph-explorer": {
      "@odata.type": "#microsoft.graph.plannerExternalReference",
      "alias": "Graph Explorer",
      "type": "Other",
      "previewPriority": "8599273",
      "lastModifiedBy": {
        "user": {
          "id": "fbab97d0-4932-4511-b675-204639209557"
        }
      },
      "lastModifiedDateTime": "2017-04-24T22:52:29.814Z"
    },
    "http%3A//developer%2Emicrosoft%2Ecom": {
      "@odata.type": "#microsoft.graph.plannerExternalReference",
      "alias": "Documentation",
      "type": "Other",
      "previewPriority": "90727736",
      "lastModifiedBy": {
        "user": {
          "id": "fbab97d0-4932-4511-b675-204639209557"
        }
      },
      "lastModifiedDateTime": "2017-04-24T22:52:29.814Z"
    }
  },
  "checklist": {
    "d280ed1a-9f6b-4f9c-a962-fb4d00dc50ff": {
      "@odata.type": "#microsoft.graph.plannerChecklistItem",
      "isChecked": true,
      "title": "Try reading task details",
      "orderHint": "a93c93c5^",
      "lastModifiedBy": {
        "user": {
          "id": "fbab97d0-4932-4511-b675-204639209557"
        }
      },
      "lastModifiedDateTime": "2017-04-24T22:52:29.814Z"
    },
    "95e27074-6c4a-447a-aa24-9d718a0b86f": {
      "@odata.type": "#microsoft.graph.plannerChecklistItem",
      "isChecked": true,
      "title": "Update task details",
      "orderHint": "8587094707721254251P]",
      "lastModifiedBy": {
        "user": {
          "id": "fbab97d0-4932-4511-b675-204639209557"
        }
      },
      "lastModifiedDateTime": "2017-04-24T22:52:29.814Z"
    }
  },
  "id": "gcrYAaAkgU2EQUvpkNNXLGQAGTtu"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update plannertaskdetails",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
