---
title: Actualizar plannertaskdetails
description: Actualizar las propiedades del objeto **plannertaskdetails**.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 04adf9c53907962f0298541f5d8c28402bc2b613
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960556"
---
# <a name="update-plannertaskdetails"></a><span data-ttu-id="d5104-103">Actualizar plannertaskdetails</span><span class="sxs-lookup"><span data-stu-id="d5104-103">Update plannertaskdetails</span></span>

> <span data-ttu-id="d5104-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d5104-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d5104-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d5104-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d5104-106">Actualizar las propiedades del objeto **plannertaskdetails**.</span><span class="sxs-lookup"><span data-stu-id="d5104-106">Update the properties of **plannertaskdetails** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="d5104-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d5104-107">Permissions</span></span>
<span data-ttu-id="d5104-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d5104-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d5104-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d5104-110">Permission type</span></span>      | <span data-ttu-id="d5104-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d5104-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d5104-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d5104-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d5104-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d5104-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="d5104-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d5104-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d5104-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d5104-115">Not supported.</span></span>    |
|<span data-ttu-id="d5104-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d5104-116">Application</span></span> | <span data-ttu-id="d5104-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d5104-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d5104-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d5104-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/<id>/details
```
## <a name="optional-request-headers"></a><span data-ttu-id="d5104-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="d5104-119">Optional request headers</span></span>
| <span data-ttu-id="d5104-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d5104-120">Name</span></span>       | <span data-ttu-id="d5104-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5104-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="d5104-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="d5104-122">Authorization</span></span>  | <span data-ttu-id="d5104-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d5104-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d5104-125">If-Match</span><span class="sxs-lookup"><span data-stu-id="d5104-125">If-Match</span></span>  | <span data-ttu-id="d5104-p104">Último valor ETag conocido para que se actualice **plannerTaskDetails**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d5104-p104">Last known ETag value for the **plannerTaskDetails** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d5104-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d5104-128">Request body</span></span>
<span data-ttu-id="d5104-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="d5104-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="d5104-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d5104-132">Property</span></span>     | <span data-ttu-id="d5104-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="d5104-133">Type</span></span>   |<span data-ttu-id="d5104-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5104-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d5104-135">checklist</span><span class="sxs-lookup"><span data-stu-id="d5104-135">checklist</span></span>|[<span data-ttu-id="d5104-136">plannerChecklistItems</span><span class="sxs-lookup"><span data-stu-id="d5104-136">plannerChecklistItems</span></span>](../resources/plannerchecklistitems.md)|<span data-ttu-id="d5104-137">Colección de elementos de la lista de comprobación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d5104-137">The collection of checklist items on the task.</span></span>|
|<span data-ttu-id="d5104-138">description</span><span class="sxs-lookup"><span data-stu-id="d5104-138">description</span></span>|<span data-ttu-id="d5104-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="d5104-139">String</span></span>|<span data-ttu-id="d5104-140">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="d5104-140">Description of the task</span></span>|
|<span data-ttu-id="d5104-141">previewType</span><span class="sxs-lookup"><span data-stu-id="d5104-141">previewType</span></span>|<span data-ttu-id="d5104-142">string</span><span class="sxs-lookup"><span data-stu-id="d5104-142">string</span></span>|<span data-ttu-id="d5104-p106">Establece el tipo de vista previa que aparece en la tarea. Los valores posibles son `automatic`, `noPreview`, `checklist`, `description` y `reference`. Si se establece en `automatic`, la aplicación que visualiza la tarea elige la vista previa mostrada.</span><span class="sxs-lookup"><span data-stu-id="d5104-p106">This sets the type of preview that shows up on the task. Possible values are: `automatic`, `noPreview`, `checklist`, `description`, `reference`. When set to `automatic` the displayed preview is chosen by the app viewing the task.</span></span>|
|<span data-ttu-id="d5104-146">references</span><span class="sxs-lookup"><span data-stu-id="d5104-146">references</span></span>|[<span data-ttu-id="d5104-147">plannerExternalReferences</span><span class="sxs-lookup"><span data-stu-id="d5104-147">plannerExternalReferences</span></span>](../resources/plannerexternalreferences.md)|<span data-ttu-id="d5104-148">La colección de referencias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d5104-148">The collection of references on the task.</span></span>|

## <a name="response"></a><span data-ttu-id="d5104-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5104-149">Response</span></span>

<span data-ttu-id="d5104-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerTaskDetails](../resources/plannertaskdetails.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d5104-150">If successful, this method returns a `200 OK` response code and updated [plannerTaskDetails](../resources/plannertaskdetails.md) object in the response body.</span></span>

<span data-ttu-id="d5104-p107">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="d5104-p107">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="d5104-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d5104-154">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d5104-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d5104-155">Request</span></span>
<span data-ttu-id="d5104-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d5104-156">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannertaskdetails"
}-->
```http
PATCH https://graph.microsoft.com/beta/planner/tasks/gcrYAaAkgU2EQUvpkNNXLGQAGTtu/details
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
      "isChecked": true
    },
    "d280ed1a-9f6b-4f9c-a962-fb4d00dc50ff":{
      "@odata.type": "microsoft.graph.plannerChecklistItem",
      "isChecked": true,
    },
    "a93c93c5-10a6-4167-9551-8bafa09967a7": null
  }
}
```
##### <a name="response"></a><span data-ttu-id="d5104-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5104-157">Response</span></span>
<span data-ttu-id="d5104-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d5104-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
