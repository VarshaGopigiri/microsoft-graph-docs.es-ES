# <a name="update-plannerbuckettaskboardtaskformat"></a><span data-ttu-id="ffd38-101">Actualizar plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="ffd38-101">Update plannerBucketTaskBoardTaskFormat</span></span>

<span data-ttu-id="ffd38-102">Actualizar las propiedades del objeto **plannerBucketTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="ffd38-102">Update the properties of **plannerBucketTaskBoardTaskFormat** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="ffd38-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="ffd38-103">Permissions</span></span>
<span data-ttu-id="ffd38-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ffd38-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ffd38-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ffd38-106">Permission type</span></span>      | <span data-ttu-id="ffd38-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ffd38-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ffd38-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ffd38-108">Delegated (work or school account)</span></span> | <span data-ttu-id="ffd38-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ffd38-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ffd38-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ffd38-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ffd38-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ffd38-111">Not supported.</span></span>    |
|<span data-ttu-id="ffd38-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ffd38-112">Application</span></span> | <span data-ttu-id="ffd38-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ffd38-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ffd38-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ffd38-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/<id>/bucketTaskBoardFormat
```
## <a name="optional-request-headers"></a><span data-ttu-id="ffd38-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="ffd38-115">Optional request headers</span></span>
| <span data-ttu-id="ffd38-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="ffd38-116">Name</span></span>       | <span data-ttu-id="ffd38-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffd38-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="ffd38-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="ffd38-118">Authorization</span></span>  | <span data-ttu-id="ffd38-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ffd38-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ffd38-121">If-Match</span><span class="sxs-lookup"><span data-stu-id="ffd38-121">If-Match</span></span>  | <span data-ttu-id="ffd38-p103">Último valor ETag conocido para que se actualice **plannerBucketTaskBoardTaskFormat**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ffd38-p103">Last known ETag value for the **plannerBucketTaskBoardTaskFormat** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ffd38-124">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="ffd38-124">Request body</span></span>
<span data-ttu-id="ffd38-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ffd38-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ffd38-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ffd38-128">Property</span></span>     | <span data-ttu-id="ffd38-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffd38-129">Type</span></span>   |<span data-ttu-id="ffd38-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffd38-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ffd38-131">orderHint</span><span class="sxs-lookup"><span data-stu-id="ffd38-131">orderHint</span></span>|<span data-ttu-id="ffd38-132">String</span><span class="sxs-lookup"><span data-stu-id="ffd38-132">String</span></span>|<span data-ttu-id="ffd38-p105">Sugerencia usada para ordenar tareas en la vista Depósito del panel de tareas. El formato se define tal como se describe [aquí](../resources/planner_order_hint_format.md).</span><span class="sxs-lookup"><span data-stu-id="ffd38-p105">Hint used to order tasks in the Bucket view of the Task Board. The format is defined as outlined [here](../resources/planner_order_hint_format.md).</span></span>|

## <a name="response"></a><span data-ttu-id="ffd38-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ffd38-135">Response</span></span>

<span data-ttu-id="ffd38-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerBucketTaskBoardTaskFormat](../resources/plannerbuckettaskboardtaskformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffd38-136">If successful, this method returns a `200 OK` response code and updated [plannerBucketTaskBoardTaskFormat](../resources/plannerbuckettaskboardtaskformat.md) object in the response body.</span></span>

<span data-ttu-id="ffd38-p106">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="ffd38-p106">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="ffd38-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ffd38-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ffd38-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ffd38-141">Request</span></span>
<span data-ttu-id="ffd38-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ffd38-142">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="ffd38-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ffd38-143">Response</span></span>
<span data-ttu-id="ffd38-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ffd38-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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