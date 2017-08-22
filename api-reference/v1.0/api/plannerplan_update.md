# <a name="update-plannerplan"></a><span data-ttu-id="2b138-101">Actualizar plannerplan</span><span class="sxs-lookup"><span data-stu-id="2b138-101">Update plannerplan</span></span>

<span data-ttu-id="2b138-102">Actualizar las propiedades del objeto **plannerplan**.</span><span class="sxs-lookup"><span data-stu-id="2b138-102">Update the properties of **plannerplan** object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2b138-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2b138-103">Prerequisites</span></span>
<span data-ttu-id="2b138-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="2b138-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="2b138-105">*Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="2b138-105">*Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="2b138-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2b138-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/plans/<id>
```
## <a name="optional-request-headers"></a><span data-ttu-id="2b138-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="2b138-107">Optional request headers</span></span>
| <span data-ttu-id="2b138-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="2b138-108">Name</span></span>       | <span data-ttu-id="2b138-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b138-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="2b138-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="2b138-110">Authorization</span></span>  | <span data-ttu-id="2b138-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b138-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2b138-113">If-Match</span><span class="sxs-lookup"><span data-stu-id="2b138-113">If-Match</span></span>  | <span data-ttu-id="2b138-p102">Último valor ETag conocido para que se actualice plannerPlan. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b138-p102">Last known ETag value for the plannerPlan to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="2b138-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="2b138-116">Request body</span></span>
<span data-ttu-id="2b138-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="2b138-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="2b138-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2b138-120">Property</span></span>     | <span data-ttu-id="2b138-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b138-121">Type</span></span>   |<span data-ttu-id="2b138-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b138-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2b138-123">owner</span><span class="sxs-lookup"><span data-stu-id="2b138-123">owner</span></span>|<span data-ttu-id="2b138-124">String</span><span class="sxs-lookup"><span data-stu-id="2b138-124">String</span></span>|<span data-ttu-id="2b138-p104">`id` del [group](../resources/group.md) que tiene el plan. Para poder establecer este campo, debe existir un grupo válido. Una vez establecido, solo lo puede actualizar el propietario.</span><span class="sxs-lookup"><span data-stu-id="2b138-p104">[Group](../resources/group.md) `id` by which the plan is owned. A valid group must exist before this field can be set. Once set, this can only be updated by the owner.</span></span>|
|<span data-ttu-id="2b138-128">title</span><span class="sxs-lookup"><span data-stu-id="2b138-128">title</span></span>|<span data-ttu-id="2b138-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="2b138-129">String</span></span>|<span data-ttu-id="2b138-130">Título del plan.</span><span class="sxs-lookup"><span data-stu-id="2b138-130">Title of the plan.</span></span>|

## <a name="response"></a><span data-ttu-id="2b138-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b138-131">Response</span></span>

<span data-ttu-id="2b138-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerPlan](../resources/plannerplan.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2b138-132">If successful, this method returns a `200 OK` response code and updated [plannerPlan](../resources/plannerplan.md) object in the response body.</span></span>

<span data-ttu-id="2b138-p105">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="2b138-p105">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="2b138-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b138-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2b138-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b138-137">Request</span></span>
<span data-ttu-id="2b138-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b138-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerplan"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/plans/xqQg5FS2LkCp935s-FIFm2QAFkHM
Content-type: application/json
Content-length: 29
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "title": "title-value"
}
```
##### <a name="response"></a><span data-ttu-id="2b138-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b138-139">Response</span></span>
<span data-ttu-id="2b138-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b138-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlan"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 357

{
  "createdBy": {
    "application": {
      "id": "95e27074-6c4a-447a-aa24-9d718a0b86fa"
    },
    "user": {
      "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
    }
  },
  "createdDateTime": "2015-03-30T18:36:49.2407981Z",
  "owner": "ebf3b108-5234-4e22-b93d-656d7dae5874",
  "title": "title-value",
  "id": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update plannerplan",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->