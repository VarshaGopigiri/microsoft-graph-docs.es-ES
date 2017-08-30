# <a name="update-plannerbucket"></a><span data-ttu-id="e6a51-101">Actualizar plannerbucket</span><span class="sxs-lookup"><span data-stu-id="e6a51-101">Update plannerbucket</span></span>

<span data-ttu-id="e6a51-102">Actualizar las propiedades del objeto **plannerbucket**.</span><span class="sxs-lookup"><span data-stu-id="e6a51-102">Update the properties of **plannerbucket** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="e6a51-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="e6a51-103">Permissions</span></span>
<span data-ttu-id="e6a51-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e6a51-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e6a51-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6a51-106">Permission type</span></span>      | <span data-ttu-id="e6a51-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6a51-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e6a51-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6a51-108">Delegated (work or school account)</span></span> | <span data-ttu-id="e6a51-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6a51-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="e6a51-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6a51-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e6a51-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6a51-111">Not supported.</span></span>    |
|<span data-ttu-id="e6a51-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6a51-112">Application</span></span> | <span data-ttu-id="e6a51-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6a51-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e6a51-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6a51-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/buckets/<id>
```
## <a name="optional-request-headers"></a><span data-ttu-id="e6a51-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="e6a51-115">Optional request headers</span></span>
| <span data-ttu-id="e6a51-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="e6a51-116">Name</span></span>       | <span data-ttu-id="e6a51-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6a51-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="e6a51-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="e6a51-118">Authorization</span></span>  | <span data-ttu-id="e6a51-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e6a51-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e6a51-121">If-Match</span><span class="sxs-lookup"><span data-stu-id="e6a51-121">If-Match</span></span>  | <span data-ttu-id="e6a51-p103">Último valor ETag conocido para que se actualice **plannerBucket**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e6a51-p103">Last known ETag value for the **plannerBucket** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="e6a51-124">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6a51-124">Request body</span></span>
<span data-ttu-id="e6a51-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="e6a51-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="e6a51-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e6a51-128">Property</span></span>     | <span data-ttu-id="e6a51-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6a51-129">Type</span></span>   |<span data-ttu-id="e6a51-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6a51-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e6a51-131">name</span><span class="sxs-lookup"><span data-stu-id="e6a51-131">name</span></span>|<span data-ttu-id="e6a51-132">String</span><span class="sxs-lookup"><span data-stu-id="e6a51-132">String</span></span>|<span data-ttu-id="e6a51-133">Nombre del depósito.</span><span class="sxs-lookup"><span data-stu-id="e6a51-133">Name of the bucket.</span></span>|
|<span data-ttu-id="e6a51-134">orderHint</span><span class="sxs-lookup"><span data-stu-id="e6a51-134">orderHint</span></span>|<span data-ttu-id="e6a51-135">String</span><span class="sxs-lookup"><span data-stu-id="e6a51-135">String</span></span>|<span data-ttu-id="e6a51-p105">Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](../resources/planner_order_hint_format.md).</span><span class="sxs-lookup"><span data-stu-id="e6a51-p105">Hint used to order items of this type in a list view. The format is defined as outlined [here](../resources/planner_order_hint_format.md).</span></span>|
|<span data-ttu-id="e6a51-138">planId</span><span class="sxs-lookup"><span data-stu-id="e6a51-138">planId</span></span>|<span data-ttu-id="e6a51-139">String</span><span class="sxs-lookup"><span data-stu-id="e6a51-139">String</span></span>|<span data-ttu-id="e6a51-140">Id. de plan al que pertenece el depósito.</span><span class="sxs-lookup"><span data-stu-id="e6a51-140">Plan id to which the bucket belongs.</span></span>|

## <a name="response"></a><span data-ttu-id="e6a51-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6a51-141">Response</span></span>

<span data-ttu-id="e6a51-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerBucket](../resources/plannerbucket.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6a51-142">If successful, this method returns a `200 OK` response code and updated [plannerBucket](../resources/plannerbucket.md) object in the response body.</span></span>

<span data-ttu-id="e6a51-p106">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="e6a51-p106">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="e6a51-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6a51-146">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e6a51-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6a51-147">Request</span></span>
<span data-ttu-id="e6a51-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6a51-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_plannerbucket"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/buckets/hsOf2dhOJkqyYYZEtdzDe2QAIUCR
Content-type: application/json
Content-length: 27
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "name": "Development"
}
```
##### <a name="response"></a><span data-ttu-id="e6a51-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6a51-149">Response</span></span>
<span data-ttu-id="e6a51-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6a51-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerBucket"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 245

{
  "name": "Development",
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  "orderHint": "85752723360752+",
  "id": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update plannerbucket",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->