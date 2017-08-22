# <a name="update-plannerbucket"></a><span data-ttu-id="8c3c1-101">Actualizar plannerbucket</span><span class="sxs-lookup"><span data-stu-id="8c3c1-101">Update plannerbucket</span></span>

<span data-ttu-id="8c3c1-102">Actualizar las propiedades del objeto **plannerbucket**.</span><span class="sxs-lookup"><span data-stu-id="8c3c1-102">Update the properties of **plannerbucket** object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8c3c1-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8c3c1-103">Prerequisites</span></span>
<span data-ttu-id="8c3c1-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="8c3c1-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="8c3c1-105">*Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="8c3c1-105">*Group.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="8c3c1-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8c3c1-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/buckets/<id>
```
## <a name="optional-request-headers"></a><span data-ttu-id="8c3c1-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="8c3c1-107">Optional request headers</span></span>
| <span data-ttu-id="8c3c1-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="8c3c1-108">Name</span></span>       | <span data-ttu-id="8c3c1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c3c1-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="8c3c1-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="8c3c1-110">Authorization</span></span>  | <span data-ttu-id="8c3c1-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8c3c1-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8c3c1-113">If-Match</span><span class="sxs-lookup"><span data-stu-id="8c3c1-113">If-Match</span></span>  | <span data-ttu-id="8c3c1-p102">Último valor ETag conocido para que se actualice **plannerBucket**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8c3c1-p102">Last known ETag value for the **plannerBucket** to be updated. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="8c3c1-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="8c3c1-116">Request body</span></span>
<span data-ttu-id="8c3c1-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="8c3c1-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="8c3c1-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8c3c1-120">Property</span></span>     | <span data-ttu-id="8c3c1-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c3c1-121">Type</span></span>   |<span data-ttu-id="8c3c1-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c3c1-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8c3c1-123">name</span><span class="sxs-lookup"><span data-stu-id="8c3c1-123">name</span></span>|<span data-ttu-id="8c3c1-124">String</span><span class="sxs-lookup"><span data-stu-id="8c3c1-124">String</span></span>|<span data-ttu-id="8c3c1-125">Nombre del depósito.</span><span class="sxs-lookup"><span data-stu-id="8c3c1-125">Name of the bucket.</span></span>|
|<span data-ttu-id="8c3c1-126">orderHint</span><span class="sxs-lookup"><span data-stu-id="8c3c1-126">orderHint</span></span>|<span data-ttu-id="8c3c1-127">String</span><span class="sxs-lookup"><span data-stu-id="8c3c1-127">String</span></span>|<span data-ttu-id="8c3c1-p104">Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](../resources/planner_order_hint_format.md).</span><span class="sxs-lookup"><span data-stu-id="8c3c1-p104">Hint used to order items of this type in a list view. The format is defined as outlined [here](../resources/planner_order_hint_format.md).</span></span>|
|<span data-ttu-id="8c3c1-130">planId</span><span class="sxs-lookup"><span data-stu-id="8c3c1-130">planId</span></span>|<span data-ttu-id="8c3c1-131">String</span><span class="sxs-lookup"><span data-stu-id="8c3c1-131">String</span></span>|<span data-ttu-id="8c3c1-132">Id. de plan al que pertenece el depósito.</span><span class="sxs-lookup"><span data-stu-id="8c3c1-132">Plan id to which the bucket belongs.</span></span>|

## <a name="response"></a><span data-ttu-id="8c3c1-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c3c1-133">Response</span></span>

<span data-ttu-id="8c3c1-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerBucket](../resources/plannerbucket.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c3c1-134">If successful, this method returns a `200 OK` response code and updated [plannerBucket](../resources/plannerbucket.md) object in the response body.</span></span>

<span data-ttu-id="8c3c1-p105">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="8c3c1-p105">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="8c3c1-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c3c1-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8c3c1-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8c3c1-139">Request</span></span>
<span data-ttu-id="8c3c1-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8c3c1-140">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="8c3c1-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c3c1-141">Response</span></span>
<span data-ttu-id="8c3c1-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8c3c1-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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