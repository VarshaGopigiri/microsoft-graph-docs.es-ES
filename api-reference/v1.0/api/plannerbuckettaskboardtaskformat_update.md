# <a name="update-plannerbuckettaskboardtaskformat"></a><span data-ttu-id="1686a-101">Actualizar plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="1686a-101">Update plannerBucketTaskBoardTaskFormat</span></span>

<span data-ttu-id="1686a-102">Actualizar las propiedades del objeto **plannerBucketTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="1686a-102">Update the properties of **plannerBucketTaskBoardTaskFormat** object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1686a-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1686a-103">Prerequisites</span></span>
<span data-ttu-id="1686a-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="1686a-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="1686a-105">*Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="1686a-105">*Group.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="1686a-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1686a-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/<id>/bucketTaskBoardFormat
```
## <a name="optional-request-headers"></a><span data-ttu-id="1686a-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="1686a-107">Optional request headers</span></span>
| <span data-ttu-id="1686a-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="1686a-108">Name</span></span>       | <span data-ttu-id="1686a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1686a-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="1686a-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="1686a-110">Authorization</span></span>  | <span data-ttu-id="1686a-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1686a-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1686a-113">If-Match</span><span class="sxs-lookup"><span data-stu-id="1686a-113">If-Match</span></span>  | <span data-ttu-id="1686a-p102">Último valor ETag conocido para que se actualice **plannerBucketTaskBoardTaskFormat**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1686a-p102">Last known ETag value for the **plannerBucketTaskBoardTaskFormat** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1686a-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="1686a-116">Request body</span></span>
<span data-ttu-id="1686a-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="1686a-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="1686a-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1686a-120">Property</span></span>     | <span data-ttu-id="1686a-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="1686a-121">Type</span></span>   |<span data-ttu-id="1686a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1686a-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1686a-123">orderHint</span><span class="sxs-lookup"><span data-stu-id="1686a-123">orderHint</span></span>|<span data-ttu-id="1686a-124">String</span><span class="sxs-lookup"><span data-stu-id="1686a-124">String</span></span>|<span data-ttu-id="1686a-p104">Sugerencia usada para ordenar tareas en la vista Depósito del panel de tareas. El formato se define tal como se describe [aquí](../resources/planner_order_hint_format.md).</span><span class="sxs-lookup"><span data-stu-id="1686a-p104">Hint used to order tasks in the Bucket view of the Task Board. The format is defined as outlined [here](../resources/planner_order_hint_format.md).</span></span>|

## <a name="response"></a><span data-ttu-id="1686a-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1686a-127">Response</span></span>

<span data-ttu-id="1686a-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerBucketTaskBoardTaskFormat](../resources/plannerbuckettaskboardtaskformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1686a-128">If successful, this method returns a `200 OK` response code and updated [plannerBucketTaskBoardTaskFormat](../resources/plannerbuckettaskboardtaskformat.md) object in the response body.</span></span>

<span data-ttu-id="1686a-p105">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="1686a-p105">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="1686a-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1686a-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1686a-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1686a-133">Request</span></span>
<span data-ttu-id="1686a-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1686a-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerbuckettaskboardtaskformat"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/tasks/hsOf2dhOJkqyYYZEtdzDe2QAIUCR/bucketTaskBoardFormat
Content-type: application/json
Content-length: 34
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "orderHint": "A6673H Ejkl!"
}
```
##### <a name="response"></a><span data-ttu-id="1686a-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1686a-135">Response</span></span>
<span data-ttu-id="1686a-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1686a-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerBucketTaskBoardTaskFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 68

{
  "id": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR",
  "orderHint": "C3665D"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update plannerbuckettaskboardtaskformat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->