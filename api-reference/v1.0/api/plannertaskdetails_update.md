# <a name="update-plannertaskdetails"></a><span data-ttu-id="d3cb7-101">Actualizar plannertaskdetails</span><span class="sxs-lookup"><span data-stu-id="d3cb7-101">Update plannertaskdetails</span></span>

<span data-ttu-id="d3cb7-102">Actualizar las propiedades del objeto **plannertaskdetails**.</span><span class="sxs-lookup"><span data-stu-id="d3cb7-102">Update the properties of **plannertaskdetails** object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d3cb7-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d3cb7-103">Prerequisites</span></span>
<span data-ttu-id="d3cb7-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="d3cb7-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="d3cb7-105">*Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="d3cb7-105">*Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="d3cb7-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d3cb7-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/<id>/details
```
## <a name="optional-request-headers"></a><span data-ttu-id="d3cb7-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="d3cb7-107">Optional request headers</span></span>
| <span data-ttu-id="d3cb7-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="d3cb7-108">Name</span></span>       | <span data-ttu-id="d3cb7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3cb7-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="d3cb7-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="d3cb7-110">Authorization</span></span>  | <span data-ttu-id="d3cb7-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d3cb7-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d3cb7-113">If-Match</span><span class="sxs-lookup"><span data-stu-id="d3cb7-113">If-Match</span></span>  | <span data-ttu-id="d3cb7-p102">Último valor ETag conocido para que se actualice **plannerTaskDetails**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d3cb7-p102">Last known ETag value for the **plannerTaskDetails** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d3cb7-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="d3cb7-116">Request body</span></span>
<span data-ttu-id="d3cb7-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="d3cb7-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="d3cb7-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d3cb7-120">Property</span></span>     | <span data-ttu-id="d3cb7-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3cb7-121">Type</span></span>   |<span data-ttu-id="d3cb7-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3cb7-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d3cb7-123">checklist</span><span class="sxs-lookup"><span data-stu-id="d3cb7-123">checklist</span></span>|[<span data-ttu-id="d3cb7-124">plannerChecklistItems</span><span class="sxs-lookup"><span data-stu-id="d3cb7-124">plannerChecklistItems</span></span>](../resources/plannerchecklistitems.md)|<span data-ttu-id="d3cb7-125">Colección de elementos de la lista de comprobación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d3cb7-125">The collection of checklist items on the task.</span></span>|
|<span data-ttu-id="d3cb7-126">description</span><span class="sxs-lookup"><span data-stu-id="d3cb7-126">description</span></span>|<span data-ttu-id="d3cb7-127">String</span><span class="sxs-lookup"><span data-stu-id="d3cb7-127">String</span></span>|<span data-ttu-id="d3cb7-128">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="d3cb7-128">Description of the task</span></span>|
|<span data-ttu-id="d3cb7-129">previewType</span><span class="sxs-lookup"><span data-stu-id="d3cb7-129">previewType</span></span>|<span data-ttu-id="d3cb7-130">string</span><span class="sxs-lookup"><span data-stu-id="d3cb7-130">string</span></span>|<span data-ttu-id="d3cb7-p104">Establece el tipo de vista previa que aparece en la tarea. Los valores posibles son `automatic`, `noPreview`, `checklist`, `description` y `reference`. Si se establece en `automatic`, la aplicación que visualiza la tarea elige la vista previa mostrada.</span><span class="sxs-lookup"><span data-stu-id="d3cb7-p104">This sets the type of preview that shows up on the task. Possible values are: `automatic`, `noPreview`, `checklist`, `description`, `reference`. When set to `automatic` the displayed preview is chosen by the app viewing the task.</span></span>|
|<span data-ttu-id="d3cb7-134">references</span><span class="sxs-lookup"><span data-stu-id="d3cb7-134">references</span></span>|[<span data-ttu-id="d3cb7-135">plannerExternalReferences</span><span class="sxs-lookup"><span data-stu-id="d3cb7-135">plannerExternalReferences</span></span>](../resources/plannerexternalreferences.md)|<span data-ttu-id="d3cb7-136">La colección de referencias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="d3cb7-136">The collection of references on the task.</span></span>|

## <a name="response"></a><span data-ttu-id="d3cb7-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3cb7-137">Response</span></span>

<span data-ttu-id="d3cb7-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerTaskDetails](../resources/plannertaskdetails.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3cb7-138">If successful, this method returns a `200 OK` response code and updated [plannerTaskDetails](../resources/plannertaskdetails.md) object in the response body.</span></span>

<span data-ttu-id="d3cb7-p105">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="d3cb7-p105">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="d3cb7-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d3cb7-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d3cb7-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d3cb7-143">Request</span></span>
<span data-ttu-id="d3cb7-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d3cb7-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannertaskdetails"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/tasks/gcrYAaAkgU2EQUvpkNNXLGQAGTtu/details
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
##### <a name="response"></a><span data-ttu-id="d3cb7-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3cb7-145">Response</span></span>
<span data-ttu-id="d3cb7-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d3cb7-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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